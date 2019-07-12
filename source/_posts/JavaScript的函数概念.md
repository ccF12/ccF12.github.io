---
title: JavaScript的函数概念
date: 2019-07-12 15:57:17
tags:
	- JavaScript
categories: 前端
---
>本文阐述了Function的声明和调用  
`var fun = new Function();`  
<!-- more -->

>function函数也是一个对象,封装一些代码使用typeof检查一个函数时,会返回function  

## 创建函数:
`var fun = new Function();`
* 封装代码写在括号内  

`var fun = new Funvtion("console.log('Hello');");`

## 声明函数:
* Function 函数名(形参一,形参二){方法体};  

```
Function fun(String str,Number i){
                docunment.write(str,i);
            }
```

## 函数表达式:
* var 函数名 = Funvtion(形参,形参N){方法体}  

```
var fun = Function fun(String str,Number i){
                docunment.write(str,i);
            }
```

## return:
* return后返回并结束函数语句
* return后不写返回值,返回undefined,不写return也返回undefined

## 调用函数:
`fun();`
* 调用函数不会检查实参的类型和数量
* 多余的实参不会被赋值,实参少于形参,没有对应实参的形参会赋值为undefined

### 匿名函数的调用:
```
(Function(){
                docunment.write("匿名函数");
            })();

```
* 立即执行,只执行一次

## 方法
>一个函数被对象属性保存,则被称为对象的方法.  

```
obj.name = Function(){
            document.write("赋值给对象属性")
        };
```
* 函数的call()和apply()方法,可以将对象设置为参数,这样可以将函数中指向的this让对象调用

`fun.call(obj);`

* call(),可以在对象之后以此传递实参

`fun.call(obj,1,2);`

* apply(),需要把实参封装到数组中进行传递

`fun.apply(obj,[1,2]);`

* arguments封装实参,argumens[index]可以访问实参