#CSS响应式布局
###基于宽度的百分比缩放工作原理
用百分比设置宽度，当父元素的宽度改变时，图像元素宽度也会相应改变并填充对应的宽度。<br>
属性height:auto的作用在于保证图片自身的高度比例不会改变。<br>
##移动端响应式布局
###媒体查询与横竖屏
```css
@media screen and (orientation:portrait){   //竖屏

}
@media screen and (orientation:landscape){   //横屏

}
```
###媒体查询与宽度(逻辑像素)
下面的语句可以匹配到所有的移动设备
```css
@media screen and (width:980px){

}
```
这里的980px指的是设备的逻辑像素而不是物理像素，设备的物理像素是实际的大小
###媒体查询与宽度(物理像素)
```css
@media (device-width:320px){

}
```
###媒体查询与宽高比例（9/16是物理像素宽:高）
```css
@media screen and (device-aspect-ratio: 9/16) {

}
```
##需要注意
媒体查询会产生css属性覆盖，以后面匹配到的为主
媒体查询匹配到的属性会覆盖最外层的属性
