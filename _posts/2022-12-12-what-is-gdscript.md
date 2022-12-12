---
layout: post
title:  "甚麼是GDscript?"
date:   2022-12-12 08:39:48 +0800
categories: jekyll update
---
GDscript是Godot專用的程式語言，他的語法與Python或是Swift很相似，我會在這篇文章中盡我所能講解GDscript的使用方式 :D
## 函式(functions)
函式是一長串可以重複使用的程式碼，它可以幫助你更容易偵錯。
函式通常長這樣:
```
print("Hello, World!")
```
`print`是一個函式的名字，`()`表示要呼叫它(這個函式)，而`"Hello, World"`這個字串(`String`)會被傳遞到這個函式裡。
### 呼叫函式
可以使用`函式名稱(要傳遞的物件)`來呼叫一個函式
### 定義函式
在GDscript 中可以使用`func`關鍵字來定義一個函式，範例:
```
func say_hello():
    print('Hi!')
```
以上的程式碼會定義一個叫做`say_hello`的函式，可以使用`say_hello()`來呼叫。
當呼叫這個函式時，`print('Hi!')`會被執行。

我們也可以把這個函式修改一下:
```
func say_hello(name):
    print('Hello' + name + '!')
```

## 變數(variables)
有時後會需要把一個'值'儲存下來，像是玩家的血量，移動的速度等

這種時候就會使用變數，在GDscript中可以用`var`來定義變數，以下是一個範例:
```
var player_health = 100
```
這行程式碼會定義一個叫做`player_health`的變數並且把它的值設定為100，我們也可以在`var`前面加一個`export`關鍵字來讓它出現在編輯器的介面上。