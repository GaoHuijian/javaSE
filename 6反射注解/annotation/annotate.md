Annotate
=========
1 定义annotate类型
--------
	@interface {}
	@Target()
	@Retention()
2 ElementType枚举值
-------------
![ElementType](https://github.com/GaoHuijian/javaSE/blob/master/annotation/images/ElementType.png)
3 RetentionPolicy枚举值
--------------------
![RetentionPolicy](https://github.com/GaoHuijian/javaSE/blob/master/annotation/images/RetentionPolicy.png)
4 注解类型
========
###元注解
####1.@Target
	@Target说明了Annotation所修饰的对象范围
	Annotation可被用于 packages、types（类、接口、枚举、Annotation类型）、类型成员（方法、构造方法、成员变量、枚举值）、方法参数和本地变量（如循环变量、catch参数）
	在Annotation类型的声明中使用了target可更加明晰其修饰的目标
####2.@Retention
	@Retention定义了该Annotation被保留的时间长短
	某些Annotation仅出现在源代码中，而被编译器丢弃；而另一些却被编译在class文件中；编译在class文件中的Annotation可能会被虚拟机忽略，而另一些在class被装载时将被读取（请注意并不影响class的执行，因为Annotation与class在使用上是被分离的）。
	使用这个meta-Annotation可以对 Annotation的“生命周期”限制。

	作用：表示需要在什么级别保存该注释信息，用于描述注解的生命周期（即：被描述的注解在什么范围内有效）

	取值（RetentionPoicy）有：
	1.SOURCE:在源文件中有效（即源文件保留）
	2.CLASS:在class文件中有效（即class保留）
	3.RUNTIME:在运行时有效（即运行时保留）
	
####3.@Documented
	@Documented用于描述其它类型的annotation应该被作为被标注的程序成员的公共API，因此可以被例如javadoc此类的工具文档化。
	Documented是一个标记注解，没有成员。

####4.@Inherited
	@Inherited 元注解是一个标记注解，@Inherited阐述了某个被标注的类型是被继承的。如果一个使用了@Inherited修饰的annotation类型被用于一个class，则这个annotation将被用于该class的子类。
###自定义注解
	使用@interface自定义注解时，自动继承了java.lang.annotation.Annotation接口，由编译程序自动完成其他细节。在定义注解时，不能继承其他的注解或接口。
	@interface用来声明一个注解，其中的每一个方法实际上是声明了一个配置参数。方法的名称就是参数的名称，返回值类型就是参数的类型（返回值类型只能是基本类型、Class、String、enum）。可以通过default来声明参数的默认值。

####定义注解格式：
	public @interface 注解名 {定义体}
	注解参数的可支持数据类型:
		1.所有基本数据类型（int,float,boolean,byte,double,char,long,short)
		2.String类型
		3.Class类型
		4.enum类型
		5.Annotation类型
		6.以上所有类型的数组

