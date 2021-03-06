#### 如何产生闭包?

\* 当一个嵌套的内部\(子\)函数引用了嵌套的外部\(父\)函数的变量\(函数\)时, 就产生了闭包

#### 闭包到底是什么?

\* 使用chrome调试查看

\* 理解一: 闭包是嵌套的内部函数\(绝大部分人\)

\* 理解二: 包含被引用变量\(函数\)的对象\(极少数人\)

\* 注意: 闭包存在于嵌套的内部函数中

#### 产生闭包的条件?

\* 函数嵌套

\* 内部函数引用了外部函数的数据\(变量/函数\)

#### 常见的闭包

* 将函数作为另一个函数的返回值
* 将函数作为实参传递给另一个函数调用

#### 闭包的作用

* 使用函数内部的变量在函数执行完后，仍然存货在内存中（延长了局部变量的生命周期）
* 让函数外部可操作（读写）到函数内部的数据（变量/函数）

问题

* 函数执行完后，函数内部声明的局部变量是否还存在
* 在函数外部能直接访问函数内部的局部变量吗

#### 闭包的生命周期

* 产生：在嵌套内部函数**定义执行完** 时就产生了（不是在调用）
  * 函数表达式是在执行定义完产生函数表达式
  * 函数声明提升  函数声明
* 死亡：在嵌套的内部函数成为垃圾对象时

```js
<script type="text/javascript">
  function fun1() {
    //问题2: 此时闭包产生了吗? 
    var a = 3;

    function fun2() {
      a++;
      console.log(a);
    }

    return fun2;
  }
```

//问题1: 此时闭包产生了吗?

var f = fun1\(\);

//问题3: 此时闭包释放了吗?

f\(\);

f\(\);

//问题4: 此时闭包释放回收了吗?

//问题5: 如何让闭包释放回收呢?

#### 闭包的应用：定义JS模块

* 具有特定功能的js文件
* 将所有的数据和功能都封装在一个函数内部（私有的）
* 指向外暴露一个包含N个方法的对象或函数
* 模块的使用者，只需通过模块暴露的对象调用方法l来实现对应的功能

##### 栗子：

![](/assets/WechatIMG9.jpeg)

#### 闭包的缺点及解决

* 缺点
  * 函数执行完后，函数内的局部变量没有释放，占用内存时间会变长
  * 容易造成内存泄漏
* 解决
  * 能不用闭包就不用
  * 及时释放

#### 面试题

```js
//代码片段一
var name = "The Window";
var object = {
    name : "My Object",
    getNameFunc : function(){
        return function(){
            return this.name;
        };
    }
};
alert(object.getNameFunc()());  //?The Window


//代码片段二
var name2 = "The Window";
var object2 = {
    name2 : "My Object",
    getNameFunc : function(){
        var that = this;
        return function(){
            return that.name2;
        };
    }
};
alert(object2.getNameFunc()()); //?My Object
```

```js
  function fun(n,o) {
        console.log(o)
        return {
            fun:function(m){
                return fun(m,n);
            }
        };
    }
    var a = fun(0);  a.fun(1);  a.fun(2);  a.fun(3);//undefined,?,?,?000
    var b = fun(0).fun(1).fun(2).fun(3);//undefined,?,?,?012
    var c = fun(0).fun(1);  c.fun(2);  c.fun(3);//undefined,?,?,?011
```



