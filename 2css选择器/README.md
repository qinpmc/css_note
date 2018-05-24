# css 选择器

## css基本选择器

* 标签选择器，如：div{ color:red; }
* 类选择器 ,如：.class1{color:yellow;}
* Id选择器，如 #id1{ color:blue;}
* 通配符选择器 *
* 属性选择器，如[href]{ border:thin solid black}

## 属性选择器

* ![属性选择器](./attrselector.png)

E[attr|=val] :只能等于val，或以val-开头
E[attr*=val] :包含val字符串
E[attr~=val] :属性值多个，有一个是val；或仅有val
E[attr^=val] :以val开头
E[attr$=val] :以val结尾


### 示例
```
<!DOCTYPE html>
<html >
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        *{

        }
        [class~="class2"] {
            border: thin red solid;
            padding: 4px;
        }
        [lang|="en"] {
            border: thick blue dashed;
            padding: 4px;
        }
    </style>
</head>
<body>
    <a id="apressanchor" class="class1 class2" href="http://apress.com">
        Visit the Apress website
    </a>
    <p>I like <span class="class2">apples</span> and oranges.</p>
    <hr>
    <a lang="en-us"   href="http://apress.com">
        Visit the Bpress website
    </a>
    <p>I like <span lang="en-gb"  >apples</span> and oranges.</p>
    <a lang="en"  href="http://w3c.org">Visit the W3C website</a>
</body>
</html>
```
### 效果
* ![属性选择器效果](./res1.png)


## 复合选择器
* 并集选择器，如a,p{ color:red;}
* 后代选择器，如p span{ color:red;},包含p中任意的span，不仅仅是子元素
* 子选择器，如 p>span{ color:red;}
* 相邻兄弟选择器，如p+span{ color:red;}
* 普通兄弟选择器，如p~span{ color:red;}，包含所有的兄弟，不仅仅是相邻的，只包括p后面的兄弟元素，不包含p前面的兄弟

## 伪类选择器
### 动态伪类选择器
* :linked
* :visited
* :hover
* :active
* :focus

### 否定选择器
* :not，css3

### 伪元素选择器
* ::first-line
* ::first-letter
* :before :after ,会生成内容，如 a:before{content:"click here" }

### 结构性伪类选择器
* :first-child
* :last-child ，css3
* :only-child ,匹配父元素包含的唯一子元素，css3
* :only-of-type
* :nth-child(n),父元素的第n个子元素（从1开始），css3
* :nth-child(2n),父元素的偶数元素（从1开始），css3
* :nth-child(2n+1),父元素的奇数元素（从1开始），css3
* :nth-last-child(n),父元素的倒数第n个子元素，css3
* :nth-of-type ：同上nth-child，区别是区分类型（先对父元素下子元素分类，然后取不同子元素的对应的序号）

### UI伪类选择器
* :enabled
* :disabled
* :checked
* :valid
* :invalid
* :rquired
* :default
* :in-range
* :out-of-range
* :optional



### 示例
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style type="text/css">
        a{
            text-decoration: none;
        }
        a:link{color:red}
        a:hover{text-decoration:underline}
        a:active{background: yellow}
        a:visited{color:grey}

        li{
            border:solid 2px red
        }
        li:not(:last-child){
            border:solid 2px blue
        }
        /*该选择器指定的是 p为第一个子元素的元素，并非是指p的第一个子元素*/
        p:first-child{
            background: brown;
        }
    </style>
</head>
<body>
    <a href="http://www.sina.com">跳转去百度</a>
    <ul>
        <li>li1</li>
        <li>li2</li>
        <li>li3</li>
    </ul>
    <div>
        <p>this is a <span>test1</span> paragrph</p>
        <p>this is a <span>test2</span> paragrph</p>
        <p>this is a paragrph</p>
    </div>
</body>
</html>
```

### 效果
![伪类选择器效果](./res2.png)

<hr>

### 示例

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        *{
            margin:0px;
            paddong:0px;
        }
        li{
            list-style: none;
            display: inline-block;
        }
/*        li.suf:after{
            content: " |";
            margin:2px;
        }*/
        li:after{
            content:"";
            display: inline-block;
            width:2px;
            height: 20px;
            background: black;
            margin: 0 8px;
            vertical-align: bottom;
        }
    </style>
</head>
<body>
    <ul>
        <li class="suf">我是测试</li>
        <li>我是测试</li>
    </ul>
</body>
</html>
```

### 效果
 ![伪类选择器效果](./res3.png)

### 选择器权重
* !import 重要声明，权重最重，如 h1{ color:gray !import; background:red !import;}
* 行内样式，权重为1000
* id 选择器 ，权重为100
* 类选择器、属性选择器、伪类选择器，权重为10
* 元素选择器、伪元素选择器，权重为1
* 通配符选择器 ，权重0
* 继承的样式权重，没有特殊性，甚至连0都没有

### 继承

#### 不可继承的css属性
1. display
2. 文本属性（vertical-align,text-decoration,text-shadow,white-space等）
3. 盒模型属性（border、margin、padding、width、height）
4. 背景属性（background）
5. 定位属性，如float、clear、position、top、right、bottom、left、overflow、clip、z-index等
6. 生成内容属性，如content、counter-reset、counter-increment
7. 轮廓样式属性，outline

#### 可继承的css属性
1. font
2. 文本系列属性，如text-indent、text-align、line-hight、direction、color等




