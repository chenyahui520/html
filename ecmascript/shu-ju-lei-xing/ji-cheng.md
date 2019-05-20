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

```js
function Parent(xxx){this.xxx = xxx}
  Parent.prototype.test = function(){};
  function Child(xxx,yyy){
      Parent.call(this, xxx);//借用构造函数   this.Parent(xxx)
  }
  var child = new Child('a', 'b');  //child.xxx为'a', 但child没有test()
```

#### 组合继承

* 原型链+借用函数的组合继承
* 利用原型链实现对父类型对象的方法继承
* 利用super（）用父类型构建函数初始化相同属性

```js
  function Parent(xxx){this.xxx = xxx}
  Parent.prototype.test = function(){};
  function Child(xxx,yyy){
      Parent.call(this, xxx);//借用构造函数   this.Parent(xxx)
  }
  Child.prototype = new Parent(); //得到test()
  var child = new Child(); //child.xxx为'a', 也有test()
```

### 

#### new一个对象背后做了些什么?

* 创建一个空对象
* 给对象设置\_\_proto\_\_, 值为构造函数对象的prototype属性值   this.\_\_proto\_\_ = Fn.prototyp
* 执行构造函数体\(给对象添加属性/方法\)



