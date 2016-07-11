#元素居中
##使用margin属性
```css
margin:0 auto
```
只能水平居中，不能垂直距离居中
##相对定位+transform进行移动
```css
top:50%;              //找到父元素的中心点
left:50%;
position:relative;
transform: translate(-50%, -50%);       //向左上移动自己宽高的一半
-webkit-transform: translate(-50%, -50%);
-moz-transform: translate(-50%, -50%);
-ms-transform: translate(-50%, -50%);
```
##使用display:flex属性   `在父元素中设置`
```css
display:flex;
align-items: center;
justify-content: center;
```
