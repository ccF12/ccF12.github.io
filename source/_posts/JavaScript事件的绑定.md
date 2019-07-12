---
title: JavaScript事件的绑定
date: 2019-07-12 16:19:58
tags:
	- JavaScript
categories: 前端
---
>本文阐述了原生JavaScript事件的绑定和增加绑定以及兼容方式  

## 事件的绑定:
>对象.事件 = function(){};  


* 响应函数都会传进一个封装的事件响应对象event
* event.target,返回事件响应元素

<!-- more -->

```
bodywindow.onmousemove = function (event) {
	alert("鼠标移入了");
	}
```
**会被相同的事件重置**

### 解决重置:
>对象.addEventListener("-on事件",回调函数,是否捕获时执行布尔值);

```
bun.addEventListener("click", function () {
                alert(1);
            }, false);
```
**ie8以下不支持**
>ie8以下可以使用对象.attachEvent("事件",回调函数);-后绑定先执行  

```
obj.attachEvent(onmousemove,function(){
                        callback.call(obj);
                    })
```


## 兼容方式:
```
function bing(obj,clickstr,callback){
                if(obj.addEventListener){
                    obj.addEventListener(clickstr,callback,false);
                }else{ 
                    obj.attachEvent("on"+clickstr,function(){
                        callback.call(obj);
                    });
            }
            }
```
