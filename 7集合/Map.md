Map
====
存放的是一对一对的数据
<K,V>
key value: key不可重复,value可以.


HashMap
=======
* 保证key无序且不可重复
* 如何保证?


* 当key重复时,put(),覆盖原来的value.


TreeMap
=======
* 不可重复,且可以排序
* 




Hashtable
=========
* Hashtable和HashMap都要求作为key的类必须要覆盖hashCode()/equals()方法.
* HashMap:新集合,速度快,非线程安全,key和value都可以为null.
* Hashtable:老集合,速度慢,线程安全,key和value不可以为null.