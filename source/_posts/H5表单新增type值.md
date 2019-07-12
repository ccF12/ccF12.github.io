---
title: H5表单新增type值
date: 2019-07-12 18:33:30
tags:
	- H5
categories: 前端
---

>本文主要列举了H5新增的表单Type的值,设定特殊的表单元素  

## "email" 
>验证邮箱，需要满足要求才能提交

`邮箱:<input type="email"/>`

![](https://s2.ax1x.com/2019/07/12/ZfNN8O.png)

<!-- more -->

## "tel"
>并不是验证号码，而是在移动端打开数字键盘，限制用户只能输入数字

`电话:<input type="tel"/>`

## "file"
>上传文件  

* multiple属性可以设置多选  

`文件:<input type="file" name="userFile" multiple />`

![](https://s2.ax1x.com/2019/07/12/Zf0y36.png)

## "url"
>验证网址，合法网址必要包含http://才能提交

`链接:<input type="url"value="http://" />`

![](https://s2.ax1x.com/2019/07/12/ZfNrVI.png)

## "number"
>只能输入数字包含小数点，可以手动增加减少，常用购物车商品数量  
  
* max最大值  
* min最小值  
* value默认值  

`数字:<input type="number"/>`

![](https://s2.ax1x.com/2019/07/12/ZfNGUx.png)

## "search"
>常用语搜索  

`搜索:<input type="search"/>`

## "range"
>设置范围  

* max最大值
* min最小值
* value默认值（默认为一半）

`数值:<input type="range" value="90" />`

![](https://s2.ax1x.com/2019/07/12/ZfNtPK.png)

## "color"
>设置颜色

* #开始，包含16进制格式的颜色值。例如：#FF0000为红色的16进制值。

`颜色:<input type="color" value="#ff0000"/>`

![](https://s2.ax1x.com/2019/07/12/ZfNU2D.png)

## "time"
>设置时间,时分秒,由于各浏览器实现方式不同,不推荐

`时间:<input type="time"/><br>`

## "date"
>设置年份 年月日  

`年份:<input type="date"/><br>`

![](https://s2.ax1x.com/2019/07/12/ZfN8V1.png)

## "datetime-local"
>设置年月日时分秒  

`时间集合:<input type="datetime-local"/>`

![](https://s2.ax1x.com/2019/07/12/ZfNJ56.png)