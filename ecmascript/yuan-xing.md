### 定义

我们所创建的没一个函数，我们的解析器都会想函数中添加一个属性prototype，这个属性对应着一个对象， 这个对象就是一个原型对象

如果函数作为普通函数调用prototype 没有任何作用

当函数以构造函数的形式调用时，它所创建的对象中都会有一个隐含的属性，指向该构造函数的远行对象

我们可以通过\_\__proto_\_\_来访问该属性

原型对象就相当于公共区域，所有同一个类的实例都可以访问到这个原型对象

当我们访问一个属性或方法时，它会先在对象自身中寻找，如果有则直接使用，如果没有则会去原型对象中寻找，如果找到直接使用户

以后我们创建函数时，可以将这些对象共有的属性和方法，统一添加到构造函数的原型对象中，这样不用分别为每一个对象添加，也不会影响到全局作用域，就可以使每个对象都具有这些属性和方法了

### 原型对象也是对象，所以它也有原型

当我们使用一个对象的属性或方法时，会先在自身中寻找，

* 自身中如果有，则直接使用
* 如果没有则去原型对象中寻找，如果原型对象中有则使用
* 如果没有则去原型的原型中寻找，直到找到Object对象的原型，
* Object对象的原型没有原型，如果在Object中依然没有找到，则返回undefined

### 当我们直接在页面中打印一个对象时，事件上输出的对象的toString\(\)方法的返回值，如果我们希望在输出对象时不输出\[object object\],可以为对象添加一个toString（）方法


