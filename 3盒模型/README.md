# 盒模型

## 盒模型概念

 ![盒模型](./box.gif)


总元素的宽度=宽度+左填充+右填充+左边框+右边框+左边距+右边距
总元素的高度=高度+顶部填充+底部填充+上边框+下边框+上边距+下边距

### 盒模型的小应用-制作三角形和箭头  

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        *{
            margin: 0px;
            padding: 0px;
        }
        body{
            background: yellowgreen;
        }
        div.arrow{
            height: 100px;
            width:100px;
            border-top:10px solid mediumvioletred;
            border-left:10px solid mediumvioletred;
            transform: rotate(225deg);
        }
        div.triangle{
            margin-top: 100px;
            height: 0px;
            width:0px;
            border-width: 100px;
            border-style:solid;
            border-color: aqua transparent transparent transparent;
        }
        div.rectangle{
            margin-top: 100px;
            height: 0px;
            width:0px;
            border-width: 100px;
            border-style:solid;
            border-color: aqua olivedrab gold blueviolet;

        }
    </style>
</head>
<body>
    <div class="arrow"></div>
    <div class="triangle"></div>
    <div class="rectangle"></div>
</body>
</html>
```
### 效果图
 ![盒模型](./box2.png)





