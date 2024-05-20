## 颜色

1. 单词 red
2. 十六进制 #000000；#fff
3. rgb rgb(255,0,0)
4. rgba raga(255,255,0,0.2)
5. HSL hsl(276, 100%, 85%);
6. HSLA hsla(240, 100%, 50%, 0.5);

## 长度值

1. px
2. 百分比
3. em 相对**父**级元素**字体**大小
4. rem 相对**根**级元素（html）**字体**大小
5. vw vh 相对屏幕的宽度和高度， 1vw 屏幕宽度的 1%， 10vw 是视口宽度的 10%

em：本元素给定字体的 font-size 值，如果元素的 font-size 为 14px ，那么 1em = 14px；如果 font-size 为 18px，那么 1em = 18px
百分比 p{font-size:12px;line-height:130%} line-height = 15.6px

## 百分比

- https://www.zhihu.com/question/36079531/answer/65809167 （css 样式的百分比都相对于谁）

- 相对于父级宽度的：width、left、right、padding、margin、max-width、min-width、text-indent、grid-template-columns、grid-auto-columns、column-gap 等；
- 相对于父级高度的：height、top、bottom、max-height、min-height、grid-template-rows、grid-auto-rows、row-gap 等；
- 相对于主轴长度的：flex-basis 等；
- 相对于继承字号的：font-size 等；
- 相对于自身字号的：line-height 等；
- 相对于自身宽高的：border-radius、background-size、border-image-width、transform: translate()、transform-origin、zoom、clip-path 等；
- 相对于行高的：vertical-align 等；
- 特殊算法的：background-position （方向长度 / 该方向除背景图之外部分总长度）、border-image-slice （相对于图片尺寸）、filter 系列函数等；如果自身设置 position: absolute，“父级”指：https://www.zhihu.com/question/35707704/answer/64079391；如果 position: fixed，“父级”指视口（父级不存在 transform 为非 none 值的情况下）。
