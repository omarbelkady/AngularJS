## Controller

- A controller in Angular is the one who controls the application data and behavior

### How To Create A Controller

```html
<!DOCTYPE html>
<html>
<head>
    <title>Sample Angular Application</title>
    <script src="~/scripts/angular.js"></script>

</head>
<body ng-app="myAngApp">
    <!-- /*Specifying a controller using the ng-controller directive*/ -->
    <div ng-controller="controllerAlpha">
        <!-- Passing a property to the controller-->
        {{aMessage}}
    </div>
    <script>
        var angApp = angular.module("myAngApp", []);
        //creating the controller
        angApp.controller("controllerAlpha", function($scope){
            $scope.aMessage("Hi There!");
        });
    </script>
</body>
</html>
```


### How To Attach Behavior(Click) to A Controller

```js
<!DOCTYPE html>
<html>
<head>
    <title>AngualrJS Controller</title>
    <script src="~/Scripts/angular.js"></script>
</head>
<body ng-app="myNgApp">
    <div ng-controller="controllerAlpha">
        Enter Message: <input type="text" ng-model="message" /> <br />
        <button ng-click="showMsg(message)">Show Message</button>
    </div>
    <script>
        var ngApp = angular.module('myNgApp', []);

        ngApp.controller('controllerAlpha', function ($scope) {
            $scope.message = "Hi There Everyone!";       
            
            $scope.showMsg = function (msg) {
                alert(msg);
            }; 
        });
    </script>
</body>
</html>
```