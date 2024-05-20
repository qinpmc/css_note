# 定位

## 绝对定位 postion:absolute
1. 可设置top、bottom、left、right值
2. 绝对定位元素脱离正常文档流（后面的元素会占据它原来的位置）,
3. 绝对定位元素的参照物为最近的具有定位属性的父元素（定位属性包含relative，fixed,absolute;如果没有，则为html根元素）
4. 如果同时设置top和bottom，只有top起作用；如果同时设置left和right，只有left起作用




```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .outer{
            height: 300px;
            width: 300px;
            background: rebeccapurple;
            /*position:relative;*/
        }
        .middle{
            height: 200px;
            width: 200px;
            background: yellowgreen;
            position:relative;
            left: 10px;

        }
        .inner{
            height: 100px;
            width: 100px;
            background: mediumvioletred;
            position: absolute;
            left: 50px;
            bottom: 0;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="middle">
            <div class="inner"></div>
        </div>
    </div>
</body>
</html>
```
## 绝对定位例子
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .pic{
            position: relative;
            width: 200px;
            height: 200px;;
        }
        .pic img{
            display: block;
            width: 100%;
            height: 100%;

        }
        .pic .bg{
            position: absolute;
            bottom: 0;
            left:0;
            width: 200px;
            height: 50px;
            background: rgba(0,0,0,0.5);
        }
        .pic .txt{
            position: absolute;
            height: 50px;
            line-height:50px;
            text-align: center;
            font-size: 16px;
            color: aquamarine;
            bottom:0;
            left: 0;
            width: 200px;
        }
    </style>
</head>
<body>
    <div class="pic">
        <img src="./播放.png" alt="">
        <div class="bg"></div>
        <div class="txt">Welcome</div>
    </div>
</body>
</html>
```
 ![绝对定位1](./absolute1.png)

### 绝对定位对块级元素和行内元素影响
与浮动类似，绝对定位的元素，块级元素不再独占一行，宽度由内容撑开；
行内元素支持设置宽和高，支持上下的padding/margin

## 相对定位 position:relative
* 不会脱离文档流，占位，后面的元素不会占据其原来的位置
* 如果同时设置top和bottom，只有top起作用；如果同时设置left和right，只有left起作用
* 其参照物为自身
* 相对定位元素的 margin / padding会让该文档空间产生偏移（和没有设置position效果/默认position 时一样）

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .outer{
            height: 300px;
            width: 300px;
            background: palegreen;
        }
        .inner1{
            height: 100px;
            width: 100px;
            background: blueviolet;
            position: relative;
            left:20px;
            top: 20px;
            margin:10px;
            z-index: 0;

        }
        .inner2{
            height: 100px;
            width:100px;
            background: yellow;
            position: relative;
            z-index: 1; /*设置position,该属性生效*/
        }
    </style>
</head>
<body>
    <div class="outer">
        <div class="inner1"></div>
        <div class="inner2"></div>
    </div>
</body>
</html>
```
 ![相对定位1](./relative1.png)



## 固定定位 position:fixed
* 会脱离文档流
* 如果同时设置top和bottom，只有top起作用；如果同时设置left和right，只有left起作用
* 参照物：整个浏览器窗口
* 可以设置z-index改变层级，值越大，越在上层

## z-index
1. 默认顺序是后面的定位元素覆盖前面的定位元素；
2. 可以用z-index 属性修改定位元素的层级关系；
3. 所有定位元素的z-index默认值是一样的；
4. z-index支持负数；
5. 一般都是同级元素进行层级的比较， 元素 z-index 值越大的在上方；如果父元素均有z-index,
先比较父元素之间的z-index（第一个父元素的z-index大于第二个父元素的z-index，第一个父元素的子元素的z-index小于
第二个父元素的子元素的z-index，第一个元素及其子元素仍会覆盖第二个元素及其子元素）


```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .parent1{
            width: 400px;
            height: 400px;
            background: blue;
            position: absolute;
            z-index: 2;
        }
        .son1{
            position: relative;
            z-index: 1;
            width: 200px;
            height: 200px;
            background: white;
        }
        .parent2{
            width: 300px;
            height: 300px;
            background: red;
            position: absolute;
            z-index: 1;
        }
        .son2{
            width: 100px;
            height: 100px;
            position: relative;
            z-index: 2;
            background: black;
        }

    </style>
</head>
<body>
<div class="parent1">
    <div class="son1"></div>
</div>
<div class="parent2">
    <div class="son2"></div>
</div>
</body>
</html>
```
 ![zindex](./z-index.png)

 

