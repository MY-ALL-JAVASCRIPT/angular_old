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
    latest version : 8.1.0-beta.0 (2019-05-30)
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


Most Angular code can be written with just the latest JavaScript,
    > using types for dependency injection,
    > and using decorators for metadata.
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
    ar lowercase = function(string) { .. }
    var uppercase = function(string) { .. }
















