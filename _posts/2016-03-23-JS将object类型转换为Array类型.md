---
layout: post
title:  "JS将object类型转换为Array类型"
date:   2016-03-23 20:10:54 +0800
categories: jekyll update
---
原文地址：[http://www.oschina.net/question/2608509_2158773](http://www.oschina.net/question/2608509_2158773)

{% highlight ruby %}
// 将Object的属性输出成Array
function objOfPropertyToArr(object) {
    var arr = [];
    var i = 0;
    for (var item in object) {
        arr[i] = item;
        i++;
    }
    return arr;
}
 
// 将Object的属性值输出成Array
function objOfValueToArr(object) {
    var arr = [];
    var i = 0;
    for (var item in object) {
        arr[i] = object[item];
        i++;
    }
    return arr;
}
 
/* 
* 测试
*/
var obj = {
    name: "oschina",
    age: "18"
}
objOfPropertyToArr(obj); // 输出["name", "age"]
objOfValueToArr(obj); // 输出["oschina", "18"]
{% endhighlight %}
