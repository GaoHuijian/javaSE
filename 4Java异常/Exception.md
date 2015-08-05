Java异常
========
当出现了异常,而没有采取处理措施,程序会从发生异常的代码处中断,后面的代码不会执行.

Java异常分类
----------
1,未检查异常(UnCheck) RuntimeException
2,已检查异常(Check)Exception及其子类(但不是RuntimeException的子类)


对于未检异常:
* 通过编程的方式进行避免
* 可以使用Java中提供的异常处理措施进行处理
		try{
			//可能发生异常的代码
		   }
		catch()
		{
		}
* 可以合起来处理,也可以分别处理
* 当多个操作之间有联系的时候,应该合着处理,当多个操作没有联系的时候,应该分着处理.
* 合着处理的时候注意事项:
* 多个catch里面的异常,必须按照继承关系从小到大排列.
* 能否用一个catch(Exception ex){}替代所有的异常分支.不可以:必须捕获不同的异常,分别采取措施.
* 必须要执行的代码,放到finally{}里面.
		try{}
		catch() {}
		catch() {}  	return 无法拦截finally System.exit(0)可以拦截finally.
		finally{}