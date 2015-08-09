Properties 类表示了一个持久的属性集。Properties 可保存在流中或从流中加载。属性列表中每个键及其对应值都是一个字符串。 

一个属性列表可包含另一个属性列表作为它的“默认值”；如果未能在原有的属性列表中搜索到属性键，则搜索第二个属性列表。 

因为 Properties 继承于 Hashtable，所以可对 Properties 对象应用 put 和 putAll 方法。但不建议使用这两个方法，因为它们允许调用者插入其键或值不是 String 的项。相反，应该使用 setProperty 方法。如果在“不安全”的 Properties 对象（即包含非 String 的键或值）上调用 store 或 save 方法，则该调用将失败。类似地，如果在“不安全”的 Properties 对象（即包含非 String 的键）上调用 propertyNames 或 list 方法，则该调用将失败。 
load(Reader) / store(Writer, String) 方法按下面所指定的、简单的面向行的格式在基于字符的流中加载和存储属性。除了输入/输出流使用 ISO 8859-1 字符编码外，load(InputStream) / store(OutputStream, String) 方法与 load(Reader)/store(Writer, String) 对的工作方式完全相同。可以使用 Unicode 转义来编写此编码中无法直接表示的字符；转义序列中只允许单个 'u' 字符。可使用 native2ascii 工具对属性文件和其他字符编码进行相互转换。 

loadFromXML(InputStream) 和 storeToXML(OutputStream, String, String) 方法按简单的 XML 格式加载和存储属性。默认使用 UTF-8 字符编码，但如果需要，可以指定某种特定的编码。XML 属性文档具有以下 DOCTYPE 声明： 

 <!DOCTYPE properties SYSTEM "http://java.sun.com/dtd/properties.dtd">
 注意，导入或导出属性时不 访问系统 URI (http://java.sun.com/dtd/properties.dtd)；该系统 URI 仅作为一个唯一标识 DTD 的字符串： 
    <?xml version="1.0" encoding="UTF-8"?>

    <!-- DTD for properties -->

    <!ELEMENT properties ( comment?, entry* ) >

    <!ATTLIST properties version CDATA #FIXED "1.0">

    <!ELEMENT comment (#PCDATA) >

    <!ELEMENT entry (#PCDATA) >

    <!ATTLIST entry key CDATA #REQUIRED>
 

从以下版本开始： 
JDK1.0 
另请参见：
native2ascii tool for Solaris, native2ascii tool for Windows 
此类是线程安全的：多个线程可以共享单个 Properties 对象而无需进行外部同步。, 序列化表格

