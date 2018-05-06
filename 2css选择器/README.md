# css 选择器

## css基本选择器

* 标签选择器，如：div{ color:red; }
* 类选择器 ,如：.class1{color:yellow;}
* Id选择器，如 #id1{ color:blue;}
* 通配符选择器 *
* 属性选择器，如[href]{ border:thin solid black}

## 属性选择器

* ![属性选择器](./attrselector.png)

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


