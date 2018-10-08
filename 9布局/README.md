## 居中

### 1 text-align  (center)
可以用于 文字/图片水平居中    
- 块级元素，设置text-align:center 居中
- 行内元素，给父级块元素添加text-align:center 居中
示例： （7-1水平居中1.html）

### 2 margin (左右margin 相等)
- 左右margin 相等（整个块级区域居中）  
示例： （7-2水平居中2(块级内容).html）

### 3垂直居中

#### 3.1 上下padding 相等
示例： （7-3垂直居中1.html）

#### 3.2 绝对定位+ 负margin
整块内容居中（如弹出框居中）
示例： （7-4垂直居中(弹出框)2.html）

#### 3.3 vertical-align实现

vertical-align 用来指定 __行内元素（inline）或表格单元格（table-cell）元素__ 的垂直对齐方式(https://developer.mozilla.org/zh-CN/docs/Web/CSS/vertical-align)。
取值 (对于行内(inline)元素):取值是相对于 __父元素__来说的   
取值 (对于table-cell元素):与同行单元格  
 
 
## 媒体查询

 1. 媒体类型
 all	用于所有设备
 print	用于打印机和打印预览
 screen	用于电脑屏幕，平板电脑，智能手机等
 speech	应用于屏幕阅读器等发声设备
 
 2. 媒体功能
 
 
device-aspect-ratio	定义输出设备的屏幕可见宽度与高度的比率。
device-height	定义输出设备的屏幕可见高度。
device-width	定义输出设备的屏幕可见宽度。
grid	用来查询输出设备是否使用栅格或点阵。
height	定义输出设备中的页面可见区域高度。
max-device-height	定义输出设备的屏幕可见的最大高度。
max-device-width	定义输出设备的屏幕最大可见宽度。
max-height	定义输出设备中的页面最大可见区域高度。
max-resolution	定义设备的最大分辨率。
max-width	定义输出设备中的页面最大可见区域宽度。
min-device-aspect-ratio	定义输出设备的屏幕可见宽度与高度的最小比率。
min-device-width	定义输出设备的屏幕最小可见宽度。
min-device-height	定义输出设备的屏幕的最小可见高度。
min-height	定义输出设备中的页面最小可见区域高度。
min-resolution	定义设备的最小分辨率。
min-width	定义输出设备中的页面最小可见区域宽度。
orientation	定义输出设备中的页面可见区域高度是否大于或等于宽度。 portrait:竖屏; landscape:横屏
resolution	定义设备的分辨率。如：96dpi, 300dpi, 118dpcm
width	定义输出设备中的页面可见区域宽度。
 
 