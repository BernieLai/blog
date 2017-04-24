这篇博客就作为今天视频课的记录
- 表单的所有内容都需要放在form标签之内
- form的"action"属性用来指定处理该表单的后台程序URL, "method"属性用于指定传送数据的方式POST还是GET(默认)
- input标签的"placeholder"属性用于展示提示语
- label标签用于关联控件常与input标签一起使用 label的"for"属性一般与input的"id"属性一致(绑定)
- form的"type"属性用于指定form的形式，默认是"text"(普通文本输入框),"radio"（单选框），"checkbox"（多选框），"password"（密码框），"file"（文档框），"submit"（提交按钮），"hidden"（隐藏）
- - textare标签用于输入多行文本
- select标签和option标签用于展示下拉菜单，示例如下：
``` html
<select>
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="opel">Opel</option>
  <option value="audi">Audi</option>
</select>
```
**需要注意的是**
- label的"value"的值控件输入或选择的内容
- type为hidden的表单多用于安全性验证
- 单选框中 name相同的值为一组，只能在一个组内单选
