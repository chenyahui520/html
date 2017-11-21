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

### 实例

当动画为 25% 及 50% 时改变背景色，然后当动画 100% 完成时再次改变：

```
@keyframes myfirst
{
0%   {background: red;}
25%  {background: yellow;}
50%  {background: blue;}
100% {background: green;}
}

@-moz-keyframes myfirst 
/* Firefox */

{
0%   {background: red;}
25%  {background: yellow;}
50%  {background: blue;}
100% {background: green;}
}

@-webkit-keyframes myfirst 
/* Safari 和 Chrome */

{
0%   {background: red;}
25%  {background: yellow;}
50%  {background: blue;}
100% {background: green;}
}

@-o-keyframes myfirst 
/* Opera */

{
0%   {background: red;}
25%  {background: yellow;}
50%  {background: blue;}
100% {background: green;}
}

```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_animation2)

### 实例

改变背景色和位置：

```
@keyframes myfirst
{
0%   {background: red; left:0px; top:0px;}
25%  {background: yellow; left:200px; top:0px;}
50%  {background: blue; left:200px; top:200px;}
75%  {background: green; left:0px; top:200px;}
100% {background: red; left:0px; top:0px;}
}

@-moz-keyframes myfirst 
/* Firefox */

{
0%   {background: red; left:0px; top:0px;}
25%  {background: yellow; left:200px; top:0px;}
50%  {background: blue; left:200px; top:200px;}
75%  {background: green; left:0px; top:200px;}
100% {background: red; left:0px; top:0px;}
}

@-webkit-keyframes myfirst 
/* Safari 和 Chrome */

{
0%   {background: red; left:0px; top:0px;}
25%  {background: yellow; left:200px; top:0px;}
50%  {background: blue; left:200px; top:200px;}
75%  {background: green; left:0px; top:200px;}
100% {background: red; left:0px; top:0px;}
}

@-o-keyframes myfirst 
/* Opera */

{
0%   {background: red; left:0px; top:0px;}
25%  {background: yellow; left:200px; top:0px;}
50%  {background: blue; left:200px; top:200px;}
75%  {background: green; left:0px; top:200px;}
100% {background: red; left:0px; top:0px;}
}

```

  


