#CSS响应式布局
##基于宽度的百分比缩放工作原理
用百分比设置宽度，当父元素的宽度改变时，图像元素宽度也会相应改变并填充对应的宽度。<br>
属性height:auto的作用在于保证图片自身的高度比例不会改变。<br>
##基于媒介查询的图像缩放工作原理
在CSS中通过逻辑条件将浏览器依据窗口属性进行区分
##媒体查询与横竖屏
```css
@media screen and (orientation:portrait){

}
@media screen and (orientation:landscape){

}
```

