# 渐变
## 线性渐变
linear-gradient
1. 只能用在背景上
2. 颜色沿着一条直线轴变化
3. 参数
   - 起点：沿着什么方向渐变（left、top、left top等）
   - 角度：xxx deg
   - 点：渐变的颜色和位置 （X% px ）

 重复线性渐变：
 repeating-linear-gradient

```
        div{
            height: 50px;
            width: 30px;
            background:blueviolet;
            margin: 10px;
            float: left;
        }
        div:nth-child(1){
            background: -webkit-linear-gradient(top,red,green); /*top:从上到下*/
            linear-gradient(top,red,green);
        }
        div:nth-child(2){
            background: -webkit-linear-gradient(left,red,green);/*left:从左到右*/
            linear-gradient(left,red,green);
        }
        div:nth-child(3){
            background: -webkit-linear-gradient(bottom,red,green);/*left:从下到上*/
            linear-gradient(bottom,red,green);
        }
        div:nth-child(4){
            background: -webkit-linear-gradient(left top,red,green);/*left top:从左上到右下*/
            linear-gradient(left top,red,green); /*left top:从左上到右下*/
        }

        div:nth-child(5){
            background: -webkit-linear-gradient(0deg,red,green);/*0deg:水平方向 （从左到右）*/
            linear-gradient(0deg,red,green); /*left top:从下往上*/
        }

        div:nth-child(6){
            background: -webkit-linear-gradient(0deg,red 30%,green 70%);/*0deg:水平方向 （从左到右）,10%-70%渐变，10%前纯红色，70%后面纯绿色*/
            linear-gradient(0deg,red 30%,green 70%); /*0deg:水平方向 （从左到右）,10%-70%渐变，10%前纯红色，70%hou纯绿色*/
        }

        div:nth-child(7){
            background: -webkit-linear-gradient(0deg,red 10px,green 20px );/*0deg:水平方向 （从左到右）,10%-70%渐变，10px前纯红色，70px后面纯绿色*/
            linear-gradient(0deg,red 10px,green 20px); /*0deg:水平方向 （从左到右）,10%-70%渐变，10px前纯红色，70px后面纯绿色*/
        }
        div:nth-child(8){
            background: -webkit-linear-gradient(0deg,red 10px,green 10px );/*0deg:水平方向 （从左到右）,无渐变，10px前纯红色，10px后面纯绿色*/
        linear-gradient(0deg,red 10px,green 10px); /*0deg:水平方向 （从左到右）,无渐变，10px前纯红色，10px后面纯绿色*/
        }
```
## 径向渐变



