---
title: JS简单的鼠标跟随事件思路
date: 2019-07-11 22:13:05
tags:
	- JavaScript
	- Demo
categories: 前端
---

>简单的实现:设置一个方块,当鼠标移入窗口时,方块跟随鼠标,当鼠标移出时方块消失,提供思路,方块可替换素材  
![](https://s2.ax1x.com/2019/07/11/ZRRvQI.gif)
<!-- more -->
**设置方块**  
```
#box1 {
		width: 20px;
		height: 20px;
		position: absolute;//需要绝对定位方块才能移动
        }
```

**获得方块和body**
```
var box = document.getElementById("box1");
var bodywindow = document.documentElement;
```

**给body设置鼠标移入事件**
```
bodywindow.onmousemove = function (event) {
		event = event || window.event;
		//pageX,pageY当对于页面的坐标,不兼容ie8
		// var x = event.pageX;
		// var y = event.pageY;
		//由于浏览器不一样,认定的父元素不一致,所以需要这种方式获得父元素并获得滚动坐标
		var st = document.body.scrollTop || document.documentElement.scrollTop;
		var sl = document.body.scrollLeft || document.documentElement.scrollLeft;
		//设置偏移量,使用event封装的对象获得属性并且拼串获得string
		box.style.left = event.clientX + sl + "px";
		box.style.top = event.clientY + st + "px";
		box.style.backgroundColor = "aqua";
			}
```
**设置鼠标移出事件**
```
bodywindow.onmouseout = function () {
                box.style.backgroundColor = "white"
            }
```


**效果展示**
![](https://s2.ax1x.com/2019/07/11/ZRRvQI.gif)