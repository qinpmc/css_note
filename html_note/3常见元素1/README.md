# 常见元素标签1

## a 标签
1. 属性 href target等
```
 I like <a href="http://en.wikipedia.org/wiki/Apples">apples</a> and
        <a href="http://en.wikipedia.org/wiki/Orange_(fruit)">oranges</a>.
        <!--禁止a标签默认跳转-->
        <a href="javascript:;">a标签不跳转</a>
        You can see other fruits I like <a href="#fruits">here</a>.

        <p id="fruits">
            I also like bananas, mangoes, cherries, apricots, plums, peaches and grapes.
        </p>
        如果找不到指定id元素，浏览器会查找name属性与之匹配的元素(a标签才行)
        You can see other fruits I like <a name="fruits">here</a>.
```
a标签链接的功能
- 电话链接 <a href ="tel:+8613812381238">+8613812381238</a>
- Email链接： <a href ="mailto:xidada@china.gov.cn?cc=pengliyuan@china.gov.cn">发送并抄送邮件</a>
- 下载链接：<a href = "https://angular.io/resource/images/logos/angular/angular.svg" download> 下载</a>
- 返回顶部链接<a href="#"> 返回顶部链接</a>
- 文档内部链接： 如上例

- a标签与iframe的结合使用：

```
<iframe src="#" frameborder="0" name="link" width="1200px" height="800px"></iframe>
<a href="http://qq.com" target="link">qq</a>
<a href="http://baidu.com" target="link">baidu</a>

```






## 文字标记标签
* em 强调内容，通常斜体
* i 表示与周围内容有本质区别，常用于外文词语、科技术语等,样式为斜体
* s 表示某段文字不再正确，样式为删除线
* b 并不表示特别的强调或重要性，通常会对内容加粗
* strong 表示重要的内容，样式为加粗
* u 凸显内容，样式为下划线
* small 小号字体内容
* sub/sup 下标和上标
* br 换行，自闭合的标签
* wbr 单词换行，浏览器根据窗口大小自行调整
* abbr 缩写
* ins del 添加和删除内容
