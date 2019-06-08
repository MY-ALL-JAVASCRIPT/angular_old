-----------------------------------------------------------------------------------------
why angular ..??
    we need a page synchronisation on a event basis,
    we can't write document.getElementById("#idName") every time
    we need a solution, that helps us manpulating the dom element efficienty...
    so ANGULR :)

npm install -g @angular/cli

version and additional information ::
    current version analysed : angular 1.7
        https://angularjs.org/
        https://ajax.googleapis.com/ajax/libs/angularjs/1.7.8/angular.js
        [tutorial]  https://www.tutorialspoint.com/angularjs/angularjs_environment.htm
                    https://www.tutorialspoint.com/angular4/
                    https://www.tutorialspoint.com/angular6/angular6_overview.htm

    current lts version : 10.15
    other version : 8.1.0-beta.0 (2019-05-30)
                    https://github.com/angular/angular
                    [https://github.com/angular/angular/blob/master/CHANGELOG.md] [important]

node js & npm
    node js [10.16.0 LTS] Node.js® is a JavaScript runtime built on Chrome's V8 JavaScript engine.
    more on mpm package manager : @[https://docs.npmjs.com/cli/install]

[https://angular.io/]
    Angular Augury : chrome extension for debugging angular application
    mgechev/codelyzer : static code analyser for angular application
    for more visit [https://angular.io/resources]
    architectural guide @[https://angular.io/guide/architecture]

angular template syntax : more about template syntax @[https://angular.io/guide/template-syntax]
    *ngFor
    *ngIf
    Interpolation {{ }}
    Property binding [ ]
    Event binding ( )
    [()]


Most Angular code can be written with just the latest JavaScript,
    > using types for dependency injection,
    > and using decorators for metadata.


console.trace();
-----------------------------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------------------------



after angular code initialised @ the -big- function get called by passing an argument of (window)
@ line number #37683
(function(window) { 'use strict'; .... }) (window); //here the -big- anonymous function is get called, with window argument..



then variable such as
    minErrConig(where error depth is decided)
    REGEX_STRING_REGEXP
    VALIDITY_STATE_PROPERTY
    hasOwnProperty
    lowercase
    uppercase have been initialised..
then @ line :302 lots of variables are initialised, 
where ngMinErr variable is initialised, by calling to minErr('ng') function,  @ :311
and by this time, following functions are initialised to javascript
    errorHandlingConfig
    isValidObjectMaxDepth
    minErr
    var lowercase = function(string) { .. }
    var uppercase = function(string) { .. }



**enum has more to do with sequencial storage date like array, properties are constant and readonly
**it have both bidirectional feature  (in the sense key=>value, value=>key)



@line no #1034  ||  @name angular.copy
<example module="copyExample" name="angular-copy">
  <div ng-controller="ExampleController">
  <label>Name: <input type="text" ng-model="user.name" /></label>
--module="copyExample" --name="angular-copy"
--ng-controller="ExampleController"
--ng-model="user.name"
<pre>form = {{user | json}}</pre>
<pre>leader = {{leader | json}}</pre>

angular.module('copyExample', []).controller('ExampleController', [
    '$scope', function($scope) {
    $scope.leader = {};
    $scope.reset = function() { $scope.user = angular.copy($scope.leader); //copying leader into user };
    $scope.update = function(user) {angular.copy(user, $scope.leader);};
    $scope.reset();
    }
  ]);
$scope is the watcher, to event on_change,on_update it is being called..



after then a lots of function and directive declaration happened, including ngCopy & others..
@line : 1738 function allowAutoBootstrap() being get called as follows [\/]
  var isAutoBootstrapAllowed = allowAutoBootstrap(window.document);



after then 
@ #1744 ngApp   @param{angular.Module}
Use this directive to **auto-bootstrap** an AngularJS application.
- with ngApp directive, the application is compiled and the "AppController" is instantiated
- ngApp is the way to bootstarp the application
angular.module('ngAppDemo', []).controller('ngAppDemoController', function($scope) {gontroller functtionality...});


@ #2264 angular.Module
@ #2308 A module is a collection of services, directives, controllers, filters, and configuration information.
The `angular.module` is a global place for creating, registering and retrieving AngularJS modules.


then @ line #3163 minErr() function is get called



then @ line #3616 forEach loop function get called
for which the following function call happened..
  forEach angular.js:836
  isFunction #836
  isArray #800
  anonymous inner function #3617
  variable lowercase is assigned a function..
  isString #742
  anonymous inner function #3617
  variable lowercase is assigned a function..
  ..



then @ line #3621 the second forEach loop get executed and the following function call happened
  forEach
  isFunction #836
  isArray #800
  (7-times) is a anonymous inner function #3622



after then @ #3646 forEach loop function get called, and the following function call happened
  forEach
  isFunction #836
  isArray #800
  isArrayLike
  isWindow #862
  isArray #800
  isString #742
  isNumber #765
  isBlankObject #724
  (4)anonymous inner function #3658



after then @ #3664 the next forEach loop function get executed, so the following function call happened
  property text: is a function #3740
  forEach
  isFunction #836
  isArray #800
  isArrayLike
  isWindow #862
  isArray #800
  isString #742
  isNumber #765
  isBlankObject #724
  anonymous function #3783



after then @ [ #3902 - #4118 ] the next forEach() loop get executed, and so the following function call happened
  forEach
  isFunction #836
  isArray #800
  isArrayLike
  isWindow #862
  isArray #800
  isString #742
  isNumber #765
  isBlankObject #724
  (2-times)anonymous inner function #4097



after then @ #4329 minErr() function get called



@ #4391
@name $injector
`$injector` is used to retrieve object instances as defined by
  {@link auto.$provide provider},
  instantiate types, invoke methods,
  and load modules.

  You can use this property to find out information about a module via the {@link angular.Module#info `myModule.info(...)`} method.
  var info = $injector.modules['ngAnimate'].info();

  The application developer is responsible for loading the code containing the modules; and for ensuring that lazy scripts are not downloaded and executed more often that desired.
  Previously compiled HTML will not be affected by newly loaded directives, filters and components.
  Modules cannot be unloaded.

  The {@link auto.$provide $provide} service has a number of methods for registering components with
  the {@link auto.$injector $injector}.
  Many of these functions are also exposed on {@link angular.Module}.

  An AngularJS **service** is a singleton object created by a **service factory**.
  These **service factories** are functions which, in turn, are created by a **service provider**.
  The **service providers** are constructor functions.
  When instantiated they must contain a property called `$get`, which holds the **service factory** function.
  
  When you request a service, the {@link auto.$injector $injector} is responsible for finding the correct **service provider**, instantiating it and then calling its `$get` **service factory** function to get the instance of the **service**.



Register a **service factory**, which will be called to return the service instance.
        * This is short for registering a service where its provider consists of only a `$get` property,
        * which is the given service factory function.
        * You should use {@link auto.$provide#factory $provide.factory(getFn)} if you do not need to
        * configure your service in a provider.

        * ```js
        *   $provide.factory('ping', ['$http', function($http) {
        *     return function ping() {
        *       return $http.send('/ping');
        *     };
        *   }]);
        * ```
        * You would then inject and use this service like this:
        * ```js
        *   someModule.controller('Ctrl', ['ping', function(ping) {
        *     ping();
        *   }]);



after then @ #5522 the minErr() function get executed, followed by in the line #8733 again minErr() got recalled



after then @ #8738 line, UNINITIALIZED_VALUE() function get called

nodeName = nodeName_(node); #10040
[#10887]
*   * `E`: element name
*   * `A': attribute
*   * `C`: class
*   * `M`: comment


after then @ #11772 minErr() function get called


after then @ #12107 minErr() function get called


after then @ #13942 minErr() function get called


after then @ #14369 minErr() function get called


after then @ #14711 minErr() function get called


after then @ #15059 with variable "locationPrototype" the |locationGetter - 4times - | function,
and |locationGetterSetter - 2times - |get called


after then with forEach() loop function #15365 the following functions get executed
  forEach
  isFunction #836
  isArray #800
  [3-times]anonymous inner function #15366


after then @ #15975 minErr() function get called

















