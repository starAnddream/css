#清除浮动，float闭合
下面是几种清除浮动的方法
##骨灰级解决办法：
```css
.clearfix{clear:both;height:0;overflow:hidden;}
```
上诉办法是在需要清除浮动的地方加个div.clearfix，我们知道这样能解决基本清浮动问题。
但是这种方法的最大缺陷就是改变了html结构，虽然只是加个div。
##最优浮动闭合方案（这是我推荐的）：
```css
.clearfix:after{content:".";display:block;height:0;clear:both;visibility:hidden}
.clearfix{*+height:1%;}
```
用法很简单，在浮动元素的父云素上添加class=”demo clearfix”。
以上写法就避免了改变html结构，直接用css解决了。
##很拉风的浮动闭合办法：
```css
.clearfix{overflow:hidden;zoom:1;}
```
下面我们来看一下zoom的工作原理吧！<br>
在平常的css编写过程中，zoom:1能够比较神奇地解决ie下比较奇葩的bug。<br>
譬如外边距（margin）的重叠，譬如浮动的清除，譬如触发ie的 haslayout属性等等。<br> 
zoom是 设置或检索对象的缩放比例。设置或更改一个已被呈递的对象的此属性值将导致环绕对象的内容重新流动。<br>
当设置了zoom的值之后，所设置的元素就会就会扩大或者缩小，高度宽度就会重新计算了，这里一旦改变zoom值时其实也会发生重新渲染，<br>
运用这个原理，也就解决了ie下子元素浮动时候父元素不随着自动扩大的问题。<br>

Zoom属是IE浏览器的专有属性，火狐和老版本的webkit核心的浏览器都不支持这个属性。然而，zoom现在已经被逐步标准化，
出现在 CSS 3.0 规范草案中。 <br>
