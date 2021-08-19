## Scope

- Object that has the app data methods

#### How To Create

```html
<!DOCTYPE html>
<html >
<head>
    <title>AngualrJS $scope object</title>
    <script src="~/Scripts/angularscr.js"></script>
</head>
<body ng-app="myAngApp">
    <!--ng-bind and ng-model are the directives in charge of displaying the data with respect to the scope-->
    <div ng-controller="theParentController">
        Controller Name: {{nameOfMyController}}
        Message: {{someMessage}}
        <div style="margin 10px 0 10px 20px" ng-controller="theChildController">
            Controller Name: {{nameOfMyController}}
            Message: {{someMessage}}
        </div>
    </div>
    
    <div ng-controller="brotherController">
        Controller Name: {{nameOfMyController}} <br />
        Message: {{someMessage}} <br />
    </div>

    <script>
        var angApp = angular.module('myAngApp', []);

        angApp.controller('theParentController', function ($scope, $theRootScope) {
            $scope.nameOfMyController = "theParentController";
            $theRootScope.message = "This is the message";
        });

        angApp.controller('theChildController', function($scope){
            $scope.nameOfMyController = "theChildController";
        });

        angApp.controller('brotherController', function($scope){
           
        });
    </script>
</body>
</html>
```


#### Built-in Methods For The Scope Object in Angular

- $apply(): Eval an exp in Angular outside of the Angular framework 
- $broadcast(): Dispatch and Deescalate your callback to the child scope
- $destroy(): Remove the current scope(i.e. and its children) from the parent
- $emit(): Dispatch and Escalate your callback to the parent(i.e. rootScope)
- $new(): To Create A New Child Scope
- $on(): Registering a callback
- $watch(): Register A Callback for it to be exectuted whenever my model prop changes
- $watchGroup(): Register A Callback for it to be executed whenever my model prop changes
    - But here I give it an array of props to keep track of them