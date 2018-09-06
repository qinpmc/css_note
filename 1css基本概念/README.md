# css 基本概念
* css 称为层叠样式表，cascading style sheets，用于规定HTML文档的呈现形式。

## css 引入方式(以下按照浏览器求索css属性值次序排列)
* 行内式
* 内嵌式（style中引入）
* 外链式（link导入）
* 用户样式（浏览器设置）
* 浏览器默认样式
* **内嵌式和外链式取决于引入的先后顺序，后引入的样式覆盖先引入的样式**
* **还可以使用导入式引入样式，@import ,但必须放在style标签或css文件中，且必须在首行**

## 外链式和导入式的区别
* link是html标签，@import是css提供的方式，要写在css文件或style标签中
* 加载顺序不同，当一个页面被加载时，link引用的css文件被同时加载，而@import引入的css文件会等页面全部下载完后再加载
* 使用js控制DOM去改变css样式时，只能用link标签，因为import不能被DOM控制

## import
* @import要写在css文件或style标签中，
 - 在style中：@import url(sheet2.css);或者@import url("sheet2.css");或者 @import "imp.css";
 - 在外部样式表中，@import url(sheet2.css);

* @import要写在其它css样式之前，如果在样式后面，会被忽略