# 其他

## overflow：hidden

1. 隐藏溢出内容
2. 清浮动
3. 解决margin-top传递问题


## BFC
Block Formatting Context，中文直译为块级格式上下文。BFC就是一种布局方式，在这种布局方式下，
盒子们自所在的containing block顶部一个接一个垂直排列，水平方向上撑满整个宽度（除非内部盒子自己建立了新的BFC）。
- 两个相邻的BFC之间的距离由margin决定。在同一个BFC内部，两个垂直方向相邻的块级元素的margin会发生“塌陷”。
- 它决定了元素如何对其内容进行定位，以及与其他元素的关系和相互作用。当涉及到可视化布局的时候，Block Formatting Context提供了一个环境，
  HTML元素在这个环境中按照一定规则进行布局。一个环境中的元素不会影响到其它环境中的布局。
  通俗一点，可以把BFC理解为一个封闭的大箱子，箱子内部的元素无论如何翻江倒海，都不会影响到外部。

### 创建BFC：
1. float属性不为none
2. overflow不为visible(可以是hidden、scroll、auto)
3. position为absolute或fixed、sticky
4. display为inline-block、table-cell、table-caption、flex、inline-flex
5. 根元素html

### BFC 特性
- 内部的box会在垂直方向，一个接一个放着
- box垂直方向的距离由margin决定，属于同一个BFC的两个相邻box 的margin会发生重叠；
- BFC 的区域不会与float box重叠
- BFC 就是页面上一个独立容器，容器里面的子元素不会影响到外面的元素，反之亦然
- 计算BFC的高度时，浮动元素也参与其中 
