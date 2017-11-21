### css3@keyframes规则

@keyframes 规则用于创建动画。在 @keyframes 中规定某项 CSS 样式，就能创建由当前样式逐渐改为新样式的动画效果。

  
实例

```
@keyframes myfirst
{
from {background: red;}
to {background: yellow;}
}

@-moz-keyframes myfirst 
/* Firefox */

{
from {background: red;}
to {background: yellow;}
}

@-webkit-keyframes myfirst 
/* Safari 和 Chrome */

{
from {background: red;}
to {background: yellow;}
}

@-o-keyframes myfirst 
/* Opera */

{
from {background: red;}
to {background: yellow;}
}

```

  
CSS3 动画

当您在 @keyframes 中创建动画时，请把它捆绑到某个选择器，否则不会产生动画效果。

通过规定至少以下两项 CSS3 动画属性，即可将动画绑定到选择器：

* 规定动画的名称
* 规定动画的时长

### 实例

把 "myfirst" 动画捆绑到 div 元素，时长：5 秒：

```
div
{
animation: myfirst 5s;
-moz-animation: myfirst 5s;	
/* Firefox */

-webkit-animation: myfirst 5s;	
/* Safari 和 Chrome */

-o-animation: myfirst 5s;	
/* Opera */

}

```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_animation1)

注释：您必须定义动画的名称和时长。如果忽略时长，则动画不会允许，因为默认值是 0。

  


