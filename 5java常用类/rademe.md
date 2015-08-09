java常用类
=========
System
-------
Runtime
-------
Math
----
String
------
* 只要用到"xxxx",创建的字符串对象,给对象创建于对象池中,对象池中的对象是被共享的.
* 用+拼接大量的String的时候,会造成大量的垃圾,所以+不适合拼接大量的String,如果仅拼接少量的String,用+还是比较方便的
* 常用方法
+ 比较

StringBuffer
-------------
可变的字符序列,适合拼接大量的字符串
StringBuild
------------
StringBuffer:速度慢,线程安全的

StringBuild: 速度快,线程不安全的

date日期类
========

格式化日期类SimpleDateFormate
----------
