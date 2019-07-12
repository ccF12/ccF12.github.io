---
title: canvas
date: 2019-07-12 19:56:10
tags:
	- H5
categories: 前端
---
>本文主要讲述了H5的canvas标签的使用,关于画布和绘画

## 画布的创建
* 使用canvas标签初始化画布

`<canvas id="myCanvas"></canvas>`

* 在css中设置边框方便查看

```
#myCanvas{
			border: #FFFF00 groove 2px;
		}
```
<!-- more -->
* 在JavaScript中动态获取或者设置画布大小

```
myCanvas.width = 500;//js里设置宽高,直接使用id
myCanvas.height = 500;
```

* 绘画需要在Js中获得canvas元素

```
var mv = document.getElementById("myCanvas");
var cva = mv.getContext("2d");
```
## fileRect方形


**开始绘画时设置颜色和起始位置和大小**
* 第一个0是x
* 第二个0是y
* 80是width
* 100是height
* fillStyle设置颜色
* fillRect设置位置和大小


```
cva.fillStyle = "aqua"//颜色
cva.fillRect(0,0,80,100);//位置大小
```

由此画出一个长方形:  
![](https://s2.ax1x.com/2019/07/12/ZfWemt.png)

### 无填充色

```
cva.strokeStyle = "#FFFF00";//无填充色,同时也是线条的颜色
cva.strokeRect(100,100,80,100);//无填充色定位
```

![](https://s2.ax1x.com/2019/07/12/ZfWm0P.png)


## 绘画重新开始时,需要重置样式和路径

```
cva.beginPath();//重置当前路径点,清除样式
cva.closePath();//关闭路径点,起始和结束闭合
```

## 直线绘画
* moveTo设置起点位置
* lineTo设置到达位置
* fill开始绘画填充

```
cva.moveTo(20,100);
cva.lineTo(100,100);
cva.lineTo(100,200);
cva.lineTo(20,200);
cva.lineTo(20,100);
cva.fillStyle = "#0000FF";//填充颜色
cva.fill();//填充开始
```

![](https://s2.ax1x.com/2019/07/12/ZfWVOI.png)

## 圆形绘画
**context.arc(x,y,r,sAngle,eAngle,counterclockwise);**
* x:横向坐标
* y纵向坐标
* r半径
* sAngle起始点
* eAngle结束点
* counterclockwise绘制方向 false顺时针 true逆时针

```
cva.beginPath();
cva.arc(300,250,50,0,2*Math.PI,false);
cva.stroke();
```

![](https://s2.ax1x.com/2019/07/12/ZfWAld.png)