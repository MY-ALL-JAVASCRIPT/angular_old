-----------------------------------------------------------------------------------------
why angular ..??
    we need a page synchronisation on a event basis, with database
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
**it have bidirectional reading feature  (in the sense key=>value, value=>key)



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
[[ -- end of 6th foreach loop -- ]]
after then @ #15975 minErr() function get called & function scope ends @ line #16011


then we are calling to createMap() function with below expression. from line no #16014
var OPERATORS = createMap();

after than forEach loop get executed, so we are calling to below functions
forEach(), isFunction(), isArray()

--
then next function call calls to minErr() happens @ line number #20623
then next function call calls to minErr() happens @ line number #22036
then next function call calls to minErr() happens @ line number #22299
--


after than, @ line #22478, we called function urlResolve() & followed by isString()

than @line #23642 we, calling dateGetter() function for several times.. along with dateStrGetter(), weekGetter() as well..

after than on line #23911 we called function valueFn()
& next call to valueFn() function is from line #23939
after than, the next call to valueFn() happened from line #24814



than @ line #25188 forEach() function loop get executed for 8 itteration & the following function get executed
  #1st iteration
    forEach
    isFunction
    isArray
    isArrayLike
    isWindow
    isArray
    isString
    isNumber
    isBlankObject
  #2nd iteration
    anonymous inner function #25189
  #3rd iteration
    anonymous inner function #25189
    directiveNormalize #11663
    anonymous inner function #11667
  #4th iteration
    anonymous inner function #25189
    directiveNormalize #11663
    anonymous inner function #11667
  #5th iteration
    anonymous inner function #25189
    directiveNormalize #11663
    anonymous inner function #11667
  #6th iteration
    anonymous inner function #25189
    directiveNormalize #11663
    anonymous inner function #11667
  #7th iteration
    anonymous inner function #25189
    directiveNormalize #11663
    anonymous inner function #11667
  #8th iteration
    anonymous inner function #25189
    directiveNormalize #11663
    anonymous inner function #11667

after than @ line #25226 forEach() function get execuetd for 7 iterations, & the following function call happened.
  #1st iteration
    forEach
    isFunction #836
    isArray #800
    isArrayLike
    isWindow #862
    isArray #800
    isString #742
    isNumber #765
    isBlankObject #724
  #2nd iteration
    anonymous inner function #25227
  #3rd iteration
    anonymous inner function #25227
  #4th iteration
    anonymous inner function #25227
  #5th iteration
    anonymous inner function #25227
  #6th iteration
    anonymous inner function #25227
  #7th iteration
    anonymous inner function #25227

than @ line #25255 the next forEach() loop for 4 iterations & the following function calls happened
  #1st iteration
    forEach
    isFunction #836
    isArray #800
  #2nd iteration
    anonymous inner function #25255
    directiveNormalize #11663
    anonymous inner function #11667
  #3rd iteration
    anonymous inner function #25255
    directiveNormalize #11663
    anonymous inner function #11667
  #4th iteration
    anonymous inner function #25255
    directiveNormalize #11663
    anonymous inner function #11667

after than @ line #25304 calls to function valueFn(), happened

than @ line #25666, calls to addSetValidityMethod() happened

after than @ line #25959 & @ line #25951 formDirectiveFactory() function get called

after than @ line #26099 function createMap() get called. followed than,,
@ line #26100 forEach() loop function get executed for 6 iterations
  #1st iteration
    forEach
    isFunction #836
    isArray #800
  #2nd iteration
    anonymous inner function #26101
  #3rd iteration
    anonymous inner function #26101
  #4th iteration
    anonymous inner function #26101
  #5th iteration
    anonymous inner function #26101
  #6th iteration
    anonymous inner function #26101

after than @ line #26105 variable "inputType" is initialised.
var inputType = {...};
for which below function calls execuetd
  createDateParser #27523
  createDateInputType #27584
  createDateParser #27523
  createDateInputType #27584
  createDateParser #27523
  createDateInputType #27584
  createDateInputType #27584
  createDateParser #27523
  createDateInputType #27584

than @ line #28810 function valueFn() get called

--
than after @ line #29165 classDirective() function get called
after tahn @ line #29274 classDirective() function get called
after than @ line #29384 classDirective() function get called
--

than @ line #29438, calling ngDirective() function, so there by calling,,
other two functions such as : isFunction() & valueFn()

than @ line #29935 forEach() loop function get executed for 19 iteration,
there by calling the following functions

  #1st Iteration
    forEach
    isFunction #836
    isArray #800
  #2nd Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #3rd Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #4th Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #5th Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #6th Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #7th Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #8th Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #9th Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #10th Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #11th Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #12th Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #13th Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #14th Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #15th Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #16th Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #17th Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #18th Iteration
    directiveNormalize #11663
    anonymous inner function #11667
  #19th Iteration
    directiveNormalize #11663
    anonymous inner function #11667

--
after than @ line #30918 we called function ngDirective(), followed by isFunction() & valueFn() function.

than we called minErr() function @ line #31090

after than @ line #32234 we called function addSetValidityMethod()
than @ line #32588 we called ModelOptions() function


after than @ line #33124 we called function ngDirective() #24793 & there by we called function isFunction() #836, valueFn() #651

than @ line #33130 we called function minErr() function
after than, @ line #34357, we called minErr() function

than @ line #35585, ngDirective() function get called, followed,, isFunction() & valueFn() is get called.

after than @ line #35806 we called ngDirective() function, so followed by isFunction(), valueFn() function is also get called.

after than @ line #35827 ngDirective() function get called & so there by we called isFunction(), valueFn() function.

than @ line #35997 we called minErr() function

than @ line #37528 we called bindJQuery() function, & there by we also called
"var jq is a function  #1384" & "isDefined #694" & "isUndefined #677"


after than we called publishExternalAPI() function @ line #37530 & so there by the following function call happened.
  publishExternalAPI #2871
  extend
  baseExtend
  isObject #712
  setHashKey
  setupModuleLoader #2283
  minErr
  minErr
  inner function ensure() #2287
  inner function ensure() #2287
  inner function ensure() inside setupModuleLoader() #2296
  module() inner function inside ensure() > inside setupModuleLoader() #2351
  var assertNotHasOwnProperty is a function inside module() ensure() > setupModuleLoader() #2354
  inner function ensure() #2287
  invokeLater is a inner function #2659
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLater is a inner function #2659
  invokeLater is a inner function #2659
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLaterAndSetModuleName is a inner function #2674
  is a anonymous function inside > inside invokeLater() #2662
  property info: is a function #2420
  isDefined #694
  isObject #712
call to publishExternalAPI() function ends here.


than @ line #37532 call to angular.module() function happens, hence call to below functions happened.
  module() inner function inside ensure() > inside setupModuleLoader() #2351
  var assertNotHasOwnProperty is a function inside module() ensure() > setupModuleLoader() #2354
  inner function ensure() #2287
  invokeLater is a inner function #2659
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLater is a inner function #2659
  invokeLater is a inner function #2659
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLaterAndSetModuleName is a inner function #2674
  invokeLaterAndSetModuleName is a inner function #2674
  is a anonymous function inside > inside invokeLater() #2662



& than @ line #37678 we called function, jqLite()
  isString #742
  JQLite #3296
  isString #742
  isFunction #836
  jqLiteReady #3568


than @ line #37685 the following function call happened
!window.angular.$$csp().noInlineStyle && window.angular.element(document.head).prepend(...)
& there by the following function call happened..
  csp declared as a function #1316
  isDefined #694
  Inner function, noUnsafeEval #1334 declared inside csp=function() #1334
  JQLite #3296
  isString #742
  JQLite #3296
  isString #742
  isFunction #836
  jqLiteAddNodes #3489
  JQLite.prototype[name] is a function #4102
  isUndefined #677
  property prepend: is a inner function #3999
  JQLite #3296
  isString #742
  varibale trim is a function #916
  isString #742
  jqLiteParseHTML #3265
  jqLiteBuildFragment #3231
  jqLiteIsTextNode #3210
  concat #1400
  forEach
  isFunction #836
  isArray #800
  anonymous inner function #3258
  jqLiteAddNodes #3489
  forEach
  isFunction #836
  isArray #800
  isArrayLike
  isWindow #862
  isArray #800
  isString #742
  anonymous inner function #4003
  isDefined #694
  isDefined #694


--------------- END OF PROGRAMME FILE ---------------
after then the below function call happened

trigger is a inner function #3570
jqLite #37679
angularInit #1895
forEach
isFunction #836
isArray #800
forEach
isFunction #836
isArray #800


--------------- END OF PROCEDURE CALLS ---------------




































------------------------------------------------------------------
sandboxing code::

(sandboxing : A sandbox is a testing environment that isolates untested code changes and outright experimentation from the production environment or repository,[1] in the context of software development including Web development and revision control.)

(sandboxing : sandboxing iframe, causes lazy loading of the videos
that means, video is not being auto played, for example from source such as instagram)

angular.js is not sandboxed
description N/A


###
from local storage value, it's not allowed to remove value through index, so it's requires to remove all the nodes and then reassign the array

###
advantage of using javascript over java,,

automatic object-property propagation, happens in javascript,,
angular.js takes advantage of the system,
indexed zero property propagatioon, that allows both synchronous & asynchronus class-property propagation.


php - without a clone operator, the object's property value is auto propagating,, through new instances..



-- : end of documentation : --
