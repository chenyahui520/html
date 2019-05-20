#### Object构造函数模式

* 套路：先创建Object对象，再动态添加属性/方法
* 使用场景：起始时不确定对象内部数据
* 问题：语句太多

```js
  var obj = {};
  obj.name = 'Tom'
  obj.setName = function(name){this.name=name}
```

#### 对象字面量模式

* 套路：使用大括号创建对象，同时指定属性/方法
* 使用场景：起始时对象内部的数据是确定的
* 问题：如果创建多个对象，有重复的代码

```js
  var obj = {
    name : 'Tom',
    setName : function(name){this.name = name}
  }
```

#### 工厂模式

* 通过工厂函数动态创建对象并返回
* 使用场景：需要创建多个对象
* 问题：对象没有一个具体的类型，都是Object类型

```js
    function Person(name,age){
            var obj ={
            name : 'name',
            age:'age'
    setName : function(name){this.name = name}
                    }
                    return obj
            }
```

#### 自定义构造函数模式

* 套路：自定义构造函数，通过new创建函数对象
* 使用场景：需要创建多个类型确定的对象
* 问题：每个对象都有相同的数据，浪费内存

```js
  function Person(name, age) {
    this.name = name;
    this.age = age;
    this.setName = function(name){this.name=name;};
  }
  new Person('tom', 12);
```

#### 构造函数+原型的组合模式

* 套路：自定义构造函数，属性在函数中初始化，方法添加到原型上
* 使用场景：需要创建多个类型的确定对象



