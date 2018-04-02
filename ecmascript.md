### 一些知识点的总结

## toString\(\)方法与toLocalString\(\)方法区别：

* toLocalString\(\)是调用每个数组元素的 toLocaleString\(\) 方法，然后使用地区特定的分隔符把生成的字符串连接起来，形成一个字符串。

* toString\(\)方法获取的是String\(传统字符串\),而toLocaleString\(\)方法获取的是LocaleString\(本地环境字符串\)。

* 如果你开发的脚本在世界范围都有人使用，那么将对象转换成字符串时请使用toString\(\)方法来完成。

* LocaleString\(\)会根据你机器的本地环境来返回字符串，它和toString\(\)返回的值在不同的本地环境下使用的符号会有微妙的变化。

* 所以使用toString\(\)是保险的，返回唯一值的方法,它不会因为本地环境的改变而发生变化。如果是为了返回时间类型的数据，推荐使用LocaleString\(\)。若是在后台处理字符串，请务必使用toString\(\)。



  




