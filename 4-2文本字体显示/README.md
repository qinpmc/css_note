## display
 块级：block，list-item,table
 行内：inline(默认),inline-table,inline-block;
 
 ```
 <p>p1</p>                    <!--display: block;-->
 <div>div1</div>              <!--display: block;-->
 <span>span</span>            <!--display: inline;-->
 图片：<img src="" alt="">   <!--display: inline;-->
 <table>                      <!-- display: table;-->
     <thead>                  <!--display: table-header-group;-->
         <tr>                 <!--display: table-row;-->
             <th>Company</th>    <!-- display: table-cell;-->
             <th>Address</th>
         </tr>
     </thead>
     <tbody>                   <!--display: table-row-group-->
     <tr>
         <td>Apple, Inc.</td>   <!-- display: table-cell;-->
         <td>1 Infinite Loop Cupertino, CA 95014</td>
     </tr>
     </tbody>
 
     <ul id="ul1">     <!--display: block;-->
         <li>li1</li>   <!--display: list-item-->
         <li>li2</li>
         <li>li3</li>
     </ul>
 
 ```
 
 ### inline-block
- 既呈现inline特性（不占据一整行，宽度有内容宽度决定），又呈现block特性（可设置宽度，内外边距）
- 缝隙问题（可包裹div，设置div font-size:0）
- 高度不一样的inline-block元素  可采用 vertical-align: top;  顶端对齐
 
```
<style type="text/css">
        .box{
            font-size: 0;  /*去除 两个span间的空格*/
        }
        .inlineBlock{
            font-size: 16px;
            border: 1px solid black;
            width: 50px;
            display: inline-block;
            vertical-align: bottom; // 底部对齐，否则文字的基线对齐
        }
        .span1{
            padding: 20px;
            background: red;
        }
        .span2{
            padding: 40px;
            background: yellow;
        }
    </style>
</head>
<body>
    <div class="box">
        <span class="inlineBlock span1">
            Hello
        </span>
        <span class="inlineBlock span2">
            Hello
        </span>
    </div>
</body>
```
 
 
 
 ## font
 font-size / font-family / font-weight 文字粗度（normal，bold,bolder,lighter），可继承
 font-style 字体风格(italic/oblique/normal/inherit)

 - 采用复合写法时，font-size 和font-family在最后2个，且必须有这2个
 - css设置字体时，直接写成中文或英文名称浏览器能够识别，如 微软雅黑；但直接写中文的情况下编码不匹配时会产生乱码，保险  
 的方式是将字体名称用Unicode来表示。 
 
 
 中文名称  英文名称      Unicode   
 宋体      Simsun       \5B8B\4F53   
 
 获取Unicode码：控制台 escape("微软雅黑")， 将 %u 替换为 \ 
 
 
 
```
 p{
     /*font:italic 16px/20px arial,sans-serif ;*/ /*字体最后，16px --字体大小 ，20px --line-height*/
     font:italic 16px arial,sans-serif ;
     /*line-height: 200%; */   /* line-height= 32px,百分比相对于字体大小 */
     line-height: 1.5em;  /* line-height= 24px,百分比相对于字体大小 */
```

## 文本

text-align :left /center/ right/ justify  
text-indent: 第一行缩进距离   
text-decoration: none/underline/line-through/overline
color：颜色   
text-decoration: none/uppercase/lowercase/capitalize
word-spacing:单词间间距  
letter-spacing:字母间间距   

### 注意：
text-align ：只应用于 __块级元素__
因此，一般用于设置在块级元素，使得该块级元素内的内联元素的文本居中，给内联元素设置text-align 无效  

text-indent ：只应用于 __块级元素__
>  取值：
>  length 
>  使用固定的<length>值来指定文本的缩进。允许使用负值。 
>  percentage 
>  使用包含块宽度的百分比作为缩进.
>  each-line 
>  文本缩进会影响第一行，以及使用<br>强制断行后的第一行。
>  hanging 
>  该值会对所有的行进行反转缩进：除了第一行之外的所有的行都会被缩进，看起来就像第一行设置了一个负的缩进值。

采用em 时，em取的参考物为父元素的字体大小（如果自身有设置字体大小，则变为以自身字体大小为参考）；
采用% 百分比，百分比取父元素的宽带（如果自身有设置字体大小，则变为以自身字体大小为参考）

```
<style type="text/css">
        body{
            font-size:40px;
        }
        div{
            font-size:20px;
            text-align: center; 
            text-indent: 20%;
            border: 1px solid black;
			width: 600px;
        }
        span{
            text-align: center;
            text-indent: 2em;
            border: 1px solid black; 
        }
        p{
            /*font-size:30px; */
            text-indent: 20%;
			width: 400px;

        }
    </style>
<body>
<div class="box">
    <!--text-align: center; 和 text-indent: 1em;均在p标签生效（p为块级元素）-->
    <p>牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、
        狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、
        狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束</p>
    <hr>
    <!--text-align: center 生效（span包裹在div中）;   text-indent: 1em不生效-->
    <span>牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、
    狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束,牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、
    狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束</span>
</div>
<br>
<br>
<!--text-align: center 不生效;   text-indent: 1em不生效-->
<span>牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、
    狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束,牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、
    狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束牛市在绝望中来临、质疑中展开、犹豫中猛涨、狂热中结束</span>
</body>

```   

### 居中    
> 块级元素水平居中 ：margin:0 auto；    
> 行内元素水平居中 ：text-align:center ，一般加在其块级父元素上；    
> inline-block 元素水平居中: 给该元素包裹一个div父元素，设置该div  样式： text-align: center;   

### line-height
行高，可继承   

行内元素设置line-height,有效果（产生间隔），但是盒子尺寸不变（即内容区大小不变）
块级元素设置line-height,盒子尺寸变化（内容撑开）
参见该图：  
![](./内联元素行高.png) 
 
__百分比,em---以父元素字体为参照物计算行高，继承给子元素__；  
__数字则是直接将行高继承给子元素，以子元素字体大小来计算行高__    


### 隐藏  
opacity:0    
visibility :hidden  
display:none   不占用位置  


### 字体图标   

1. http://www.iconfont.cn/ 找到所需的图标，加入购物车，然后加入项目


