
## 1.浮动元素有什么特征？对父容器、其他浮动元素、普通元素、文字分别有什么影响？
对元素设置浮动以后，元素会脱离文档流，根据设定的值向左或向右偏移，直到其边缘遇到父元素的边界或者另一个浮动元素的边框
对父元素的影响是如果父容器内的元素均设置了浮动，那么他们脱离普通流无法撑起父容器的高度，导致父元素的塌陷
对其他浮动元素的影响是同一父容器内的浮动元素按照设定的方向并排排列，当父元素的宽度不够时，后面的元素会向下移动，直到有足够的空间；如果浮动元素的高度不同，那么有可能挡住移动的路径
对普通元素的影响就是普通元素会把浮动元素当做不存在一样依旧按照文档流排列，，可能被会浮动元素遮盖
对文本的影响就是会围绕着浮动元素排列
## 2.清除浮动指什么？ 如何清除浮动？ 两种以上方法
清除浮动是指结合clear属性让父元素在视觉上包围浮动元素
而清除浮动的方法如下  
- 在父元素的子元素最后添加一个空div，并对其设置样式：clear:both
- 使用:after 伪元素 消除浮动
- 因为BFC可以包含浮动，因此可以让父元素生成一个新的BFC从而包围浮动的子元素。
## 3.有几种定位方式，分别是如何实现定位的，参考点是什么，使用场景是什么？
- absolute 绝对定位 根据不为默种定位方式认定位的第一个父元素进行定位
- static 默认值 没有定位，元素出现在常规的文档流中
- fixed 生成绝对定位的元素，相对于浏览器窗口进行定位
- relative：相对定位，相对于元素本身正常位置进行定位，通过top、bottom、left、right属性来设置偏移量。使用场 景为绝对定位设定参照物或对元素自身位置进行局部调整
- inherit 从父元素继承定位属性
- sticky：对象在常态时遵循普通流。它就像是 relative和fixed的合体，当在屏幕中时按常规流排版，当卷动到屏幕外 时则表现如fixed，然而兼容性太差，不推荐使用
## 4.z-index 有什么作用?？如何使用？
绝对定位的元素脱离了普通流，所以绝对定位的元素可以覆盖页面上的其它元素。这时可以通过给元素设置z-index属性来控制叠放顺序，该属性值越高，元素位置越上层
## 5.position:relative和负margin都可以使元素位置发生偏移，二者有什么区别？
区别是使用relative，只会影响使用了relative属性的单个元素，不会影响别的元素，而使用了负值margin属性元素会影响其他元素，因为margin会使元素在文档流中的位置发生偏移，它会放弃偏移之前占据的空间，紧挨其后的元素会填充这部分空间
## 6.BFC 是什么？如何生成 BFC？BFC 有什么作用？举例说明
块级格式上下文，其定义是：浮动、绝对定位（绝对定位、固定定位）元素、块级容器（如inline-block、 table-cell、table-caption）并不是块级盒子，还包括哪些overflow属性值取值visible以外的块级盒子，会为它们的内容物创建一个新的块级格式化上下文。对元素设置以下属性就可以生成BFC：
```CSS
float: left | right;
overflow: hidden | auto | scroll;
display: table-cell | table-caption | inline-block;
position: absolute | fixed;
```
BFC的作用：  
解决margin合并（margin collapse）问题，是指处于同一个BFC的相邻元素、嵌套元素，只要它们之间没有阻挡（如：边框、非空内容、padding等）就会发生margin合并。这是只要让其中一个元素生成新的BFC就能解决margin合并问题  

清除浮动。因为BFC可以包含浮动，所以让父容器生成新的BFC可以让父容器在视觉上包围了浮动的子元素，从而清除掉了浮动
## 7.在什么场景下会出现外边距合并？如何合并？如何不让相邻元素外边距合并？给个父子外边距合并的范例
发生外边距合并的条件：
必须是处于常规文档流（非float和绝对定位）的块级盒子,处于同一个BFC当中而且没有padding和border将它们分隔开，并且都属于垂直方向上相邻的外边距  
**合并规则： ** 
两个外边距都是正数，取两者之中的较大者  
两个外边距都是负数，取两者之间绝对值较大者  
当两个外边距一正一负时，取两者的和
## Code
- 第一题:  
[代码地址](https://github.com/BernieLai/blog/blob/master/task10/t10_d1.html)  
[预览地址](https://bernielai.github.io/blog/task10/t10_d1)
- 第二题：  
[代码地址](https://github.com/BernieLai/blog/blob/master/task10/t10_d2.html)  
[预览地址](https://bernielai.github.io/blog/task10/t10_d2)
- 第三题：  
[代码地址](https://github.com/BernieLai/blog/blob/master/task10/t10_d3.html)  
[预览地址](https://bernielai.github.io/blog/task10/t10_d3)
- 第四题：  
[代码地址](https://github.com/BernieLai/blog/blob/master/task10/t10_d4.html)  
[预览地址](https://bernielai.github.io/blog/task10/t10_d4)

