---
layout: post
title:  "AngularJS学习笔记"
date:   2016-04-04 14:27:46 +0800
categories: jekyll update
---
项目地址：[https://github.com/cikai/angularjs.git](https://github.com/cikai/angularjs.git)

### 1. 数据绑定 data bind

    <textarea ng-model="text" type="text" placeholder="text here"></textarea>
    <p>正在输入： {{ text }}</p>

### 2. 模块 module

声明一个模块：

    // 第一个是模块的名称，第二个是依赖列表，也就是可以被注入到模块中的对象列表。
    angular.module('myApp', []);  // 类比require.js。

引用一个模块：

    angular.module('myApp');    // 类比require.js。

### 3. 作用域 scope

首先在<html>、<body>中声明：

    <html ng-app="appName">
    <body ng-controller="taskcontrol">

之后在angular.js中声明：

    angular.module('appName', [])
        .controller('taskcontrol', function($scope) { 
            code here ...
    })

button绑定click事件：

    <button ng-click="add()">button</button>

#### 注：将控制器命名为[Name]Controller而不是[Name]Ctrl是一个最佳实践。

默认情况下，AngularJS在当前作用域中无法找到某个属性时，便会在父级作用域中进行查找。如果AngularJS找不到对应的属性，会顺着父级作用域一直向上寻找，直到抵达$rootScope为止。如果在$rootScope中也找不到，程序会继续运行，但视图无法更新。

controller不要写进行DOM操作和数据操作的东西
