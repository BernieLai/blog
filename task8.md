# task-8
## 1.块级元素和行内元素分别有哪些？并说说他们的区别？
- 常见块级元素：h1~6, p, div, form, table, th, tr, td, ul, ol, li, dl, dt, dd, hr
- 常见行内元素：span, a, em, i, input, strong, br,
select, button
- 二者之间的区别：
1. 块级元素无论内容多少，都将占满一整行，而行内元素是根据内容长度决定的
2. 块级元素可以设置width和height，而行内元素不行
3. 块级元素设置margin,padding时盒模型正常扩展，而行内元素设置margin,padding时盒模型只有左右正常扩展，上下的区域不扩展，只有边框和背景时可以应用
4. 块级可以包含块级和行内，行内只能包含文本和行内
## 2.什么是 CSS 继承? 哪些属性能继承，哪些不能？
CSS 继承：子元素没有指定值的情况继承父元素的属性。
- 不可继承的：display、margin、border、padding、background、height、min-height、max- height、width、min-width、max-width、
overflow、position、left、right、top、 bottom、z-index、float、clear、table-layout、vertical-align、page-break-after、 
page-bread-before和unicode-bidi
- 所有元素可继承：visibility和cursor
- 内联元素可继承：letter-spacing、word-spacing、white-space、line-height、color、font、 font-family、font-size、font-style、
font-variant、font-weight、text- decoration、text-transform、direction
- 块状元素可继承：text-indent和text-align
- 列表元素可继承：list-style、list-style-type、list-style-position、list-style-image
- 表格元素可继承：border-collapse
## 3.如何让块级元素水平居中？如何让行内元素水平居中?
块级元素使用margin:0 auto; 行内元素使用text-align:center
## 4.实现一个三角形
[实现一个三角形](http://js.jirengu.com/lomucejocu/1/edit)
## 5.单行文本溢出加 ...如何实现?
```css
overflow: hidden;  /*多余的文字变成...*/
text-overflow: ellipsis; /*超过边框的文字隐藏*/
white-space: nowrap;/*文本不会换行，文本会在在同一行上继续，直到遇到 <br> 标签为止*/
```
## 6.px, em, rem 有什么区别?
px：像素
em：值并不是固定的，会继承父级元素的字体大小，是默认字体大小的倍数
rem：是一个相对单位，相对的只是HTML根元素，使用它既可以做到只修改根元素就成比例地调整所有字体大小，又可以避免字体大小逐层复合的连锁反应
## 7.解释下面代码的作用?为什么要加引号? 字体里\5b8b\4f53代表什么?
```css
body{
  font: 12px/1.5 tahoma,arial,'Hiragino Sans GB','\5b8b\4f53',sans-serif;
}
```
代码作用是设置字体大小12px、行高1.5和字体  
有的字体名称中间有空格，加引号是为了不让浏览器认为这是2种字体，例子 'Hiragino Sans GB'  
'\5b8b\4f53'是Unicode码编号，表示“宋体”;在控制用escape()函数可以查看对应的Unicode码
## 代码题：
