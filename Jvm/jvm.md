JVM规范
======
	
类加载器
=======
* Bootstrap ClassLoader
* ExtClassLoader
* AppClassLoader	

jvm指令
======	

jvm内存管理
=========
###需要内存的组件
	java堆 
	线程-堆栈
	类和类加载器
	NIO
	JNI
###jvm内存结构
	java堆
	Java栈
	静态方法区
	本地方法去
	计算机寄存器
	程序计数器
###安全校验

### 初始化
* 1 给属性分配空间,并且属性赋初始值.
* 2 调用构造方法,给属性重写赋值
### 空间分配
* Java堆 :对象及其对象的属性都是在堆中分配的
* Java栈 :非对象及其对象的属性是在栈中分配的
JVM执行顺序
------------
1,ClassLoader把字节码从硬盘加载