---
layout: post
title:  "甚麼是GDscript?"
date:   2022-12-12 08:39:48 +0800
categories: jekyll update
---
GDscript是Godot專用的程式語言，他的語法與Python或是Swift很相似，我會在這篇文章中盡我所能講解GDscript的使用方式 :D

## 註解(comment)
註解是給人類看的「筆記」，註解不會被Godot執行。

在GDscript 中，我們會使用"#"來註解。
以下是一個範例:
```swift
#This is a comment
print("Hi!")
```
`#This is a comment` 就是一段註解，通常我們會用它們來描述一段程式會做甚麼，方便理解。
## 函式(functions)
函式是一長串可以重複使用的程式碼，它可以幫助你更容易偵錯。
函式通常長這樣:
```swift
print("Hello, World!")
```
`print`是一個函式的名字`()`表示要呼叫它(這個函式)，而`"Hello, World"`這個字串(`String`)會被傳遞到這個函式裡。
這個函式會把傳遞的物件顯示在終端上，用來debug很方便。
#### 呼叫函式
可以使用`函式名稱(要傳遞的物件)`來呼叫一個函式。
也有些函式不用傳遞任何東西，這樣的話我們只要留下空的括號就好了，範例:
```swift
print()
#如果沒有傳遞任何東西，print會空出一行。
```
#### 定義函式
在GDscript 中可以使用`func`關鍵字來定義一個函式，範例:
```swift
func say_hello():
    print('Hi!')
```
以上的程式碼會定義一個叫做`say_hello`的函式，可以使用`say_hello()`來呼叫。
當呼叫這個函式時，`print('Hi!')`會被執行。



我們也可以把這個函式修改一下:
```swift
func say_hello(name):
    print('Hello' + name + '!')
```
## 條件判斷(conditions)
在GDscript 中，有 `if`, `else`, `elif`這三種用來條件判斷的關鍵字，這些關鍵字能夠在條件滿足時執行一段程式碼，範例:

### if 
`if` 會在後面的條件是`True`時執行下面的程式碼。
```swift
if player.health <= 0:
    #如果玩家血量小於等於零
    player.die()
    #讓玩家死亡
```
### elif
`elif` 需要在 `if` 的下面才能起作用，`elif`會在上面的`if`條件不成立，且他後面的條件是`True`時執行下面的程式碼。
```swift
if player.score > 5000:
    # 如果玩家的分數大於5000
    player.stars = 3
    # 玩家能獲得三顆星
elif player.score <5000 and player.score > 3000:
    #或者如果玩家的分數小於5000但是大於3000
    player.stars = 2
    # 玩家能獲得兩顆星
```
`elif` 簡單來說就是「或者如果」。

### else
`else` 需要在`if`或者`elif`下面才能起作用，當上面的`if`，`elif`都是`False`時，`else`會執行下面的程式碼
```swift
if player.health <= 0:
    #如果玩家的血量小於等於零
    player.die()
    #讓玩家死亡
else:
    # 否則 (如果玩家血量大於零)
    player.health -= damage
    # 將玩家的血量扣除玩家受到的傷害
```

## 變數(variables)
有時後會需要把一個'值'儲存下來，像是玩家的血量，移動的速度等

這種時候就會使用變數，在GDscript中可以用`var`來定義變數，以下是一個範例:
```swift
var health = 100
```
這行程式碼會定義一個叫做`health`的變數並且把它的值設定為100，我們也可以在`var`前面加一個`export`關鍵字來讓它出現在編輯器的介面上。