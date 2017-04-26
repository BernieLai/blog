# 任务6
---
## 1.CSS的全称是什么？
Cascading Style Sheets层叠样式表，用来表现HTML或者XML等文件样式的语言，能够对网页中元素位置的排班进行像素级的精确控制，支持几乎所有的字体字号样式拥有对网页对象和模型样式编辑的能力。

##2.CSS有几种引入方式? link 和@import 有什么区别?
一共有4中引入方式：
- 行内CSS，直接对标签使用 *style="XXXXX"*,如下：
```HTML
<h1 style="clolor: red;">
```
- 内嵌样式，将样式写在style标签之中。如下：
```HTML
<style type="text/css">
body, div, a{
	margin: 10px;
}
</style>
```
- 链接样式，最常使用的形式，将样式表地址放在link标签中。如下：
```HTML
<link rel="stylesheet" href="xxx.css">
```
- 导入样式，利用@import(这是css的语法)来导入：
```HTML
<style>
	@import url("xxx.css");
	@import "xxxx.css"
</style>
```
link和@import的区别：
- link 是 HTML 的一个标签，可以放在HTML中的任何一个位置，而 @import 是 CSS 提供的一种方法，需要放在 HTML 的 style 标签里，或是放在一个样式表里，不能直接放在 HTML 里。因此 link 除了加载 CSS 之外还做其他的事情，而 @import 就只能加载 CSS 了。
- link是在加载页面前把css加载完毕，而@import url() 则是读取完文件后再加载样式，所以如果遇到网速很慢的情况，会出现先显示没有样式的页面，然后在闪烁一下之后才出现样式。
- @import 是 css2 里提出的，所以古老的 ie5 浏览器不支持，而 link 则没有这个问题
- 当使用javascript控制dom去改变样式的时候，只能使用link标签，@import不是dom可以控制的

## 3.以下这几种文件路径分别用在什么地方，代表什么意思?
- css/a.css 相对路径，当前目录css文件夹下的a.css文件
- ./css/a.css 相对路径，当前目录css文件夹下的a.css文件
- b.css 相对路径，当前目录下的b.css文件
- ../imgs/a.png 相对路径，上级目录的imgs文件夹下的a.png文件
- /User/hunger/projects/css/a.css 绝对路径，本地路径/User/hunger/projects/css文件夹下的a.css文件
- /static/css/a.css 网络相对路径 
- http://cdn.jirengu.com/kejian1/8-1.png 网络路径

## 4.如果我想在js.jirengu.com上展示一个图片，需要怎么操作?
把图片上传服务器，然后引用相对路径；或者直接从别的网站获取图片的网络地址

## 5.html和 css 的书写规范
http://codeguide.bootcss.com/#html-syntax
里面很详细，不做累述。

## 6.截图介绍 chrome 开发者工具的功能区
![chrome开发者工具](http://upload-images.jianshu.io/upload_images/4028061-928a80b6fcfabd1b.jpg?imageMogr2/auto-orient/strip%7CimageView2/2)