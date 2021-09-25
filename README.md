## Angular JS


### Expressions in Angular

- An Expression is simply a JS expression wrapped in curly braces and is outputed to the DOM
- Expressions can be:
    - Some Computation Logic
    - Literals
    - Operators
    - Variables

```html
<!DOCTYPE html>
<html >
<head>
    <script src="~/Scripts/angular.js"></script>
</head>
<body >
    <div ng-app ng-init="sayHi='Hi There Everyone!'; luckyNum= 13; rate = 10.5; time= 11; myArr = [458, 812]; individual = { fName:'Omar', lName :'Belkay'}">
        {{ (luckyNum * rate * time)/100 }}<br />
        {{myArr[1]}} <br />
        {{individual.fName + " " + individual.lName}}
    </div>
</body>
</html>

```

### ng-init directive

- I use the ng-init directive to declare variables within my application and they can be of any datatype

### NO-FLY ZONES FOR EXPRESSIONS
- ![DeniedIcon](https://iconarchive.com/download/i98435/dakirby309/simply-styled/Security-Denied.ico)

1. Contain a conditional
2. Have a loop
3. Exceptions
4. RegEx
5. Declare Functions
6. Have A Comma
7. Have A Void
8. Have the return keyword in them


### Install Angular CLI
```bash
npm i -g @angular/cli
```

### How To Create An Angular Application Using The Angular CLI

```bash
ng new nameofangapp
```

#### Flags When Creating An Angular App
- --verboase=true     Telling Angular to output more info to the console 
- --skipTests=true    Telling Angular to not generate test files for my project
- --skipGit=true      Telling Angular to not initialize a Git Repo for my project
- --routing=true      Telling Angular that I want routing in my app and to have it listed in my modules



### Project Structure

```
├── README.md
├── /node_modules ======> 3rd party libs are installed here that we use in my app
└── /src
    └── /myapp ======> All the files necessary to generate the UI of my app are here
    |   ├── myapp-routing.module.ts
    |   ├── myapp.component.css ======> CSS Stylesheet for the root component
    |   ├── myapp-component.html ======> Create the html file for me
    |   ├── myapp.component.spec.ts ======> Unit tests for the root component
    |   ├── myapp.component.ts ======> Definition of module and properties
    |   └── myapp.module.ts  ======> Root Component i.e. App.js in ReactJS
	├── /assets ======> Static files i.e. images, fonts, etc.
	├── /environments ======> configuration for development and production environments
    |   ├── environment.prod.ts
    |   └── environment.ts
	├── favicon.ico 
	├── index.html ======> Bootstraps my app
	├── main.ts  ======> Main entry point of your Angular app tells Angular to start my app
	├── polyfills.ts 
    ├── styles.css  ======> Global styling
    └── test.ts  ======> Unit Tests
├── angular.json ======> Defines structure to my angular application
├── karma.conf.js ======> Test runner file
├── package-lock.json ======> Gives Angular Details in regards to the version for all the packages in node_modules dir
├── package.json ======> Configures all your npm package dependencies
├── README.md ======> Documentation
├── tsconfig.app.json
├── tsconfig.json ======> Typescript configuration file... Gives instructions to the typescript compiler
├── .browserslistrc
├── .editorconfig
└── .gitignore ======> List the files you do not want Git To Track Here
```



### Fire Your Angular App in The Browser
```bash
ng serve
```


### How To Create A Component In Angular
```bash
ng generate component navbar
```

### 2nd Way ofHow To Create A Component In Angular
```bash
ng g c navbar
```


### Dependency Injection In Angular

- @ Injectable Decorator tells Angular that this specified Service Class should be visible to everyone
    - within your Application.
- Since Components consume services 
- I need Dependency Injection to give my component all the power my service has for functionality purposes

### Good Practices 

- ALWAYS keep your Components and Services Separate
- Failure to do so will require you to FIRST declare your Service THEEEN your Component
    - IF you fail to follow this order it results in:
        - RUNTIME NULL REFERENCE ERROR