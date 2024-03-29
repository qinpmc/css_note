## 文档分节

### 文档分节标签
* h1~h6 标题
* hgroup 将多个标题元素作为一个整体处理，解决子标题的问题
* section 文档的一节，包含的是那种应该列入文档大纲或目录的内容，通常包含一个或多个段落及一个标题（标题非必须）
* header 首部
* footer 尾部
* nav 导航区域
* article 一段独立成篇的内容
* aside 附注栏，表示跟周边内容稍微沾一点边的内容，类似书籍或杂志的侧栏
* main 呈现了文档<body>或应用的主体部分
* address 文档或article 元素的联系信息
* details 可以展开了解更多详情，常和summary元素一起用，展开前只显示summary的内容

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <!--解决html5不支持的问题-->
    <!--[if lt IE 9]>
        <script src="htmlt.min.js"></script>
    <![endif]-->
</head>
<body>
    <header>
        <h1>XXX有限公司</h1>
        <nav>
            <a href=""></a><a href=""></a><a href=""></a><a href=""></a><a href=""></a><a href=""></a>
            <span>热线电话</span>
        </nav>
        <div class="banner"></div>
    </header>
    <main>
        <aside>
            <section>
                <h3>产品分类</h3>
                <ul>
                    <li></li>
                    <li></li>
                    <li></li>
                </ul>
            </section>
            <section>
                <h3>联系我们</h3>
                <ul>
                    <li></li>
                    <li></li>
                    <li></li>
                    <li></li>
                    <li></li>
                    <li></li>
                </ul>
            </section>
        </aside>
        <secction>
            <h3>公司简介</h3>
            <figure>
                <img src="" alt="">
                <!--<figcaption></figcaption>-->
            </figure>
            <p>XXX</p>
        </secction>
        <secction>
            <h3>应用领域</h3>
            <p>XXX</p>
        </secction>
        <secction>
            <h3>产品展示</h3>
            <ul>
                <li><img src="" alt=""><span></span></li>
                <li><img src="" alt=""><span></span></li>
                <li><img src="" alt=""><span></span></li>
            </ul>
        </secction>
    </main>
    <footer>
        <ul>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
        </ul>
    </footer>
</body>
</html>

```
## 效果图:
![文档分节](./demo1.png)