Java输入输出
==========
* Input/Output,Java把IO这些功能成为流
* 流:从起点到接手电有序的数据序列

流的分类:
-------
* 按照方向分:

		输入流(只读) 
		输出流(只写)
* 安照处理的数据分:

		字节流   读取/写入,以字节为单位 
		字符流 读取/写入,以字符为单位
* 安照处理的功能分

		低级流:直接从数据的源头读取或写入的流成为低级流,也称节点流
		高级流:对一个已经存在的流的链接和封装,也叫处理流.

1 字节流
-------
类层次结构

###输入流

![InputStream](https://github.com/GaoHuijian/javaSE/blob/master/Io/images/InputStream.png)

###输出流

![OutputStream](https://github.com/GaoHuijian/javaSE/blob/master/Io/images/OutputStream.png)
2 字符流
------
类层次结构

###输入流

![Reader](https://github.com/GaoHuijian/javaSE/blob/master/Io/images/Reader.png)

###输出流

![Writer](https://github.com/GaoHuijian/javaSE/blob/master/Io/images/Writer.png)
3 文件操作
----------
4 基本操作
----------
* FileInputStrea
* FileOutStream
* 换行处理,需要自己处理

5 用流的套路
-----------
* 1 不要单独使用低级流,都是用低级流和高级流搭配使用.
* 2 流基本上都是成对出现的,
* 3 初始化的时候先初始化低级流,再初始化高级流
* 4 我们只要关闭高级流,关闭后,不需要flush();
* 5 根据不同的功能,可以让不同高级流和低级流搭配使用,低级流操作不便的地方, 可以让高级流来完成.




6 File
-----
7何时需要使用字符流?何时需要使用字节流?
----------------
* 需要读取GBK编码的纯文本的内容的时候,才需要字符流,其他都用字节流.

8 能读能写的流
------------
* RandomAccessFile
* 不支持GBK 的编码格式,只支持ISO-8859-1编码格式. 要编码格式转换
* 强项:随机读写文件.


9 ObjectOutputStream
---------------------
* 将对象写入流中
* 把对象写到文件中或网络中,被称为序列化. 要实现:Serializable接口
* Serializable是标记类型<接口是空的>
* 序列化的实质:把对象的信息写的文件中,对象的完整类名信息,对象的实例属性信息会被写到文件中.这就要求类的所有的实例属性都要实现Serializable接口.
* 对象的静态属性信息,方法,构造方法,局部变量,不会写到文件中.
* 反序列化:从文件或网络中读取对象,成为反序列化.
* 反序列实质:从文件读取对象的信息,然后JVM根据这些信息,在内存中重新创建了一个新的对象(也就是克隆了一份).
* serialVersionUID 序列化的时候

10 序列化安全
------------------
* 对于重要的敏感数据,不要写入序列化,用transient修饰符修饰
* 对于不能序列化的实例属性,用transient修饰,忽略序列化.
* 定制序列化<加密> 

























