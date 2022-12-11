# GDscript教學

## 甚麼是GDscript?
GDscript是Godot專用的程式語言，他的語法與Python或是Swift很相似，我會在這篇文章中盡我所能講解GDscript的使用方式 :D

## 變數
有時後會需要把一個'值'儲存下來，像是玩家的血量，移動的速度等

這種時候就會使用變數，在GDscript中可以用`var`來定義變數，以下是一個範例:
```
var player_health = 100
```
這行程式碼會定義一個叫做`player_health`的變數並且把它的值設定為100，我們也可以在`var`前面加一個`export`關鍵字來讓它出現在編輯器的介面上。
