#清除浮动，float闭合
下面是几种清除浮动的方法
##骨灰级解决办法：
```css
.clearfix{clear:both;height:0;overflow:hidden;}
```
上诉办法是在需要清除浮动的地方加个div.clear或者br.clear，我们知道这样能解决基本清浮动问题。

但是这种方法的最大缺陷就是改变了html结构，虽然只是加个div。
最优浮动闭合方案（这是我们推荐的）：

.clearfix:after{content:".";display:block;height:0;clear:both;visibility:hidden}
.clearfix{*+height:1%;}

用法很简单，在浮动元素的父云素上添加class=”demo clearfix”。

你会发现这个办法也有个弊端，但的确是小问题。改变css写法就ok了：

.demo:after,.demo2:after{content:".";display:block;height:0;clear:both;visibility:hidden}
.demo,.demo2{*+height:1%;}

以上写法就避免了改变html结构，直接用css解决了。
很拉轰的浮动闭合办法：

.clearfix{overflow:auto;_height:1%}

这种办法是我看国外的一篇文章得到的方案，测试了，百试不爽，真的很简单，很给力。喜欢的同学也可以试试这个办法。

这种方法是端友radom提供的，测试通过：

.clearfix{overflow:hidden;_zoom:1;}
