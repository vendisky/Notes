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

作为最佳实践，component内部要避免运用$scope，controller内部用this替代，template中可以用$ctrl作为controller内部的this