# angular tutorial

[link](https://code.angularjs.org/1.5.6/docs/tutorial)

### 0

ng-app是一个directive，定义一个angular module

从ng-app开始，为root scope

<br/>

### 2

$scope是和controller绑定的

$scope是继承的，依靠prototypal inheritance（原型继承，在JavaScript的教程中看过，但是没有深入了解）

<br/>

### 3

component是类似directive的抽象

好处有两点：1. 可以复用。2. isolate scope，没有原型继承，可以避免命名冲突

作为最佳实践，component内部要避免运用$scope。controller内部用this替代，template中可以用$ctrl作为controller内部的this

<br/>

### 4

如何使代码更加模块化？

1. One Feature per File

2. Organizing by Feature，就是同一个特性的几个部件，放同一个文件夹中

<br/>

### 7

var self = this; 这是因为回调函数中，this的值没有定义

$http是angular的内置service。因为有依赖注入，所以直接函数传参即可

As a naming convention, Angular's built-in services, Scope methods and a few other Angular APIs have a $ prefix in front of the name.

<br/>

### 8

ngSrc directive, which prevents the browser from treating the Angular {{ expression }} markup literally.

<br/>

### 9

$locationProvider.hashPrefix('!'); Setting a prefix is not necessary, but it is considered a good practice.

<br/>

### 14

 Be sure to use jQuery version 2.1 or newer, when using Angular 1.5; jQuery 1.x is not officially supported. In order for Angular to detect jQuery and take advantage of it, make sure to include jquery.js before angular.js