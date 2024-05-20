# 1 display

display 是 CSS 中最重要的用于控制布局的属性。每个元素都有一个默认的 display 值，这与元素的类型有关。对于大多数元素它们的默认值通常是 block 或 inline 。一个 block 元素通常被叫做块级元素。一个 inline 元素通常被叫做行内元素。

- 其他 display 值：还有很多的更有意思的 display 值，例如 list-item 和 table

- 每个元素都有一个默认的 display 类型。不过你可以**随时随地的重写**它！常见的例子是：把 li 元素修改成 inline，制作成水平菜单。

# 2 margin 左右居中

```
#main {
        width: 600px;
        margin: 0 auto;
        background-color: yellowgreen;
      }
```

# 3 盒模型

总元素的宽度=content 宽度+左填充+右填充+左边框+右边框+左边距+右边距  
总元素的高度=content 高度+顶部填充+底部填充+上边框+下边框+上边距+下边距

# 4 position

## 4.1 static

static 是默认值。任意 position: static; 的元素不会被特殊的定位。一个 static 元素表示它不会被“positioned”，一个 position 属性被设置为其他值的元素表示它会被“positioned”。

## 4.2 relative

relative 表现的和 static 一样，除非你添加了一些额外的属性

## 4.3 fixed

一个固定定位（position 属性的值为 fixed）元素会相对于视窗来定位，这意味着即便页面滚动，它还是会停留在相同的位置。和 relative 一样， top 、 right 、 bottom 和 left 属性都可用。

## 4.4 absolute

absolute 是最棘手的 position 值。 absolute 与 fixed 的表现类似，但是它不是相对于视窗而是相对于最近的“positioned”祖先元素。如果绝对定位（position 属性的值为 absolute）的元素没有“positioned”祖先元素，那么它是相对于文档的 body 元素，并且它会随着页面滚动而移动。记住一个“positioned”元素是指 position 值不是 static 的元素。

# 5 float

布局中常用的 CSS 属性是 float 。Float 可用于实现文字环绕图片，如下：

```
img {
  float: right;
  margin: 0 0 1em 1em;
}


```

# 6 inline-block 布局

可以使用 inline-block 来布局。有一些事情需要你牢记：

- vertical-align 属性会影响到 inline-block 元素，你可能会把它的值设置为 top 。
- 需要设置每一列的宽度
- 如果 HTML 源代码中元素之间有空格，那么列与列之间会产生空隙
