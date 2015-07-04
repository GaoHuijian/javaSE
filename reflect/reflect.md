java反射
=======
<h3>Java类继承Object类，Object类定义了一个getClass()方法，该方法返回一个类型为Class的对象。利用Class对象可以访问返回该对象的描述信息。</h3>
通过反射可以访问的描述信息
-----------------------
![reflect](https://github.com/GaoHuijian/javaSE/blob/master/reflect/images/reflect.png)

如果为数组类型则
--------------
	用public Class<?> getComponentType()方法返回数组类型。
	然后用Array以下方法
	static Object newInstance(Class<?> componentType, int... dimensions)
	static Object newInstance(Class<?> componentType, int length) 
 	生成数组。

主要反射类
=========
	AccessibleObject
	
	Executable
	Field
	Array
	Constructor<T>
	Method
	Modifier
	Parameter
	Proxy
	ReflectPermission
