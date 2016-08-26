#display:flex多栏多列布局
* flex:1
让所有弹性盒模型对象的子元素都有相同的长度，忽略它们内部的内容
```css
{
flex:1;
}
```
* flex-basis
```css
div:nth-of-type(2) {flex-basis: 80px;}
```
* flex-direction 属性规定灵活项目的方向。
```css
div
{
display:flex;
flex-direction:row-reverse;
}
```
其余值还有：row,row-reverse,column,column-reverse
* flex-wrap 属性规定flex容器是单行或者多行，单行还是多行
```css
display:flex;
flex-wrap: wrap;
```
其余的属性值还有nowrap,wrap,wrap-reverse
* flex-flow 属性是 flex-direction 和 flex-wrap 属性的复合属性。
```css
display:flex;
flex-flow:row-reverse wrap;
```
* flex-grow扩展
```css
div:nth-of-type(1) {flex-grow: 1;}
div:nth-of-type(2) {flex-grow: 3;}
div:nth-of-type(3) {flex-grow: 1;}
```
* flex-shrink收缩

##align-items
demo:http://1.ajaxreq.applinzi.com/flex/align-item.html
