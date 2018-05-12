# 其他

## overflow：hidden

1. 隐藏溢出内容
2. 清浮动
3. 解决margin-top传递问题


## BFC
Block Formatting Context，中文直译为块级格式上下文。BFC就是一种布局方式，在这种布局方式下，
盒子们自所在的containing block顶部一个接一个垂直排列，水平方向上撑满整个宽度（除非内部盒子自己建立了新的BFC）。
两个相邻的BFC之间的距离由margin决定。在同一个BFC内部，两个垂直方向相邻的块级元素的margin会发生“塌陷”。
通俗一点，可以把BFC理解为一个封闭的大箱子，箱子内部的元素无论如何翻江倒海，都不会影响到外部。

## 创建BFC：
1. float属性不为none
2. overflow不为visible(可以是hidden、scroll、auto)
3. position为absolute或fixed
4. display为inline-block、table-cell、table-caption