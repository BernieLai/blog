##怎样理解内容与样式分离的原则
在web页面中，html控制的是结构，css控制的是样式，js控制的是行为，要求结构、样式、行为分离目的在于降低耦合度，方便日后开发中的修改或者文件的复用
- 写HTML的时候先不管样式,重点放在HTML的结构和语义化上，让HTML能体现页面结构或者内容。之后再去写样式
- HTML 内不允许出现属性样式，尽量不要出现行内样式
- 写JS的时候，尽量不要用JS去直接操作样式，而是通过给元素添加删除class来控制样式变化
---
##有哪些常见的meta标签?
``` html
<!-- 关键字，搜所引擎 SEO -->
<meta http-equiv="keywords" content="关键字1,关键字2,..."> 
<!-- 页面描述 -->
<meta http-equiv="description" content="网页描述"> 
<!-- content的取值为webkit,ie-comp,ie-stand之一，区分大小写，分别代表用webkit内核，IE兼容内核，IE标准内核。 -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
<!-- 若页面需默认用极速核，增加标签： -->
<meta name="renderer" content="webkit">
<!-- 若页面需默认用ie兼容内核，增加标签： -->
<meta name="renderer" content="ie-comp">
<!-- 若页面需默认用ie标准内核，增加标签： -->
<meta name="renderer" content="ie-stand">
<!-- 如果安装了GCF，则使用GCF来渲染页面，如果没有安装GCF，则使用最高版本的IE内核进行渲染。
 X-UA-Compatible：这是个是IE8的专用标记,用来指定IE8浏览器去模拟某个特定版本的IE浏览器的渲染方式(比如人见人烦的IE6)，以此来解决部分兼容问题。 -->
<meta http-equiv="X-UA-Compatible" content="IE=Edge,chrome=1" >
<!-- 强制页面在当前窗口以独立页面显示。 -->
<meta http-equiv="Window-target" content="_top">
<!-- 自动刷新，并指向新的页面 -->
<meta http-equiv="Refresh" content="2；URL=http://">
<!-- 禁止浏览器缓存 -->
<!-- 是用于设定禁止浏览器从本地机的缓存中调阅页面内容，设定后一旦离开网页就无法从Cache中再调出
用法： -->
<meta http-equiv="pragram" content="no-cache"> 
<!-- 清除缓存（再访问这个网站要重新下载！） -->
<meta http-equiv="cache-control" content="no-cache, must-revalidate"> 
<!-- 设定网页的到期时间 -->
<meta http-equiv="expires" content="0"> 
<!-- 手机端 -->
<meta name="format-detection" content="telphone=no, email=no"/>
<!-- 忽略页面中的数字识别为电话，忽略email识别 -->
<meta name="apple-mobile-web-app-status-bar-style" content="black"/>
<!-- 设置苹果工具栏颜色 -->
<!-- 不让百度转码 -->
<meta http-equiv="Cache-Control" content="no-siteapp" />
<!-- 不缓存 -->
<meta http-equiv="cache-control" content="no-cache" />
<!-- 初始化设备 -->
<meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no, minimal-ui" />
<!-- 网站开启对iphone私有 web app 程序的支持 -->
<meta content="yes" name="apple-mobile-web-app-capable" />
<!-- 改变顶部状态条的颜色 iphone私有的属性-->
<meta content="black" name="apple-mobile-web-app-status-bar-style" />
```
---
##浏览器乱码的原因是什么？如何解决？
大多数原因是文档本身的编码与<meta charset>中声明的不符，导致浏览器解析错误
解决办法：
1. 设置<meta charset>标签声明文档使用的字符编码
2. 设置正确的字符编码
3. 设置浏览器显示正确的编码
---
##常见的浏览器有哪些？分别是什么内核？
- IE(4~11) *Trident*
- Edge *EdgeHTML*
- Chrome *Blink*
- Opera *Blink*
- Firefox *Gecko*
- Safari *Webkit*
- 一众国产浏览器 *IE内核+chromium内核*
---
##列出常见标签，并简单介绍用在什么场景
常见标签还挺熟悉的，就列几个容易混淆的吧
- 例如<em>和<i>，<b>和<stong>
虽然em标签也是显示为斜体的效果，但不能说因为效果一样就使用i标签来代替em标签。因为二者表示的含义不同，em还有表示强调，同样的道理也适用于<b>和<strong>标签。<em>和<strong>同样表示强调，但是<strong>的意味更重一些。
- html5的新标签<figure>
<figure>标签规定独立的流内容（图像、图表、照片、代码等等）。figure元素的内容应该与主内容相关，但如果被删除，则不应对文档流产生影响。