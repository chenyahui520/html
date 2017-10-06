### 继承性

**作用：**给父元素设置一些属性，子元素也可以使用，这个我们就称之为继承性

**注意点**

* 并不是所有的属性都可以继承，只有color/font-/text-/line开头的属性才可以继承
* 在CSS的继承中不仅仅是儿子可以继承，只要是后代都可以继承
* 继承性中的特殊性
* * a标签的文字颜色和下划线是不能继承的
  * h标签的文字大小是不能继承的

#### 应用场景

一般用于设置网页上的一些共性信息，例如网页的文字颜色字体，字体大小等内容body{}

---

### 层叠性

**作用**

css处理冲突的一种能力

**注意点**

层叠性只有在多个选择器选中“同一个标签”，然后又设置了“相同的属性”，才会发生层叠性

#### CSS全称  Cascading StyleSheet   层叠式样式表


