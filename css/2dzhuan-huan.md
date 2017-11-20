## 2D 转换

在本章中，您将学到如下 2D 转换方法：

* translate\(\)---值 translate\(50px,100px\) 把元素从左侧移动 50 像素，从顶端移动 100 像素。
* rotate\(\)--值 rotate\(30deg\) 把元素顺时针旋转 30 度。
* scale\(\)---值 scale\(2,4\) 把宽度转换为原始尺寸的 2 倍，把高度转换为原始高度的 4 倍。
* skew\(\)
* matrix\(\)

### 实例

```
div
{
transform: rotate(30deg);
-ms-transform: rotate(30deg);		
/* IE 9 */

-webkit-transform: rotate(30deg);	
/* Safari and Chrome */

-o-transform: rotate(30deg);		
/* Opera */

-moz-transform: rotate(30deg);		
/* Firefox */

}

```

---

## translate\(\) 方法

通过 translate\(\) 方法，元素从其当前位置移动，根据给定的 left（x 坐标） 和 top（y 坐标） 位置参数：

  
实例

```
div
{
transform: translate(50px,100px);
-ms-transform: translate(50px,100px);		
/* IE 9 */

-webkit-transform: translate(50px,100px);	
/* Safari and Chrome */

-o-transform: translate(50px,100px);		
/* Opera */

-moz-transform: translate(50px,100px);		
/* Firefox */

}

```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_transform_translate)

值 translate\(50px,100px\) 把元素从左侧移动 50 像素，从顶端移动 100 像素。

---

## rotate\(\) 方法

通过 rotate\(\) 方法，元素顺时针旋转给定的角度。允许负值，元素将逆时针旋转。

  
实例

```
div
{
transform: rotate(30deg);
-ms-transform: rotate(30deg);		
/* IE 9 */

-webkit-transform: rotate(30deg);	
/* Safari and Chrome */

-o-transform: rotate(30deg);		
/* Opera */

-moz-transform: rotate(30deg);		
/* Firefox */

}

```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_transform_rotate)

值 rotate\(30deg\) 把元素顺时针旋转 30 度。

---

### scale\(\) 方法

###### 通过 scale\(\) 方法，元素的尺寸会增加或减少，根据给定的宽度（X 轴）和高度（Y 轴）参数： 

### 实例

```
div
{
transform: scale(2,4);
-ms-transform: scale(2,4);	
/* IE 9 */

-webkit-transform: scale(2,4);	
/* Safari 和 Chrome */

-o-transform: scale(2,4);	
/* Opera */

-moz-transform: scale(2,4);	
/* Firefox */

}

```

[亲自试一试](http://www.w3school.com.cn/tiy/t.asp?f=css3_transform_scale)

值 scale\(2,4\) 把宽度转换为原始尺寸的 2 倍，把高度转换为原始高度的 4 倍。



