# task9
## 1.text-align: center的作用是什么，作用在什么元素上？能让什么元素水平居中？
text-align作为HTML元素属性其主要是用来文本水平居中的。text-align属性只能针对文本文字和img标签，对其他标签无效  
作用在block元素上，能让块级元素内的inline元素和inline-block元素水平居中
## 2.IE 盒模型和W3C盒模型有什么区别?
主要的区别在于width属性的划分，在IE盒模型中，*width=content的宽 +border +padding*；而在W3C盒模型中width单单指content的宽  
![w3c盒模型](https://github.com/BernieLai/blog/blob/master/task9/w3cbox.jpg?raw=true)
![ie盒模型](https://github.com/BernieLai/blog/blob/master/task9/iebox.jpg?raw=true)
## 3. *{ box-sizing: border-box;}的作用是什么？
让所有元素使用ie盒模型
## 4.line-height: 2和line-height: 200%有什么区别?
line-height: 2 行高等于内容高度的2倍  
line-height: 200% 是相对高度，行高等于父元素字体大小的200%
## 5.inline-block有什么特性？如何去除缝隙？高度不一样的inline-block元素如何顶端对齐？
具有inline的特性，不占据整行，宽度由内容宽度决定，又具有block的特性，能设置宽高，可以设置内外边距，但是有缝隙问题  
解决缝隙：在html文件中，将两个目标标签之间不留空隙或者或者在目标元素的父元素中设置：font-size：0；之后在子元素中把字体设置恢复  
顶端对齐：在inline-block元素中添加vertical-align：top；
## 6.CSS sprite 是什么？
CSS精灵图，是一种网页图片应用处理方式，将小图标合并在单个图片上  
这么做是因为每一次对图片的加载都会降低web的性能，这样可以减少网络请求,减轻服务器压力
## 7.让一个元素"看不见"有几种方式？有什么区别?
- opacity:0 变透明，仍占据空间
- vidibility:hidden 隐藏，仍占据空间
- display:none 消失，不占据位置
## 代码题
[第一题](http://js.jirengu.com/soquyuvoje/2/edit?html,css,output)  
[第二题](https://github.com/BernieLai/blog/blob/master/task9/demo2.jpg?raw=true)
