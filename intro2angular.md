# -> AngularJS <-
### -> Superheroic JavaScript MVW Framework <-
-> ![Angular logo](http://www.invokemedia.com/wp-content/uploads/2015/07/angular.png) <-


---

## What is AngularJS?
 - [https://angularjs.org/](https://angularjs.org/)
 - Client side JS Framework
 - Add interactivity to HTML
 - MV... Whatever... just be dynamic


---

## 2-Way Data Binding
 - Code re-evaluated when a property changes
 -> ![2-Way Data Binding](http://www.dotnet-tricks.com/Content/images/angularjs/two-waybinding.png) <-

 ---

## Basic Components of Angular
- Modules
- Directives
- Expressions
- Filters
---

## Modules
- A module is a collection of services, directives, controllers, filters, and configuration information.
- Where we write pieces of angular app & define dependencies
- First thing to do is write Angular app module
```
var app = angular.module('appName', ['dependencies']);
```
---

## Directives
- A marker on a HTML tag that tells Angular to run or reference JS code. Binds behavior from JS function to HTML.
- Examples: ng-app - attach app module to html, ng-controller - attach controller to html, ng-show - show only if true, ng-hide - don't show if true, ng-repeat - like a for-in loop for app data template, ng-src - for including images from data, ng-click, ng-init, ng-class, ng-model, ng-submit, ng-route, etc. etc.
---
## Expressions
- Insert dynamic values into HTML {{can include JS logic inside}}
- Put the data into the app, and can be used to create templates.
- Perform logic ex: string concat or math
```
{{ "good, good" + "let the angular flow through you" }}
```
```
{{ 1+2 }}
```
---
## Controllers
- a Directive (ng-controller)
- Help get JS in HTML by defining functions and values. Controller names must be capitalized "NameController".
```
app.controller('HomeController', function(){

});
```
---
## Filters
- A filter formats the value of an expression for display to the user. They can be used in view templates, controllers or services and it is easy to define your own filter.
- Filters change data to look good in the view.
- Ex: currency, date, time, uppercase or lowercase, orderby: price
```
{{ data.value | filter:options }}
```
---
## $scope Object
- Both the controller MainController and the view index.html have access to $scope. This means we can use $scope to communicate between the controller and the view.
- Any new properties attached to $scope will become available to use in the view through the use of expressions.
```
app.controller('MainController', ['$scope', function($scope){
  $scope.title = "Cool Title",
  $scope.user = "Cool UserName"
}]);
```
