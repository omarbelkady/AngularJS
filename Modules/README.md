## Modules 

- Angular Apps are modular that means I can add/remove any part of my app w/o affecting other parts of my application
- Modules are piles of code in order to serve a specific purpose of the app, domain or workflow
- Modules have the ability to hold:
    - components
    - services
    - providers
    - filters
    - directives
- In short modules bring us functionality which I can export to use in other modules 
- An Angular application must have at least one **NgModule** class which is the root Module similar to React(index.html) which is in charge of bootstrapping your application
- It lives in the file called app.module.ts

### NgModule Info

- I use the decorator @NgModule and pass to it props which describe it i.e.

    1. declarations:

    2. exports:
    
    3. imports:

    4. providers:

    5. bootstrap: 

### Installing A Module i.e. library in Angular

- Every Module starts with @ symbol to install a module within your app I prefix it with the @ symbol

```js
//for example I want to tell Angular that this is a component file
import { Component } from "@angular/core";
```


```html
<!DOCTYPE html>
<html >
<head>
    <script src="~/Scripts/angular.js"></script>
</head>
<body ng-app="myApp">
    @* HTML content *@
    <script>
        /*
        creating a module named myApp 
        first param: name of module 
        second param: array of dependencies
        */
        var myApp = angular.module("myApp", []); 
    </script>
</body>
</html>


```