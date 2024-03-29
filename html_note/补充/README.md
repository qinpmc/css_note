Emmet 常用语法介绍
绝大多数代码编辑器都支持 Emmet 语法，下面介绍一些常见的 Emmet 语法快捷键，根据下面的教程打开 jsbin测试吧~， 更多使用方法参考Emmet 文档

! 表示 输入!再按下 Tab

场景1

!
生成

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
</head>
<body>

</body>
</html>
场景2

p
生成

<p></p>
场景3

.header
生成

<div class="header"></div>
场景4

#header
生成

<div id="header"></div>
场景5

#header.logo
生成

<div id="header" class="logo"></div>
场景6

p#header.logo.layout
生成

<p id="header" class="logo layout"></p>
场景7

li*3
生成

  <li></li>
  <li></li>
  <li></li>
场景8

li*3>div.box
生成

  <li>
    <div class="box"></div>
  </li>
  <li>
    <div class="box"></div>
  </li>
  <li>
    <div class="box"></div>
  </li>
场景9

li*3>{hello}
生成

<li>hello</li>
<li>hello</li>
<li>hello</li>
场景10

li*3>{hello$}
生成

<li>hello1</li>
<li>hello2</li>
<li>hello3</li>
场景11

#header+#content+#footer
生成

  <div id="header"></div>
  <div id="content"></div>
  <div id="footer"></div>
场景12

(#header>.logo+.nav)+#content+#footer
生成

<div id="header">
  <div class="logo"></div>
  <div class="nav"></div>
</div>
<div id="content"></div>
<div id="footer"></div>