# Display
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
 
 ### font
 font-size / font-family / font-weight 文字粗度（normal，bold,bolder,lighter），可继承
 line-height: 行高，可继承
 - 采用复合写法时，font-size 和font-family在最后2个，且必须有这2个
 
 
```
 p{
     /*font:italic 16px/20px arial,sans-serif ;*/ /*字体最后，16px --字体大小 ，20px --line-height*/
     font:italic 16px arial,sans-serif ;
     /*line-height: 200%; */   /* line-height= 32px,百分比相对于字体大小 */
     line-height: 1.5em;  /* line-height= 24px,百分比相对于字体大小 */
```
