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

├── /node_modules

├── package.json

├── .gitignore ------- list the files you do not want git to track here

├── public

│   ├── favicon.ico

│   ├── index.html ------ to bootstrap your react app import it here

│   └── manifest.json

└── /src

    └── /myapp

        ├── myapp-routing.module.ts

        ├── myapp.component.css

        ├── myapp-component.html

        ├── myapp.component.ts

        ├── myapp.module.ts

	├── /assets

	├── /environments

	├── favicon.ico

	├── index.html

	├── main.ts

	├── polyfills.ts

    ├── styles.css

    ├── test.ts
├── .browserslistrc

├── .editorconfig

├── .gitignore

├── angular.json

├── karma.conf.js

├── package-lock.json

├── package.json

├── README.md

├── tsconfig.app.json

├── tsconfig.json

├── tsconfig.spec.json
```



### Fire Your Angular App in The Browser
```bash
ng serve
```


### How To Create A Component In Angular
```bash
ng generate component navbar
```

### Dependency Injection In Angular

- @Injectable Decorator tells Angular that this specified Service Class should be visible to everyone
    - within your Application.
- 

### Good Practices 

- ALWAYS keep your Components and Services Separate
- Failure to do so will require you to FIRST declare your Service THEEEN your Component
    - IF you fail to follow this order it results in:
        - RUNTIME NULL REFERENCE ERROR


### Handling Exceptions in Angular