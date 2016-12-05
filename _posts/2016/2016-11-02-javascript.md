--- 
layout: post
title: javascript tittle tattle
categories:
- programming
tags:
- javascript
---

## language core  
构造函数问题：  
```
alert(cat1.constructor == Cat); //true
alert(cat2.constructor == Cat); //true
alert(cat1.instanceof Cat); //true
alert(cat2.instanceof Cat); //true
```

### Several ways to find this in javascript

1. Function Invocation Pattern
2. Method Invocation Pattern
   
    eg:
```
function car(){}
car.show = function(){
    return this;//this is the object car
}
```
3. Constructor Pattern
4. Apply Pattern

### sea.js example deploy problem (window7)
- 在gitbash中按照readme.md步骤不能执行成功，之后再cmd中交替执行结果可以执行成功，应该是环境变量的问题吧---->**TODO** 真是乱搞，还是之用cmd吧，用什么gitbash，要什么自行车！！！
- exports 本来是module.exports的一个引用，当只用module.exports（即exports）不够用的时候，此时可以对module.exports重新赋值，这样的话就能够有exports能够保留，module.exports也能够被当作另外的一个接口使用！！！
- seajs使用首先将sea.js引入到html文件中，教程中的使用spm安装的情况应该是 **node** 中使用的场景 
- 使用spm进行合并和压缩（eg：spm build main.js --combine --app-url zxx)

### ajax problem
- 无可奈何，为了实现异步中的异步，只能再发一次ajax请求不过结果倒也不错

### things about event
- 事件注册方法 ele.addEventListener(type,handler,flag),flag 是一个布尔值，true表示捕捉阶段执行，false表示事件冒泡阶段执行

### angularJs
- 模块中定义指令  
```
var app = angular.module("myApp",[]);
app.directive("runoobDirective",function(){
    return {
         template:"<!<h1>self define directive</h1>"
    }
});
```  

| directives | introduction |
|------------|:------------:|
|ng-init|initiate|
|
