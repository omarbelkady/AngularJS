## Services

- Services in Angular are JS functions designed to perform certain tasks which are obviously
    - intended to be reused throughout our app
- Any data or logic that isn't related to a view which you want to be shared in between your components
    - you use a Service Class
- Each of our services interact with the controller, custom directive or model
- There are exceptions where some of our services may interact with the view i.e. U.I.
- Every Angular Service is lazy instantiated and singleton(meaning only instantiates when it needs it)
- Every component share the same instance of the service

### How Do We Tell Angular it is a Service Class    

   - By using the decorator:

```js
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root',
})
export class CarService {
    constructor()
    { 
        
    }
}
```

### Creating A Service Through The CLI:

```bash
ng generate service cars/car
```



### Built-in AngularJS services

    - $anchorscroll
    - $animate
    - $cachefactory
    - $compile
    - $controller
    - $document
    - $exceptionHandler
    - $filter
    - $http
    - $httpBackend
    - $httpParamSerializer
    - $httpParamSerializerJQLike
    - $interpolate
    - $interval
    - $locale
    - $location
    - $log
    - $parse
    - $q
    - $rootElement
    - $rootScope
    - $sce
    - $sceDelegate
    - $templateCache
    - $templateRequest
    - $timeout
    - $window
