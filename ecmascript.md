### 一些知识点的总结

## toString\(\)方法与toLocalString\(\)方法区别：

* toLocalString\(\)是调用每个数组元素的 toLocaleString\(\) 方法，然后使用地区特定的分隔符把生成的字符串连接起来，形成一个字符串。

* toString\(\)方法获取的是String\(传统字符串\),而toLocaleString\(\)方法获取的是LocaleString\(本地环境字符串\)。

* 如果你开发的脚本在世界范围都有人使用，那么将对象转换成字符串时请使用toString\(\)方法来完成。

* LocaleString\(\)会根据你机器的本地环境来返回字符串，它和toString\(\)返回的值在不同的本地环境下使用的符号会有微妙的变化。

* 所以使用toString\(\)是保险的，返回唯一值的方法,它不会因为本地环境的改变而发生变化。如果是为了返回时间类型的数据，推荐使用LocaleString\(\)。若是在后台处理字符串，请务必使用toString\(\)。

#### window的一些的属性和方法

* screenLeft和screenTop分别用于表示窗口相对于屏幕左边和上边的位置
* moveTo\(\)和moveBy（）方法都接收两个参数，地一个接收的是新位置的x和y坐标值，而move（）接收的是在水平和垂直方向上移动的像素数，

  * 注意这两个方法可能被浏览器禁用，而且，在Opera和IE7及其高版本中默认是禁用的，另外，这两个方法都不适用于框架，只能对最外层的window对象使用，

* resizeTO\(\)和 resizeBy\(\)方法可以调整浏览器窗口的大小，这两个方法都接收两个参数，其中resizeTO\(\)接收浏览器窗口的新宽度和高度，而resizeBy\(\)接收新窗口与原窗口的宽度和高度之差。

#### 导航和打开窗口

* 使用window。open\(\)方法既可以导航到一个特定的URL，也可以打开一个新的浏览器窗口。这个方法可以接收四个参数：要加载的URL、窗口目标、一个特性字符创以及一个表示新页面是否取代浏览器历史记录中当前加载页面的布尔值，通常只需要传递第一个参数，最后一个参数在只在不打开新窗口的情况下使用
  * 新创建的window对象有个opener属性，其中保存着打开它的原始窗口对象，这个属性只在弹出窗口的最外层window对象（top）中有定义，而且指向调用window.open（）窗口或框架
  * 将新创建的标签页的opener的属性设置为null，即表示在单独的进程中运行新标签页，就是告诉浏览器新创建的标签页不需要与打开它的标签页通信，因此可以在独立的进程中运行，标签页之间的联系一旦切断了将没有办法恢复

#### 间歇调用和超时调用

* 超时调用需要使用window对象的setTimeout\(\)方法，它接收两个参数：要执行的代码和以毫秒表示的时间
* 间歇调用的方法是setIntererval\(\),这个方法和上面的方法的参数相同。第一个参数不建议传递字符串，

### 闭包的定义

有权访问另一个函数作用域中变量的函数

`(document)`

和

`$(window)`

的差别（为了看得清楚，用了JQ写法）?

#### document和widow的区别

**Window -- 代表浏览器中一个打开的窗口：**

**document对象 -- 代表整个HTML 文档,可用来访问页面中的所有元素：**

# document.documentElement和document.body的区别

[https://blog.csdn.net/gaoqiang1112/article/details/79376326](https://blog.csdn.net/gaoqiang1112/article/details/79376326)

页面具有 DTD，或者说指定了 DOCTYPE 时，使用 document.documentElement。

页面不具有 DTD，或者说没有指定了 DOCTYPE，时，使用 document.body。

在 IE 和 Firefox 中均是如此。

为了兼容，不管有没有 DTD，可以使用如下代码：

**$\(document.body\).scrollTop\(\)+$\(document.documentElement\).scrollTop\(\)**

**  读取页面滚动条的Y坐标\(兼容chrome和IE\)**

```
var scrollTop = window.pageYOffset  //用于FF
                || document.documentElement.scrollTop  
                || document.body.scrollTop  
                || 0;
```



