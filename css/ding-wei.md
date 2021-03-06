### 定位

#### 定位流分类

#### 1相对定位

#### 2绝对定位

#### 3固定定位

#### 4静态定位

### 什么是相对定位

相对定位就是相对于自己以前在标准流中的位置来移动

#### 相对定位注意点

* 相对定位是不能脱离标准流的，会继续在标准流中占用一份空间

* 在相对定位中同一个方向上的定位属性只能使用一个

* 由于相对定位是不脱离标准流的，所以在相对定位中是区分块级元素/行内元素/行内块级元素

* 由于相对定位是不脱离标准流的，并且相对定位的元素会占用标准流中的位置，所以当给相对定位的元素设置margin/padding等属性的时候会影响到标准流的布局

positon;relative

### 什么是绝对定位

绝对定位就是相对于body来定位

#### 绝对定位注意点

* 绝对定位的元素是脱离标准流的
* 绝对定位的元素是不区块级元素/行内元素/行内块级元素

#### 绝对定位规律

* 默认情况下所有的绝对定位的元素，无论有没有祖先元素，都会以body作为参考点

* 如果一个绝对定位的元素有祖先元素，并且祖先元素也是定位流，那么这个绝对定位的元素就会以定位流的那个祖先元素作为参考点

* * 只要是这个绝对定位元素的祖先元素都可以
* * 只的定位流是指绝对定位/相对定位/固定定位
* * 定位流中只有静态定位不行
* 如果一个绝对定位的元素有祖先元素,并且祖先元素也是定位流，而且祖先元素中有多个元素都是定位流

position:absolute

**注意**

如果一个绝对定位的元素是以body作为参考点，那么其实是以网页首屏看度和高度作为参考点，而不是以整个网页的宽度和高度作为参考点

2一个绝对定位的元素会忽略祖先元素的padding

#### 相对定位的弊端

相对定位不会脱离标准流，会继续在标准流中占用一份空间，所以不利于布局界面

#### 绝对定位弊端

默认情况下绝对定位的元素会以body作为参考点，所以会随着浏览器的宽度高度的变化而变化

### 子绝父相  可以参考[https://blog.csdn.net/fungleo/article/details/50056111](https://blog.csdn.net/fungleo/article/details/50056111)

子元素用绝对定位，父元素用相对定位

#### 如何让绝对定位的元素水平居中

只需要设置绝对定位元素的left：50%；

然后在设置绝对定位元素的margin—left：元素宽度的一半px;

### 固定定位

#### 什么是固定定位

固定定位和前面学习的背景关联方式很像

背景定位可以让背景图片不随着滚动条的滚动而滚动，而固定定位可以让某个盒子不随着滚动条的滚动而滚动

#### 注意点

* 固定定位的元素是脱离标准流的，不会占用标准流中的空间
* 固定定位和绝对定位一样不区分行内/块级/行内块级
* IE6不支持固定定位

#### 固定定位应用场景：

* 网页对联广告

* 网页头部通栏\(穿透效果）

### 静态定位

* 什么是静态定位?

  * 默认情况下标准流中的元素position属性就等于static, 所以静态定位其实就是默认的标准流

* 静态定位应用场景:

  * 一般用于配合JS清除定位属性

position: relative;不会脱离文档流，position: fixed;position: absolute;会脱离文档流

position: relative; 相对于自己在文档流中的初始位置偏移定位。

position: fixed; 相对于浏览器窗口定位。

position: absolute; 是相对于父级非position:static 浏览器定位。 

如果没有任何一个父级元素是非position:static属性，则会相对于文档定位。

这里它的父级元素是包含爷爷级元素、祖爷爷级元素、祖宗十八代级元素的。任意一级都可以。

如果它的父级元素和爷爷级元素都是非position:static 属性，则，它会选择距离最近的父元素

--------------------- 

作者：FungLeo 

来源：CSDN 

原文：https://blog.csdn.net/fungleo/article/details/50056111 

版权声明：本文为博主原创文章，转载请附上博文

### z-index

* 默认情况下所有的元素都有一个默认的z-index属性，取值是0，z-index属性的作用是专门用于控制定位流元素的覆盖关系的

* 默认情况下定位流的元素会盖住标准流的元素

* 默认情况下定位流的元素后面编写的会盖住前面编写的

#### 从父现象

* 如果两个元素的父元素都没有设置z-index属性，那么谁的z-index属性比较大谁就显示在上面
* 如果两个元素的父元素设置了z-index属性，那么子元素的z-index属性就会失效，也就是说谁的父元素的z-index属性比较大谁就会显示在上面

**z-index应用场景**

* 控制界面上的定位元素的覆盖关系，例如网页中后面的定位元素不能覆盖前面的导航条通栏。

详情参考

[http://www.jianshu.com/p/454a0eaa39ef](http://www.jianshu.com/p/454a0eaa39ef)

