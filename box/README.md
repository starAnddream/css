#css盒模型
* width/height:元素区域内容的尺寸，不包含边框和内边距
* 在IE6之前和IE6-IE8的怪异模式下显示一个页面时（页面缺少<!DOCTYPE>）,width/height包含内边距和边框宽度。
* top/left:不是从容器<b>内容区域</b>的左上角开始度量的，而是从容器<b>内边距</b>的左上角开始
###box-sizing
* IE的行为是一个bug,但是IE得非标准盒模型非常有用<br/>
box-sizing:content-box(内容盒模型，标准盒模型)默认属性<br/>
box-sizing:broder-box(IE盒模型，边框盒模型)width/height:包含边框和内边距<br/>
* 可以用于想用百分比设置总体尺寸，又想以像素单位指定边框和内边距，边框盒模型特别有用
```html
<div  style="box-sizing:border-box;widthL:50%;padding:10px;border:solid black 2px">
```
###calc()边框模型在未来CSS3中的一个可选方案是使用盒子尺寸计算值：
```html
<div style="width:calc(50%-12);padding:10px;border:solid black 2px;">
```

