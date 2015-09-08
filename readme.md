- create new directory in mean_vader directory named msNGr
- create index.html
- include skeleton css
- create app.js
- include AngularJS in application with CDN or download and include in app
- include angular app module in app.js

```
var app = angular.module('msNGr', []);
```

- include ng-app directive in HTML tag

```
<html ng-app="msNGr">
```

- create header in HTML
- create HeaderController in app.js with $scope

```
app.controller('HeaderController', ['$scope', function($scope){
  $scope.title = "msNgr",
  $scope.tagLine = "Facebook combined with Twitter... but not really"
}]);
```

- attach HeaderController to HTML

```
<header ng-controller="HeaderController">
```

- write expressions for header title and tagLine

```
<h1>{{title}}</h1>
<h4>{{tagLine}}</h4>
```

- load page in chrome
- create MessageController in app.js with $scope

```
app.controller('MessageController', ['$scope', function($scope) {
}]);
```

- attach MessageController to new div in HTML

```
<div ng-controller="MessageController">
```

- create $scope.messages object in app.js. Each message should contain a user, date created, and message with values for each.

```
$scope.messages =
    [
  {
    user: 'Tom',
    date: new Date('2015', '09', '09'),
    text: 'Backbone suuuuuuucks',
    image: 'http://i.dailymail.co.uk/i/pix/2014/07/05/article-2681224-1F678F7A00000578-381_634x843.jpg',
    likes: 0,
  },
  ```

- use ng-repeat directive to create a template for messages view (user, date, and message) inside the div with ng-controller="MessageController" directive. Use a filter to display the date.

```
<article ng-repeat="message in messages">
  UserName:<h3> {{message.user}} </h3>
  Date:<p> {{message.date | date}} </p>
  Message:<h5> {{message.text}} </h5>
  </article>
```

- include a new key:value pair for image: 'url' in messages object for each message
- using ng-source add an image with each message in the template on the index.html page

```
<img ng-src="{{message.image}}"><br>
```
- include some dynamically rendering views with interactivity
  - add a new key: value pair in our messages object likes: 0
  - in our MessageController we'll create 2 methods to add to likes and subtract for dislikes

  ```
  $scope.plusLike = function(index) {
    $scope.messages[index].likes += 1;
  };
  ```

  - Use ng-click directive on a button to perform the plusLike and minusLike methods

  ```
  <p ng-click="plusLike($index)"><button type="button" name="button">Like</button></p>
  ```

- ???
- Profit




### Labs
1. Write a basic angular app that uses expressions to list at least 5 attributes of a person.

2. Write a basic angular app that uses the ng-repeat method to list items in a to-do list. The list should have 4 attributes including a date created. Use a filter to include the date.

3. Write a basic angular app that uses ng-repeat to list out the 4 TMNT and their attributes of name, color, weapon, a picture, and number of Foot Soldiers killed(start the death count at 0). Also write a method that can add to their total of Foot Soldiers killed.
