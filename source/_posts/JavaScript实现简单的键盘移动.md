---
title: JavaScript实现简单的键盘移动
date: 2019-07-12 16:43:07
tags:
	- JavaScript
	- Demo
categories: 前端
---
>用JavaScript实现键盘方向键控制移动  

![](https://s2.ax1x.com/2019/07/12/ZfixfO.gif)

<!-- more -->

* onkeydown 某个键被按下  
* onkeyup某个键被松开  
* event.keycode返回按键编码  

获取方块元素:  
`var box1 = document.getElementById("box1");`

设置初始速度和初始化方向
```
    var spane = 10;//初始速度
    var go = 0;//初始化方向
```

>绑定onkeydown事件获得按键编码

```
document.onkeydown = function (event) {
                event = event || window.event;
                //是否按下ctrl键,按住了速度+1,没有按住速度等于10
                event.ctrlKey ? spane += 1 : spane = 10;
                // 测试时用alert(event.keyCode);获得数值
                go = event.keyCode;//获得方向按键编码
            }
```

>调用定时器,在定时器里通过方面编码给方块设置style属性实现位移  

```
var tmer1 = setInterval(function () {
			switch (go) {
				case 37:
					box1.style.left = box1.offsetLeft - spane + "px";
					break;
				case 38:
                    box1.style.top = box1.offsetTop - spane + "px";
                    break;
                case 39:
                    box1.style.left = box1.offsetLeft + spane + "px";
                    break;
                case 40:
                    box1.style.top = box1.offsetTop + spane + "px"
                    break;
             clearInterval(tmer1);
                }
            }, 30);
```

完成.