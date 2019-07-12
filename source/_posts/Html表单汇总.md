---
title: html表单汇总
date: 2019-07-11 21:07:58
tags:
	- html
	- 表单
categories: 前端
---
>不包含h5
### form标签
  form是表单标签,属性action是服务器地址  
 `<labie>`设置表达提示文字 其中可以设置属性for="id"  
 `<fieldset>`设置分组 其中再使用`<legend>`可以设置分组名
```
<form action="#">
</form>
```

>表单元素必须在form标签中  

#### type
**input type="text"为文本输入框**  
**input type="passworld"为密码框,设置name值指定回调**  
**input type="submit"为提交按钮,可以在后面加value属性指定显示的文字**  
* 当希望提交到服务器时,需要给此属性加上name指定唯一性  
* value可以指定默认值  
* disabled = "disable" 不可用  
```
用户:<input type="text" name="uesrname" />
密码:<input type="password" name="uesrpassworld" />
<input type="submit" value="提交" />
```
![](https://s2.ax1x.com/2019/07/11/ZRdADs.png)
***

<!-- more -->
**input type="radio单选框"**  
* name属性设置同一个组  
* value属性设置回调
```
性别<input type="radio" name="man" value="man" />男
	<input type="radio" name="man" value="wuman" checked="checked" />女
```
![](https://s2.ax1x.com/2019/07/11/ZRdkuj.png)
***
**input type="checkbox"多选框**
* name属性设置分组
* value设置属性回调
* checked="checked"默认选中
```
最爱的游戏:<input type="checkbox" name="game" value="1" />刺客信条
		  <input type="checkbox" name="game" value="2" />巫师3
		  <input type="checkbox" name="game" value="3" />地铁2033
		  <input type="checkbox" name="game" value="4" />赛博朋克2077
```
![](https://s2.ax1x.com/2019/07/11/ZRdivQ.png)
***
**select 设置下拉列表**
* name属性  
* option标签设置拉下选项  
* value属性回调
* selected="selected"默认选中
* multiple="multiple"设置为多选下拉列表
* `<optgroup label="组名">`可以设置下拉列表的分组
```
游戏:<select name="game">
		<option value="1">刺客信条</option>
		<option value="2">巫师3</option>
		<option value="3">地铁2033</option>
		<option value="4" selected="selected">赛博朋克2077</option>
	</select>
```
![](https://s2.ax1x.com/2019/07/11/ZRdEbn.png)
***
**textarea设置文本域**
* placeolder设置提示文字  
**`<input type="reset" value="reset" />`**
**`<input type="button">` 空白按钮**
```
<textarea name="myself" id="me" cols="30" rows="10" placeholder="自我介绍"></textarea>
```
![](https://s2.ax1x.com/2019/07/11/ZRdPgg.png)