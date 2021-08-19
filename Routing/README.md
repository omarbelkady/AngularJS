## How To Setup Routing In Angular

- Every Angular Application will have some to hundreds maybe thousands of components in large-scale applications

- Every Component will have its own view

- I need to render some views due to the user's action

- Angular Router provides me with Routing Functionality

- Say I have two buttons Car and Bike Link within my application

- I want my Angular application to render the appropriate view whenever I hit the corresponding button of the view

- I also want my Angular application to render the BikeList View whenever I click the Bike button


### Steps 

1. Create My Angular App with the routing flag


2. Add the base tag in the index.html file


3. Create the two components:
    - Bike
    - Car


4. Configure the routes for Car and Bike


5. I add Buttons and Directives to my app


I.

```bash
ng new myapprouting --routing
```

II. Goto your index.html file to add the base href tag
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Routing Example</title>
    <!-- Required so that your app knows how to construct URL when navigating-->
    <base href="/" >

    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

</head>
<body>
    
</body>
</html>
```

III. Navigate to your app folder and goto app-routing-module.ts file

- This file holds the routing module for the application
```ts
import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';
import { BikeListComponent } from './bike-list/bike-list.component';
import { CarListComponent } from './car-list/car-list.component';
import { PageNotFoundComponent } from './page-not-found/page-not-found.component';



const routes: Routes = [
  { path: '', redirectTo: '/departments', pathMatch: 'full' },
  { path: 'bike', component: BikeListComponent },
  { path: 'car',   component: CarListComponent },
  { path: '**',   component: PageNotFoundComponent }
  
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
export const routingComponents = [CarListComponent, 
                                  BikeListComponent,
                                  PageNotFoundComponent]
```

IV. Goto app.module.ts file and import this:

```ts
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';

import { AppRoutingModule, routingComponents } from './app-routing.module';

import { AppComponent } from './app.component';


@NgModule({
  declarations: [
    AppComponent,
    routingComponents,
  ],
  imports: [
    BrowserModule,
    AppRoutingModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

V. Create my components with inline templates(-it) and inline styling(-is)

```bash
cd myapprouting/
ng g c bike -it -is
ng g c car -it -is
```

VI. Configure Routes

1. Head to app-routing.module.ts

```ts
import { NgModule } from "@angular/core";
import { Routes, RouterModule } from "@angular/router";
import { BikeListComponent } from "./bike-list/bike-list.component";
import { CarListComponent } from "./car-list/car-list.component";


const routes : Routes  = [
    /*each route is nothing but a simple object first is path 
    then the component to render when hitting that path*/
    {   path:   'bike',  component:  BikeListComponent},
    {   path:   'car',  component:  CarListComponent   }

];

@NgModule({
    imports: [RouterModule.forRoot(routes)],
    exports: [RouterModule]
})

export class AppRoutingModule {};

export const routingComps = [BikeListComponent, CarListComponent]
```

2. Head over to app-module.ts

```ts
import { BrowserModule } from "@angular/platform-browser";
import { NgModule } from "@angular/core";


import { AppRoutingModule } from "./app-routing-module";

import { AppComponent } from "./app.component";




@NgModule({

    declarations: [
        AppComponent, 
        routingComponents
    ],

    imports:[
        BrowserModule,
        AppRoutingModule
    ],

    providers: [],

    bootstrap: [AppComponent]
});
```


3. Now I must tell Angular Router where to display the View

- I goto the app.component.html and use the routerLink directive and specify the path

```html
<div style="text-align: center">
    <h1>Hi There Everyone I will show you 
        how to use routing and navigate within
        your Angular App
    </h1>
</div>
<nav>
    <a routerLink="/bike" routerLinkActive="active">Bike</a>
	<a routerLink="/car" routerLinkActive="active">Car</a>
</nav>
<router-outlet></router-outlet>
<!-- ALL your router views should be placed here-->
```

