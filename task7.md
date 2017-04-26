# task7
## 1.class 和 id 的使用场景?
一般原则是，类应该应用于概念相似的元素，这些元素可以出现在同一页面的多个位置，而ID应该用于不同的唯一元素上。

## 2.CSS选择器常见的有几种？
六种，分别是：
- 通用选择器 *
- 标签选择器 element
- ID选择器 #id
- 类选择器 .class
- 伪类选择器 a:hover
- 伪元素选择器 a::before

## 3.选择器的优先级是怎样的?对于复杂场景如何计算优先级？
一般情况下，从高到低排列：
1. 属性添加了!important有最高权限
2. 作为style属性写在元素标签上的行内样式
3. id选择器 #id
4. 类选择器 .class
5. 伪类选择器 a:hover
6. 属性选择器 input[text]
7. 标签选择器
8. 通配符选择器 *
9. 浏览器自带样式

复杂情况下：
**重要级别按高到低,a>b>c>d，高级权重相同时再比较低级别权重**
a：行内样式
b: id选择器
c: 类、属性和伪类选择器
d: 标签、伪元素选择器

## 4.a:link, a:hover, a:active, a:visited 的顺序是怎样的？ 为什么？
顺序如下 a:link a:visited a:hover a:active
原因如下：
因为 a:visited 在链接点击过一次之后永久生效，如果放在最后会覆盖掉其他的样式，在链接访问过一次之后 a:hover 和 a:active 样式都会被覆盖。
## 5.以下选择器的含义：
```HTML
#header{
}
<!-- id为"header"的元素-->

.header{
}
<!-- 类名为"header"的元素-->

.header .logo{
}
<!-- 类名为"header"的元素后代中类名为"logo"的元素-->

.header.moblie{
}
<!-- 类名同时为"header"和"moblie"的元素-->

.header p, .header h3{
}
<!--类名为"header"的后代元素中的所有p标签和所有的h3标签-->

#header .nav>li{
}
<!-- id为"header"的元素的后代中类名为"nav"的直接子元素中的li标签 -->

#header a:hover{
}
<!-- id为"header"的元素的后代中a标签处于hover状态时的样式 -->

#header .logo~p{
}
<!-- id为"header"的元素的后代中类名为"logo"之后的同级元素(.logo和p标签要有相同的父元素)中的p标签 -->

#header input[type="text"]{
}
<!-- id为"header"的元素后代中属性为"type="text"的input的标签 -->
```
## 6.列出你知道的伪类选择器
```
E:first-child       匹配元素E的第一个子元素
E:link              匹配未被点击的链接
E:visited           匹配点击过的链接
E:active            匹配当前被鼠标点下未释放的元素
E:hover             匹配鼠标悬停其上的元素
E:focus             匹配当前获得焦点的元素
E:lang(c)           匹配lang属性值等于c的元素
E:enabled           匹配表单中可用的元素
E:disabled          匹配表单中禁用的元素
E:checked           匹配表单中被选中的radio或checkbook元素
E:selection         匹配当前用户选中的元素
E:first-of-type     匹配父元素下使用同种标签的第一个子元素
E:first-child       匹配父元素下第一个子元素
```
## 7. div:first-child、div:first-of-type、div :first-child和div :first-of-type的作用和区别?
- div:first-child 属于其父元素的第一个子元素而且是div的元素
- div: first-of-style 属于其父元素所有子元素中首个div元素
- div :first-child是选择所有div元素中属于其父元素的首个子元素
- div :first-of-type 是选择所有div元素中属于其父元素的首个该类型的子元素
## 8.解释效果呈现的原因
- aa字体为红色： 
.item1:first-child  匹配元素item1的第一个子元素 aa，所以为颜色变为红色
- aa bb的背景色为蓝色：
.item1:first-of-type  匹配的是item1其父元素下相同类型子元素中的第一个，所以第一个p 第一个h3变蓝
