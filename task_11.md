## 什么是 CSS hack？
由于不同厂商的浏览器，比如Internet Explorer,Safari,Mozilla Firefox,Chrome等，或者是同一厂商的浏览器的不同版本，如IE6和IE7，  
对CSS的解析认识不完全一样，因此会导致生成的页面效果不一样，得不到我们所需要的页面效果。简而言之，CSS hack的作用就是使你的CSS代码兼容不同的浏览器。

## 谈一谈浏览器兼容的思路？
**做还是不做兼容？**
1. 产品的角度（产品的受众、受众的浏览器比例、效果优先还是基本功能优先）
2. 成本的角度 (有无必要做某件事)
**兼容做到什么程度？**
最低兼容到IE哪个版本？（一般来说IE是主要考虑对象）
**怎么去做这个兼容？**
1. 根据需求选择技术框架（jquery/vue/react/bootsrap等等）
2. 根据需求选择兼容工具（html5shiv.js、respond.js、css reset、normalize.css、Modernizr等等兼容工具）
3. postcss[用法介绍](https://segmentfault.com/a/1190000003909268)
4. 条件注释、css hack、js能力检测上做一些适配

## 列举5种以上浏览器兼容的写法？
- 清除浮动
```CSS
/* 非IE6~7浏览器*/
.clearfix:after{
  content: '';
  display: block;
  clear: both;
}
/* IE6~7浏览器*/
.clearfix{
  *zoom: 1;
}
```
- inlineblock 元素在IE6~7
```css
display{
  *zoom: 1;
  *display: inline;
}
```
- 兼容低版本ie可以使用合适的框架
```css
/*
Bootstrap (>=ie8)
jQuery 1.~ (>=ie6), jQuery 2.~ (>=ie9)
Vue (>= ie9)
*/
```
- img标签
img标签在IE6 7中左右会存在一个像素的间距，必须给img设置左浮动，img最好设置全局属性display: block

- 使用js兼容库
5.使用modernizr

## 以下工具/名词是做什么的？
- IE Hack：
针对IE浏览器编写不同的CSS的让IE能够正常渲染的过程
- js 能力检测：
检测浏览器的能力
- html5shiv.js：
用于解决IE9以下版本浏览器对HTML5新增标签不识别，并导致CSS不起作用的问题。
- respond.js：
用于为 IE6-8 以及其它不支持 CSS3 媒体查询功能的浏览器提供媒体查询的 min-width 和 max-width 特性，实现响应式网页设计。
- css reset：
将浏览器的默认样式全部去掉(过于暴力，不推荐使用)
- normalize.css：
可以定制的CSS文件
- Modernizr： 
在页面加载后立即检测特性；然后创建一个包含检测结果的 JavaScript 对象，同时在 html 元素加入方便你调整 CSS 的 class 名
- postCSS：
它可以被理解为一个平台，可以让一些插件在上面跑，它提供了一个解析器，可以将CSS解析成抽象语法树，  
通过PostCSS这个平台，我们能够开发一些插件，来处理CSS。热门插件如autoprefixer，它可以帮我们处理兼容问题，  
只需正常写CSS，autoprefixer可以帮我的自动生成兼容性代码
## 一般在哪个网站查询属性兼容性？
[caniuse](http://caniuse.com/)
