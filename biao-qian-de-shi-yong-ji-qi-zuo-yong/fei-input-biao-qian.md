#### select标签

作用：用于定义下拉列表

格式

```
<select>
   <optgroup label="第一组数据">
   <option  selected="selected"></option>
   <option></option>
   </optgroup>
   <optgroup label="第二组数据">
   <option></option>
   <option></option>
   </optgroup>
</select>
```

注意点

* 下拉列表不能输入内容，但是可以直接在列表中选择内容
* 可以通过给option标签添加一个selseted属性来指定列表的默认值
* 可以通过给option标签包裹一层optgroup 标签来给下拉列表中的数据分类

#### textarea标签

定义一个多行的输入框

格式

```
<textarea>
</textarea>
```

注意点

* 默认情况下输入框可以无限换行
* 默认情况下输入框有自已的宽度和高度
* 可以通过cols和rows来hiding输入框的宽度和高度，但是虽然指定了列数和行数，但是还是可以无限往下输入
* 默认情况下输入框是可以是手动拉伸的



