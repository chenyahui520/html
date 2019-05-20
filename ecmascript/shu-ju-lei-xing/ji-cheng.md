#### 原型链继承（得到方法）

* 套路
  * 定义父类型构造函数
  * 给父类型的原型添加方法
  * 定义子类型的构造函数
  * 创建父类型的对象那个赋值给子类型的原型
  * 将子类型原型中的构造属性设置为子类型
  * 给子类型原型添加方法
  * 创建子类型的对象：可以调用父类型的方法
* 关键
  * **子类型的原型为父类型的一个实例对象**

```js
  function Parent(){}
  Parent.prototype.test = function(){};
  function Child(){}
  Child.prototype = new Parent(); // 子类型的原型指向父类型实例
  Child.prototype.constructor = Child
  var child = new Child(); //有test()
```

#### 借用构造函数继承（得到属性）（假的）

* 套路：
  * 定义父类型构造函数
  * 定义子类型构造函数
  * 在子类型构造函数中调用父类型构造
* 关键
  * 在子类型构造函数中通用super（）调用父类型构造函数

#### 组合继承



