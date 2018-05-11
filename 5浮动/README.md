# 浮动
## 浮动元素特点
1. 浮动元素在一行显示
2. float值为left的元素，会依次从左向右排布；float值为right的元素，会依次从右向左排布；
3. 浮动元素自动具有块级元素的属性
4. 浮动元素脱离文档流
5. 浮动元素的子元素，不会继承浮动
6. 浮动元素下面的元素，不能识别浮动元素的高度和位置（从而会占据浮动元素原来的位置）
7. float可取的值，left，right，none，inherit


## 文档流
1. 文档流：指的是元素排版过程中，元素自动从左向右，从上向下流式排列。最终窗体自上而下分成一行行，并在每行中从左向右排放元素；
2. 脱离文档流：文档流内的正常元素无法识别脱离文档流的元素（脱离文档流的元素相当于漂浮在文档流之上）


## 清浮动
1. 给浮动元素的父元素手动添加一个固定的高度；
2. 给浮动元素的父元素设置overflow:hidden/auto ;加 overflow:visible; 不可行，加overflow:scroll;,清除了浮动，但有滚动条
3. 浮动元素父父元素结束标签之前加一个具有块元素特点的标签（一般用div），添加clear:both 即<div style="clear:both:>
4. 利用clearfix清除浮动
          .clearfix:after{ /*可以多处使用----项目常用方式*/
              display: block;
              clear: both;
              content: "";

              /*低版本浏览器 默认有height：1px*/
              height: 0;
              font-size: 0;
              overflow: hidden;
              visibility: hidden;
          }



