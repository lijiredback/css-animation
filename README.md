# css-animation

learn CSS3 animation

### CSS3 @keyframes 规则

如果需要在 CSS3 中创建动画，需要学习 @keyframes 规则

@keyframes 规则用于创建动画。在 @keyframes 中规定某项 CSS 样式，就能创建由当前样式逐渐改为新样式的动画效果

**注意：IE9 及以下版本，不支持 @keyframes 规则或 animation 属性**

```
@keyframes myfirst
{
from {background: red;}
to {background: yellow;}
}

@-moz-keyframes myfirst /* Firefox */
{
from {background: red;}
to {background: yellow;}
}

@-webkit-keyframes myfirst /* Safari 和 Chrome */
{
from {background: red;}
to {background: yellow;}
}

@-o-keyframes myfirst /* Opera */
{
from {background: red;}
to {background: yellow;}
}
```

### CSS 动画

当在 @keyframes 中创建动画时，请把它捆绑到某个选择器，否则不会产生动画效果。

通过规定至少以下两项 CSS3 动画属性，即可将动画绑定到选择器：
+ 规定动画的名称
+ 规定动画的时长

把 myfirst 动画绑定到 div 元素，时长：5秒：
```
div
{
animation: myfirst 5s;
-moz-animation: myfirst 5s;	/* Firefox */
-webkit-animation: myfirst 5s;	/* Safari 和 Chrome */
-o-animation: myfirst 5s;	/* Opera */
}
```

**注意：必须定义动画的名称和时长**

### 什么是 CSS3 中的动画？

动画是使元素从一种样式逐渐变化为另一种样式的效果。

可以改变任意多的样式任意多的次数。

请用百分比来规定变化发生的时间，或用关键词 "from" 和 "to"，等同于 0% 和 100%。

0% 是动画的开始，100% 是动画的完成。

为了得到最佳的浏览器支持，应该始终定义 0% 和 100% 选择器。

#### 实例

当动画为 25% 及 50% 时改变背景色，然后当动画 100% 完成时再次改变

```
@keyframes myfirst
{
0%   {background: red;}
25%  {background: yellow;}
50%  {background: blue;}
100% {background: green;}
}
```