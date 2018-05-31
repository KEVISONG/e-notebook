# Java SE Study Notes
> By Kevin Song
<!-- MarkdownTOC autolink="true" -->

- [01 Java SE 概述](#01-java-se-%E6%A6%82%E8%BF%B0)
	- [01-01 基础常识](#01-01-%E5%9F%BA%E7%A1%80%E5%B8%B8%E8%AF%86)
	- [01-02 Java语言概述](#01-02-java%E8%AF%AD%E8%A8%80%E6%A6%82%E8%BF%B0)
	- [01-03 Java语言的坏境搭建](#01-03-java%E8%AF%AD%E8%A8%80%E7%9A%84%E5%9D%8F%E5%A2%83%E6%90%AD%E5%BB%BA)
	- [01-04 Hello World](#01-04-hello-world)
- [02 Java SE 语言基础](#02-java-se-%E8%AF%AD%E8%A8%80%E5%9F%BA%E7%A1%80)
	- [02-01 关键字](#02-01-%E5%85%B3%E9%94%AE%E5%AD%97)
	- [02-02 标识符](#02-02-%E6%A0%87%E8%AF%86%E7%AC%A6)
	- [02-03 注释](#02-03-%E6%B3%A8%E9%87%8A)
	- [02-04 常量和变量](#02-04-%E5%B8%B8%E9%87%8F%E5%92%8C%E5%8F%98%E9%87%8F)
		- [常量](#%E5%B8%B8%E9%87%8F)
		- [变量](#%E5%8F%98%E9%87%8F)
		- [数据类型：](#%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B%EF%BC%9A)
	- [02-05 运算符](#02-05-%E8%BF%90%E7%AE%97%E7%AC%A6)
	- [02-06 语句](#02-06-%E8%AF%AD%E5%8F%A5)
		- [顺序结构](#%E9%A1%BA%E5%BA%8F%E7%BB%93%E6%9E%84)
		- [判断结构](#%E5%88%A4%E6%96%AD%E7%BB%93%E6%9E%84)
		- [选择结构](#%E9%80%89%E6%8B%A9%E7%BB%93%E6%9E%84)
		- [循环结构](#%E5%BE%AA%E7%8E%AF%E7%BB%93%E6%9E%84)
		- [break & continue](#break--continue)
	- [02-07 方法](#02-07-%E6%96%B9%E6%B3%95)
		- [方法重载](#%E6%96%B9%E6%B3%95%E9%87%8D%E8%BD%BD)
	- [02-08 数组（引用数据类型）](#02-08-%E6%95%B0%E7%BB%84%EF%BC%88%E5%BC%95%E7%94%A8%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B%EF%BC%89)
		- [一维数组](#%E4%B8%80%E7%BB%B4%E6%95%B0%E7%BB%84)
		- [二维数组](#%E4%BA%8C%E7%BB%B4%E6%95%B0%E7%BB%84)
- [03 Java SE 面向对象](#03-java-se-%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1)
	- [03-01 类与对象](#03-01-%E7%B1%BB%E4%B8%8E%E5%AF%B9%E8%B1%A1)
		- [成员变量和局部变量的区别](#%E6%88%90%E5%91%98%E5%8F%98%E9%87%8F%E5%92%8C%E5%B1%80%E9%83%A8%E5%8F%98%E9%87%8F%E7%9A%84%E5%8C%BA%E5%88%AB)
		- [类类型参数使用](#%E7%B1%BB%E7%B1%BB%E5%9E%8B%E5%8F%82%E6%95%B0%E4%BD%BF%E7%94%A8)
	- [03-02 封装](#03-02-%E5%B0%81%E8%A3%85)
	- [03-03 构造方法](#03-03-%E6%9E%84%E9%80%A0%E6%96%B9%E6%B3%95)
		- [构造方法和一般方法的区别](#%E6%9E%84%E9%80%A0%E6%96%B9%E6%B3%95%E5%92%8C%E4%B8%80%E8%88%AC%E6%96%B9%E6%B3%95%E7%9A%84%E5%8C%BA%E5%88%AB)
		- [this关键字](#this%E5%85%B3%E9%94%AE%E5%AD%97)
		- [static关键字](#static%E5%85%B3%E9%94%AE%E5%AD%97)
		- [成员变量和静态变量的区别](#%E6%88%90%E5%91%98%E5%8F%98%E9%87%8F%E5%92%8C%E9%9D%99%E6%80%81%E5%8F%98%E9%87%8F%E7%9A%84%E5%8C%BA%E5%88%AB)
		- [静态代码块](#%E9%9D%99%E6%80%81%E4%BB%A3%E7%A0%81%E5%9D%97)
		- [构造代码块](#%E6%9E%84%E9%80%A0%E4%BB%A3%E7%A0%81%E5%9D%97)
		- [数组工具类](#%E6%95%B0%E7%BB%84%E5%B7%A5%E5%85%B7%E7%B1%BB)
	- [03-04 单例设计模式](#03-04-%E5%8D%95%E4%BE%8B%E8%AE%BE%E8%AE%A1%E6%A8%A1%E5%BC%8F)
	- [03-05 继承](#03-05-%E7%BB%A7%E6%89%BF)
		- [子父类中成员的特点体现：](#%E5%AD%90%E7%88%B6%E7%B1%BB%E4%B8%AD%E6%88%90%E5%91%98%E7%9A%84%E7%89%B9%E7%82%B9%E4%BD%93%E7%8E%B0%EF%BC%9A)
		- [对象实例化和初始化过程](#%E5%AF%B9%E8%B1%A1%E5%AE%9E%E4%BE%8B%E5%8C%96%E5%92%8C%E5%88%9D%E5%A7%8B%E5%8C%96%E8%BF%87%E7%A8%8B)
		- [final关键字](#final%E5%85%B3%E9%94%AE%E5%AD%97)
		- [抽象类](#%E6%8A%BD%E8%B1%A1%E7%B1%BB)
	- [03-06 接口](#03-06-%E6%8E%A5%E5%8F%A3)
		- [接口和抽象类的异同点](#%E6%8E%A5%E5%8F%A3%E5%92%8C%E6%8A%BD%E8%B1%A1%E7%B1%BB%E7%9A%84%E5%BC%82%E5%90%8C%E7%82%B9)
	- [03-07 多态](#03-07-%E5%A4%9A%E6%80%81)
		- [多态中的成员特点](#%E5%A4%9A%E6%80%81%E4%B8%AD%E7%9A%84%E6%88%90%E5%91%98%E7%89%B9%E7%82%B9)
	- [03-08 内部类](#03-08-%E5%86%85%E9%83%A8%E7%B1%BB)
		- [匿名内部类](#%E5%8C%BF%E5%90%8D%E5%86%85%E9%83%A8%E7%B1%BB)
	- [03-09 异常](#03-09-%E5%BC%82%E5%B8%B8)
		- [异常体系](#%E5%BC%82%E5%B8%B8%E4%BD%93%E7%B3%BB)
		- [异常处理方式](#%E5%BC%82%E5%B8%B8%E5%A4%84%E7%90%86%E6%96%B9%E5%BC%8F)
		- [异常应用](#%E5%BC%82%E5%B8%B8%E5%BA%94%E7%94%A8)
	- [03-10 Object类](#03-10-object%E7%B1%BB)
		- [Object类常用方法](#object%E7%B1%BB%E5%B8%B8%E7%94%A8%E6%96%B9%E6%B3%95)
	- [03-11 包](#03-11-%E5%8C%85)
		- [包与包之间的访问](#%E5%8C%85%E4%B8%8E%E5%8C%85%E4%B9%8B%E9%97%B4%E7%9A%84%E8%AE%BF%E9%97%AE)
- [04 Java SE 多线程](#04-java-se-%E5%A4%9A%E7%BA%BF%E7%A8%8B)
	- [04-01 多线程概述](#04-01-%E5%A4%9A%E7%BA%BF%E7%A8%8B%E6%A6%82%E8%BF%B0)
	- [04-02 JVM中的多线程](#04-02-jvm%E4%B8%AD%E7%9A%84%E5%A4%9A%E7%BA%BF%E7%A8%8B)
	- [04-03 多线程创建](#04-03-%E5%A4%9A%E7%BA%BF%E7%A8%8B%E5%88%9B%E5%BB%BA)
		- [创建多线程](#%E5%88%9B%E5%BB%BA%E5%A4%9A%E7%BA%BF%E7%A8%8B)
			- [创建线程方式一](#%E5%88%9B%E5%BB%BA%E7%BA%BF%E7%A8%8B%E6%96%B9%E5%BC%8F%E4%B8%80)
			- [创建线程方式二](#%E5%88%9B%E5%BB%BA%E7%BA%BF%E7%A8%8B%E6%96%B9%E5%BC%8F%E4%BA%8C)
	- [04-04 多线程同步](#04-04-%E5%A4%9A%E7%BA%BF%E7%A8%8B%E5%90%8C%E6%AD%A5)
		- [多线程同步](#%E5%A4%9A%E7%BA%BF%E7%A8%8B%E5%90%8C%E6%AD%A5)
	- [04-05 多线程中的单例模式](#04-05-%E5%A4%9A%E7%BA%BF%E7%A8%8B%E4%B8%AD%E7%9A%84%E5%8D%95%E4%BE%8B%E6%A8%A1%E5%BC%8F)
	- [04-06 多线程死锁](#04-06-%E5%A4%9A%E7%BA%BF%E7%A8%8B%E6%AD%BB%E9%94%81)
	- [04-07 多线程通信](#04-07-%E5%A4%9A%E7%BA%BF%E7%A8%8B%E9%80%9A%E4%BF%A1)
		- [等待唤醒机制](#%E7%AD%89%E5%BE%85%E5%94%A4%E9%86%92%E6%9C%BA%E5%88%B6)
		- [JDK1.5新特性](#jdk15%E6%96%B0%E7%89%B9%E6%80%A7)
	- [04-08 多线程停止](#04-08-%E5%A4%9A%E7%BA%BF%E7%A8%8B%E5%81%9C%E6%AD%A2)
		- [停止线程](#%E5%81%9C%E6%AD%A2%E7%BA%BF%E7%A8%8B)
- [05 常用API](#05-%E5%B8%B8%E7%94%A8api)
	- [05-01 String类](#05-01-string%E7%B1%BB)
		- [String类特点](#string%E7%B1%BB%E7%89%B9%E7%82%B9)
		- [String类构造方法](#string%E7%B1%BB%E6%9E%84%E9%80%A0%E6%96%B9%E6%B3%95)
		- [String类常见功能](#string%E7%B1%BB%E5%B8%B8%E8%A7%81%E5%8A%9F%E8%83%BD)
		- [String类练习](#string%E7%B1%BB%E7%BB%83%E4%B9%A0)
		- [StringBuffer类](#stringbuffer%E7%B1%BB)
		- [StringBuilder类](#stringbuilder%E7%B1%BB)
	- [05-02 基本数据类型对象包装类](#05-02-%E5%9F%BA%E6%9C%AC%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B%E5%AF%B9%E8%B1%A1%E5%8C%85%E8%A3%85%E7%B1%BB)
		- [概述](#%E6%A6%82%E8%BF%B0)
		- [字符串和基本数值互相转换](#%E5%AD%97%E7%AC%A6%E4%B8%B2%E5%92%8C%E5%9F%BA%E6%9C%AC%E6%95%B0%E5%80%BC%E4%BA%92%E7%9B%B8%E8%BD%AC%E6%8D%A2)
		- [进制转换](#%E8%BF%9B%E5%88%B6%E8%BD%AC%E6%8D%A2)
		- [JDK 1.5自动装箱拆箱](#jdk-15%E8%87%AA%E5%8A%A8%E8%A3%85%E7%AE%B1%E6%8B%86%E7%AE%B1)
	- [05-03 集合框架](#05-03-%E9%9B%86%E5%90%88%E6%A1%86%E6%9E%B6)
		- [05-03-01 Collection概述](#05-03-01-collection%E6%A6%82%E8%BF%B0)
			- [迭代器](#%E8%BF%AD%E4%BB%A3%E5%99%A8)
		- [05-03-02 List集合](#05-03-02-list%E9%9B%86%E5%90%88)
		- [05-03-03 Set集合](#05-03-03-set%E9%9B%86%E5%90%88)
			- [HashSet集合](#hashset%E9%9B%86%E5%90%88)
		- [05-03-04 泛型](#05-03-04-%E6%B3%9B%E5%9E%8B)
			- [泛型概述](#%E6%B3%9B%E5%9E%8B%E6%A6%82%E8%BF%B0)
			- [泛型在集合中的应用](#%E6%B3%9B%E5%9E%8B%E5%9C%A8%E9%9B%86%E5%90%88%E4%B8%AD%E7%9A%84%E5%BA%94%E7%94%A8)
			- [泛型类](#%E6%B3%9B%E5%9E%8B%E7%B1%BB)
			- [泛型方法](#%E6%B3%9B%E5%9E%8B%E6%96%B9%E6%B3%95)
			- [泛型接口](#%E6%B3%9B%E5%9E%8B%E6%8E%A5%E5%8F%A3)
			- [泛型限定](#%E6%B3%9B%E5%9E%8B%E9%99%90%E5%AE%9A)
		- [05-03-05 Map集合](#05-03-05-map%E9%9B%86%E5%90%88)
			- [Map集合概述](#map%E9%9B%86%E5%90%88%E6%A6%82%E8%BF%B0)
			- [Map集合常用子类对象](#map%E9%9B%86%E5%90%88%E5%B8%B8%E7%94%A8%E5%AD%90%E7%B1%BB%E5%AF%B9%E8%B1%A1)
		- [05-03-06 工具类（Collections，Arrays）](#05-03-06-%E5%B7%A5%E5%85%B7%E7%B1%BB%EF%BC%88collections%EF%BC%8Carrays%EF%BC%89)
			- [Collections类](#collections%E7%B1%BB)
			- [Arrays类](#arrays%E7%B1%BB)
		- [Array和Collections相互转换](#array%E5%92%8Ccollections%E7%9B%B8%E4%BA%92%E8%BD%AC%E6%8D%A2)
		- [05-03-07 JDK1.5 新特性](#05-03-07-jdk15-%E6%96%B0%E7%89%B9%E6%80%A7)
			- [ForEach循环](#foreach%E5%BE%AA%E7%8E%AF)
			- [方法可变参数](#%E6%96%B9%E6%B3%95%E5%8F%AF%E5%8F%98%E5%8F%82%E6%95%B0)
			- [静态导入](#%E9%9D%99%E6%80%81%E5%AF%BC%E5%85%A5)
	- [05-04 其他对象API](#05-04-%E5%85%B6%E4%BB%96%E5%AF%B9%E8%B1%A1api)
		- [05-04-01 System类](#05-04-01-system%E7%B1%BB)
		- [05-04-02 Runtime类](#05-04-02-runtime%E7%B1%BB)
		- [05-04-03 Math类](#05-04-03-math%E7%B1%BB)
		- [05-04-04 Date类](#05-04-04-date%E7%B1%BB)
		- [05-04-05 Calendar类](#05-04-05-calendar%E7%B1%BB)
- [06 Java SE IO](#06-java-se-io)
	- [06-01 IO流概述](#06-01-io%E6%B5%81%E6%A6%82%E8%BF%B0)
		- [概述](#%E6%A6%82%E8%BF%B0-1)
	- [06-02 字节流和字符流](#06-02-%E5%AD%97%E8%8A%82%E6%B5%81%E5%92%8C%E5%AD%97%E7%AC%A6%E6%B5%81)
		- [06-02-01 字符流](#06-02-01-%E5%AD%97%E7%AC%A6%E6%B5%81)
			- [FileWirter类](#filewirter%E7%B1%BB)
			- [FileReader类](#filereader%E7%B1%BB)
			- [缓冲区](#%E7%BC%93%E5%86%B2%E5%8C%BA)
			- [BufferWirter类](#bufferwirter%E7%B1%BB)
			- [BufferReader类](#bufferreader%E7%B1%BB)
			- [LineNumberReader类](#linenumberreader%E7%B1%BB)
			- [装饰设计模式](#%E8%A3%85%E9%A5%B0%E8%AE%BE%E8%AE%A1%E6%A8%A1%E5%BC%8F)
		- [06-02-02 字节流](#06-02-02-%E5%AD%97%E8%8A%82%E6%B5%81)
			- [IO流键盘输入](#io%E6%B5%81%E9%94%AE%E7%9B%98%E8%BE%93%E5%85%A5)
		- [06-02-03 转换流](#06-02-03-%E8%BD%AC%E6%8D%A2%E6%B5%81)
		- [06-02-04 IO流的操作规律](#06-02-04-io%E6%B5%81%E7%9A%84%E6%93%8D%E4%BD%9C%E8%A7%84%E5%BE%8B)
	- [06-03 File类](#06-03-file%E7%B1%BB)
			- [常用方法](#%E5%B8%B8%E7%94%A8%E6%96%B9%E6%B3%95)
		- [06-03-01 递归](#06-03-01-%E9%80%92%E5%BD%92)
	- [06-04 Properties集合](#06-04-properties%E9%9B%86%E5%90%88)
		- [基本功能](#%E5%9F%BA%E6%9C%AC%E5%8A%9F%E8%83%BD)
			- [练习](#%E7%BB%83%E4%B9%A0)
	- [06-05 其他IO类](#06-05-%E5%85%B6%E4%BB%96io%E7%B1%BB)
		- [06-05-01 打印流](#06-05-01-%E6%89%93%E5%8D%B0%E6%B5%81)
			- [PrintStream](#printstream)
			- [PrintWriter](#printwriter)
		- [06-05-02 序列流](#06-05-02-%E5%BA%8F%E5%88%97%E6%B5%81)
			- [SequenceInputStream](#sequenceinputstream)
			- [文件切割合并](#%E6%96%87%E4%BB%B6%E5%88%87%E5%89%B2%E5%90%88%E5%B9%B6)
		- [06-05-03 ObjectStream](#06-05-03-objectstream)
			- [ObjectStream](#objectstream)
			- [Serializable接口](#serializable%E6%8E%A5%E5%8F%A3)
		- [06-05-04 RandomAccessFile类](#06-05-04-randomaccessfile%E7%B1%BB)
		- [06-05-05 管道流](#06-05-05-%E7%AE%A1%E9%81%93%E6%B5%81)
		- [06-05-06 DataStream](#06-05-06-datastream)
		- [06-05-07 操作数组的流](#06-05-07-%E6%93%8D%E4%BD%9C%E6%95%B0%E7%BB%84%E7%9A%84%E6%B5%81)
			- [ByteArrayStream](#bytearraystream)
		- [06-05-08 编码表](#06-05-08-%E7%BC%96%E7%A0%81%E8%A1%A8)
			- [常见的编码表](#%E5%B8%B8%E8%A7%81%E7%9A%84%E7%BC%96%E7%A0%81%E8%A1%A8)
			- [简单的编码解码](#%E7%AE%80%E5%8D%95%E7%9A%84%E7%BC%96%E7%A0%81%E8%A7%A3%E7%A0%81)
- [07 Java SE GUI](#07-java-se-gui)
	- [07-01 GUI概述](#07-01-gui%E6%A6%82%E8%BF%B0)
		- [继承关系](#%E7%BB%A7%E6%89%BF%E5%85%B3%E7%B3%BB)
		- [布局](#%E5%B8%83%E5%B1%80)
		- [Frame演示](#frame%E6%BC%94%E7%A4%BA)
	- [07-02 事件监听](#07-02-%E4%BA%8B%E4%BB%B6%E7%9B%91%E5%90%AC)
- [08 Java SE 网络编程](#08-java-se-%E7%BD%91%E7%BB%9C%E7%BC%96%E7%A8%8B)
	- [08-01 网络模型概述](#08-01-%E7%BD%91%E7%BB%9C%E6%A8%A1%E5%9E%8B%E6%A6%82%E8%BF%B0)
	- [08-02 TCP和UDP协议](#08-02-tcp%E5%92%8Cudp%E5%8D%8F%E8%AE%AE)
		- [UDP协议](#udp%E5%8D%8F%E8%AE%AE)
		- [TCP协议](#tcp%E5%8D%8F%E8%AE%AE)
	- [08-03 网络编程其他](#08-03-%E7%BD%91%E7%BB%9C%E7%BC%96%E7%A8%8B%E5%85%B6%E4%BB%96)
		- [常见客户端和服务端](#%E5%B8%B8%E8%A7%81%E5%AE%A2%E6%88%B7%E7%AB%AF%E5%92%8C%E6%9C%8D%E5%8A%A1%E7%AB%AF)
		- [自定义客户端和服务端](#%E8%87%AA%E5%AE%9A%E4%B9%89%E5%AE%A2%E6%88%B7%E7%AB%AF%E5%92%8C%E6%9C%8D%E5%8A%A1%E7%AB%AF)
		- [URL&URL Connection](#urlurl-connection)
		- [常见网络架构](#%E5%B8%B8%E8%A7%81%E7%BD%91%E7%BB%9C%E6%9E%B6%E6%9E%84)
- [09 Java SE 反射](#09-java-se-%E5%8F%8D%E5%B0%84)
	- [获取Class对象](#%E8%8E%B7%E5%8F%96class%E5%AF%B9%E8%B1%A1)
	- [获取Class中的构造方法](#%E8%8E%B7%E5%8F%96class%E4%B8%AD%E7%9A%84%E6%9E%84%E9%80%A0%E6%96%B9%E6%B3%95)
	- [获取Class中的字段](#%E8%8E%B7%E5%8F%96class%E4%B8%AD%E7%9A%84%E5%AD%97%E6%AE%B5)
	- [获取Class中的方法](#%E8%8E%B7%E5%8F%96class%E4%B8%AD%E7%9A%84%E6%96%B9%E6%B3%95)
	- [反射练习](#%E5%8F%8D%E5%B0%84%E7%BB%83%E4%B9%A0)
- [10 Java SE 正则表达式](#10-java-se-%E6%AD%A3%E5%88%99%E8%A1%A8%E8%BE%BE%E5%BC%8F)
	- [概述](#%E6%A6%82%E8%BF%B0-2)
	- [常见的规则](#%E5%B8%B8%E8%A7%81%E7%9A%84%E8%A7%84%E5%88%99)
	- [常见功能](#%E5%B8%B8%E8%A7%81%E5%8A%9F%E8%83%BD)
	- [正则表达式练习](#%E6%AD%A3%E5%88%99%E8%A1%A8%E8%BE%BE%E5%BC%8F%E7%BB%83%E4%B9%A0)
	- [网页爬虫](#%E7%BD%91%E9%A1%B5%E7%88%AC%E8%99%AB)

<!-- /MarkdownTOC -->

# 01 Java SE 概述

## 01-01 基础常识  
1. 软件开发
软件：一系列按照特定顺序组织的计算机数据和指令的集合  
常见的软件：
    - 系统软件：DOS，windows，Linux等。
    - 应用软件：扫雷，迅雷，QQ等。
    - 开发就是软件制作
2. 人机交互方式
    - 图形化界面GUI  
    - 命令行方式CLI Command Line Interface 
3. 常用的DOS命令
    - cd: 进入目的文件夹  
    - cd\ 退回根目录  
    - cd..返回上一级目录  
    - dir 显示所有文件和文件夹  
    - exit退出DOS

## 01-02 Java语言概述

是SUN（Stanford University Network，斯坦福大学网络公司）1995年推出的一门高级编程语言。
是一种面向Internet的语言。

- Java语言的三种技术架构
    1. Java EE 企业版
    2. Java SE 标准版
    3. Java ME 小型版
- Java语言的特点：跨平台性（Write Once, Run Anywhere）

## 01-03 Java语言的坏境搭建

- 明确什么是JRE,JDK
- 下载JDK
- 安装JDK
- 配置环境变量
- 验证是否成功

JRE （Java Runtime Environment  Java运行环境）
包括Java虚拟机（JVM Java Virtual Machine）  

JDK（Java Development Kit  Java开发工具包）

**JDK包含了Java的开发工具和JRE**

**配置环境变量**：把Java/bin目录复制到Path  

验证环境变量是否配置成功：直接输入Java或者Javac可以识别  

## 01-04 Hello World
1. 将Java代码编写到扩展名为.Java的文件中  
2. 通过Javac命令对Java文件进行编译  
3. 通过Java命令对生成的Class文件进行运行。  

```
graph LR
JavacHelloWorld.java-->HelloWorld.clas
HelloWorld.clas--> JavaHelloWorld.clas
```
1. 代码编写  
2. Javac 编译
3. Java 运行  

```
public class Demo {//定义类
    public static void main(String[] args) {//定义主函数
        System.out.println("Hello World");
    }
}
```

主函数  
1. 是程序的入口  
2. 被虚拟机所调用
3. 有了主函数可以保证一个类的独立运行
4. 只有一个主函数

println 自动换行  
print 不自动换行

# 02 Java SE 语言基础
## 02-01 关键字

Java里先定义的，有特别意义的标识符。所有字母都是小写  

- 定义数据类型的关键字：class, interface, byte, short, int, long, float, double, char, boolean, void.  
- 定义数据类型值的关键字：true, false, null.  
- 定义流程控制的关键字：if, else, switch, case, default, while, do, for, break, continue, return.  
- 定义访问权限修饰符的关键字：private, protected, public.  
- 定义类，方法，变量修饰符的关键字：abstract, final, static, synchronized.  
- 定义类与类之间关系的关键字：extends, implements.  
- 定义建立实例，引用实例，判断实例的关键字：new, this, super, instanceof.  
- 用于异常处理的关键字：try, catch, finally, throw, throws.  
- 用于包的关键字：package, import.  
- 其他修饰符关键字：native, strictfp, transient, volatile, assert.

## 02-02 标识符

程序中自定义的名称，由26个英文字母大小写，数字，_$组成。  
规则：
- 数字不能开头
- 不可以使用关键字  

## 02-03 注释
用于注解说明解释程序的文字就是注释  
注释的格式：

1. 单行注释：// 注释文字
2. 多行注释：/*注释文字 */
3. 文档注释：/**注释文字 */

## 02-04 常量和变量  

### 常量

不能改变的数值  

常量分类：

1. 整数常量：所有整数
2. 小数常量：所有小数
3. 布尔型常量：true false
4. 字符常量：将一个数字字母或者符号用单引号（‘’）标识
5. 字符串常量。将一个或多个字符用双引号（“”）标识
6. null常量：null

整数有四种表现形式

- 二进制：0，1
- 八进制：0 - 7
- 十进制：0 - 9
- 十六进制： 0 - 9，A - F，0x开头。

负数的补码表现形式 

- 对应正数二进制取反加1

### 变量
- 内存中的一个存储区域
- 该区域有自己的名称（变量名）和类型（数据类型）
- 该区域的数据可以在同一类型范围内不断变化

定义变量的格式：变量名=初始化值  

---

### 数据类型：

1. 基本数据类型
   1. 数值型
      1. 整数类型
         1. byte 字节 8bit (-2^7^, 2^7^-1) (-128, 127)
         2. short 短整型 16bit (-2^15^, 2^15^-1) (-32768, 32767)
         3. int 整型 32bit（-2^31^, 2^31^-1）
         4. long 长整型 64bit（-2^63^, 2^63^-1）
      2. 浮点类型
         1. float
         2. double
   2. 字符型（char）（0, 65535)
   3. 布尔型（boolean）
2. 引用数据类型
   1. 类（class）
   2. 接口（interface）
   3. 数组（[ ]）

```
//变量基本演示
public class VarDemo {
    public static void main(String[] args) {
        byte b = 3;
        short s = 4000;
        int x = 12;
        long l = 123l;
        
        float f = 2.3f;
        double d = 3.4;
        
        char ch = 'K';
        boolean bl = true;
        System.out.println(ch);
    }
}
```
自动类型转换  
强制类型转换
```
//自动类型提升和强制转换
public class VarDemo2 {
    public static void main(String[] args){

        int x = 3;
        byte b = 5;
        x = x + b; //b会进行自动类型提升

        byte b = 3;
        b = b + 4; //报错，因为4为int。
        b = (byte)(b + 4); //结果是7。强制类型转换
        b = (byte)(b + 200); //结果是-53

        System.out.println(b);
    }
}

```
字符类型运算过程  
```
System.out.println('a'+1);
//输出为98
System.out.println(char('a'+1));
//输出为b
System.out.println(char('你'+1));
//输出为20321
```
## 02-05 运算符  

1. 算数运算符
    1. “ + ”
    2. “ - ”
    3. “ * ” 
    4. “ / ”
    5. “ % ” 取余，模 
    6. “ ++ ” 自增，++ a先加再算，a++ 先算再加 
    7. “ -- ” 自减，-- a先减再算，a-- 先算再减  
2. 赋值运算符
    1. “ = ” 赋值
    2. “ += ” a+=1 一次赋值运算， a=a+1 一次算数运算和一次赋值运算
    3. “ -= ”
    4. “ *= ”
    5. “ /= ”
    6. “ %= ” 
3. 比较运算符（运算完的结果必须是true或者false）  
    1. “ == ” 相等于
    2. “ > ” 大于
    3. “ < ” 小于
    4. “ >= ” 大于等于
    5. “ <= ” 小于等于
    6. “ != ” 不等于
    7. “ instanceof ” 检查是否是类的对象
4. 逻辑运算符（用于连接两个boolean类型的表达式）  
    1. “ & ” AND（与）
    2. “ | ” OR （或）
    3. “ ^ ” XOR（异或）两边相同则false
    4. “ ! ” NOT（非）
    5. “ && ”AND（短路）左边为false时，右边不参与运算
    6. “ || ”OR （短路）左边为true时，右边不参与运算
5. 位运算符（二进制位）  
    1. “ << ” 左移：左移几位就是该数据乘以2的几次方
    2. “ >> ” 右移：右移几位就是该数据除以2的几次方，高位出现的空位用原来高位的数字补
    3. “ >>> ” 无符号右移：高位用0补
    4. “ & ” 与
    5. “ | ” 或
    6. “ ^  ” 异或
    7. “ ~ ” 反码
6. 三元运算符：三个元素参与运算的符号

格式：（条件表达式）？表达式1：表达式2；

如果条件为true，运算后的结果是表达式1，如果条件为false，运算后的结果是表达式2.

## 02-06 语句  

### 顺序结构

按照顺序从上往下执行

### 判断结构

if语句

```
1. if(条件表达式) {  
        执行语句;  
    }
```
```
2.  if(条件表达式) {  
        执行语句;  
    } else {  
        执行语句;  
    }
```
```
3.  if(条件表达式) {  
        执行语句;  
    } else if {  
        执行语句;  
    }  
    ...  
    else {  
        执行语句;  
    }
```


局部代码块：局部代码块可以定义局部变量的生命周期

### 选择结构

switch语句

```
switch(表达式) {  //byte,short,int,char.  
        case 取值1:  
        执行语句;  
        break;  
        case 取值2:  
        执行语句;  
        break;  
        ...  
        default: //永远最后执行  
        执行语句;  
        break;  
     }
```

---

if和switch的应用  

if

- 对具体的值进行判断
- 对区间判断
- 对运算结果是boolean类型的表达式进行判断  

switch是

- 对具体的值进行判断
- 值的个数通常是固定的  
对于几个固定的值判断，建议使用switch语句，因为switch语句会将具体的答案都加载进内存


### 循环结构

当对某些代码执行很多次时，使用循环结构。

1. while循环  
        while(条件表达式){  
            执行语句;  
        }
```
        //1到10累加
        int x = 2;
        int y = 1;
        while (x <= 10) {
            y = y + x;
            x++;
        }
        System.out.println(y);
```

```
        //1-100之间6的倍数出现的次数
        int x = 1;
        int Count = 0;
        while (x <= 100) {
            if ( x%6==0 )
                Count++;
                x++;
        }
        System.out.println(Count);
```

2. do while循环//循环体至少执行一次  

```
    do {  
    执行语句;  
} while(条件表达式);
```
3. for循环  

```
for(初始化表达式; 循环条件表达式; 循环后的操作表达式){  
        执行语句;
    }
```

for和while的特点：

1. for和while可以互换。
2. for中的变量只能在for循环中有效。  

无限循环的简单形式  
```
// while(true) {}  

//for(;;) {}
```

- for循环嵌套  

```
for(初始化表达式; 循环条件表达式; 循环后的操作表达式) {  
    for(初始化表达式；循环条件表达式；循环后的操作表达式) {  
        执行语句;  
    }  
}
```

```
*****
*****
*****
*****
*****
for(int x=0; x<5; x++) {  //外层控制行数
        for (int y=0; y<5; y++) {  //内层控制个数
            System.out.print("*");
        }
        System.out.println();
}
```

```
*****
****
***
**
*
for(int x=0; x<5; x++) {  //外层控制行数
        for (int y=x; y<5; y++) {  //内层控制个数
            System.out.print("*");
        }
        System.out.println();
}
```
```
*
**
***
****
*****
for(int x=0; x<5; x++) {  //外层控制行数
        for (int y=-1; y<x; y++) {  //内层控制个数
            System.out.print("*");
        }
    System.out.println();
}
```
```
1*1=1
1*2=2 2*2=4
1*3=3 2*3=6 3*3=9
for(int x=1; x<=3; x++) {  //外层控制行数
        for (int y=1; y<=x; y++) {  //内层控制个数
            System.out.print(y+"*"+x+"="+x*y + "  ");
        }
        System.out.println();
}
```  
```
* * * * * 
 * * * *
  * * *
   * *
    *
for(int x=1; x<=5; x++) { 
    for (int y=1; y<=x; y++) {  
        System.out.print(“ ”);
    }
    for (int z=x; z<=5; z++) {  
        System.out.print(“* ”);
    }
    System.out.println();
}
```

### break & continue

break语句：应用于选择结构和循环结构。  

```
firstloop: for(int x=1; x<=5; x++) { 
        secondloop: for (int y=1; y<=5; y++) {  
            System.out.print(“x=”+x);
            break firstloop;
        }
}
```

continue语句：应用于循环结构。

转义字符  
- \n: 回车  
- \t: 制表符  
- \b: 退格  
- \r: 按下回车键

## 02-07 方法  

定义在类中的具有特定功能的一段独立小程序

```
修饰符 返回值类型 方法名（参数类型  形式参数1，参数类型 形式参数2，...）
｛
    执行语句；
    return返回值；
｝
```

- 返回值类型：方法运行后的结果的数据类型  
- 参数类型：形式参数的数据类型  
- 形式参数：是一个变量，用于储存调用方法时传递给方法的实际参数  
- 实际参数：传递给形式参数的具体数值  
- return：结束方法  
- 返回值：该方法运算后的结果，该结果会返回给调用者  

```
public static int add(int a,int b) {
 c = a + b;
 return c;
}

int c = add(3, 4);
```


方法名一般格式（驼峰原则）：addTestOne


特殊情况：方法没有具体的返回值

- return后面直接用分号结束
- 返回值类型用void关键字表示

```
public static void myPrint() {
 System.out.print(“Hello World”);
 return;
}

myPrint();
```
两个明确：  

1. 明确方法的返回值类型
2. 明确参数列表

### 方法重载

定义：在同一个类中，允许存在一个以上的同名方法，只要他们的参数个数或者参数类型不同。

重载特点：

- 同一个类
- 同名
- 参数列表不同
- 和返回值无关  

```
//两个整数的和
public static int add(int a, int b) {
    return a+b;
}
//两个小数的和
public static double add(double a, double b) {
    return a+b;
}
//三个整数的和
public static int add(int a, int b, int c) {
    return add(a,b)+c;
}
```
重载的好处：方便与阅读，优化代码。

## 02-08 数组（引用数据类型）  
### 一维数组
同一种类型数据的集合，数组中的数据从0开始编号，方便操作。  

```
//格式一
数据类型 [] 数组名 = new 数据类型 [数据的个数]；  
int [] arr = new int[5];
```
```
//格式二
数据类型 [] 数组名 = new 数据类型 []｛数据，数据，……｝；  
int [] arr = new int[]{3, 5, 1, 7};
int [] arr = new int{3, 5, 1, 7};
x = arr[0]; //取arr中0号位的值赋给x
```
- 栈内存：存储的都是局部变量，变量所属的作用域一旦结束，变量自动释放。  
- 堆内存：存储的是数组和对象 凡是new建立在堆中。都有默认初始化值  

arr存在栈内存中，存的不是具体数据，而是数据在堆内存中的地址。
```
int [] arr = new int [6];
```
左边在栈内存，右边在堆内存。
arr引用了对内存中的数据
```
//例子
//在栈内存中创建x和y，x和y的地址指向在堆内存中创建默认值为0的数组
int[] x = new int [3];
int[] y = new int [3];
//在堆内存中把x和y0号位的数据替换成9和34
x[0] = 9;
y[0] = 34;
//在栈内存中把x的地址改成y的地址
x = y;
```
常见问题
```
int[] arr = new int [3];
System.out.println(arr[3]);
//ArraryIndexOutOfBoundsException
//访问到数组中不存在的位，会发生该异常
arr = null;
System.out.println(arr[0])；
//NullPointerException
//当引用型变量没有任何实体指向时，还在用其操作实体，会发生该异常。
```
常见操作  

- 数组遍历：printArray(arr)
```

public static int printArray(int[] arr) {
    System.out.print("[");
    for (int x=0; x<arr.length; x++) {
        if(x!=arr.length-1)
            System.out.print(arr[x]+",");
        else
            System.out.println(arr[x]+"]");
        System.out.println(arr[x]);
    }
}
```
- 数组最值：getMax(arr)

```
public static int getMax(int[] arr) {
    int max = arr[0]；
    for (int x =1; x<arr.length; x++) {
        if (arr[x]>max)
            max = arr[x];
    }
    return max;
}

```
- 选择排序：selectSort(arr)
```
public static int selectSort(int[] arr) {
    for(int x=0; x<arr.length-1; x++) {
        if (arr[x]>arr[y]) {
            swap(arr, a, b)；
        }
    }
}
```
-  冒泡排序：bubbleSort(Arr)
```
public static int bubbleSort(int[] arr) {
    for(int x=0; x<arr.length-1; x++) {
        for(int y=0; y<arr.length-1-x; y++) {//-1是为了避免角标越界，-x是为了让外循环增加一次，内循环参数与比较的元素个数递减
            if(arr[y]>arr[y+1]) {
                swap(arr, y, y+1)；
            }
        }
    }
}
```
排序位置置换代码提取

```
public static void swap(int [] arr, int a,int b) {
    int temp = arr[a];
    arr[a] = arr[b];
    arr[b] = temp;
}
```
数组查找

```
public static void getIndex(int [] arr, int key) {
    for(int x = 0; x<arr.length; x++) {
        if(arr[x]==key)
            return x;
    }
    return -1;
}
```
### 二维数组
格式1：
```
int[][] arr = new int[3][2];
arr[0][1] = 78;
```
格式2：
```
int[][] arr = new int[3][];
arr[0] = new int [3];
arr[1] = new int [1];
arr[2] = new int [2];
```
# 03 Java SE 面向对象

面向对象的四个基本特征
- 封装
- 继承
- 抽象
- 多态

## 03-01 类与对象

类：事物的描述  

对象：该类事物的实例  

描述汽车

- 属性
    - 轮胎数
    - 颜色
- 行为
    - 运行
```
class Car {
    int num;//成员变量
    String color; //成员变量
    void run() { //成员方法
        System.out.println(num+"..."+color);
    }
}

class CarDemo {
public static void main(String[ args[]) {
        Car c = new Car();//c是一个类类型的引用变量，指向了该类的对象。
        c.num = 4;
        c.color = "Red";
        c.run();
    }
}
```
### 成员变量和局部变量的区别

- 定义**位置**不同
    - 成员变量定义在**类**中，整个类中都可以访问
    - 局部变量定义在**方法，语句，局部代码块**中，只在所属的区域有效
- 存放内存不同
   - 成员变量存在于**堆内存**的对象中
   - 局部变量存在于**栈内存**的方法中
- 释放时间不同
    - 成员变量随着**对象**的创建而存在，随着对象的消失而消失
    - 局部变量随着**所属区域**的执行而存在，随着所属区域的结束而释放
- 初始化不同
    - 成员变量**都有**默认初始化值
    - 局部变量**没有**默认初始化值

### 类类型参数使用

```
//骑车改装厂
public static void show(Car c) { //类类型的变量一定指向对象，要不就是null。
    c.num = 3;
    c.color = "black";
    System.out.println(c.num+“...”+c.color);
}
```
匿名对象：当对象对方法仅调用一次，就可以简化成匿名对象

```
new Car();//定义对象的简写格式
new Car().run();
```
## 03-02 封装

**隐藏**对象的属性和实现细节，仅对外提供公共**访问方式**。

```
class Person {
    private int age; //私有：只在本类中有效，外部无法访问
    
    public void setAge(int a) {
        if (a>0 && a<130)
            age = a;
        else
            System.out.println("数据错误")；
    }
    void speak() {
        System.out.println("age="+age);
    }
}
clasee PersonDemo {
    public static void main(String[] args) {
        Person p = new Person();
        p.setAge(20);
        p.speak();
    }
}
``` 
## 03-03 构造方法

构造对象的时候用的方法

**特点：**

- 方法名与类名相同
- 不用定义返回值类型
- 没有具体的返回值

**作用：**

给**单一**对象进行**初始化**  

**默认构造方法：**

一个类中如果没有定义过构造方法，那么该类中会有一个默认的空参数构造方法。

```
class Person {
    private int age;
    private String name;//私有：只在本类中有效，外部无法访问
    
    //定义一个Person类的构造方法
    Person() {
        Syetem.out.println("person run");
    }
    
    //初始化就有名字
    Person(String n) {
    name = n;
    }
    
    //初始化就有名字和年龄
    Person(String n, int a) {
    name = n;
    age = a;
    }
    
    void speak() {
        System.out.println("age="+age);
    }
}
clasee PersonDemo {
    public static void main(String[] args) {
        Person p = new Person();//构造方法：构建创造对象时用的方法
        Person p1= new Person("就很舒服");//重载构造方法
        Person p2= new Person("就很舒服",10)//重载构造方法
    }
}
``` 
### 构造方法和一般方法的区别

1. - 构造方法：对象创建时，就会被调用，进行对象初始化
    - 一般方法：对象创建后，需要方法的功能时才调用
2. - 构造方法：对象创建时，只调用**一次**
    - 一般方法：对象创建后，可以被**重复**调用

### this关键字

当成员变量和局部变量**重名**，可以用关键字this区分
```
class Person {
    private int age;
    private String name;//私有：只在本类中有效，外部无法访问
    
    //定义一个Person类的构造方法

    Person(String name) {
    this.name = name;//this代表当前对象
    }

    void speak() {
        System.out.println("age="+age);
    }
}
```
**this关键字细节：**  

1.  一般方法不能调用构造方法，因为构造方法是给对象初始化，被对象所调用。
2.  构造方法之间**互相调用**：

```
Person(String name) {
    this.name = name;
}
    
Person(String name, int age) {
    this(name);//必须放在构造方法第一行
    this.age = age;
}
```
### static关键字

- static是一个修饰符，用于修饰成员（成员变量和成员方法）
- static修饰的成员被所有对象**共享**
- static**优先于**对象存在，因为static成员随着类创建而存在
- static修饰的变量可以被类名**直接**调用Person.country

### 成员变量和静态变量的区别

```
String name;
static String country = "CN";
```
- 两个变量的**生命周期**不同
    - 成员变量随着**对象**的创建而存在，随着对象的被回收而释放。
    - 静态变量随着**类**的加载而存在，随着类的消失而消失。
- **调用方式**不同
    - 成员变量只能被**对象**调用
    - 静态变量可以被**对象**和**类名**调用
- **别名**不同
    - 成员变量也称为**实例变量**
    - 静态变量称为**类变量**
- 数据存储**位置**不同
    - 成员变量存储在**堆内存**的对象中，是对象的**特有数据**
    - 静态变量数据存储在**方法区**，是对象的**共享数据**

**static注意事项**

- 静态方法**只能**访问静态成员
- 静态方法中**不可以**使用**this**或者**super**关键字
- 主方法是静态的

**主方法解析**

```
public static void main(String[] args)
```

- public：因为**权限**必须是**最大**的
- static：不需要对象的，直接用主方法所属类名调用即可  
- void：主方法没有具体的返回值
- main：方法名，JVM识别的固定的名字
- String[] args：主方法的参数列表，是一个数组类型的参数，元素都是字符串类型

**static关键字使用场合**

- **静态对象：** 如果是**相同的数据**，对象不需要做修改，只需要使用即可，不需要存储在对象中，这个变量可以用static修饰
- **静态方法：** 如果方法不需要访问非静态的成员变量，可以定义成static

### 静态代码块

**特点**：随着类的加载而执行。而且只执行**一次**

**作用**：给**类**初始化

```
class StaticCode {
    static {
        System.out.println("haha");
    }
}
```
### 构造代码块

```
{//构造代码块。可以给所有对象进行初始化
    System.out.println("Person run");
}
```

- 构造方法给**对应的对象**进行针对性的初始化
- 构造代码块给**所有对象**初始化

### 数组工具类
```
class ArraryToolDemo {
    public static void main(String[] args) {
        int[] arr = {3,5,7,72,6};
        int max = ArrayTool.getIndex(arr,10);//静态方法可以直接被类名调用，不需要创建对象，节约内存空间
        System.out.println("max="+max);
    }
}
/**
建立一个用于操作数组的工具类，期中包含着对数组常见的操作
@author Kevin Song
@version V1.0
*/
class ArrayTool {
    private ArrayTool() {}//该类中的方法都是静态的，所以该类不需要创建对象，为了保证不让其他人创建该类对象可以将构造方法私有化
    /**
    获取整形数组的最大值
    @param arr 接收一个元素为int类型的数组
    @return 该数组的最大的元素值
    */
    public static int getMax(int[] arr) {
        int max = arr[0]；
        for (int x =1; x<arr.length; x++) {
            if (arr[x]>max)
                max = arr[x];
        }
        return max;
    }
}
```
## 03-04 单例设计模式  

**作用**：可以保证一个类在内存中的**对象**是**唯一**的 

**实现思想：**

1. 不允许其他程序用new创建该类对象。
2. 在该类创建一个本类实例
3. 对外提供一个方法让其他程序可以获取该对象

步骤：

1. **私有化**该类构造方法
2. 通过new在本类中创建一个本类**对象**
3. 定义一个公有的**方法**，将创建的对象返回
```
//通过在类中创建一个对象供其他程序使用
//不允许其他程序自己new对象
//对该类对象的修改都是对同一个对象的修改

//饿汉式
class Single {//类一加载，对象就已经建立
    private static Single s = new Single();
    private Single(){}//私有构造方法不允许其他程序new对象
    public static Single getInstance() {
        return s;
    }
}
//懒汉式
class Single2 {//只有调用了getInstance方法才会建立对象

    private static Single2 s = null;
    private Single2() {}//私有构造方法不允许其他程序new对象
    public static Single2 getInstance() {
        if(s==null)
            s = new Single();
        return s;
    }
}
class SingleDemo {
    public static void main(String[] args) {
        Single s = Single.getInstance();
    }
}
```
## 03-05 继承

从已有的类中派生出新的类，新的类能吸收已有类的数据属性和行为，并能扩展新的能力。

```
class Person {
    String name;
    int age;
}
//继承Person类的数据
class Student extends Person {
    void study() {
        System.out.println(name+"..student study.."+age);
    }
}
//继承Person类的数据
class Worker extends Person {
    void work() {
        System.out.println(name+"..worker work.."+age);
    }
}
class ExtendsDemo {
    public static void main(String[] args) {
        Student s = new Student();
        s.name = "Kevin";
        s.age = 24;
        s.study;
    }
}
```

**继承的优点**：

- 提高代码的**复用性**
- 让类与类之间产生了**关系**，给第三个特征多态提供了**前提**

**Java中继承的特点**：  

Java中支持**单继承**。不直接支持**多继承**，但对C++中的多继承机制进行改良

- 单继承：一个子类只能有**一个**直接父类
- 多继承：一个子类可以有**多个**直接父类（Java中用接口进行改良）不直接支持，因为多个父类中有相同成员，会产生调用的不确定性

java支持**多层**（多重）继承

### 子父类中成员的特点体现：

**1. 成员变量**

- 本类的成员和局部变量同名用**this**区分本类成员变量  
- 子父类中的成员变量同名用**super**区分父类  

**原理**：

- this：代表一个**本类对象**的引用  
- super：代表一个**父类空间**

```
class Fu {
    private int num = 4;//子类不能直接访问父类中的私有内容
    //子类可以通过父类提供的方法间接访问父类中的私有内容
    public int getNum() {
        return num;
    }
}
class Zi extends Fu {
    private int num = 5;
    void show() {
        System.out.println(this.num+"....."+super.getNum());
    }
}
class ExtendsDemo2 {
    public static void main(String[] args) {
        Zi z = new Zi();
        z.show();
    }
}
```

**2. 成员方法**

**方法的两个特性**：

- 重载（Overload）：同**一个类**中，方法名**相同**参数列表**不同**的方法使用叫**重载**
- 重写（Override）：在**子父类**中，出现成员方法**完全相同**的情况，会运行子类方法

**重写注意事项：**

- 子类方法重写父类方法时，子类权限必须**大于等于**父类权限
- 静态**只能**覆盖静态，或被静态覆盖
```
class Fu {
    void show() {
        System.out.println("fu show run");
    }
}
class Zi extends Fu {
    void show() { //重写父类方法
        System.out.println("zi show run");
        super.show();
    }
}
class ExtendsDemo3 {
    public static void main(String[] args) {
        Zi z = new Zi();
        z.show();
    }
}
```
**3. 构造方法**

- 子类构造对象时，访问子类**构造方法**时，父类**构造方法**也会运行。  
原因：在子类的构造方法中第一行有一个默认的隐式语句。**super()；** 

- 子类的实例化过程：子类中所有的构造方法**默认**都会访问父类中的空参数的构造方法  
原因：子类继承父类，获取了父类中内容，需要了解父类是如何对内容进行**初始化**的。

- 如果父类中没有定义空参数构造方法，子类的构造方法必须在**第一行**用**super**明确要调用父类中哪个构造方法。同时子类构方法数中如果使用**this**调用了本类构造方法时，super就没有了，因为super和this都**只能**定义在**第一行**。
```
class Fu {
    Fu() {
        System.out.println("A fu run");
    }
    Fu(int x) {
        System.out.println("B fu run");
    }
}
class Zi extends Fu {
    Zi() {
        //super();隐式语句，调用父类中空参数的构造方法
        System.out.println("C zi run");
    }
    Zi(int x) {
        //super();隐式语句，调用父类中空参数的构造方法
        System.out.println("D zi run");
    }
}
class ExtendsDemo4 {
    public static void main(String[] args) {
        new Zi(6);//输出结果A D
    }
}
```
### 对象实例化和初始化过程  

**一个对象实例化过程**
```
Person p = new Person();
```
1. JVM读取指定路径下的Person.class文件，并加载进内存，并会**先加载**Person的**父类**
2. 在**堆内存**中开辟空间，分配地址
3. 在对象空间中，对对象中的属性进行**默认初始化**
4. 调用对应的构造方法进行**初始化**
5. 在构造方法中第一行调用**父类**中的构造方法进行初始化
6. 父类初始化完毕后对子类的属性进行**显式初始化**
7. 进行子类构造方法的**特定初始化**
8. 初始化完毕后，将地址值复制给引用变量

**对象的初始化过程：**

1. 加载**子类构造方法**
2. super();加载**父类构造方法**
3. 父类构造方法调用被子类**重写**的方法
4. **显示初始化**
5. **构造代码块**初始化
6. 子类构造方法**具体初始化**
```
class Fu {
    Fu() {
        System.out,println("fu constructor run");
        show();
    }
    void show() {
        System.out.println("hehe");
    }
}
class Zi extends Fu {
    int num = 9; 
    { //第五步 构造代码快初始化
        System.out.println("constructor code..."+num);
    }
    Zi() { //第一步
        super; //第二步
        //第四步 显示初始化 
        System.out.println("zi constructor..."+ num); //第六步
    }
    void show() { //第三步
        System.out.println("show..."+num);
    }
}
```
### final关键字

- final是一个修饰符，可以修饰类，方法，变量
- final修饰的类**不可以**被**继承**
- final修饰的方法**不可以**被**重写**
- final修饰的变量是一个**常量**，只能被赋值一次
- 内部类**只能**访问被final修饰的局部变量

```
class Fu { //final修饰的类不可以被继承
    void method() { //final修饰的方法不可以被重写
        //调用底层系统资源
    }
}
class Zi extends Fu {
    void method() {
        public static final double MY_PI = 3.14; //final修饰的变量是一个常量，只能被赋值一次
        System.out.println(MY_PI);
    }
}
class FinalDemo {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

**常量命名规则**： 

全部**大写**，不同单词之间用 **_** 分隔。例：MY_PI  

**全局变量**：public static修饰的变量

```
public static int num = 9;
```

**全局常量**：public static final修饰的变量


```
public static final double MY_PI = 3.14;
```

### 抽象类  

当一个类描述一个事物时，**没有足够**的信息描述事物，就是抽象类

```
abstract class Pet { //含有抽象方法的类是抽象类
    abstract void voice();//抽象修饰的方法
}
class Dog extends Pet{
    void voice() {
        System.out.println("woof")
    }
}
class Cat extends Pet{
    void voice() {
        System.out.println("meow")
    }
}
class AbstractDemo {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```
**抽象类特点**：

1. 方法只有声明**没有方法体** **{   }** ，需要被abstract修饰，抽象方法**必须**定义在**抽象类**中
2. 抽象类**不能**被实例化
3. 抽象类中的抽象方法必须被子类**全部重写**后才可以被实例化，否则这个子类也是抽象类

**抽象类细节**：

1. 抽象类中**有构造方法**，因为需要给子类对象初始化
2. 抽象类中**可以不定义抽象方法**，但是很少见，目的是不让这个类创建对象
3. **abstract**关键字**不可以**和这些关键字共存
    - **private**：因为子类需要重写抽象父类，private无法访问
    - **static**：静态成员可以直接被类名调用
    - **final**：final类**无法被继承**而抽象类**必须被继承**，final方法**无法被重写**而抽象方法**必须被重写**
4. 抽象类和一般类的异同
    - **相同点**：抽象类和一般类都用来**描述事物**。
    - **不同点**：
        - 一般类有**足够**的信息描述事物  
            抽象类描述事物的信息有可能**不足**
        - 一般类中**不能**定义抽象方法  
            抽象类中**可以**定义抽象和非抽象方法
        - 一般类**可以**被实例化  
            抽象类**不可以**被实例化
5. 抽象类**一定是父类**，因为需要子类覆盖其方法后才可以对子类实例化。

示例：
```
/*
员工：
    属性：姓名，工号，薪水
    行为：工作。
程序员：
    属性：姓名，工号，薪水。
    行为：工作。
经理：
    属性：姓名，工号，薪水，奖金。
    行为：工作。
*/
abstract class Employee {
    private String name;
    private String id;
    private double pay;
    Employee(String name, String id, double pay) {
        this name = name;
        this id = id;
        this pay = pay;
    }
    public abstract void work(); //没有方法体的抽象方法
}
class Programmer extends Employee { //描述程序员
    Programmer(String name, String id, double pay) {
        super(name, id, pay);
    }
    public void work() { //加入方法体，重写父类方法
        System.out.println("programming");
    }
}
class Manager extends Employee { //描述经理
    Manager(String name, String id, double pay, int bonus) {
        super(name, id, pay);
        this.bonus = bonus;
    }
    public void work() { //加入方法体，重写父类方法
        System.out.println("managing");
    }
}
class AbstractTest {
    public static void main(String[] args) {
        System.out.println("Hello World");
        Programmer Kevin = new Programmer(Kevin, 1110009945, 7330);
    }
}
```
## 03-06 接口  
```
interface {}
```
抽象类中的方法**都是抽象**的抽象类就可以定义为接口

**接口中的成员都是公共权限：**

1. 全局常量：
```
public static final int NUM = 3;
```
2. 抽象方法：
```
public abstract void show(); //返回值类型void可以改变
```

- 类与类之间是**继承关系**
- 类与接口之间是**实现关系**
- 接口与接口之间是**继承关系**，而且接口之间可以多继承

接口不可以实例化

只能由实现了接口的子类重写了接口中所有的方法后，该子类才可以实例化，否则这个子类是一个**抽象类**
```
interface Demo {
    public static final int NUM = 3; //全局常量
    public abstract void show1(); //抽象方法
}
class DemoImp1 implements Demo {
    public static final int NUM = 3; 
    public abstract void show1(){}
}
class InterfaceDemo {
    public static void main(String[] args) {
        DemoImp1 d = new DemoImp1();
        System.out.println(d.NUM);
        System.out.println(DemoImp1.NUM);
        System.out.println(Demo.NUM);
}
```

**接口多实现**  

接口的方法前修饰符是固定的都是**public abstract 返回值类型**，因此只要两个接口中的方法名相同，多实现不会存在不确定性
```
interface A {
    public void show();
}
interface B {
    public void show();
}
class Test implements A, Z {
    public void show(){} //接口都是抽象方法，不存在不确定性，因此可以多实现
}
```
一个类实现另一个类的同时，还可以实现多个接口，避免了单继承的局限性

```
class Test2 extends Q implements A,Z {}
```

### 接口和抽象类的异同点

**相同点**：都是向上抽取而来  

**不同点**：  

与子类的关系：

- 抽象类需要被继承，而且只能多继承
- 接口需要被实现，而且可以多实现  

方法的定义：

- 抽象类中可以定义抽象与非抽象方法，子类继承后可以直接使用非抽象方法
- 接口中只能定义抽象方法，必须由子类去实现

性质

- 抽象类中的继承是is a关系，在定义该体系的基本共性内容
- 接口的实现是 like a 关系，在定义体系额外功能  

示例：  
```
//Dog Classification: GuideDog, DetectDog
abstract class Dog {
    abstract void bark();
}
interface Guide {
    abstract void guide();
}
class GuideDog extends Dog implement Guide{
    public void bark() {}
    public void guide() {}
}
```
**接口的应用**  

```
/*
Laptop Usage
为了扩展笔记本的功能，定义一个规则，以后不论什么设备只要符合这个规则就可以使用
*/
interface USB {
    public void open();
    public void close();
}
//一年后，出现了U盘和鼠标
//实现规则
class Udisk implement USB {
    public void open() {
        System.out.println("Udisk Open");
    }
    public void open() {
        System.out.println("Udisk Open");
    }
}
class UsbMouse implement USB {
    public void open() {
        System.out.println("UsbMouse Open");
    }
    public void open() {
        System.out.println("UsbMouse Open");
    }
}
class Laptop {
    public static void main(String[] args) {
        useUSB(new Udisk());
        useUSB(new UsbMouse());
    }
    //使用规则
    public static void useUSB(USB u) { //接口类型的引用，用于指向接口的子类对象
        u.open();
        u.close();
    }
}
```
## 03-07 多态  

**定义**：某一类事物的多种存在形态

**体现**：父类或者接口的引用指向其子类的对象

```
Fu z = new Zi();
```
**多态优缺点**

- 优点：提高了代码的扩展性，前期定义的代码可以使用后期的内容
- 缺点：父类引用不能调用子类的特有内容

**多态的前提**  

- 必须有关系，继承或者实现
- 必须要重写
```
/*
狗具备狗形态，也具备动物形态
猫具备猫形态，也具备动物形态
*/
abstract class Animal {
    abstract void eat();
}
class Dog extends Animal {
    void eat() {
        System.out.println("eat bone");
    }
    void housekeep() {
        System.out.println("house keeping");
    }
}
class Cat extends Animal {
    void eat() {
        System.out.println("eat fish");
    }
    void catchMouse() {
        System.out.println("catching mouse");
    }
}
class DuoTaiDemo {
    public static void main(String[] args) {
        Animal c = new Cat();//父类引用指向子类对象
        Animal d = new Dog();//父类引用指向子类对象
        method(c);
        method(d);
    public static void method(Animal a) {
        a.eat(); //Animal父类特有内容可以直接调用
        if(a instanceof Cat) { //判断对象是否为猫类，如果是
            Cat c = (Cat)a; //转换成猫类
            c.catchMouse(); //调用猫类特有方法
        } else if(a instanceof Dog) { //判断对象是否为狗类，如果是
            Dog d = (Dog)a; //转换成狗类
            d.housekeep(); //调用狗类特有方法
        }
    }
}
```
**转型**  

- 向上转型：限制对特有功能的访问
- 向下转型：可以使用特有功能

父类引用指向子类对象时，对象只能访问子父类共有内容。
```
Animal c = new Cat();//向上转型，猫对象提升到动物类型
c.eat();//只能访问共有功能，不能访问特有功能
Cat c = (Cat)a;//向下转型，猫对象降低到猫类
c.catchMouse//可以访问特有功能
```
**类型判断**  

instanceof：用于判断对象的具体类型。只能用于引用数据类型判断

```
public static void method(Animal a) {
    a.eat(); //Animal父类特有内容可以直接调用
    if(a instanceof Cat) { //判断对象是否为猫类，如果是
        Cat c = (Cat)a; //转换成猫类
        c.catchMouse(); //调用猫类特有方法
    } else if(a instanceof Dog) {
        Dog d = (Dog)a;
        d.housekeep();
    }
}
```

### 多态中的成员特点  

**成员变量**

- 编译时，参考引用型变量所属的类中是否有调用的成员变量。有，编译通过；没有，编译失败。
- 运行时，参考引用型变量所属的类中是否有调用的成员变量。并运行该所属类中的成员变量
- 总结：参考引用型变量所属的类中的成员变量

示例：

```
class Fu {
    int num = 3;//如果父类没有num，则编译失败
}
class Zi extends Fu {
    int num = 5;
}
class DuoTaiDemo {
    public static void main(String[] args) {
        Fu f = new Zi();
        System.out.println(f.num);// 输出3
    }
}
```

**成员方法**

- 编译时，参考引用型变量所属的类中是否有调用的方法。有，编译通过；没有，编译失败。
- 运行时，参考的是对象所属的类中是否有调用的方法。并运行该所属类中的成员变量
- 总结：编译看左边，运行看右边  

写程序时只能调用父类的方法，实际运行时调用的是子类重写父类后的方法。  
```
class Fu {
    void show() {
        System.put.println("fu show");
    }
}
class Zi extends Fu {
    void show() {
        System.put.println("zi show");
    }
}
class DuoTaiDemo {
    public static void main(String[] args) {
        Fu f = new Zi();
        f.show();//输出"zi show"
    }
}
```

**静态方法**

- 编译时，参考引用型变量所属的类中是否有调用的静态方法
- 运行时，参考引用型变量所属的类中是否有调用的静态方法
- 总结：编译运行都看左边

其实对于静态方法，是不需要对象的，可以直接被类名调用
```
class Fu {
    static void method() {
        System.put.println("fu static");
    }
}
class Zi extends Fu {
    static void method() {
        System.out.println("zi static");
    }
}
class DuoTaiDemo {
    public static void main(String[] args) {
        Fu f = new Zi();
        f.method();//输出"fu static"
    }
}
```

## 03-08 内部类

定义在一个类内部的类，又称为内置类，嵌套类

**内部类访问特点**：

- 内部类可以直接访问外部类中的成员
- 外部类需要建立内部类的对象才能访问内部类成员
```
class Outer {
    private int num = 3; //内部类可以直接访问私有内容
    static class Inner { //内部类
        void show() {
            System.out.println("show run.."+num);
        }
        //如果内部类中方法是静态的，则内部类也是静态的
        static void staticShow() { //静态直接调用，不需要对象
            System.out.println("staticShow run.."+num);
        }
    }
    //外部类需要创建内部类对象才能访问非静态内部类内容
    public void method() { 
        Inner in = new Inner();
        in.show();
    }
}
class InnerClassDemo {
    public static void main(String[] args) {
        //直接访问外部类的成员
        Outer out = new Outer();
        o.method;
        
        //直接访问外部类中的内部类中的成员
        Outer.Inner in = new Outer().new Inner();
        in.show();
        
        //如果内部类是静态的，相当于一个外部类
        Outer.Inner in = new Outer.Inner();
        in.show();
        
        //如果内部类是静态的，成员也是静态的，直接调用，不需要对象
        Outer.Inner.staticShow();
    }
}
```

内部类可以存放在局部位置上

内部类在局部位置上只能访问局部中被**final**修饰的变量

```
class Outer {
    int num = 3;
    void method() {
        final int x = 9; //内部类中访问的局部变量必须是final
        class Inner {
            void show() {
                System.out.println("show..."+x);
            }
        Inner in = new Inner();
        in.show();
        }
    }
}
```
### 匿名内部类

内部类的简写格式

```
new 父类or接口() {
    子类内容;
}
```
**前提**：内部类必须继承一个外部类，或者实现一个接口 

匿名内部类其实就是一个子类对象
```
abstract class Demo {
    abstract void show();
}
class Outer {
    int num = 4;
    
    //匿名内部类不能有名字，所以不能这样定义
    //class Inner extends Demo {
    //    void show() {
    //        System.out.println("show..."+num);
    //    }
    //}
    
    public void method() { 
        //相当于 new Inner().show();
        new Demo() { //创建匿名内部类
            void show() { //重写Demo抽象方法
                System.out.println("show..."+num);
            }
        }.show();
    }
}
class InnerClassDemo {
    public static void main(String[] args) {
        new Outer().method();
    }
}
```

**匿名内部类应用**  

当方法参数是接口类型时，而且接口中的方法**不超过三个**，可以用匿名内部类作为实际参数进行传递
```
interface Inter {
    void show1();
    void show2();
}
class Outer {
    //class Inner implements Inter {
    //    public void show1() {}
    //    public void show2() {}
    //}
    public void method() {
    //    Inner in = new Inner();
    //    in.show1();
    //    in.show2();
        Inter in = new Inter() { //重写接口方法，创建匿名内部类对象
            public void show1() {}
            public void show2() {}
        }
        in.show1;
        in.show2;
    }
}
```

## 03-09 异常

**异常**：运行时发生的不正常情况，根据面向对象的思想被java封装成了对象  

**异常类**：在java中用类的形式对不正常的情况进行了描述和封装对象，描述不正常的情况的类，就称为异常类。

```
class ExceptionDemo {
    public static void main(Stirng[] args) {
        int[] arr = new int[3];
        arr = null;
        System.out.println(arr[3]);
    }
    public static void sleep(int time) {
        if(time < 0) {
            //抛出一个对象
            new FuTime();//新建一个负time对象，这个对象中包含问题的名称，信息，位置等信息
        }
        if (time > 100000) {
            //抛出一个对象
            new BigTime();
        }
    }
}
```
### 异常体系  

不正常的情况分成两类

Throwable（可抛出）：可以被**throws**和**throw**两个关键字操作的类和对象都具备可抛性

- **Error**：不可处理的问题  
    特点：由JVM抛出的严重性的问题，这种问题一般不针对处理，直接修改代码
- **Exception**：可处理的问题

**该体系的特点**：子类的后缀名都是用其父类名作为后缀
```
ArrayIndexOutOfBoundsException
```
### 异常处理方式

**自动抛出异常**
```
//自动抛出异常：
class Demo {
    public void method(int[] arr, int index) {  
        //JVM在这里封装了一个对象然后丢出：throw new ArrayIndexOutOfBoundsException(index)
        System.out.println(arr[index]);
    }
}
class ExceptionDemo {
    public static void main(Stirng[] args) {
        int[] arr = new int[3];
        Demo d = new Demo();
        d.method(arr,3);
    }
}
```

**手动抛出异常：**   

**自定义异常**：java中没有定义过的异常，按照java异常的创建思想和面向对象的思想，对异常进行自定义描述，并封装成对象。  

**自定义异常类**：自定义异常类必须继承异常体系，因为只有称为异常体系的子类才具有可抛性，才可以被throw，throws操作。要么继承Exception，要么继承RuntimeException

- 继承**Exception**或者其子类（编译时异常）：
    - **声明**：只声明不捕捉，无法通过编译，可以自定义报错的信息
        - 自定义异常类，继承Exception或者其子类
        - 通过**throws 类名** 在方法名后声明自定义异常类
        - 通过**throw new 类名();** 创建对象
        - 如果需要程序通过编译正常运行，需要用**Try-Catch**对抛出的异常进行处理
    - **捕捉**：try-catch捕捉处理异常，处理完输出提示信息并且程序继续运行
- 继承**RuntimeException**（运行时异常）：继承了RuntimeException的子类可以不用**Try-Catch**或者**throws**就可以通过编译。

**throw**：异常抛出的关键字  
**throws**：声明自定义异常类的关键字

**throws和throw的区别**

- throws使用在方法上  
    throw使用在方法内
- throws抛出的是异常类，可以抛出多个，用逗号隔开  
    throw抛出的是对象

**Exception**类的所有子类中分为**两种**

- 编译时异常：其他子类
- 运行时异常：**RuntimeException**和其子类



**异常声明**

只声明，不处理的异常，无法通过编译，可以自定义报错信息
```
//手动抛出异常
/*
角标为负的异常在java中没有定义过，需要自定义
*/
class FuShuIndexException extends Exception {
    FuShuIndexException() {}//空参数构造方法
    FuShuIndexException(String msg) {
        super(msg);//直接调用父类构造方法
    }
}
class Demooo {
    //创建自定义异常类对象的方法需要用throws声明自定义异常
    public int method(int[] arr, int index) throws FuShuIndexException {
        if(index>=arr.length) {
            //手动抛出异常
            throw new ArrayIndexOutOfBoundsException("数组角标越界"+index);
        } else if(index<0) {
            throw new FuShuIndexException("数组角标不能是负数"+index);
        }
        return arr[index];
    }
}
class ExceptionDemo {
    //有自定义异常的主方法需要用throws声明自定义异常
    public static void main(String[] args) throws FuShuIndexException {
        int[] arr = new int[3];
        Demooo d = new Demooo();
        d.method(arr,3);
    }
}
```
**异常捕捉**  

try-catch处理完程序可以继续运行
```
try {
    需要被检测异常的代码
}
catch(FuShuIndexException e) {
    处理异常的代码
}
catch(Exception e) { //多个catch，父类catch一定要放在后面
    处理异常的代码
}
finally {
    一定会被执行的代码
}
```
**try-catch-finally代码块特点**：

- try catch finally
- try catch：当没有资源需要释放时，可以不用finally
- try finally：异常无法直接catch处理，但是资源需要关闭
```
class FuShuIndexException extends Exception {
    FuShuIndexException() {}//空参数构造方法
    FuShuIndexException(String msg) {
        super(msg);//直接调用父类构造方法
    }
}
class Demoo {
    public int method(int[] arr, int index) throws FuShuIndexException {
            if(index<0) {
               throw new FuShuIndexException("Index must be positive");
            }
        return arr[index];
    }
}
class ExceptionDemo {
    public static void main(String[] args) {
        int[] arr = new int[3];
        Demoo d = new Demoo();
        try {
            int num = d.method(arr, -3);
            System.out.println("num=" + num);
        } catch (FuShuIndexException e) { 
            //FuShuIndexException e = new FuShuIndexException("Index must be positive")
            //获得自定义的异常提示信息
            System.out.println("Message:"+e.getMessage());
            //获得字符串形式的自定义异常类信息
            System.out.println("String:"+e.toString());
            //获得出现异常的代码位置
            e.printStackTrace();
            System.out.println("负数角标异常");
        }
        System.out.println("over");
    }
}
/*
输出：
Message:Index must be positive
FuShuIndexException: Index must be positive
String:FuShuIndexException: Index must be positive
	at Demoo.method(ExceptionDemo.java:10)
负数角标异常
	at ExceptionDemo.main(ExceptionDemo.java:20)
over
*/
```
**异常处理的原则**：

- 方法内如果抛出（**throw**）需要检测的异常，那么方法名后面必须要声明（**throws**），否则必须在方法内部用**try-catch**捕捉，否则编译失败。
- 如果调用到了声明异常的方法，要么**try-catch**，要么**throws**，否则编译失败
- 功能内容可以解决，就用**try-catch**。解决不了，用**throws**让调用者解决。
- 一个方法如果抛出多个异常，那么调用时，必须有对应多个catch进行针对性处理。

**finally**代码块  

通常用于关闭（释放）资源，比如关闭数据库连接
```
class Demo {
    public void show(int index) throws ArrayIndexOutOfBoundsException :
        if(index < 0)
            throw new ArrayIndexOutOfBoundsException("越界");
        int[] arr = new int[3];
        return arr[index];
    }
}
class ExceptionDemo {
    public static void main(String[] args) {
        Demo d = new Demo();
        try {
            int num = d.show(-3);
            System.out.println("num"+num);
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println(e.toString());
            //return; 如果加了return;则不会运行over
            //System.exit(o);如果加了这句，则不会运行finally代码块，直接退出JVM
        } finally { //一定会被执行，除非System.exit(0);退出JVM
            System.out.println("finally");
        }
        System.out.println("over");
    }
}
```

### 异常应用

```
//自定义蓝屏异常类
class BlueScreenException extends Exception {
    BlueScreenException(String msg) {
        Super(msg);
    }
}
//自定义冒烟异常类
class MaoYanException extends Exception {
    MaoYanException(String msg) {
        Super(msg);
    }
}
//自定义无法处理异常类
class NoPlanException extends Exception {
    NoPlanException(String msg) {
        Super(msg);
    }
}
class Computer {
    private int state = 0;
    //定义电脑运行功能
    public void run() throws BlueScreenException, MaoYanException { 
        if(state == 1) { //状态值为1时电脑蓝屏
            throw new BlueScreenException("蓝屏");
        } else if(state == 2)
            throw new MaoYanException("冒烟");
        System.out.println("电脑运行");
    }
    //定义电脑重启功能
    public void reboot() {
        state = 0; //重置电脑到正常状态
        System.out.println("重启");
    }
}
class Teacher {
    private String name;
    private Computer comp;
    Teacher(String name) {
        this.name = name;
    }
    public void teach() throws NoPlanException { 
        try {
            comp.run(); //电脑运行
            System.out.println("讲课"); //正常讲课
        } catch (BlueScreenException e) {
            System.out.println(e.toString());
            comp.reset();
            teach();
        } catch (MaoYanException e) {
            System.out.println(e.toString());
            test();
            //异常转换：收到冒烟异常，转换成NoPlan异常对外进行告知
            throw new NoPlanException("课时进度无法完成");
        }
    }
    public void test() {
        System.out.println("大家练习");
    }
}
class ExceptionTest {
    public static void main(String[] args) {
        Teacher t = new Teacher("Kevin");
        try (
            t.teach();
        ) catch(NoPlanException e) {
            System.out.println(e.toString()+"...");
            System.out.println("换老师");
        }
    }
}
```
异常的注意事项：

- 子类在重写父类方法时，父类的方法如果跑出了异常，那么子类的方法只能抛出父类的异常或者该异常的子类
- 如果父类抛出多个异常，那么子类只能抛出父类异常的子集


## 03-10 Object类

Object类是所有类的根类，是不断抽取而来，具备所有对象都具备的共性内容

### Object类常用方法

**equals方法**  

当两个引用值指向同一个对象时才返回true
```
class Person extends Object {
    private int age;
    Person(int age) {
        this.age = age;
    }
}
Class EqualsDemo {
    public static void main(String[] args) {
        Person p1 = new Person();
        Person p2 = new Person();
        Person p3 = p1;
        
        System.out.println(p1 == p2);//false
        System.out.println(p1.equals(p2));//false
        System.out.println(p1.equals(p3));//true
    }
}
```

**equals方法重写**  

equals方法一般都会被重写，根据对象的特有内容，建立判断对象是否相同的依据
```
class Person extends Object {
    private int age;
    Person(int age) {
        this.age = age;
    }
    public boolean equals(Object obj) {//重写Object类中的equals方法，进行对象年龄比较
        if(!(obj instanceof Person)) {
            return false;
            throw new ClassCastException("类型错误");
        }
        Person p = (Person)obj;
        return this.age == p.age;
    }
}
Class EqualsDemo {
    public static void main(String[] args) {
        Person p1 = new Person(20);
        Person p2 = new Person(20);
        
        System.out.println(p1 == p2);//false
        System.out.println(p1.equals(p2));//true
        System.out.println(p1.equals(new Demo()));//报错，类型错误
    }
}
```
**hashCode方法**  

判断两个对象是否完全相同
```
class Person extends Object {
    private int age;
    Person(int age) {
        this.age = age;
    }
    public int hashCode() { //重写object类中的hashCode方法，输出年龄
        return age;
    }
}
Class EqualsDemo {
    public static void main(String[] args) {
        Person p1 = new Person(20);
        Person p2 = new Person(20);
        
        System.out.println(p1);//输出p1的哈希值
        System.out.println(p1.hashCode());//输出p1的哈希值
        System.out.println(Integer.toHexString(p1.hashCode()));//输出p1的十六进制哈希值
        
    }
}
```

**getClass方法**  

获取当前对象所属字节码**对象**
```
Class clazz1 = p1.getClass();
Class clazz1 = p2.getClass();
System.out.println(clazz1 == clazz2);//true
System.out.println(clazz1.getNma());//Person
```
**toString方法**  

返回对象的字符串表示形式，它的值等于：

```
getClass().getNmae() + '@' + Integer.toHexString(hashCode())
```

建议重写该方法

```
public String toString() {
    return "Person: " + age;
}

System.out.println(p1);//Person: 20
System.out.println(p1.getClass().getNmae() + '@' + Integer.toHexString(hashCode()));////Person@61de33
```
## 03-11 包

对类文件进行分类管理

```
package allpack.boypack.mypack;

class PackageDemo {
    public static void main(String[] args) {
        System.out.println("Hello Package!");
    }
    
}
//javac -d . PackageDemo.java
//java mypack.PackageDemo
```
### 包与包之间的访问

包与包之间的类进行访问，被访问的包中的类必须是public的，被访问的包中的类的方法也必须是public

```
package packa;

public class DemoA { //包与包之间访问必须是public
    public void show() //包与包之间访问必须是public{
        System.out.println("demoa show run");
    }
}
```
```
package packb;

public class DemoA { //包与包之间访问必须是public
    protected void method() { //protected只能被继承了父类的访问
        System.out.println("demoa show run");
    }
}
```
```
package mypack;

class PackageDemo {
    public static void main(String[] args) {
        packa.DemoA d = new packa DemoA();
        d.show()；
        System.out.println("Hello Package!");
    }
}
```

位置| public | protected | default | private |
---|---|---|---|---
同一类中| ok | ok | ok | ok
同一包中|ok|ok|ok|
子类中|ok|ok||
不同包中|ok|||

**导入import**  

```
package packa;

public class DemoA { //包与包之间访问必须是public
    public void show() //包与包之间访问必须是public{
        System.out.println("demoa show run");
    }
}
```
```
package packb;

public class DemoA { //包与包之间访问必须是public
    protected void method() {
        System.out.println("demoa show run");
    }
}
```
```
package mypack;
import packa.*//导入了packa包中所有的类
class PackageDemo {
    public static void main(String[] args) {
        packa.DemoA d = new packa DemoA();
        d.show()；
        System.out.println("Hello Package!");
    }
}
```
**Jar包**  
Java的压缩包
# 04 Java SE 多线程

## 04-01 多线程概述

**进程**：正在进行中的程序  

**线程**：进程中的一个负责程序执行的控制单元（执行路径）  

- 一个进程中可以有**多个**线程
- 一个进程中至少有**一个**线程

**多线程作用**：开启多个线程是为了同时运行多部分代码

**多线程的优缺点**：

- 优点：可以同时运行多个程序
- 缺点：内存处理到程序频率变低，运行速度变慢

## 04-02 JVM中的多线程
 
JVM启动时就启动了多个线程，至少有两个线程

- 执行主方法的线程：该线程的任务代码都定义在主方法中
- 负责垃圾回收的线程

**Object 类中的 finalize() 方法**：

当垃圾回收器确定不存在该对象的更多引用时，由对象的垃圾回收器调用此方法  

**System类中的 System.gc() 方法**：运行垃圾回收器，垃圾回收器运行时间随机
```
class Demo extends Object {
    public void finalize() {
        System.out.println("Recycle Complete");
    }
}
class ThreadDemo {
    public static void main(String[] args) {
        new Demo();
        new Demo();
        System.gc(); //
        new Demo();
        System.out.println("Hello World!");
    }
}
/*
输出
Hello World!
Recycle Complete
Recycle Complete
因为是两个线程，先运行主线程，JVM关闭前运行垃圾回收线程
*/
```

## 04-03 多线程创建

**主方法单线程运行**  

不创建多线程
```
class Demo {
    private String name;
    Demo (Srting name) {
        this.name = name;
    }
    public void show() {
        for(int x = 0; x < 10; x++) {
            //y的for循环让每次输出都有一定的延迟，但是必须d1都输出完才输出d2，这时就需要多线程来让他们同时输出
           for(int y =-9999999; y < 999999999; y++) {}
           System.out.println(name+"...x="+x);
        }
    }
}
class ThreadDemo {
    public static void main(String[] args) {
        Demo d1 = new Demo("Sequence Initializing");
        Demo d2 = new Demo("序列初始化中");
        d1.show();
        d2.show();
    }
}
```
### 创建多线程

**目的**：开启一条执行路径，使得指定的代码和其他代码实现**同时运行**，而此执行路径运行的指定代码就是这个执行路径的**任务**

**任务存放位置**：
- JVM创建的**主线程的任务**都定义在了**主方法**中
- **自定义线程的任务**定义在Thread类的**run方法**中

创建多线程有**两种方法**

- 继承**Thread**类
- 实现**Runnable**接口

#### 创建线程方式一

继承**Thread**类  

步骤：

1. 定义一个类，继承**Thread**类
2. 重写Thread类中的 **run();** 方法
3. 直接创建Thread类的子类对象（创建线程）
4. 调用 **start();** 方法开启线程，并调用线程的任务**run();** 方法
```
class Demo extends Thread{
    private String name;
    Demo (Srting name) {
        this.name = name;
    }
    public void run() {
        for(int x = 0; x < 10; x++) {
           //currentThread()获取当前运行中线程的引用
           System.out.println(name+"...x="+x+"...Thread Name="+Thread.currentThread().getname());
        }
    }
}
class ThreadDemo {
    public static void main(String[] args) {
        Demo d1 = new Demo("Sequence Initializing");
        Demo d2 = new Demo("序列初始化中");
        d1.start();//开启线程，调用run方法
        d2.start();//开启线程，调用run方法
        //CPU在主线程，d1，d2之间随机高速切换
    }
}
```
**Thread类中的方法&线程名称**  

**getName()方法**  

获取线程的名称Thread-编号（从0开始）  
主线程的名字main

**currentThread()方法**  

获取当前运行中线程的引用，该方法为静态，可以直接被类名调用

**多线程异常问题**  

有异常的线程结束运行，**run()** 方法出栈，线程之间互不影响。

**线程的状态** 

- **new**被创建
    -  **start()** 运行（具备执行资格，具备执行权）
        - 冻结（释放执行权，释放执行资格）
            - **sleep(time)** 冻结 时间到自动唤醒
            -  **wait()** 冻结 **notify** 唤醒
        - 阻塞（具备执行资格，不具备执行权，正在等待执行权）
        - 消亡
            - **run()** 方法结束
            - **stop()** 停止线程

CPU的执行资格：可以被CPU处理，在处理队列中排队  
CPU的执行权：正在被CPU处理


#### 创建线程方式二

实现**Runnable**接口  

步骤：

1. 定义一个类，实现**Runnable**接口
2. 重写接口中的run方法，将线程的任务代码封装到run方法中
3. 通过Thread类创建线程对象，将Runnable接口的子类对象作为构造方法的参数进行传递
4. 调用线程对象的**start();** 方法开启线程

```
class Demo extends Fu implements Runable{ //无法继承Thread但是需要多线程，通过接口形式完成
    public void run() {
        show();
    }
    public void show() {
        for(int x = 0; x < 20; x++) {
            System.out.println(Thread.currentThread().getName()+"..."+x);
        }
    }
}
class ThreadDemo {
    public static void main(String[] args) {
        Demo d = new Demo();
        Thread t1 = new Thread(d);
        Thread t2 = new Thread(d);
        t1.start;
        t2.start;
    }
}
```
**第二种方法的好处**：

- 将线程的任务从线程的子类中分离出来，进行了单独的封装，按照面向对象的思想将任务封装成对象
- 避免了java单继承的局限性

## 04-04 多线程同步

**卖票示例**

四个线程，每个线程都卖100张票
```
class Ticket extends Thread{
    private int num = 100;
    public void run() {
        sale();
    }
    public void sale() {
        while(true) {
            if(num > 0) {
                System.out.println(Thread.currentThread().getName()+“...sale...”num--);
            }
        }
    }
}
class TicketDemo {
    public static void main(String[] args) {
        //四个对象，每个对象都有100张票
        Ticket t1 = new Ticket();
        Ticket t2 = new Ticket();
        Ticket t3 = new Ticket();
        Ticket t4 = new Ticket();
        
        t1.start();
        t2.start();
        t3.start();
        t4.start();
    }
}
```
四个线程一起卖100张票
```
class Ticket implements Runnable {
    private int num = 100;
    public void run() {
        sale();
    }
    public void sale() {
        while(true) {
            if(num > 0) {
                System.out.println(Thread.currentThread().getName()+“...sale...”num--);
            }
        }
    }
}
class TicketDemo {
    public static void main(String[] args) {
        Ticket t = new Ticket(); //一个对象，所有一共只有100张票
        Thread t1 = new Thread(t);
        Thread t2 = new Thread(t);
        Thread t3 = new Thread(t);
        Thread t4 = new Thread(t);
        
        t1.start();
        t2.start();
        t3.start();
        t4.start();
        
    }
}
```
**线程安全问题的现象**  

会出现0，-1，-2张票的情况，因为线程1还没运行到num--的时候，线程2，线程3有可能就已经加载进来，当num--运行完之后，线程还会继续运行，这就导致0，-1，-2的出现。

**安全问题产生的原因**  

- 多个线程在操作共享的数据
- 操作共享数据的线程代码有多条

当一个线程在执行操作共享数据的多条代码过程中，其他线程参与了运算

### 多线程同步

将多条操作共享的数据的线程代码封装起来，当有线程在执行这些代码的时候，其他线程不可以参与运算。

**同步代码块**  

格式
```
synchronized(对象) {
    需要被同步的代码;
}
```

```
class Ticket implements Runnable {
    private int num = 100;
    Object obj = new Object; //此对象为了传给synchronized作为锁
    public void run() {
        sale();
    }
    public void sale() {
        while(true) {
            synchronized(obj) { //synchronized修饰的代码块只能同一时间被一个线程调用
                if(num > 0) {
                    try {
                        Thread.sleep(10);
                    } catch (InterruptedException e) {}
                    System.out.println(Thread.currentThread().getName()+“...sale...”num--);
                }
            }
        }
    }
}
class TicketDemo {
    public static void main(String[] args) {
        Ticket t = new Ticket(); //一个对象，所有一共只有100张票
        Ticket t1 = new Ticket();
        Ticket t2 = new Ticket();
        Ticket t3 = new Ticket();
        Ticket t4 = new Ticket();
        
        t1.start();
        t2.start();
        t3.start();
        t4.start();
        
    }
}
```

**同步的前提**：

- 同步中必须有**多个**线程并使用**同一个锁**
- 当作锁的对象必须在 **run()** 方法外创建

**同步的优缺点**：

- 优点：解决了线程的安全问题
- 缺点：相对降低了效率，因为同步外的线程都会判断同步锁

**同步方法**
```
/*
两个客户每次去银行存100，存三次
*/
class Bank {
    private int sum;
    private Object obj = new Object();
    public synchronized void add(int num) {//同步方法
//        synchronized(obj) {
            sum = sum + num;
            System.out.println("sum="+sum);
//        }
    }
}
class Cus implements Runnable {
    private Bank b = new Bank();
    public void run() {
        for(int x = 0; x < 3; x++) {
            b.add(100);
        }
    }
}
class BankDemo {
    public static void main(String[] args) {
        Cus c = new Cus;
        Thread t1 = new Thread(c);
        Thread t2 = new Thread(c);
        t1.start();
        t2.start();
    }
}
/*
输出：
sum=100
sum=200
sum=300
sum=400
sum=500
sum=600
*/
```
**同步代码块和同步方法同时使用**
```
class Ticket implements Runnable {
    private int num = 100;
    Object obj = new Object; //此对象为了传给synchronized
    boolean flag = true;
    public void run() {
        if(flag)//flag为true则运行同步代码快
            while(true) {
                synchronized(this) {
                    if(num>0) {
                        try {
                            Thread.sleep(10);
                        } catch(InterruptedException e) {}
                        System.out.println(Thread.currentThread().getName()+"...obj..."+num--);
                    }
                }
            }
        else //flag为false则运行同步方法
            while(true)
                this.show();
    }
    public synchronized void show() {
        if(num > 0) {
            try {
                Thread.sleep(10);
            } catch ()
            System.out.println(Thread.currentThread().getName()+“...syn...”num--);
        }
    }
}
class TicketDemo {
    public static void main(String[] args) {
        Ticket t = new Ticket(); //一个对象，所有一共只有100张票
        Ticket t1 = new Ticket();
        Ticket t2 = new Ticket();

        t1.start();
        
        try {
            Thread.sleep(10);
        } catch(InterruptedException e) {}
        
        t.flag = false;
        t2.start();
    }
}
```
同步方法和同步代码快的**区别**：

- 同步方法的锁是**固定**的**this**（当前对象）
- 同步代码块的锁是**任意**的对象

**静态同步方法**使用的锁：
该方法所属字节码文件对象，可以用如下方式获取

- **this.getClass()** 仅限非静态方法中使用
- **Ticket.class**

## 04-05 多线程中的单例模式

使用同步虽然可以避免安全问题，但是会导致程序运行效率变低，因为每个线程都需要判断是否可以拿锁
```
//饿汉式（单例设计模式）
class Single {
    private static final Single s = new Single();
    private Single() {}
    public static Single getInstance() {
        return s;
    }
}
//懒汉式（延迟加载单例设计模式）
class Single {
    private static Single s = null;
    private Single() {}
    public static Single getInstance() {
        if(s == null) {//解决效率问题：多加一句判断，后续线程不会判断是否可以拿锁
            //不用this.getClass()是因为getClass()是非静态方法
            synchronized(Single.class) {//解决安全问题
                if(s == null)
                    s = new Single();
            }
        }
        return s;
    }
}
class SingleDemo {
    public static void main(String[] args) {
        System.out.println();
    }
}
```
## 04-06 多线程死锁

同步代码块嵌套
```
class Test implements Runnable{
    private boolean flag;
    Test(boolean flag) {
        this.flag = flag;
    }
    public void run() {
        if(flag) {
            synchronized(MyLock.locka) {
                System.out.println("if...locka...");
                synchronized(MyLock.lockb) {
                    System.out.println("if...lockb...");
                }
            }
        } else {
            synchronized(MyLock.lockb) {
                System.out.println("if...lockb...");
                synchronized (MyLock.locka) {
                    System.out.println("if...locka...");
                }
            }
        }
    }
}
class MyLock {
    public static final Object locka = new Object();
    public static final Object lockb = new Object();
}
class DeadLockTest {
    public static void main(String[] args) {
        Test a = new Test(true);
        Test b = new Test(false);
        
        Thread t1 = new Thread(a);
        Thread t2 = new Thread(b);
        
        t1.start;
        t2.start;
    }
}
```

## 04-07 多线程通信

**定义**：多个线程在处理同一资源，任务却不同  

### 等待唤醒机制

**涉及的方法**：

- **wait();** 让线程处于**冻结状态**，释放执行权和执行资格，存储到线程池中
- **notify();** 唤醒线程池中**一个**线程
- **notifyAll();** 唤醒线程池中**所有**线程，防止多生产多消费的死锁问题

这些方法都必须定义在同步中，因为这些方法都是用于线程状态的方法，必须要明确到底操作的是哪个锁上的线程。

等待唤醒机制中的方法（**wait(); notify(); notifyAll();**）定义在Object类中，因为这些方法是监视器的方法，监视器其实就是锁
```
//资源
class Resource {
    private String name;
    private String sex;
    privateboolean flag = false; //用来判断是否可以输入输出
    public synchronized void set(String name) {
        if(flag) //如果flag为false，则不wait
            try {
                this.wait();
            } catch (InterruptException e) {}
        this.name = name;
        this.sex = sex;
        flag = true;
        this.notify();
    }
    public synchronized void out() {
        if(!flag)
            try {
                this.wait();
            } catch (InterruptException e) {}
        System.out.println(name+"..."+sex);
        flag = false;
        notify();
    }
}
//输入
class Input implements Runnable {
    Resource r;
    Input(Resource r) {
        this.r = r;
    }
    public void run() {
        int x = 0;
        while(true) {
            if(x == 0) { //控制两种数据输入
                r.set("Kevin","Male")
            } else {
                r.set("Lily","Female");
            }
            x = (x+1)%2;
        }
    }
}
//输出
class Output implements Runnable {
    Resource r;
    Output(Resource r) {
        this.r = r;
    }
    public void run() {
        while(true) { 
            r.out();
            }
        }
    }
}
class ResourceDemo {
    public static void mian(String[] args) {
        //创建资源
        Resource r = new Resource();
        //创建任务
        Input in  = new Input(r);
        Output out = new Output(r);
        //创建线程
        Thread t1 = new Thread(in);
        Thread t2 = new Thread(out);
        //开启线程
        t1.start();
        t2.start();
    }
}
```

**多生产者多消费者问题**  

多生产多消费与单生产单消费的区别

flag判断语句区别

- if只判断标记一次，会导致不该运行的线程开始运行，出现数据错误
- while可以循环判断标记，解决了线程获取执行权后，是否要运行的问题

唤醒语句区别

- notify()只能唤醒一个线程，如果唤醒了本方，没有意义，并且会导致死锁，所有线程都进线程池
- notifyAll()解决了，本方线程一定会唤醒对方线程
```
//定义资源
class Resource {
    private String name;//资源名称
    private int count = 1;//计数器
    private boolean flag = false;
    public synchronized void set(String name) {
        while(flag)//flag为false时不wait，直接运行下面内容。
            try {
                this.wait();//当flag为true时进入wait状态
            } catch (InterruptException e) {}
        this.name = name + count;
        count++;
        System.out.println(Thread.currentThread().getName()+"...生产者..."+this.name);
        flag = true; //flag改成true
        notify(); //随机唤醒一个线程，如果是多生产多消费者则用notifyAll();
    }
    public synchronized void out() {
        while(!flag)
            try {
                this.wait();
            } catch (InterruptException e) {}
        System.out.println(Thread.currentThread().getName()+"...消费者..."+this.name);
        flag = false;
        notify();//随机唤醒一个线程，如果是多生产多消费者则用notifyAll();
    }
}
class Producer implements Runnable {
    private Resource r;
    Producer(Resource r) {
        this.r = r;
    }
    public void run() {
        while(true) {
            r.set("烤鸭");
        }
    }
}
class Producer implements Runnable {
    private Resource r;
    Producer(Resource r) {
        this.r = r;
    }
    public void run() {
        while(true) {
            r.out();
        }
    }
}
class ProducerConsumerDemo {
    public static void main(String[] args) {
        Resource r = new Resource();
        Producer pro = new Producer(r);
        Consumer con = new Consumer(r);
        
        Thread t0 = new Thread(pro);
        Thread t1 = new Thread(con);
        t0.start();
        t1.start();
    }
}
```
### JDK1.5新特性

**Lock**  
Lock接口：代替了同步代码快或者同步方法，将同步的隐式锁操作变成显式锁操作，更为灵活，可以一个锁上加多组监视器。

- **lock();** 获取锁
- **unlock();** 释放锁，通常需要定义在**finally**代码块中
```
Lock lock = new ReentrantLock();
public void run() {
    lock.lock();
    try {
        code;
    } finally {
        lock.unlock();
    }
}
```

**Condition**  

Condition接口：代替了**Object**中的**wait notify notifyAll**方法。这些监视器被封装，变成Condition监视器对象，可以任意锁进行组合

- **await()**; 功能同wait()
- **signal()**; 同notify()
- **signalAll()**; 同notifyAll()
  
**1.5版本的多生产者多消费者代码**
```
//定义资源
class Resource {
    private String name;//资源名称
    private int count = 1;//计数器
    private boolean flag = false;
    //创建一个锁对象
    Lock lock = new ReentrantLock();
    
    //通过已有的锁获取该锁上的监视器对象
    //Condition con = lock.newCondition();
    
    Condition Producer_con = lock.newCondition();
    Condition Consumer_con = lock.newCondition();
    
    public void set(String name) {
        lock.lock();
        try {
            while(flag)//flag为false时不wait，直接运行下面内容。
                try {
                    Producer_con.await();//当flag为true时进入wait状态
                } catch (InterruptException e) {}
            this.name = name + count;
            count++;
            System.out.println(Thread.currentThread().getName()+"...生产者..."+this.name);
            flag = true; //flag改成true
            //notifyAll();
            //con.signalAll();
            consumer_con.signal();
        } finally {
            lock.unlock();
        }
    }
    public synchronized void out() {
        lock.lock();
        try {
            while(!flag)
                try {
                    consumer_con.await();
                } catch (InterruptException e) {}
            System.out.println(Thread.currentThread().getName()+"...消费者..."+this.name);
            flag = false;
            //notifyAll();
            //con.signalAll();
            //Producer_Con.signal();
        } finally {
            lock.unlock();
        }
    }
}
class Producer implements Runnable {
    private Resource r;
    Producer(Resource r) {
        this.r = r;
    }
    public void run() {
        while(true) {
            r.set("烤鸭");
        }
    }
}
class Consumer implements Runnable {
    private Resource r;
    Producer(Resource r) {
        this.r = r;
    }
    public void run() {
        while(true) {
            r.out();
        }
    }
}
class ProducerConsumerDemo {
    public static void main(String[] args) {
        Resource r = new Resource();
        Producer pro = new Producer(r);
        Consumer con = new Consumer(r);
        
        Thread t0 = new Thread(pro);
        Thread t1 = new Thread(con);
        t0.start();
        t1.start();
    }
}
```

**wait和sleep区别**

- 时间指定不同
    - **wait**可以指定时间也可以不指定
    - **sleep****必须**指定时间
- 在同步中时，对CPU的**执行权**和**锁**的处理不同
    - **wait**：释放执行权，释放锁
    - **sleep**：释放执行权，不释放锁

## 04-08 多线程停止

### 停止线程

- stop方法，已经过时
- 定义标记，使run方法结束

**定义标记**  

定义一个标记flag，当flag为true时线程可以运行，当flag为负时线程停止运行。  

局限性：当有**wait()** 的时候会导致线程无法继续判断flag而进程冻结
```
class StopThread implements Runnable {
    boolean flag = true; //定义flag标记
    public void run() {
        while(flag) { //flag标记为true时运行run方法
            System.out.println(Thread.currentThread().getName()+"...");
        }
    }
    public void setFlag() { //定义设置flag为false的方法
        flag = false;
    }
}
class StopThreadDemo {
    public static void main(String[] args) {
        StopThread st = new StopThread();
        
        Thread t1 = new Thread(st);
        Thread t2 = new Thread(st);
        
        t1.start();
        t2.start();
        
        int num = 1;
        for(;;) {
            if(++num==50) {
                st.setFlag();
                break;
            }
            System.out.println("main..."+num);
        }
        System.out.println("over");
    }
}
```
**interrupt()方法**  

**Interrput()** 方法可以把线程从冻结状态强制恢复到运行状态中来
```
class StopThread implements Runnable {
    boolean flag = true; //定义flag标记
    public synchronized void run() {
        while(flag) { //flag标记为true时运行run方法
            try {
                wait();
            } catch (InterruptedException e) {
                System.out.println(Thread.currentThread().getNmae()+"..."+e);
                flag = false;
            }
            System.out.println(Thread.currentThread().getName()+"...");
        }
    }
    public void setFlag() { //定义设置flag为false的方法
        flag = false;
    }
}
class StopThreadDemo {
    public static void main(String[] args) {
        StopThread st = new StopThread();
        
        Thread t1 = new Thread(st);
        Thread t2 = new Thread(st);
        
        t1.start();
        t2.start();
        
        int num = 1;
        for(;;) {
            if(++num==50) {
                //st.setFlag();
                t1.interrupt();//强制恢复运行
                t2.interrupt();//强制恢复运行
                break;
            }
            System.out.println("main..."+num);
        }
        System.out.println("over");
    }
}
```

**setDaemon()方法**  

使线程变成守护线程（后台线程），前台线程结束之后后台线程自动结束

**join()方法**  
执行权让给t1
```
t1.join()；
```
**setPriority()方法**  
设置线程优先级
```
t1.setPriority(Thread.MAX_PRIORITY);
```
- MAX_PRIORITY
- MIN_PRIORITY
- NORM_PRIORITY

# 05 常用API

## 05-01 String类
### String类特点
**特点1**：字符串一旦初始化就不可以被改变

**特点2**：  

s0字符串创建在常量池中  
s1字符串直接在常量池中找abc  
s0==s1输出为true因为是同一个abc
```
String s0 = "abc";//“abc”存在字符串常量池中
String s1 = "abc";//在字符串常量池中找abc
s0==s1;//输出为true，因为指向同一个abc
```
**特点3**：  

s0字符串创建在常量池中  
s1指向堆内存中的字符串对象  
s0==s1输出为false因为内存地址不一样  
s0.equals(s1)输出为true因为比较的是字符串内容，都是abc所以为true
```
String s0 = "abc";//“abc”存在字符串常量池中
String s1 = new String("abc");//新建一个字符串对象
s0==s1;//输出为false，因为地址不一样
s0.equals(s1);//输出为true，String类中的equals()重写了Object中的equals，比较字符串内容而不是地址值
```
### String类构造方法
**构造方法一**
```
String(byte[] bytes)
```
**作用**：将一个**字节数组**变成字符串  

```
byte[] arr = {65，66，67，68}；
String s = new String(arr);
System.out.println(s);
//输出ABCD
```
**构造方法二**
```
String(char[] value)
String(char[] value, int offset, int count)
```
**作用**：将一个**字符数组**变成字符串
```
char[] arr = {G，r，e，a, t}；
String s0 = new String(arr);
System.out.println(s0);
//输出Great
String s1 = new String(arr, 2, 3);
System.out.println(s1);
//输出eat
```
### String类常见功能
1. 获取
    - 获取字符串中字符的**个数**（长度）
        - **int length();**
    - 根据位置获取**字符**
        - **char charAt(int index);**
    - 根据字符\字符串获取**位置**
        - 从前向后找
            - **int indexOf(int ch);** 获取字符第一次出现的位置
            - **int indexOf(int ch, int fromIndex)** 从指定位置进行对字符第一次出现位置的查找
            - **int indexOf(String str);** 获取字符串第一次出现的位置，找不到则为-1
            - **int indexOf(String str, int fromIndex);** 从指定位置进行对字符串第一次出现位置的查找
        - 从后向前找
            - **int lastIndexOf(int ch);** 获取字符最后一次出现的位置
            - **int lastIndexOf(int ch, int fromIndex)** 从指定位置进行对字符最后一次出现位置的查找
            - **int lastIndexOf(String str);** 获取字符串最后一次出现的位置
            - **int lastIndexOf(String str, int fromIndex);** 从指定位置进行对字符串最后一次出现位置的查找
    - 获取字符串中的一部分字符串，也叫**子串**
        - **String substring(int beginIndex, int endIndex)** 获取字符串从**beginIndex**到**endIndex-1**位置的字串
        - **String substring(int beginIndex)** 获取字符串从**beginIndex**开始到结尾的字串
2. 转换
    - 将字符串转换成字符串数组（字符串的切割）
        - **String[] split(String regex)**
    - 将字符串转换成字符数组
        - **char [] toCharArray()**
    - 将字符串转换成字节数组
        - **byte[] getBytes()**
    - 将字符串转换成大写小写
        - **String toUpperCase()** 大写
        - **String toLowerCase()** 小写
    - 将字符串中的指定内容替换
        - **String replace(char oldChar, char newChar)** 用newChar替换所有oldChar
        - **String replace(String s1, string s2)** 用s2替换所有s1
    - 将字符串两端的空格去除
        - **String trim()**
    - 将字符串进行连接
        - **String concat(string)** 
```
String s = "One, Two, Three";
String [] arr = s.split(",");//用","切割原字符串
Char [] chs = s.toCharArray();
```
- 将字符串转换成字符：toCharArray() 方法
- 将字符转换成字符串: String(char[] value) 构造方法

3. 判断
    - 判断两个字符串内容是否相同
        - **boolean equals(Object obj)**
        - **boolean equalsIgnoreCase(String anotherString)** 忽略大小写比较字符串内容
    - 判断字符串中是否包含指定字符串
        - **boolean contains(string str)**
    - 判断字符串是否以指定字符串开头或结尾
        - **boolean startsWith(string)** 开头
        - **boolean endsWith(string)** 开头
4. 比较 比较基于字符串中各个字符的Unicode值
    - **int compareTo(String anotherString)** 比较基于字符串中各个字符的Unicode值
        - 如果此字符串等于参数字符串，则返回0
        - 如果此字符串小于参数字符串，则返回负数
        - 如果此字符串大于参数字符串，则返回正数
5. intern()方法
    - inter()方法：对字符串池进行操作

```
String s0 = new String(“abc”);
String s1 = s0.intern();//获取字符串池中的数据
s0==s1;//false
```

### String类练习
**练习一**  
给定一个字符串数组，按照字典顺序进行从小到大的排序  
**{“nba”,“abc”,“cba”,“zz”,“qq”,“haha”}**

```
public class StringTest_1 {
    public static void main(String[] args) {
        printArray(arr);
        sortString(arr);
        printArray(arr);
    }
    public static void sortString(String[] arr) {
        for(int i = 0; i < arr.length - 1; i++) {
            for(int j = i + 1; j < arr.length; j++) {
                if(arr[i].compareTo(arr[j])) //字符串比较用compareTo方法完成
                    swap(arr,i,j);
            }
        }
    }
    private static void swap(String[] arr, int i, int j) {
        String temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
    }
    public static void printArray(String[] arr) {
        Syetem.out.println("[");
        for(int i = 0; i < arr.length - 1; i++) {
            if(i !=arr.length - 1)
                System.out.print(arr[i] + ", ");
        }
    }
}
```
**练习二**  
一个子串在整串中出现的次数  
**"nbagrwnbaxxznbaedqenba"**  
思路：
- 判断要找的子串是否存在，如果存在，用**indexOf**获取其出现位置
- 如果找到了，记录出现的位置并在剩余的字符串中继续查找该子串，剩余字符串的起始位置是出现位置+子串长度
- 通过循环完成查找，如果找不到就是-1，并且每次找到用计数器记录
```
public class StringTest_2 {
    public static void main(String[] args) {
        String str = "nbagrwnbaxxznbaedqenba";
        String key = "nba";
        int count = getKeyStringCount(str,key);
        System.out.println("count="+count);
    }
    public static int getKeyStringCount(String str, String key) {
        //定义计数器
        int ciount = 0;
        //定义变量记录key出现的位置
        int index = 0;
        
        while((index =str.indexOf(key, index))!=-1) {
            index = index + key.length();
            count++;
        }
        return count;
    }
}
```
**练习三**  
最大相同子串  
**qwerabcdtyuiop**  
**xcabcdvbn**  
思路：  
- 先看短字符串是否是长字符串的子串，如果是，那么短的就是最大子串
- 如果短的不是最大子串，那就让子串长度递减，去继续判断
```
public class StringTest_3 {
    public static void main(String[] args) {
        String s1 = "qwerabcdtyuiop";
        String s2 = "xcabcdvbn";
        String s =getMaxSubstring(s1, s2);
        System.out.println("s="+s);
    }
    public static String getMaxSubstring(String s1, String s2) {
        for(int i = 0; i < s2.length(); i++) {
            for(int a = 0, b = s2.length() - i; b != s2.length + 1; a++, b++) {
                String sub = s2.substring(a, b);
                if(s1.contacins(sub))
                    return sub;
            }
        }
    }
}
```
### StringBuffer类
**StringBuffer**：字符串缓冲区，用于存储数据的容器  

**特点**

- 长度是可变的
- 可以存储不同类型的数据
- 最终转换成字符串进行输出

**功能**

- 添加
    - **StringBuffer append(data)** 尾部添加
    - **StringBuffer insert(index, data)** 在指定位置添加
- 删除
    - **StringBuffer delete(start, end)** 删除start到end-1的字符串
    - **StringBuffer deleteCharAt(int index)** 删除指定位置的元素
- 查找
    - **char charAt(index)**
    - **int indexOf(string)**
    - **int lastIndexOf(srting)**
- 修改
    - **StringBuffer replace(start, end, string)** 
    - **void setCharAt(index, char);**


```
public static void bufferMethodDemo() {
    StringBuffer sb = new String Buffer();
    StringBuffer s1 = sb.append(4);
    System.out.println(sb); //4
    System.out.println(s1); //4
    System.out.println(s1==sb); //true
}
```
### StringBuilder类

- StringBuilder：线程不同步，用于单线程
- StringBuffer：线程同步，用于多线程

练习
将一个int数组变成字符串

```
public static String arrayToString(int[]  arr) {
    StringBuilder sb = new StringBuilder();
    sb.append("[");
    for(int i = 0; i < arr.length; i++) {
        if(i != arr.length-1)
            sb.append(arr[i] + ",");
        else
            sb.append(arr[i] + "]");
    }
    return sb.toString();
}
```
## 05-02 基本数据类型对象包装类
### 概述
**目的**：为了方便操作基本数据类型值，将其封装成对象，在对象中定义了属性和行为，丰富了该数据的操作。用于描述该对象的类就称为基本数据类型对象包装类

- Byte
- Short
- Integer
- Long
- Float
- Double
- Character
- Boolean

### 字符串和基本数值互相转换
**Integer类的字符串转换成基本数值**  
**public static int parseInt(String s)方法**
```
Integer.parseInt("123"+1); //124
```
**基本类型转字符串**

- **方法1**：基本类型数值+“”
- **方法2**：用String类中的静态方法valueOf(基本类型数值);
- **方法3**：用Integer的静态方法valueOf(基本类型数值);

**字符串转基本类型**

- **方法1**：使用包装类中的静态方法 **xxx parseXxx("xxx类型的字符串")**
    - int parseInt("intstring");
    - int parseByte("bytestring");
    - int parseShort("shortstring");
    - int parseLong("longstring");
    - int parseFloat("floatstring");
    - int parseDouble("doublestring");
    - int parseBoolean("booleanstring");
    - int parseInt("intstring")
    - 没有parseChar
- **方法2**：使用非静态方法 **intValue()**, 将一个Integer对象转换成基本数据类型值

### 进制转换

**十进制 --> 其他进制**

- toBinaryString(DecNum);
- toOctalString(DecNum);
- toHexString(DecNum);
- toString(DecNum, 需要转的进制)
```
System.out.println(Integer.toBinaryString(60))；
System.out.println(Integer.toOctalString(60))；
System.out.println(Integer.toHexString(60))；
System.out.println(Integer.toString(60,4))；//把十进制的60转换成4进制的数
```
**其他进制 --> 十进制**

```
System.out.println(Integer.parseInt("110",2))把二进制的110转换成10进制
```

### JDK 1.5自动装箱拆箱

```
Integer i = 4; //i = new Integer(4); 自动装箱 简化书写
i = i + 6; // i = new Integer(i.intValue() + 6); i.intValue() 自动拆箱
```

```
Integer a = new Integer(127);
Integer b = new Integer(127);

a==b false
a.equals(b) true
```
自动装箱如果装的是一个字节，那么该数据会被共享而不是重新开辟空间，
```
Integer x = 127; //如果是128那么x==y是false
Integer y = 127;
x==y; true
x.equals(y); true
```
## 05-03 集合框架

### 05-03-01 Collection概述

**集合定义**：集合是用于存储对象的容器

**集合特点**

- 用于储存对象的容器
- 集合的长度是可变的
- 集合中不可以存储基本数据类型值

**集合框架定义**：集合容器因为内部的数据结构不同，有多种具体容器，不断向上抽取，形成了集合框架。  

- Collection
    - List
        - Vector
        - ArrayList
        - LinkedList
    - Set：
        - HashSet
        - TreeSet

**集合使用技巧**

- 是否需要唯一
    - 需要：**Set**
        - 有序：**TreeSet**（Comparable，Comparator）
        - 无序：**HashSet**（hashCode(), equals()）
        - 和存储顺序一致（有序）：LinkedHashSet
    - 不需要：**List**
        - 增删快，查询慢：**LinkedList**
        - 增删慢，查询快：**ArrayList**

后缀名就是该集合所属的体系  
前缀名就是该集合的数据结构

    
    
**框架的顶层Collection接口的常见方法**

- 添加
    - boolean add(Object obj)
    - boolean addAll(Collection coll)
- 删除
    - boolean remove(Object obj)
    - boolean removeAll(Collection coll)
    - void clear()
- 判断
    - boolean contains(object obj)
    - boolean containsAll(Collection coll)
    - boolean isEmpty() 如果没有元素，返回true
- 获取
    - int size()
    - Iterator iterator(); 取出元素的方式，迭代器，该对象必须依赖于具体容器，因为每一个容器的数据结构都不同，所以该迭代器对象是在容器中进行内部实现的。
- 其他
    - boolean retainAll(Collection coll) 取交集
    - Object[] toArray(); 将集合转成数组

**方法演示**

```
public class CollectionDemo {
    public static void main(String[] args) {
        Collection coll new ArrayList();
        show(coll);
    }
    public static void show(Collection coll) {
        //添加元素 add()
        coll.add("abc1");
        coll.add("abc2");
        coll.add("abc3");
        
        //删除元素 remove()
        coll.remove("abc2") //会改变集合的长度
        
        System.out.println(coll);
    }
}
```
#### 迭代器

**迭代器原理**  :迭代器就是一个实现了Iterator接口的每一个容器内部的内部对象

**迭代器演示**

```
import java.util.ArrayList;
import java.util.Collection;

public class IteratorDemo {
    public static void main(String[] args) {
        Collection coll = new ArrayList();
        
        coll.add("abc1");
        coll.add("abc2");
        coll.add("abc3");
        coll.add("abc4");
        
        //使用了Collection中的iterator()方法，调用集合中的迭代器方法，是为了获取集合中的迭代器对象
        
        Iterator it = coll.iterator();
        while(it.hasNext()) {
            System.out.println(it.next());
        }
        for(Iterator it = coll.iterator(); it.hasNext();) {
            System.out.println(it.next());
        }
        
    }
}
```

### 05-03-02 List集合  

**List和Set特点**

- Collection
    - List
        - 有序（存入和取出的顺序一致）
        - 元素都有索引（角标）
        - 元素可以重复
    - Set：
        - 无序
        - 元素不能重复

**特有的常见方法**

- 添加
    - void add(index, element)
    - void add(index, collection)
- 删除
    - Object remove(index)
- 修改
    - Object set(index, element)
- 获取
    - Object get(index)
    - int idexOf(Object)
    - int lastIndexOf(object)
    - List sublist(from, to) 包含头不包含尾


```
public class ListDemo {
    public static void main(String[] args) {
        List list = new ArrayList();
        show(list);
    }
    public static void show(List list) {
        //添加元素
        list.add("abc1");
        list.add("abc2");
        list.add("abc3");
        System.out.println(list); //[abc1, abc2, abc3]
        //插入元素
        list.add(1, "abc9");
        //删除元素
        System.out.println(list.remove(2));
        //修改元素
        System.out.println(list.set(1, "abc8"));
        //Iterator获取
        Iterator it = list.iterator();
        while(it.hasNext()) {
            System.out.println(it.next());
        }
    }
}
```
**List中的迭代器**  

迭代器操作集合中的元素时，集合不可以操作，否则迭代器报错 **ConcurrentModificationException**

```
Iterator it = list.iterator();
while(it.hasNext()) {
    Object obj = it.next(); //java.util.ConcurrentModificationException
    if(obj.equals("abc2")) {
        list.add("abc9");//集合不可以再操作元素
    } else
        System.out.println(obj);
}
System.out.println(list);
```
解决方法：Iterator接口的子接口ListIterator来完成在迭代中对元素进行更多的操作。  
可以在迭代过程中完成对元素的增删改查

```
ListIterator it = list.listIterator(); //获取列表迭代器对象
while(it.hasNext()) {
    Object obj = it.next();
    if(obj.equals("abc2")) {
        it.add("abc9");
    }
}
```
**List中的子类对象**

- **Vector**：内部是数组数据结构，是同步的，增删，查询都很慢
- **ArrayList**：内部是数组数据结构，是不同步的，代替Vector。查询速度快
- **LinkedList**：内部是链表数据结构，是不同步的，增删元素的速度很快

**Vector演示**  

```
Vector v = new Vector();
v.addElement("abc1");
v.addElement("abc2");
v.addElement("abc3");
v.addElement("abc4");
Iterator it = v.Iterator;
while(it.hasNext()) {
    System.out.println(it.next());
}
```
**LinkedList演示**  

- 添加
    - addFirst(); 在前面添加
    - addLast(); 在后面添加
- 移除
    - removeFirst(); 移除第一个元素，如果链表为空，抛出**NoSuchElementException**
    - removeLast(); 移除最后一个元素
    - JDK 1.6 以后
        - pollFirst(); 如果链表为空，返回null
        - pollLast();
- 获取
    - getFirst(); 获取第一个元素，如果链表为空，抛出**NoSuchElementException**
    - getLast(); 
    - JDK 1.6 以后
        - peekFirst(); 如果链表为空，返回null
        - peekLast(); 
```
LinkedList link = new LinkedList();
link.addFirst("abc1");
link.addFirst("abc2");
link.addFirst("abc3");
link.addFirst("abc4");

System.out.println(link.getFirst());//获取第一个但不删除
System.out.println(link.removeFirst());//获取第一个并且删除

Iterator it = link.Iterator;
while(it.hasNext()) {
    System.out.println(it.next());//输出4321因为addFirst是加在前面
}
```
**LinkedList练习**

- 堆栈数据结构：先进后出 First In Last Out FILO
    - addFirst()
    - removeFirst()
- 队列数据结构：先进先出 First In First Out FIFO
    - addLast()
    - removeFirst()

**ArrayList集合储存自定对象**

```
public class Person {
    private String name;
    private int age;
    public Person() {
        super();
    }
    public Person(String name, int age) {
        super();
        this.name = name;
        this.age = age;
    }
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }
    void int getAge() {
        return age;
    }
    public void setAge(int age) {
        this.age = age;
    }
}
public class ArrayListTest {
    public static void main(String[] args) {
        ArrayList a1 = new ArrayList();
        a1.add(new Person("Kevin",24));
        a1.add(new Person("Steve",25));
        a1.add(new Person("Tony",26));
        a1.add(new Person("Peter",29));
        Iterator it = a1.iterator();
        while(it.hasNext()) {
            //System.out.println((Person)it.next().getName());
            Person p = (Person) it.next();//把
            System.out.println(p.getName()+"-"+p.getAge());
        }
    }
}
```

### 05-03-03 Set集合

set接口中的方法和collection一致

- **HashSet**：内部数据结构是哈希表，无序，不重复，不同步
    - **LinkedHashSet**
- **TreeSet**：可以对Set集合中的元素进行排序，是不同步的

#### HashSet集合
```
public class HashSetDemo {
    public static void main(String[] args) {
        HashSet hs = new HashSet();
        
        hs.add("aaa");
        hs.add("bbb");
        hs.add("ccc");
        hs.add("ccc");
        
        Iterator it = hs.iterator();
        while(it.hasNext()) {
            System.out.println(it.next());//输出是无序的，而且没有重复的ccc
        }
    }
}
```
**哈希表**  

把一个数据经过哈希算法，存在一个位置，查找时直接把新数据经过哈希算法找到数据所在位置，速度很快，哎就很舒服

**HashSet保证该集合元素唯一性的方式**  

通过**hashCode**和**equals**方法来完成对象唯一性判断

- 对象的hashCode值不同，不用判断equals方法，直接存储到哈希表
- 对象的hashCode值相同，判断对象的equals方法是否为true
    - 如果为true，则视为相同元素，不存
    - 如果为false，则视为不同元素，进行存储

注意：如果元素要存储到HashSet集合中，必须覆盖HashCode方法和equals方法。如果定义类会产生很多对象，比如人，学生，书，通常都需要覆盖equals， hashCode方法，建立对象判断是否相同的依据 

**HashSet存储自定义对象**
```
public class Person {
    private String name;
    private int age;
    public Person() {
        super();
    }
    public Person(String name, int age) {
        super();
        this.name = name;
        this.age = age;
    }
    @Override
    public int hashCode() {
        return age;
    }
    public boolean equals(Object obj) {
        Person p = (Person)obj;
        return this.name.equals(p.name) && this.age == p.age;
    }
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }
    void int getAge() {
        return age;
    }
    public void setAge(int age) {
        this.age = age;
    }
}
public class HashSetTest {
    public static void main(String[] args) {
        HashSet hs = new HashSet();
        hs.add(new Person("Kevin",24));
        hs.add(new Person("Kevin",24));
        hs.add(new Person("Steve",25));
        hs.add(new Person("Tony",26));
        hs.add(new Person("Peter",23));
        
        Iterator it = hs.iterator();
        while(it.hasNext()) {
            Person p = (Person)it.next();
            System.out.println(p.getName()+"..."+p.getAge());
        }
    }
}
```
**集合框架练习**  

定义功能去除ArrayList中的重复元素
```
public class HashSetTest {
    public static void main(String[] args) {
        ArrayList a1 = new ArrayList();
        a1.add("abc1");
        a1.add("abc2");
        a1.add("abc2");
        a1.add("abc1");
        a1.add("abc");
        System.out.println(a1); //[abc, abc2, abc2, abc1, abc]
        a1 = getSingleElement(a1);
        System.out.println(a1); //[abc1, abc2, abc]
        }
    }
    public static ArrayList getSingleElement(ArrayList al) {
        //定义一个临时容器
        ArrayList temp = new ArrayList();
        //迭代a1集合
        Iterator it = a1.iterator();
        while(it.hasNext()) {
            Object obj = it.next();
            //判断被迭代到的元素是否在临时容器存在
            if(!temp.contains(obj)) {
                temp.add(obj);
            }
        }
        return temp;
    }
}
```
**LinkedHashSet**  

有序的HashSet

```
HashSet hs = new LinkedHashSet();
hs.add("a");
hs.add("b");
hs.add("c");
hs.add("d");
hs.add("e");
        
Iterator it = hs.iterator();
while(it.hasNext()) {
    System.out.println(it.next());
}
```

**TreeSet集合**  

可以对Set集合中的元素进行排序，是不同步的

```
public class TreeSetDemo {
    public static void main(String[] args) {
        TreeSet ts = new TreeSet();
        
        ts.add("aaa");
        ts.add("bbb");
        ts.add("zzz");
        ts.add("ccc");
        
        Iterator it = hs.iterator();
        while(it.hasNext()) {
            System.out.println(it.next());//按照元素字典顺序排序
        }
    }
}
```

- **TreeSet保证该集合元素唯一性的方式**  
    - 比较方法的返回结果是否是0，是0就是相同元素，不存。
- **TreeSet对元素进行排序的方式**
    - 方式一：按照自然顺序排序
        - 让元素自身具备比较功能，需要实现Comparable接口，重写compareTo()方法
    - 方式二：不按照自然顺序排序
        - 让集合自身具备比较功能，定义一个类实现Comparator接口，重写compare()方法。将该类对象作为参数传递给TreeSet集合的构造方法
  
**TreeSet存储自定义对象**  
排序方式一
```
public class Person implements Comparable {
    private String name;
    private int age;
    public Person() {
        super();
    }
    public Person(String name, int age) {
        super();
        this.name = name;
        this.age = age;
    }
    @Override
    public int compareTo(Object o) {
        Person p = (Person)o;
        //比较年龄
        int temp = this.age - p.age;
        return temp == 0?this.name.compareTo(p.name):temp;//如果年龄相等，则比较名字，否则直接存入
        //比较名字
        int temp = this.name.compareTo(p.name);
        return temp ==0?this.age - p.age:temp;//如果名字一样，则比较年龄，否则直接存入
    }
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }
    void int getAge() {
        return age;
    }
    public void setAge(int age) {
        this.age = age;
    }
}
public class TreeSetTest {
    public static void main(String[] args) {
        TreeSet ts = new TreeSet(new ComparatorByName());//排序方式二
        
        hs.add(new Person("Kevin",24));
        hs.add(new Person("Kevin",24));
        hs.add(new Person("Steve",25));
        hs.add(new Person("Tony",26));
        hs.add(new Person("Peter",23));
        
        Iterator it = hs.iterator();
        while(it.hasNext()) {
            Person p = (Person)it.next();
            System.out.println(p.getName()+":"+p.getAge());
        }
    }
}
```
排序方式二

- 定义一个比较器类，实现**Comparator**接口
- 重写**Comparator**接口中的**compare()** 方法
- 把传进来**的Object**类对象转型成需要比较的对象
- 创建一个存储**compareTo()** 方法结果的变量
    - 如果先比较名字，则用**p1.getName().compareTo(p2.getName())**
    - 如果先比较年龄，则用**p1.getAge() - p2.getAge()**
- 把这个类的对象传给**TreeSet**类的构造方法

```
//创建一个根据Person类的name进行排序的比较器
public class ComparatorByName implements Comparator {
    @Override
    public int compare(Object o1, Object o2) {
        //把传进来的两个对象转换成Person类才可以调用getAge()方法
        Person p1 = (Person)o1;
        Person p2 = (Person)o2;
        
        int temp = p1.getName().compareTo(P2.getName());
        return temp==0?p1.getAge() - p2.getAge():temp;
    }
}
```

**比较器应用**

```
//把字符串按长度排序
public class TreeSetTest {
    public static void main(String[] args) {
        TreeSet ts = new TreeSet(new ComparatorByLength());
        
        ts.add("cccc");
        ts.add("aaa");
        ts.add("bbbbb");
        ts.add("abc");
        ts.add("dddddd");
        
        Iterator it = ts.iterator();
        while(it.hasNext()) {
            System.out.println(it.next());
        }
    }
}
public class ComparatorByLength implements Comparator {
    @Override
    public int compare(object o1, object o2) {
        String s1 = (String)obj;
        String s2 = (String)obj;
        int temp = s1.Length() - s2.Length;
        return temp==0?s1.compareTo(s2):temp;//这里的compareTo是String类里的方法
    }
}
```

### 05-03-04 泛型
#### 泛型概述

JDK1.5出现的安全机制  

优点

- 将运行时期的问题ClassCastException转到了编译时期
- 不需要强制转换

格式<>
当操作的引用数据类型不确定的时候，就用<>将要操作的引用数据类型传入即可
```
ArrayList<String> a1 = new ArrayList<String>();

a1.add("abc");
a1.add("hahaha");

Iterator<String> it = a1.iterator();
while(it.hasNext()) {
    //String str = (String)it.next();不需要强转
    String str = it.next();
    System.out.println(str);
}
```
泛型技术是给编译器使用的技术，用于编译时期，确保了类型的安全  

**泛型擦除**：运行时，会将泛型去掉，生成的class文件中是不带泛型的  
**泛型补偿**：运行时，通过获取元素的类型，进行转换动作，不用使用者再强制转换了

```
ArrayList<E>
ArrayList<String> a = new ArrayList<String>();

Tools<E1, E2, E3, E4>
Tools<Tinjing, Lvdian, Restaurant, Movie> a = new Tools<Tinjing, Lvdian, Restaurant, Movie>();
```

#### 泛型在集合中的应用

```
public class GenericDemo {
    public static void main(String[] args) {
        TreeSet<Person> ts = new TreeSet<Person>(new ComparatorByName());
        ts.add(new Person("Kevin", 24));
        ts.add(new Person("Tony", 21));
        ts.add(new Person("Steve", 26));
        ts.add(new Person("Peter", 19));
    }
    Iterator<Person> it = ts.iterator();
    
    while(it.hasNext()) {
        Person p = (Person)it.next();
        System.out.println(p);
    }
}
public class ComparatorByName implements Comparator<Person> {
    public int compare(Person o1, Person o2) {
        int temp = o1.getName().compareTo(o2.getName());
        return temp==0?o1.getAge() - o2.getAge():temp;
    }
}
```
#### 泛型类
JDK1.5以后，使用泛型来接收类中要操作的引用数据类型
泛型类：当类中操作的引用数据类型不确定的时候，就用泛型来表示

```
public class Tool<T> {
    private T t;
    
    public T getObject() {
        return t;
    }
    
    public void setObject(T object) {
        this.t = object;
    }
}

public class GenericDefineDemo {
    public static void main(String[] args) {
        Tool<Student> tool = new Tool<Student>();
        //只能传Student。如果传Worker无法通过编译
        tool.setObject(new Student());
        Studengt stu = tool.getObject();
    }
}
```
**如果不使用泛型**

- setObject传入Worker时会编译错误
- stu需要强制转换成Student
```
public class GenericDefineDemo {
    public static void main(String[] args) {
        Tool tool = new Tool();
        
        tool.setObject(new Student());
        Studengt stu = (Student)tool.getObject();
    }
}
```
#### 泛型方法

- public void print(T str) {}
    - print能处理的数据根据对象的泛型来定
- public <A> void show(A str) {}
    - show能处理的数据自定义为A类型

泛型定义在方法上
```
修饰符 <A> 返回值类型 方法名() {}
```
**注意**：静态方法只能将泛型定义在方法上
```
public class Tool<T> {
    //把泛型定义在方法上
    public <W> void show(W str) { //show的泛型在方法上自定义
        System.out.println("show:"+str.toString());
    }
    public void print(T str) {//print的泛型跟着对象走
        System.out.println("print:"+str);
    }
    
    //当方法静态时，不能访问类上定义的泛型。
    public static void method(T obj) {
        System.out.println("method:"+ obj);
    }
    //当方法静态时，只能将泛型定义在方法上
    public static <Y> void method(Y obj) {
        System.out.println("method:" + obj);
    }
}
public class GenericDemo {
    public static void main(String[] args) {
        Tool<String> tool = new Tool<String>();
        
        //非静态
        tool.show(new Integer(4));
        tool.show("abc");
        tool.print("haha");
        tool.print(new Integer(6));//报错，因为print的泛型跟着对象走只能处理String类型的参数
        
        //静态
        tool.method(new Integer(8));
        tool.method("abcd");
    }
}
```

#### 泛型接口
把泛型定义在接口上

```
interface Inter<A> {
    public void show(A a);
}
//实现Inter时知道类型
class InterImp1 implements Inter<String> {
    public void show(String str) {
        System.out.println("show:"+ str)
    }
}
//实现Inter时不知道类型
class InterImp2<B> implements Inter<B> {
    public void show(B b) {
        System.out.println("show:"+b);
    }
}
public class GenericDemo {
    public static void main(String[] args) {
        InterImp1 in1 = new InterImp();
        in1.show("abc");
        
        InterImp2<Integer> in2 = new InterImp2<Integer>();
        in2.show(5);
    }
}
```
#### 泛型限定
类型的通配符
**<?>**
  
- **泛型限定（上限）**  
**<? extends E>**  
接收E类型或者E的子类型对象

- **泛型限定（下限）**   
**<? super E>**  
接收E类型或者E的父类型


- 一般在储存元素的时候都是用上限，因为这样取出都是按照上限类型来运算的，不会出现类型安全隐患
- 一般在取出元素的时候都是用下限：**Comparator <? super E> comparator**
```
public class GenericDemo {
    public static void main(String[] args) {
        ArrayList<Teacher> a1 = new ArrayList<Teacher>();
        a1.add("John", 32);
        a1.add("Smith", 28);
        
        ArrayList<Student> a2 = new ArrayList<Student>();
        a2.add("Leo", 23);
        s2.add("Kevin", 24);
        
        printCollection(a1);
        printCollection(a2);
    }
    public static void printCollection(Collection<? extends Person> a1) {
        Iterator<? extends Person> it = a1.iterator();
        while(it.hasNext()) {
            System.out.println(it.next().toString());
        }
    }
}
```
### 05-03-05 Map集合

#### Map集合概述
Map和Collection区别

- Map（双列集合） 一次添加一对元素
- Collection（单列集合） 一次添加一个元素

Map集合中必须保证Key的唯一性

**Map集合常用方法**

- 添加
    - V put(key, value) 返回前一个和key关联的值，如果没有返回null
- 删除
    - void clear() 清空map集合
    - V remove (key) 根据指定的key删除键值对
- 判断
    - boolean containsKey(key)
    - boolean containsValue(value)
    - boolean isEmpty()
- 获取
    - V get(key) 通过键获取值，如果没有该键，返回null
    - int size() 获取键值对个数

```
public class MapDemo {
    public static void main(String[] args) {
        Map<Integer, String> map = new HashMap<Integer, String> ();
        method(map);
    }
    //method_2获取所有的value
    public static void method_2(Map<Integer, String> map) {
        map.put(1,"abc");
        map.put(2,"cde");
        map.put(3,"efg");
        map.put(4,"ghi");
        //获取map中所有Key所在的set集合
        Set<Integer> keySet = map.keySet();
        //用迭代器获取每一个键
        Iterator<Integer> it = keySet.iterator();
        while(it.hasNext()) {
            Integer key = it.next();
            //通过key获取值
            String value = map.get(Key);
            System.out.println(key+":"+value);
        }
    }
    //method演示基本功能
    public static void method(Map<Integer, String> map) {
        //添加元素（相同Key，值会覆盖）
        System.out.println(map.put(24, "Kevin"));//输出null
        System.out.println(map.put(24, "Leo"));//输出Leo
        map.put(20, "Peter");
        map.put(29, "Tony");
        //删除
        map.remove(20);//Peter被删
        //判断
        map.containsKey(24);//true
        //获取
        map.get(29);//Tony
        
        
    }
}
```
**取出Value方式一**  

- 用keySet()方法获取Key所在的Set集合
- 用迭代器获取每一个Key
- 通过map.get(Key)获取Value
```
//获取map中所有Key所在的set集合
Set<Integer> keySet = map.keySet();
//用迭代器获取每一个键
Iterator<Integer> it = keySet.iterator();
while(it.hasNext()) {
    Integer key = it.next();
    //通过key获取值
    String value = map.get(Key);
        System.out.println(key+":"+value);
}
```
**取出Value方式二**  

- entrySet()方法把Key和Value的映射关系作为**一个**对象存储到了set集合中
- 这个映射对象是Map.Entry类型，Entry是Map的内部接口

```
Set<Map.Entry<Integer, String>> entrySet = map.entrySet();
Iterator<Map.Entry<Integer, String>> it = entrySet.iterator();
while(it.hasNext()) {
    Map.Entry<Integer, String> me =it.next();
    Integer key = me.getKey();
    String value = me.getValue();
    System.out.println(key+":"+value);
}
```
**取出Value方式三**

用Collection values()方法取出values值

```
Collection <String> values = map.values();
Iterator<String> it = values.iterator();
while(it2.hasNext()) {
    System.out.println(it2.next());
}
```
#### Map集合常用子类对象

Map常用的子类

- **Hashtable**：内部结构是哈希表，是**同步**的，不允许null作为Key或Value
    - Properties类：用来存储键值对型的配置文件信息
- **HashMap**：内部结构是哈希表，是**不同步**的，允许null作为Key或Value
- **TreeMap**：内部结构是二叉树，是**不同步**的，可以对Map中的Key**排序**


**HashMap存储自定义对象**  
将学生对象和学生的归属地通过Key和Value存储到Map集合中

```
public class HashMapDemo {
    public static void main(String[] args) {
        HashMap<Student, String> hm = new HashMap<Student, String>();
        
        hm.put(new Student("Kevin",24), "CN");
        hm.put(new Student("Tony",32), "US");
        hm.put(new Student("Seb",29)，"RU");
        
        //Set<Student> keySet = hm.keySet();
        Iterator<Student> it = hm.keySet().iterator();
        while(it.hasNext()) {
            Student key = it.next();
            String value = hm.get(key);
            System.out.println(key.getName()+":"+key.getAge()+"-"+value);
        }
    }
}
```
**TreeMap存储自定义对象**  
```
public class TreeMapDemo {
    public static void main(String[] args) {
        TreeMap<Student, String> tm = new TreeMap<Student, String>();
        
        hm.put(new Student("Kevin",24), "CN");
        hm.put(new Student("Tony",32), "US");
        hm.put(new Student("Seb",29)，"RU");
        
        Iterator<Map.Entry<Student, String>> it = tm.entrySet().iterator();
        while(it.hasNext()) {
            Map.Entry<Student, String> me = it.next();
            Student key = me.getKey();
            String value = me.getValue();
            System.out.println(key.getName()+":"+key.getAge()+"-"+value);
    }
}
```

**LinkedHashMap**  
有序的HashMap
```
public class LinedHashMap {
    public static void main(String[] args) {
        HashMap<Integer,String> hm = new LinkedHashMap<Integer,String>();
        hm.put(3,"KK");
        hm.put(1,"AA");
        hm.put(2,"LL");
        Iterator<Map.Entry<Integer,String>> it = hm.entrySet().iterator();
        while(it.hasNext()) {
            Map.Entry<Integer,String> me = it.next();
            Integer key = me.getKey();
            String value = me.getValue();
            System.out.println(key+":"+value);
        }
    }
}
```
**Map集合练习**  

练习："asdfdsadfa"获取该字符串中每一个字母出现的次数  
要求打印结果是：a（2）b（1）...；

思路：

- 字母和次数之间存在映射关系，而且无有序编号，所以用Map集合（有有序编号才用Array）
- 保证唯一性一方有顺序如a，b，c。用TreeMap
- 把字符串转换成字符数组
- 遍历字符数组，用每一个字母作为Key去查Map集合这个表
    - 如果Key不存在，就将该子母Key作为1存储到map集合中
    - 如果Key存在，就将该字母键对应值取出并+1，再存储到Map集合中
```
public class MapTest {
    public static void main(String[] args) {
        String str = "asdfdsadfa";
        String s = getCharCount(str);
        System.out.println(s);
    }
    public static String getCharCount(String str) {
        //将字符串变成字符数组
        char[] chs = str.toCharArray();
        //定义map集合表
        Map<Character,Integer> map = new TreeMap<Character,Integer>();
        for(int i = 0; i < chs.length; i++) {
            //将数组中的字母作为key去查map表
            Integer value = map.get(chs[i]);
            //判断值是否为null
            /*
            if(value == null) {
                map.put(cha[i],1);
            } else {
                map.put(cha[i],value + 1)
            }
            */
            if(value!=null) {
                count = value + 1;
            ]
            map.put(chs[i],count);
        }
        return mapToString(map);
    }
    private static String mapToString(Map<Character, Integer> map) {
        StringBuilder sb = new StringBuilder();
        Iterator<Charater> it = map.keySet().iterator();
        while(it.hasNext()) {
            Character key = it.next();
            Integer value = map.get(key);
            sb.append(key+"("+value+")");
        }
        return sb;
    }
}
```
### 05-03-06 工具类（Collections，Arrays）

#### Collections类

Collections类里的方法都是静态的  

**sort()方法**
```
public static void demo_1() {
    List<String> list = new ArrayList<String>();
    list.add("bbb");
    list.add("aaa");
    list.add("ccc");
    System.out.println(list);
    //对list集合进行指定顺序的排序
    Collections.sort(list);
    mySort(list);
    System.out.println(list);
}
//自定泛型T，传进来的List里的元素必须是可以比较的所以extends Comparable，
//而Comparable<>也要定义泛型，只要是T或者T的子类都可以传进来所以Comparable的泛型是<？ super T>
public static <T extends Comparable<? super T>> void mySort(List<T> list) {
    for(int i = 0; i < list.size() - 1; i++) {
        for(int j = i + 1; j < list.size(); j ++) {
            if(list.get(i).compareTo(list.get(j))>0) {
                T temp = list.get(i);
                listset(i, list.get(j));
                list.set(j, temp);
            }
        }
    }
}
```
**binarySearch()方法**  
二分查找（折半查找）前必须先排序
```
int index = Collections.binarySearch(list, "abc");
```
**max()方法**  
最大值

```
String max = Collections.max(list);
```
**reverseOrder()逆序方法**  
逆向排序
```
TreeSet<String> ts = new TreeSet<String>(Collections.reverseOrder());
```
原理：

```
TreeSet<String> ts = new TreeSet<String>(new Comparator<String>()) {
    @Override
    public int compare(String o1, String o2) {
        int temp = o2.comareTo(o1);
        return temp;
    }
}
```
**replace()替换方法**  
```
Collections.replaceAll(list, "cba", "nba");//用nba替换cba
```
**fill()全部替换方法**  

```
//全替换成cc
Collections.fill(list, "cc");
```
**shuffle()随机排序方法**  
```
Collections.shuffle(list)
```

**synchronizedList()方法**  
返回一个同步list  
**原理**：
```
//非同步的list
List list = new ArrayList();
//返回一个同步的list
list = MyCollections.synList(list);

class MyCollections {
    public static List synList(List list) {
        return new MyList(list);
    }
}
class MyList {
    private List list;
    MyList(List list) {
        this.list = list;
    }
    public boolean add(Object obj) {
        synchronized(lock) {
            return list.add(obj);
        }
    }
    public boolean remove(Object obj) {
        synchronized(lock) {
            return list.remove(obj);
        }
    }
}
```
#### Arrays类
Arrays类里的方法都是静态的

**toString()方法**
```
public class ArraysDemo {
    public static void main(String[] args) {
        int[] arr = {3,1,5,6,3,6};
        System.out.println(Arrays.toString(arr))
    }
}
```
toString的实现方式

```
public static String myToString(int[] a) {
    int iMax = a.length - 1;
    if (iMax == -1)
        return "[]";
    StringBuilder b = new StringBuilder();
    b.append('[');
    for(int i = 0;; i++) { //中间省略判断条件，默认true
        b.append(a[i]);
        if(i == iMax)
            return b.append(']').toString();
        b.append(", ");
    }
}
```

###Array和Collections相互转换
**数组转成集合** 

**Arrays类中的asList()方法**  

**作用**：可以使用集合的方法操作数组中的元素（比如**contains()**）  

**注意**：数组长度固定，所以对于集合的增删方法是不可以使用的，否则会发生**UnsupportedOperationException**

```
public class ArraysDemo {
    public static void main(String[] args) {
        String[] arr = {"abc", "haha", "xixi"};
        List<String> list = Arrays.asList(arr);
        boolean b = list.contains("xixi");
        System.out.println("b="+b);
    }
}
```
- 如果数组中的元素是对象，那么转成集合时，直接将数组中的元素作为集合中的元素进行存储
- 如果数组中的元素是基本类型数值，那么会将该数组作为集合中的元素进行存储

**集合转成数组**  

**Collections接口中的toArray()方法**  

**作用**：可以对集合中的元素操作的方法进行限定，不允许对其进行增删  

**toArray()**方法需要传入一个指定类型的数组

- 指定类型数组的长度如果小于集合的size，那么该方法会创建一个同类型并和集合相同size的数组
- 指定类型数组的长度如果大于集合的size，那么该方法会使用指定的数组，存储集合中的元素，其他位置默认为null
```
public class ToArray {
    public static void main(String[] args) {
        List<String> list = new ArrayList<String>();
        list.add("abc1");
        list.add("abc2");
        list.add("abc3");

        String[] arr = list.toArray(new String[list.size()]);
    }
}
```
### 05-03-07 JDK1.5 新特性


#### ForEach循环  
格式：

```
for(类型 变量：Collection集合|数组) {
    Code;
}
```
遍历集合
```
public class ForEachDemo {
    public static void main(String[] args) {
        List<String> list = new ArrayList<String>();
        list.add("abc1");
        list.add("abc2");
        list.add("abc3");
        //传统迭代遍历
        Iterator<String> it = list.iterator();
        while(it.hasNext) {
            System.out.println(it.next());
        }
        //foreach语句
        for(String s : list) {
            System.out.println(s);
        }
    }
}
```
遍历数组
```
int[] arr = {3,1,5,7,4};
for(int i : arr) {
    System.out.println(i);
}
```
For循环和ForEach的区别

- 传统for可以完成对语句执行很多次，因为可以定义控制循环的增量和条件
- 高级for是一种简化形式，它必须有被遍历的目标，该目标要么是数组，要么是Collection单列集合

Map集合必须转换成单列set才可以使用ForEach遍历

```
Map<Integer,String> map = new HashMap<Integer,String>();
map.put(3,"a");
map.put(1,"b");
map.put(2,"c");

for(Integer key : map.keySet()) {
    String value = map.get(key);
    System.out.println(key+":"+value);
}
for(Map.Entry<Integer,String> me : map.entrySet()) {
    Integer key = me.getKey();
    String value = me.getValue();
    System.out.println(key+":"+value);
}
```
#### 方法可变参数

方法的可变参数：其实就是一个数组，但是接收的数组的元素，自动将这些元素封装成数组，简化了调用者的书写  

**注意**：可变参数类型，必须定义在参数列表的结尾
```
public class ParameterDemo {
    public static void main(String[] args) {
        int[] arr = {5,1,4,7,3};
        int sum = add(arr);
        
        int sum_new = newAdd(5,1,4,7,3);
        System.out.println("sum_new="+sum_new);
    }
    //方法的可变参数
    public static int newAdd(int... arr) {
        int sum = 0;
        for(int i = 0; i < arr.length; i++) {
            sum = sum + arr[i];
        }
        return sum;
    }
    //参数列表接收一个数组
    public static void add(int[] arr) {
        int sum = 0;
        for(int i = 0; i < arr.length; i++) {
            sum = sum + arr[i];
        }
        return sum;
    }
}
```
#### 静态导入

```
import static java.util.Collections.sort;
import static java.lang.System.*;
```
```
public class StaticImportDemo {
    public static void main(String[] args) {
        List<String> list = new ArrayList<String>();
        list.add("abc3");
        list.add("abc1");
        list.add("abc2");
        out.println(list);
        sort(list);
        out.println(list);
    }
}
```
## 05-04 其他对象API
### 05-04-01 System类
System类中的方法和属性都是静态的，所以不可以被实例化  

**常见方法**  

- **long currentTimeMillis()** 获取当前时间到UTC 1970.1.1之间的毫秒值
```
long l1 = System.currentTimeMillis();
System.out.println(l1);
```
- **Properties getProperties()** 获取系统的属性，并储存到Properties集合中
    - Properties集合中存储的都是String类型的Key和Value
    - 最好使用Properties集合自己的储存和取出方法来完成元素的操作
```
Property prop = System.getProperties();
Set<String> nameSet = prop.stringProperyNames();
for(String name : nameSet) {
    String value = prop.getProperty(name);
    System.out.println(name+":"+value);
}
```
- **String getProperty()** 获取String类型的属性
```
private static final String LINE_SEPARATOR = System.getProperty("line.separator");
System.out.println("Hello"+LINE_SEPARATOR+"world");
```
- **setProperty("mykey", "myvalue")** 给系统设置属性信息

### 05-04-02 Runtime类
特点

- Runtime类没有构造方法，说明该类不可以创建对象。
- Runtime类有非静态的方法**getRuntime()**，说明该类提供静态返回该类对象的方法，而且只有一个对象（单例设计模式）
```
Runtime r = Runtime.getRuntime();
```
- **process exec()** 方法：执行
```
//用notepad运行Runtime.txt
r.exec("notepad.exe c:\\Runtime.txt");
//打开QQ
r.exec("c:\\abc\\QQ.exe");

Process p = r.exec("notepad.exe c:\\Runtime.txt");
p.destroy();
```
### 05-04-03 Math类
Math类包含用于执行基本数学运算的方法，如初等指数、对数、平方根和三角函数。  

**常用方法**

- **ceil()** 返回大于参数的最小整数
- **floor()** 返回小于参数的最大整数
- **round()** 返回四舍五入的整数
- **pow(a,b)** a的b次方
```
double d1 = Math.ceil(12.56);
double d2 = Math.floor(12.56);
double d3 = Math.round(12.56);
double d4 = Math.poe(10,2);
System.out.println("d1="+d1); 13.0
System.out.println("d2="+d2); 12.0
System.out.println("d3="+d3); 13.0
System.out.println("d4="+d4); 1000
```
**随机数生成**  
方法一：Math类，ramdom()方法
- **ramdom()** 返回0到1之间的随机数，包括0
```
double d = Math.random();
```
方法二：Random类实例化对象
```
Random r = new Random();
int d = r.nextInt(10)
//返回1到10之间随机的整数
```
### 05-04-04 Date类
构造方法
```
public class DateDemo {
    public static void main(String[] args) {
        long time = System.currentTimeMillis();
        
        Date date1 = new Date();//当前日期和时间封装成对象
        Date date2 = new Date(time)//指定毫秒封装成对象
    }
}
```
--------------------------------------
**日期对象和毫秒值之间的转换**

**毫秒值 --> 日期对象**  
- 通过Date对象的构造方法new Date(timeMillis);
- setTime()设置

**日期对象 --> 毫秒值**
- getTime()获取
---------------------------------------

**日期对象的格式化**   

**日期对象 --> 日期格式字符串**

用DateFormat类中的format方法
```
Date date = new Date();
//获取默认风格日期格式对象, FULL，LONG可以指定风格
DateFormat dateFormat = DateFormat.getDataInstance(DateFormat.FULL);
String str_date = dateFormat.format(date);
```
自定义风格的日期对象
```
Date date = new Date();
DateFormat dateFormat = new SimpleDateFormat("yyyy--MM--dd");
String str_date = dateFormat.format(date);
```
**日期格式字符串 --> 日期对象**  
用DateFormat类中的parse方法
```
String str_date = "2017-6-20";
//获取默认风格日期格式对象, FULL，LONG可以指定风格
DateFormat dateFormat = DateFormat.getDateInstance();
Date date = dateFormat.parse(str_date);
```
自定义风格的日期格式字符串
```
String str_date = "2017---6---20";
DateFormat dateFormat = new SimpleDateFormat("yyyy---MM---dd");
Date date = dateFormat.parse(str_date);
```
----------------------------------------
**Date练习**  
2012-9-1到2017-6-20中间有多少天  
思路：
- 将日期字符串转换成日期对象
- 将Date对象转换成毫秒值
- 相减再变成天数

```
public class DateTest {
    public static void main(String[] args) {
        String str_date1 = "2012-9-1";
        String str_date2 = "2017-6-20";
        compareDate(str_date1, str_date2);
    }
    public static void compareDate(String str_date1, String str_date2) {
        //将日期字符串转换成日期对象
        DateFormat dateFormat = DateFormat.getDateInstance();
        dateFormat = new SimpleDateFormat("yyyy--MM--dd");
        Date date1 = dateFormat.Parse(str_date1);
        Date date2 = dateFormat.Parse(str_date2);
        //将Date对象转换成毫秒值
        long time1 = date1.getTime();
        long time2 = date2.getTime();
        long time = Math.abs(time1 - time2);
        
        int day = getDay(time);
        System.out.println(day);
    }
    private static int getDay(long time) {
        int day = (int)(time/1000/60/60/24);
        return day;
    }
}
```
### 05-04-05 Calendar类
```
public class CalendarDemo {
    public static void main(String[] args) {
        Calendar c = Calendar.getInstance();
        c.set(2011, 3, 10);//设置时间
        c.add(Calendar.YEAR, 2)//加2年
        showDate(c);
    }
    public static void showDate(Calendar c) {
        Calendar c = Calendar.getInstance();
        int year = c.get(Calendar.YEAR);
        int month = c.get(Calendar.MONTH) + 1;
        int day = c.get(Calendar.DAY_OF_MONTH);
        int week = c.get(Calendar.DAY_OF_WEEK);
        System.out.println(year+"年"+month+"月"+day+"日"+getWeek(weel));
    }
    public static void getWeek(int[] i) {
        String[] weeks = {"", "星期日", "星期一", "星期二", "星期三", "星期四", "星期五", "星期六"}
        returns weeks[i];
    }
}
```
# 06 Java SE IO

## 06-01 IO流概述

### 概述

- IO流用来处理设备之间的数据传输
- Java对数据的操作是通过流的方式
- Java用于操作流的对象都在IO包中

IO流对于内存设备而言

- 输入：把外设中的数据读取到内存中
- 输出：把内存的数写入到外设中

**IO流分类**

- 流按操作数据分为两种
    - 字节流
    - 字符流
- 流按流向分为
    - 输入流
    - 输出流

## 06-02 字节流和字符流

### 06-02-01 字符流

**IO体系**
- 字节流的顶层父类
    - InputStream
        - FileInputStream
        - BufferedInputStream
    - OutputStream
        - FileOutputStream
        - BufferedOutputStream
- 字符流的顶层父类
    - Reader
        - FileReader
        - BufferedReader
        - InputStreamReader 转换流
    - Writer
        - FileWirter
        - BufferedWirter
        - OutputStreamWriter 转换流

**字符流特点**：只能操作文字  

**字符流由来**：字节流读取文字字节数据后，不直接操作，而是先查指定的编码表。获取对应的文字，再对这个文字进行操作

字符流 = 字节流 + 编码表

#### FileWirter类
**定义**：字符输出流子类，其对象可以向文件中写入字符数据  

**注意**：
- 该类没有空构造方法因为往文件中写入文字数据必须在创建对象时明确该文件
- 如果文件不存在，自动创建
- 如果文件已存在，自动覆盖

**方法**
- wirte("Hello World!") 写入数据到临时存储缓冲区
- flush() 刷新，把数据从临时存储缓冲区存储到目的地
- close() 关闭流，关闭资源，关闭前会调用flush刷新缓冲中的数据到目的地
```
public class FileWriter {
    public static void main(String[] args) {
        //创建一个可以往文件中写入字符数据的字符输出流对象
        //创建对象时必须初始化
        FileWriter fw = new FileWriter("JAVA.txt", true);
        //把数据写入临时存储缓冲区
        fw.wirte("Hello World!");
        //刷新，将数据直接写入目的地
        fw.flush();
        //关闭流，关闭资源，关闭前会调用flush刷新缓冲中的数据到目的地
        fw.close();
    }
}
```
**细节**
- 换行：创建变量private static final String LINE_SEPARATOR = null; 进行换行
- 续写：在构造方法里写上true，可以在原有的文件上续写
    - new FileWirter("JAVA.txt",true)

**IO异常处理**
```
public class FileWriter {
    public static void main(String[] args) {
        
        FileWriter fw = null
        try {
            new FileWriter("JAVA.txt", );
            fw.wirte("Hello World!");
        } catch(IOException e) {
            System.out.println(e.toString());
        } finally {
            if(fw != null)
            try {
                fw.close();
            } catch(IOException e) {
                throw new RuntimeException("关闭失败");
            }
        }
    }
}
```
#### FileReader类
**定义**：字符输出流子类，其对象可以读取一个文本文件，并且打印到控制台

**注意**：
- 该类没有空构造方法因为读取文件的时候该文件必须存在
- 其实就是用一个读取流关联一个已存在的文件
- 读取时一个read只能读取一个字符

**方法**
- 读取方式
    - 读取方式一 read() 读取字符，一次只能读一个
    - 读取方式二 read(char []) 读取字符，存入数组
- close() 关闭流，关闭资源，关闭前会调用flush刷新缓冲中的数据到目的地

读取方式一
```
public class FileWriter {
    public static void main(String[] args) {
        //创建读取字符数据的流对象
        //一定要确定文件是存在的
        //用一个读取流关联一个已存在的文件
        FileReader fr = new FileReader("JAVA.txt");
        
        //用Reader中的read方法读取字符
        int ch = fr.read();
        System.out.println(ch);
        //重复读取
        while((ch=fr.read())！= -1) {
            System.out.println((char)ch);
        }
        fr.close;
    }
}
```
读取方式二
```
public class FileWriter {
    public static void main(String[] args) {

        FileReader fr = new FileReader("JAVA.txt");
        //创建字符数组
        char[] buf = new char[3];
        //把读取的数据存入数组
        int num = fr.read(buf);
        System.out.println(new String(buf));
        //重复读取
        while((len=fr.read(buf)) != -1) {
            System.out.println(new String(buf,0,len ));
        }
    }
}
```
**读写练习**  
复制一个文件到C盘  

思路

- 读取源数据
- 将读取的数据写入目的地
- 用字符流操作文本数据

复制方式一
```
public class FileTest {
    public static void main(String[] args) throws IOExcepion {
        //读取文本文件
        FileReader fr = new FileReader("JAVA.txt");
        //存储文本文件
        FileWriter fw = new FileWirter("JAVA_COPY.txt");
        //重复读取
        int ch = 0;
        while((ch=fr.read()) != -1) {
            fw.wirte(ch);
        }
        fr.close();
        fw.close();
    }
}
```
复制方式二
```
public class FileTest {
    private static final int BUFFER_SIZE = 1024;
    public static void main(String[] args) throws IOExcepion {
    
        FileReader fr = null;
        FileWirter fw = null;
        try {
            fr = new FileReader("JAVA.txt");
            fw = new FileWirter(JAVA_COPY.txt);
            //创建一个临时容器
            char[] buf = new char[BUFFER_SIZE];
            //定义一个变量记录读取到的字符数
            int len = 0；
            while((len=fr.read(buf)) != -1)
                fw.wirte(buf, 0, len);
        } catch(Excepion e) {
            throw new RuntimeException("读写失败");
        } finally {
            if(fw != null)
                try {
                    fw.close;
                } catch(IOException e) {
                    e.printStackTrace();
                }
            if(fw != null)
                try {
                    fr.close;
                } catch(IOException e) {
                    e.printStackTrace();
                }
        }
    }
}
```

#### 缓冲区

提高了IO流操作效率

- BufferedReader
- BufferedWirter

#### BufferWirter类
  
**构造方法**：传入一个要被缓冲的流对象  

**常用方法**

- wirte：写入
- newLine()：换行
- flush：刷新
- close：关闭，缓冲区关闭之后，被缓冲的流对象也被自动关闭
```
public class BufferWirterDemo {
    public static void main(String[] args) {
        //创建写入流对象
        FileWriter fw = new FileWriter("buf.txt");
        //创建一个字符写入流的缓冲区对象
        //缓冲区对象和要被缓冲的流对象关联
        BufferedWriter bufw = new BufferedWriter(fw);
        
        bufw.write("abc");
        bufw.newLine();//换行
        bufw.write("def");
        
        bufw.flush();
        bufw.close();
    }
}
```
#### BufferReader类

**构造方法**：传入一个要被缓冲的流对象  

**常用方法**

- read()；读取一个字符
- readLine()：读取一整行
    - 原理：使用了读取缓冲区的read方法，将读取到的字符进行缓冲并判断换行标记，返回标记前的缓存数据

```
public class BufferReaderDemo {
    public static void main(String[] args) {
        //创建读取流对象
        FileReader fr = new FileReader("buf.txt");
        //创建一个字符读取流的缓冲区对象
        //缓冲区对象和要被缓冲的流对象关联
        BufferedReader bufr = new BufferedReader(fr);
        String line = null;
        while((line = bufr.readLine()) != null) {
            System.out.println(line);
        }
    }
}
```
**缓冲区复制文件**  
方式一
```
public class CopyDemo {
    public static void main(String[] args) {
        FileReader fr = new FileReader("buf.txt");
        BufferedReader bufr = new BufferedReader(fr);
        
        FileWriter fw = new FileWriter("buf_copy.txt");
        BufferedWirter bufw = new BufferedWirter(fw);
        
        inc ch = 0;
        while((ch=bufr.read())!=-1) {
            bufw.write(ch);
        }
        bufw.close();
        bufr.close();
    }
}
```
方式二  
一行一行复制
```
public class CopyDemo {
    public static void main(String[] args) {
        FileReader fr = new FileReader("buf.txt");
        BufferedReader bufr = new BufferedReader(fr);
        
        FileWriter fw = new FileWriter("buf_copy.txt");
        BufferedWirter bufw = new BufferedWirter(fw);
        
        String line = null;
        while((line=bufr.readLine())!= -1) {
            bufw.write(line);
        }
        bufw.close();
        bufr.close();
    }
}
```
**自定义BufferReader**

```
public class MyBufferReader {
    private FileReader r;
    //缓冲区全局数组
    private char[] buf = new charp[1024];
    //操作数组中元素指针
    private int pos = 0;
    //计数器：记录缓冲区中的数据个数
    MyBufferedReader(FileReader r) {
        this.r = r;
    }
    public int myRead() throws IOException {
        If(count == 0) {
            count = r.read(buf);
            pos = 0;
        }
        if(count < 0)
            return -1;
        char ch = buf[pos++];
        count--;
        return ch;
        /*
        if(count==0) {
            count = r.read(buf);
            if(count < 0) {
                return -1;
            }
            pos = 0;//每次获取数据到缓冲区后，角标归零
            char ch = buf[pos];
            pos++;
            count--;
            return ch;
        } else if(count > 0) {
            char ch = buf[pos];
            pos++;
            count--;
            return ch;
        }
        */
    }
    public String myReadLine() {
        StringBuilder sb = new StringBuilder();
        int ch = 0;
        while((ch = myRead())!=-1) {
            if(ch == '\r') {
                continue;
            } else if(ch == '\n') {
                return sb.toString();
            } else {
                //从缓冲区中读到的字符存储到缓存行数据的缓冲区中
                sb.append((char)ch);
            }
        }
        return null;
    }
    public void myClose() {
        r.close();
    }
}
```

#### LineNumberReader类

**作用**：可以读取行数  

**方法**

- setLineNumber()：设置起始行数
- readLine()：整行读取
- close()：关闭

```
public class LineNumberReaderDemo {
    public static void main(String[] args) {
        FileReader fr = new FileReader();
        LineNumberReader lnr = new LineNumberReader(fr);
        
        String line = null;
        //设置起始行数
        lnr.setLineNumber(1);
        while((line=lnr.readLine())!=null) {
            System.out.println(lnr.getLineNumber()+":"+line);
        }
        lnr.close(0;)
    }
}
```


#### 装饰设计模式

**定义**：对一组对象的功能进行增强的设计模式

**特点**：装饰类和被装饰类都必须所属同一个接口或者父类

**装饰和继承异同**

- 相同点：都能实现对象功能的增强
- 不同点
    - 装饰比继承灵活

**装饰灵活性的体现**  

传统继承扩展  

Writer

- TextWriter：用于操作文本
    - BufferedTextWriter
- MediaWriter：用于操作媒体
    - BufferedMediaWriter
- WebWriter：用于操作网页
    - BufferedWebWriter
- ServerWriter：用于操作服务器
    - BufferedServerWriter

装饰设计扩展  

Writer

- TextWriter：用于操作文本
- MediaWriter：用于操作媒体
- WebWriter：用于操作网页
- ServerWriter：用于操作服务器
- BufferedWriter：提高效率
```
public class PersonDemo {
    public static void main(String[] args) {
        Person p = new Person();
        EnhancedPerson p1 = new EnhancedPerson(p);
        p1.eat();
        EnhancedPerson2 p2 = new EnhancedPerson2();
        p2.eat();
    }
}
class Person {
    void eat() {
        System.out.println("Steak");
    }
}
//装饰
class EnhancedPerson {
    private Person p;
    EnhancedPerson(Person p) {
        this.p = p;
    }
    public void eat() {
        System.out.println("Appetizer");
        p.eat();
        System.out.println("Dessert");
        
    }
}
//继承
class EnhancedPerson2 extends Person{
    public void eat() {
        System.out.println("Appetizer");
        super.eat();
        System.out.println("Dessert");
    }
}
```
### 06-02-02 字节流

- 字节流的顶层父类
    - InputStream
        - FileInputStream
    - OutputStream
        - FileOutputStream

常用方法

- FileInputStream
    - read();
    - available(); 获取字节长度
- FileOutputStream
    - write()

**字节流操作文件基本演示**
```
public class ByteStreamDemo {
    public static void main(String[] args) {
        demo_read();
        demo_write();
    }
    public static void demo_read() {
        //创建字节读取流对象，和指定文件关联
        FileInputStream fis = new FileInputStream("bytedemo.txt");
        //一次读取一个字节
        int ch = fis.read();
        System.out.println((char)ch);
        //全部读取完毕
        int ch = 0;
        while((ch=fis.read())!=-1) {
            System.out.println((char)ch);
        }
        //用数组来读取
        byte[] buf = new byte[1024];
        int len = 0;
        while((len=fis.read(buf))!=0) {
            System.out.println(new String(buf,0,len));
        }
        //用available()方法读
        byte[] buf = new byte[fis.available()];
        fis.read(buf);
        System.out.println(new String(buf));
    }
    public static void demo_write() {
        //创建字节输出流对象，用于操作文件
        FileOutputStream fos = new FileOutputStream("bytedemo.txt");
        //写数据，直接写入到目的地中
        fos.write("abc".getBytes());
    }
}
```
**字节流读取MP3练习**
```
public class CopyDemo {
    public static void main(String[] args) {
        copy_1();
        copy_2();
        copy_3();
    }
    //1024字节复制一次
    public static void copy_1() throws IOException {
        FileInputStream fis = new FileInputStream("c:\\0.mp3");
        FileOutputStream fos = new FileOutputStream("c:\\1.mp3");
        byte[] buf = new byte[1024];
        int len = 0;
        while((buf=fis.read())!=0) {
            System.out.println(new String(buf,0,len));
        }
    }
    //用Buffered的复制
    public static void copy_2() throws IOException {
        FileInputStream fis = new FileInputStream("c:\\0.mp3");
        BufferedInputStream bufis = new BufferedInputStream(fis);
        FileOutputStream fos = new FileOutputStream("c:\\1.mp3");
        BufferedOutputStream bufos = new BufferedOutputStream(fos);
        
        int ch = 0;
        while((ch=bufis.read())!=-1) {
            bufos.write(ch);
            bufos.flush();
        }
        bufos.close();
        bufis.close();
    }
    public static void copy_3() throws IOException {
        FileInputStream fis = new FileInputStream("c:\\0.mp3");
        FileOutputStream fos = new FileOutputStream("c:\\1.mp3");
        byte[] buf = new byte[fis.available()];
        fis.read(buf);
        fos.write(buf);
        fos.close();
        fis.close();
    }
}
```
#### IO流键盘输入

**键盘输入演示**
```
public class ReadKey {
    public static void main(String[] args) throws IOException {
        readKey1();
        readKey2();
    }
    public static void readKey1() throws IOException {
        //创建输入流对象
        InputStream in = System.in;
        //读取输入流对象的内容
        int ch = in.read();
        System.out.println(ch);
    }
    public static void readKey2() throws IOException {
        inputStream in = System.in;
        int ch = 0;
        while((ch=in.read()!=-1)) {
            System.out.println(ch);
        }
    }
}
```
**键盘录入转换成大写**  

获取用户键盘录入的数据，并且转换成大写显示在控制台上，exit退出录入  

思路

- 因为键盘录入只读取一个字节，要判断是否是over，需要将读取到的字节拼成字符串
- 需要一个容器StringBuilder来存储字符串
- 回车之前把录入的数据变成字符串判断
```
public class ReadKey {
    public static void main(String[] args) throws IOException {
        readKey();
    }
    获取用户键盘录入的数据，并且转换成大写显示在控制台上，exit退出录入
    public static void readKey() throws IOException {
        //创建容器
        StringBuilder sb = new StringBuilder();
        //获取键盘读取流
        inputStream in = System.in;
        //定义变量记录读取到的字节，循环获取
        int ch = 0;
        while((ch=in.read())!=-1) {
            if (ch=='\r')
                continue;
            if (ch=='\n') {
                String temp = sb.toString();
                    if("exit".equals(temp))
                        break;
                    System.out.println(temp.toUpperCase());
                    sb.delete(0,sb.length());
            } else {
                sb.append((char)ch);
            }
        }
    }
}
```
### 06-02-03 转换流

- **InputStreamReader** 
    - 字节流 --> 字符流
    - 字节 **解码**成 字符
- **OutputStreamWriter**
    - 字符流 --> 字节流
    - 字符 **编码**成 字节

**作用**

- **InputStreamReader**：把字节流解码成字符流，使其可以使用诸如readLine()之类的方法
- **OutputStreamWriter**：把字符流编码成字节流，进行输出

**转换关系**  

这两句代码功能相同  
FileWriter：相当于用了本机默认码表的转换流。是一个便捷类
```
InputStreamReader isr = new InputStreamReader(new FileInputStream("a.txt"),"GBK");  
FileReader fr = new FileReader("a.txt");
```

```
OutputStreamWriter osw = new OutputStreamWriter(new FileOutputStream("a.txt"))   
FileWriter fw = new FileWriter("a.txt");
```


**转换流实现键盘录入转换成大写**  

需求：键盘录入数据显示在控制台上
```
public class TransStreamDemo {
    public static void main(String[] args) throws IOException {
        /*
        字节流获取
        InputStream in = System.in; 
        字节流解码成字符流
        InputStreamReader isr new InputStreamReader(in);
        字符流装饰
        BufferedReader bufr = new BufferedReader(isr);
        */
        BufferedReader bufr = new BufferedReader(new InputStreamReader(System.in));
        
        /*
        字节流
        OutputStream out = System.out;
        字符流编码成字节流
        OutputStreamWriter osw = new OutputStreamWriter(out);
        字符流装饰
        BufferedWriter bufw = new BufferedWriter(osw);
        */
        BufferedWriter bufw = new BufferedWriter(new OutputStreamWriter(System.out));
        
        
        String line = null;
        while((line=bufr.readLine())!=null) {
            if("exit".equals(line))
                break;
            bufw.write(line.toUpperCase());
            bufw.newLine();
            bufw.flush();
        }
    }
}
```
需求：键盘录入数据写入一个文件中

```
BufferedReader bufr = new BufferedReader(new InputStreamReader(System.in));

BufferedWriter bufw = new BufferedWriter(new OutputStreamWriter(new FileOutputStream("a.txt"));
```
需求：文本文件内容显示在控制台上

```
BufferedReader bufr = new BufferedReader(new InputStreamReader(new FileInputStream("a.txt"));

BufferedWriter bufw = new BufferedWriter(new OutputStreamWriter(System.out);
```
需求：文本文件内容写入另一个文件中（复制）
```
BufferedReader bufr = new BufferedReader(new InputStreamReader(new FileInputStream("a.txt"));

BufferedWriter bufw = new BufferedWriter(new OutputStreamWriter(new FileOutputStream("b.txt"));
```

**转换关系**  

```
InputStreamReader isr = new InputStreamReader(new FileInputStream("a.txt"),"GBK");  
FileReader fr = new FileReader("a.txt");
```

```
OutputStreamWriter osw = new OutputStreamWriter(new FileOutputStream("a.txt"))   
FileWriter fw = new FileWriter("a.txt");
```
这两句代码功能相同   
FileWriter：相当于用了本机默认码表的转换流。是一个便捷类   
如果要用别的编码，必须使用转换流。   

用UTF-8写
```
OutputStreamWriter osw = new OutputStreamWriter(new FileOutputStream("a.txt"), "UTF-8");
```
用UTF-8读
```
InputStreamReader isr = new InputStreamReader(new FileInputStream("a.txt"), "UTF-8");  
```
**转换流使用场合**

- 源目对应的设备是字节流但是操作的确是文本数据，可以使用转换作为桥梁
- 操作文本需要用制定编码表时，必须使用转换流

### 06-02-04 IO流的操作规律 

**四个明确**

- 明确源和目的（汇）
    - 源
        - InputStream 字节流
        - Reader 字符流
    - 目的
        - OutputStream 字节流
        - Writer 字符流
- 明确数据是否是纯文本数据
    - 源
        - 是纯文本 Reader
        - 不是纯文本 InputStream
    - 目的
        - 是纯文本 Writer
        - 不是纯文本 OutputStream
- 明确据具体设备
    - 源
        - 硬盘：File
        - 键盘：System.in
        - 内存：数组
        - 网络：Socket流
    - 目的
        - 硬盘：File
        - 控制台：System.out
        - 内存：数组
        - 网络：Socket流
- 是否需要额外功能
    - 是否需要高效（Buffer）
    - 是否需要转换

**需求体现**  

**需求1：复制一个文本文件**

- 明确源目的
    - 源 InputStream Reader
    - 目的 OutputStream Writer
- 是否纯文本：是
    - 源：Reader
    - 目的：Writer
- 明确设备
    - 源：硬盘File
        - FileReader fr = new FileReader("a.txt");
    - 目的：硬盘File
        - FileWriter fw = new FileWriter("b.txt");
- 明确是否需要额外功能：需要高效
    - 源：
        - BufferedReader bufr = new BufferedReader(fr);
    - 目的：
        - BufferedWriter bufw = new BufferedWriter(fw);

**需求2 键盘录入数据，存入文件**

- 明确源目的
    - 源 InputStream Reader
    - 目的 OutputStream Writer
- 是否纯文本：是
    - 源：Reader
    - 目的：Writer
- 明确设备
    - 源：键盘 System.in
        - InputStream in = System.in;
    - 目的：硬盘 File
        - FileWriter fw = new FileWriter("b.txt");
- 明确是否需要额外功能：
    - 需要转换
        - 源：
            - InputStreamReader isr = new InputStreamReader(System.in);
        - 目的：
            - FileWriter fw = new FileWriter("b.txt");
    - 需要高效
        - 源：
            - BufferedReader bufr = new BufferedReader(new InputStreamReader(System.in));
        - 目的：
            - BufferedWriter bufw = new BufferedWriter(new FileWriter("b.txt"));

**需求3 读取文本文件显示在控制台上**

- 明确源目的
    - 源 InputStream Reader
    - 目的 OutputStream Writer
- 是否纯文本：是
    - 源：Reader
    - 目的：Writer
- 明确设备
    - 源：硬盘 File
        - FileReader fr = new FileReader("a.txt");
    - 目的：控制台 System.out
        - OutputStream out = System.out;
- 明确是否需要额外功能：
    - 需要转换
        - 源：
            - FileReader fr = new FileReader("a.txt");
        - 目的：
            - OutputStreamWriter osw = new OutputStreamWriter(System.out);
    - 需要高效
        - 源：
            - BufferedReader bufr = new BufferedReader(new FileReader("a.txt"));
        - 目的：
            - BufferedWriter bufw = new BufferedWriter(new OutputStreamWriter(System.out));

**需求4 键盘录入数据显示在控制台上**

- 明确源目的
    - 源 InputStream Reader
    - 目的 OutputStream Writer
- 是否纯文本：是
    - 源：Reader
    - 目的：Writer
- 明确设备
    - 源：控制台 System.in
        - InputStream in = System.in;
    - 目的：控制台 System.out
        - OutputStream out = System.out;
- 明确是否需要额外功能：中文一个字两个字节，所以需要转换成字符串操作
    - 需要转换
        - 源：
            - InputStreamReader isr = new InputStreamReader(System.in);
        - 目的：
            - OutputStreamWriter osw = new OutputStreamWriter(System.out);
    - 需要高效
        - 源：
            - BufferedReader bufr = new BufferedReader(new InputStreamReader(System.in));
        - 目的：
            - BufferedWriter bufw = new BufferedWriter(new OutputStreamWriter(System.out));

## 06-03 File类


**File类特点**

- 用来将文件或者文件夹封装成对象
- 方便对文件和文件夹的属性信息进行操作
- File对象可以作为参数传递给流的构造方法

**构造方法**  

- 传入一个字符串文件路径
```
File file1 = new File("c:\\a.txt");
```
- 传入一个字符串文件夹路径，一个文件名
```
File file2 = new File("c:\\", "a.txt");
```
- 传入一个文件对象，一个文件名
```
File f = new File("c:\\");
File file3 = new File(f, "a.txt");
```
分隔符的应用
```
File file4 = new File("c:"+File.separator+"abc"+File.separator+"a.txt");
```

```
public class FileDemo {
    public static void main(String[] args) {
        constructiorDemo()；
    }
    public static void constructiorDemo() {
        //可以将一个已存在的，或者不存在的文件或者目录封装成file对象
        File file1 = new File("c:\\a.txt");
        File file2 = new File("c:\\", "a.txt");
        File f = new File("c:\\");
        File file3 = new File(f, "a.txt");
        File file4 = new File("c:"+File.separator+"abc"+File.separator+"a.txt");
    }
}
```
#### 常用方法

- **获取**
    - 获取文件名称：getName()
    - 获取文件路径
        -  获取相对路径：getAbsolutePath()
        -  获取绝对路径：getPath()
    - 获取文件大小：getLength()
    - 获取文件修改时间：lastModified()
```
public static void getDemo() {
    File file = new File("a.txt");
    String name = file.getName(); a.txt
    
    String absPath = file.getAbsolutePath(); C:\abc\a.txt //绝对路径
    String path = file.getPath(); a.txt
    
    long len = file.length(); 123
    
    long time = file.lastModified(); 1236102144203
}
```
- **创建与删除**
    - 创建删除文件
        - boolean createNewFile()
            - 如果文件不存在，则创建
            - 如果文件存在，则不创建
        - boolean delete()
    - 创建删除文件夹
        - 创建单级目录
            - mkdir()
        - 创建多级目录
            - mkdirs()
        - 删除文件夹
            - boolean delete()
```
public static void createAndDeleteDemo() {
    File file = new File("file.txt");
    boolean a = file.createNewFile();
    System.out.println(a); true
    boolean b = file.delete();
    System.out.println(b); true
}
```
-  **判断**
    -  判断是否存在 isDemo()
    -  判断是否是文件 isFile()
    -  判断是否是文件夹 isDirectory()
```
public static void isDemo() {
    File file = new File("aa.txt");
    boolean b = file.exists();
    System.out.println(b);true
}
```
- **重命名**
    - renameTo();
```
public static void isDemo() {
    File file1 = new File("aa.txt");
    File file2 = new File("bb.txt");
    file1.renameTo(file2);
}
```
- **获取系统根目录**
    - listRoots();
```
public static void listRootsDemo() {
    File[] file1 = File.listRoots();
    for(File file : files) {
        System.out.println(file);
    }
}
```
- **获取容量**
    - getFreeSpace() 获取空闲空间 
    - getTotalSpace() 获取总空间 
    - getUsableSpace() 获取已用空间 

```
public static void getSpaceDemo() {
    File file = new File("d:\\");
    file.getFreeSpace();
    file.getTotalSpace();
    file.getUsableSpace();
}
```
- **获取目录**
    - String list()
        - file必须是一个目录
        - 否则发生NullPointerException
        - 访问系统级目录也会发生空指针异常
        - 如果目录没有内容，会返回一个数组，长度为0
        - 返回的是文件和文件夹名字
    - File listFiles()
        - 返回的是文件对象数组

```
public static void listDemo() {
    File file = new File("c:\\");
    String[] names = file.list();
    for(String name : names) {
        System.out.println(name);
    }
}
```
- **过滤器**

只要Java文件
```
public static void listDemo2() {
    File dir = new File("c:\\");
    String[] names = dir.list(new FilterByJava());
    for(String name : names) {
        System.out.println(name);
    }
}
public class FilterByJava implements FilenameFilter {
    @Override
    public boolean accept(File dir, String name) {
        return name.endsWith(".java");
    }
}
```
自定义过滤器
```
public static void listDemo2() {
    File dir = new File("c:\\");
    String[] names = dir.list(new FilterByJava());
    for(String name : names) {
        System.out.println(name);
    }
}
public class SurffixFilter implements FilenameFilter {
    private String suffix;
    public SurffixFilter(String suffix) {
        super();
        this.suffix = suffix;
    }
    @Override
    public boolean accept(File dir, String name) {
        return name.endsWith(".java");
    }
}
```
**深度遍历**  
列出所有文件和目录
```
public class FileTest {
    public static void main(String[] aregs) {
        File dir = new File("e:\\demodir");
        listAll(dir);
    }
    public static void listAll(File dir) {
        System.out.println(getSpace(level)+dir.getName());
        level++;
        File[] files = dir.listFiles();
        for(int x = 0; x<files.length; x++) {
            if(files[x].idDirectory()) {
                listAll(files[x]);
            } else {
                System.out.println(getSpace(level)+files[x].getName());
            }
        }
    }
    private static String getSpace(int level) {
        StringBuilder sb = new StringBuilder;
        for(int x = 0; x<level; x++) {
            sb.append("     ");
        }
        return sb.toString();
    }
}
```
删除所有文件和目录  
原理：从里往外删
```
public class FileDeleteTest {
    public static void main(String[] aregs) {
        File dir = new File("e:\\demodir");
        removeDir(dir);
    }
    public static void removeDir(File dir) {
        File[] files = dir.listFiles();
        for(File file : files) {
            if(file.isDirectory()) {
                removeDir(file);
            } else {
                file.delete();
            }
        }
        dir.delete();
    }
}
```
### 06-03-01 递归

**定义**：方法自身调用自身

**注意**：
- 递归一定要明确条件，否则容易栈溢出

转成二进制
```
public static void toBinary(int num) {
    if(num>0) {
        System.out.println(num%2);
        toBinary(num/2);
    }
0
1
1
}
```
```
public static void toBinary(int num) {
    if(num>0) {
        toBinary(num/2);
        System.out.println(num%2);
    }
1
1
0
}
```
求和
```
public static int getSum(int num) {
    if(num == 1)
        return 1;
    return num+getSum(num-1);
}
```
求和栈内存图解
```
int getNum(2 - 1) {
    if(1 == 1)
        return;                 1
    return 1 + getSum(1 - 1);
}
int getNum(3 - 1) {
    if(2 == 1)
        return;
    return 2 + getSum(2 - 1);   1+2
}
int getNum(4 - 1) {
    if(3 == 1)
        return;
    return 3 + getSum(3 - 1);   3+3
}
int getNum(5 - 1) {
    if(4 == 1)
        return;
    return 4 + getSum(4 - 1);   4+6
}
int getNum(5) {
    if(5 == 1)
        return;
    return 5 + getSum(5 - 1);   5+10
}
```

## 06-04 Properties集合
### 基本功能
- Map
    - Hashtable
        - **Properties**
    - HashMap
    - TreeMap

**Properties集合特点**：

- 集合中的Key和Value都是字符串类型
- 集合中的数据可以保存到流中，获取从流中获取数据

**Properties集合作用**：通常该集合用于操作该键值对形式存在的配置文件

- **一 存取功能**
    - setProperty
    - getProperty

```
public static void propertiesDemo() {
    //创建一个Properties集合
    Properties prop = new Properties();
    //储存元素
    prop setProperty("Kevin", 24);
    prop setProperty("Tony", 21);
    prop setProperty("Brian", 19);
    prop setProperty("Peter", 29);
    //取出元素
    Set<String> names = prop.stringPropertyName();
    for(String name : names) {
        String value = prop.getProperty(name);
        System.out.println(name+":"+value);
    }
}
```
- **二 list方法列出**
```
public static void propertiesDemo() {
    //创建一个Properties集合
    Properties prop = new Properties();
    //储存元素
    prop setProperty("Kevin", 24);
    prop setProperty("Tony", 21);
    prop setProperty("Brian", 19);
    prop setProperty("Peter", 29);
    //列出元素
    prop.list(System.out);
}
```
- **三 store方法存储**
```
public static void propertiesDemo() {
    //创建一个Properties集合
    Properties prop = new Properties();
    //储存元素
    prop setProperty("Kevin", 24);
    prop setProperty("Tony", 21);
    prop setProperty("Brian", 19);
    prop setProperty("Peter", 29);
    //储存到文件中
    FileOutputStream fos = new FileOutputStream("info.txt");
    prop.store(fos,"name+age");
    fos.close();
}
```
- **四 读取文件，输出到控制台**
```
public static void propertiesDemo() {
    //创建一个集合
    Properties prop = new Properties();
    //文件和输入流绑定
    FileInputStream fis = new FileInputStream("info2.txt");
    //把文件加载进集合
    prop.load(fis);
    //输出集合到控制台
    prop.list(System.out);
}
//模拟load方法
public static void myLoad() {
    Properties prop = new Properties();
    BufferedReader bufr = new BufferedReader(new FileReader("info.txt"));
    String line = null;
    while((line=bufr.readLine())!=null) {
        if(line.startsWith("#")) {
            continue;
        } else {
            String[] arr = line.split("=");
            prop.setProperty(arr[0], arr[1]);
        }
    }
    bufr.close();
}
```
- **五 对已有的配置文件进行修改**

思路

- 读取文件
- 把文件中的Key和Value数据存入集合
- 通过集合修改Key和Value数据
- 把修改后的数据存入文件
```
public static void propertiesDemo() {
    //文件封装成对象
    File file = new File("info.txt");
    //判断文件是否存在
    if(!file.exists()) {
        file.createNewFile();
    }
    
    //文件读取
    FileReader fr = new FileReader(file);
    //创建集合存储信息
    Properties prop = new Properties();
    //将流中信息存储到集合中
    prop.load(fr);
    //修改数据
    prop.setProperties("Kevin", "24");
    //文件和输出流绑定
    FileWriter fw = new FileWriter(file);
    //存储修改后的数据
    prop.store(fw,"");
    
    fw.close();
    fr.close();
}
```
#### 练习
练习一：获取一个应用程序的运行次数，如果超过5次，给出使用次数已到请注册的提示。并结束运行

思路
- 计数器：每次程序启动都计数一次
- 计数器不能随着程序的关闭而重置，所以储存在硬盘里
- 计数器原理
    - 程序启动时，先读取

```
public class PropertiesTest {
    public static void main (String[] args) {
        
    }
    public static void getAppCount() {
        File confile = new File("count.properties");
        if(!confile.exists()) {
            confile.createNewFile();
        }
        FileInputStream fis = new FileInputStream(confile);
        Properties prop = new Properties();
        prop.load(fis);
        
        //从集合中通过Key获取次数
        String value = prop.getProperty("time");
        //定义计数器，记录获取到的次数
        int count = 0;
        if(value!=null) {
            count = Integer.parseInt(value);
            if(count >= 5) {
                System.out.println("使用次数已到");
            }
        }
        count++;
        //改变后的次数重新存储到集合中
        prop.setProperty("time",count+"");
        
        FileOutputStream fos = new FileOutputStream(confile);
        fos.close();
        fis.close();
    }
}
```
练习二：建立一个制定扩展名的文件的列表

思路：

- 需要进行深度遍历
- 要在遍历的过程中进行过滤，将符合条件的内容存储到容器中
- 对容器中的内容进行遍历，并将绝对路径写入文件中

```
public class Test {

	/**
	 * @param args
	 * @throws IOException 
	 */
	public static void main(String[] args) throws IOException {
			
		File dir = new File("e:\\java0331");
		
		FilenameFilter filter = new FilenameFilter(){
			@Override
			public boolean accept(File dir, String name) {
				
				return name.endsWith(".java");
			}			
		};
		
		List<File> list = new ArrayList<File>();
		
		getFiles(dir,filter,list);
		
		File destFile = new File(dir,"javalist.txt");
		
		write2File(list,destFile);
		
	}
	/**
	 * 对指定目录中的内容进行深度遍历，并按照指定过滤器，进行过滤，
	 * 将过滤后的内容存储到指定容器List中。
	 * @param dir
	 * @param filter
	 * @param list
	 */
	public static void getFiles(File dir,FilenameFilter filter,List<File> list){
		
		File[] files = dir.listFiles();
		
		for(File file : files){
			if(file.isDirectory()){
				//递归啦！
				getFiles(file,filter,list);
			}else{
				//对遍历到的文件进行过滤器的过滤。将符合条件File对象，存储到List集合中。 
				if(filter.accept(dir, file.getName())){
					list.add(file);
				}
			}
		}
		
	}
	
	public static void write2File(List<File> list,File destFile)throws IOException{
		
		BufferedWriter bufw = null;
		try {
			bufw = new BufferedWriter(new FileWriter(destFile));
			for(File file : list){
				bufw.write(file.getAbsolutePath());
				bufw.newLine();
				bufw.flush();
			}
			
			
		} /*catch(IOException e){
			
			throw new RuntimeException("写入失败");
		}*/finally{
			if(bufw!=null)
				try {
					bufw.close();
				} catch (IOException e) {
					
					throw new RuntimeException("关闭失败");
				}
		}
	}

}
```
## 06-05 其他IO类
### 06-05-01 打印流


- PrintStream 字节
- PrintWriter 字符

装饰其它输出流。它能为其他输出流添加了功能，使它们能够方便地打印各种数据值表示形式。

#### PrintStream
**特点**：

- 提供了print方法，可以对多种数据类型值进行打印，并保持数据的表示形式
- 不抛出IOException

**构造方法**：能接收三种类型的值

- 字符串路径 (String fileName)
- File对象 (File file)
- 字节输出流 (OutputStream out)

**方法**

- write(97) 
    - 输出a：只写最低8位
- print(97) 
    - 输出97：把97变成字符保持原样将数据打印到目的地
```
public class PrintDemo {
    public static void main(String[] args) {
        PrintStream out = new PrintStream("print.txt");
        out.write(97); a
        out.print(97); 97
    }
}
```
#### PrintWriter
字符打印流

**构造方法**

- 字符串路径
- File对象
- 字节输出流
- 字符输出流

```
public class PrintWriterDemo {
    public static void main(String[] args) {
        BufferedReader bufr = new BufferedReader(new InputStreamReader(System.in));
        PrintWriter out = new PrintWriter(System.out);
        String line = null;
        while((line = bufr.readLine())!=null) {
            if("over".equals(line))
                out.println(line.toUpperCase());
                out.flush();
        }
        out.close();
        bufr.close();
    }
}
```
### 06-05-02 序列流
#### SequenceInputStream

**作用**：把其他输入流进行逻辑串联

**构造方法**

- SequenceInputStream(InputStream s1, InputStream s2)


低效率三个文件合成一个
```
public class SequenceInputStreamDemo {
    public static void main() {
        Vector<FileInputStream> v = new Vector<FileInputStream>)();
        
        v.add(new FileInputStream("1.txt"));
        v.add(new FileInputStream("2.txt"));
        v.add(new FileInputStream("3.txt"));
        
        Enumeration<FileInputStream> en = v.elements();
        
        SequenceInputStream sis = new SequenceInputStream(en);
        
        FileOutputStream fos = new FileOutputStream("4.txt");
        
        byte[] buf = new byte[1024];
        
        int len = 0;
        
        while((len=sis.read(buf))!=-1) {
            fos.write(buf,0,len);
        }
        fos.close();
        sis.close();
    }
}
```
高效率三个文件合成一个

```
public class SequenceInputStreamDemo {

	/**
	 * @param args
	 * @throws IOException 
	 */
	public static void main(String[] args) throws IOException {

		
		/*
		 * 需求：将1.txt 2.txt 3.txt文件中的数据合并到一个文件中。
		 */
		
//		Vector<FileInputStream> v = new Vector<FileInputStream>();		
//		v.add(new FileInputStream("1.txt"));
//		v.add(new FileInputStream("2.txt"));
//		v.add(new FileInputStream("3.txt"));
//		Enumeration<FileInputStream> en = v.elements();
		
		ArrayList<FileInputStream> al = new ArrayList<FileInputStream>();
		for(int x=1; x<=3; x++){
			al.add(new FileInputStream(x+".txt"));
		}
		
		Enumeration<FileInputStream> en = Collections.enumeration(al);
		
		
		
		/*
		final Iterator<FileInputStream> it = al.iterator();
		Enumeration<FileInputStream> en = new Enumeration<FileInputStream>(){

			@Override
			public boolean hasMoreElements() {
				
				return it.hasNext();
			}

			@Override
			public FileInputStream nextElement() {
				
				return it.next();
			}
			
		};*/
		
		SequenceInputStream sis = new SequenceInputStream(en);
		
		FileOutputStream fos = new FileOutputStream("1234.txt");
		
		byte[] buf = new byte[1024];
		
		int len = 0;
		
		while((len=sis.read(buf))!=-1){
			fos.write(buf,0,len);
		}
		
		fos.close();
		sis.close();
		
	}

}

```
#### 文件切割合并
**文件切割**

- 按照文件个数切
    - 切成固定等分
- 按照文件大小切
    - 切成固定大小
```
public class SplitFileDemo {
    private static final int SIZE = 1024*1024;
    public static void main(String[] args) {
        File file = new File("c:\\0.bmp");
        splitFile(file);
    }
    public static void splitFile(File file) {
        //读取流关联文件
        FileInputStream fis = new FileInputStream(file);
        //定义一个1M的缓冲区
        byte[] buf = new byte[SIZE];
        //创建目的
        FileOutputStream fos = null;
        
        int len = 0;
        int count = 1;
        
        File dir = new File("c:\\partfiles");
        if(!dir.exists())
            dir.mkdirs();
        
        while((len=fis.read(buf))!=-1) {
            fos = new FileOutputStream(new File((count++)+".part"));
            fos.write(buf,0,len);
        }
        fos.close();
        fis.close();
    }
}
```
**文件合并**

```
public class MergeFile {
    public static void static main(String[] args) {
        File dir = new File("c:\\partfiles");
        mergeFile(fir);
    }
}
public static void mergeFile(File dir) {
    ArrayList<FileInputStream> a1 = new ArrayList<FileInputStream>();
    
    for (int x = 1; x <= 3; x++) {
        a1.add(new FileInputStream(new File(dir, x+".part")));
    }
    
    SequenceInputStream sis = new SequenceInputStream(en);
    
    FileOutputStream fos = new FileOutputStream(new File(dir, "1.bmp"));
    
    byte[] buf = new byte[1024];
    
    int len = 0;
    while((len = fos.read(buf))!= -1) {
        fos.write(buf,0,len);
    }
    fos.close();
    sis.close();
}
```

**文件切割合并**


```
public class SplitFileDemo {
	private static final int SIZE = 1024 * 1024;
	/**
	 * @param args
	 * @throws Exception
	 */
	public static void main(String[] args) throws Exception {
		File file = new File("c:\\aa.mp3");
		splitFile_2(file);
	}
	private static void splitFile_2(File file) throws IOException {
		// 用读取流关联源文件。
		FileInputStream fis = new FileInputStream(file);
		// 定义一个1M的缓冲区。
		byte[] buf = new byte[SIZE];
		// 创建目的。
		FileOutputStream fos = null;
		int len = 0;
		int count = 1;
		/*
		 * 切割文件时，必须记录住被切割文件的名称，以及切割出来碎片文件的个数。 以方便于合并。
		 * 这个信息为了进行描述，使用键值对的方式。用到了properties对象
		 * 
		 */
		Properties prop  = new Properties();
		
		File dir = new File("c:\\partfiles");
		if (!dir.exists())
			dir.mkdirs();
		while ((len = fis.read(buf)) != -1) {
			fos = new FileOutputStream(new File(dir, (count++) + ".part"));
			fos.write(buf, 0, len);
			fos.close();
		}
		//将被切割文件的信息保存到prop集合中。
		prop.setProperty("partcount", count+"");
		prop.setProperty("filename", file.getName());
		fos = new FileOutputStream(new File(dir,count+".properties"));
		//将prop集合中的数据存储到文件中。 
		prop.store(fos, "save file info");
		fos.close();
		fis.close();
	}
}
	public static void mergeFile_2(File dir) throws IOException {
		/*
		 * 获取指定目录下的配置文件对象。
		 */
		File[] files = dir.listFiles(new SuffixFilter(".properties"));
		if(files.length!=1)
			throw new RuntimeException(dir+",该目录下没有properties扩展名的文件或者不唯一");
		//记录配置文件对象。
		File confile = files[0];
		

		//获取该文件中的信息================================================。
		
		Properties prop = new Properties();
		FileInputStream fis = new FileInputStream(confile);
		
		prop.load(fis);
		
		String filename = prop.getProperty("filename");		
		int count = Integer.parseInt(prop.getProperty("partcount"));

		//获取该目录下的所有碎片文件。 ==============================================
		File[] partFiles = dir.listFiles(new SuffixFilter(".part"));
		
		if(partFiles.length!=(count-1)){
			throw new RuntimeException(" 碎片文件不符合要求，个数不对!应该"+count+"个");
		}
		//将碎片文件和流对象关联 并存储到集合中。 
		ArrayList<FileInputStream> al = new ArrayList<FileInputStream>();
		for(int x=0; x<partFiles.length; x++){
			al.add(new FileInputStream(partFiles[x]));
		}
		//将多个流合并成一个序列流。 
		Enumeration<FileInputStream> en = Collections.enumeration(al);
		SequenceInputStream sis = new SequenceInputStream(en);
		
		FileOutputStream fos = new FileOutputStream(new File(dir,filename));
		
		byte[] buf = new byte[1024];
		
		int len = 0;
		while((len=sis.read(buf))!=-1){
			fos.write(buf,0,len);
		}
		fos.close();
		sis.close();
	}
```
### 06-05-03 ObjectStream


#### ObjectStream
- ObjectOutputStream
    - ObjectOutputStream把Java对象的基本数据类型和图形通过序列化的方式写入硬盘
- ObjectInputStream
    - ObjectInputStream可以通过反序列化的方式读取对象

**序列化**

- 对象通过**序列化**永久存储到硬盘，实现持久化

**反序列化**

- 通过反**序列化**读取硬盘上的对象进内存

**注意**

- 被序列化的对象的类必须实现**Serializable**接口
- Serializable是**标记接口**
- 一般扩展名为 **.object** 

```
public class ObjectStreamDemo {
    public static void main(String[] args) throws IOException {
        writeObj();
        readObj();
    }
    public static void writeObj() throws IOException, ClassNotFoundException {
        ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream("obj.object"));
        oos.writeObject(new Person("Steve", 30));
        oos.close();
    }
    public static void readObj() throws IOException {
        ObjectInputStream ois = new ObjectInputStream(new FileInpuStream("obj.object"));
        Person obj = (Person)ois.readObject();
        System.out.println(p.getName()+":"+p.getAge());
    }
}
```
#### Serializable接口
**作用**：用于给被序列化的类加入ID号（serialVersionUID）用于判断类和对象是否是同一版本

**注意**：如果不自定义UID，系统会默认使用UID，不过如果被序列化的对象的类被改变就会改变UID而导致无法被反序列化

**自定义ID号**

```
ANY-ACCESS-MODIFIER static final long serialVersionUID = 42L;
```

**transient关键字** transient修饰的非静态数据，不可以被序列化

### 06-05-04 RandomAccessFile类

**特点**

- 该对象可以**读写**
- 该对象内部维护了一个byte数组，并通过指针可以操作数组中的元素
- 可以通过**getFilePointer**方法获取指针的位置，通过**seek**方法设置指针的位置
- 该对象把**字节输出流**和**输入流**进行了**封装**
- 该对象的**源**和**目的**只能是**文件**

**常见方法**：

- 写入
    - 如果文件不存在，则创建
    - 如果文件存在，不创建

```
public class RandomAccessFileDemo {
    public static void main(String[] args) {
        writeFile();
    }
    //使用RandomAccessFile对象写入一些人员信息
    public static void writeFile() throws IOException {
        RandomAccessFile raf = new RandomAccessFile("ranacc.txt","rw");
        raf.write("Tony".getBytes());
        raf.write(97);
        raf.write("Steve".getBytes());
        raf.write(97);
        
        raf.close();
    }
    public static void readFile() throws IOException {
        RandomAccessFile raf = new RandomAccessFile("ranacc.txt","r");
        //通过seek设置指针位置
        ref.seek(1*8);//随机的读取，指定指针的位置即可
        
        byte[] buf = new byte[4];
        raf.read(buf);
        
        String name = new String(buf);
        int age = raf.readInt();
        
        System.out.println("name="+name);
        System.out.println("age="+age);
        
        raf.close();
    }
}
```

**随机写入**  
用seek方法设置写入位置
```
public static void randomWrite() throws IOException {
        RandomAccessFile raf = new RandomAccessFile("ranacc.txt","r");
        //从指定位置开始写入
        raf.seek(3*8);//从第三个八位开始写
        raf.write("Steve".getBytes());
        raf.writeInt(102);
        
        raf.close();
    }
```
### 06-05-05 管道流

PipedStream

- PipedInputStream
- PipedOutputStream


```
public class PipedStream {

	/**
	 * @param args
	 * @throws IOException 
	 */
	public static void main(String[] args) throws IOException {

		PipedInputStream input = new PipedInputStream();
		PipedOutputStream output = new PipedOutputStream();
		
		input.connect(output);
		
		new Thread(new Input(input)).start();
		new Thread(new Output(output)).start();
	}
}
class Input implements Runnable{
	private PipedInputStream in;
	Input(PipedInputStream in){
		this.in = in;
	}
	public void run(){
		try {
			byte[] buf = new byte[1024];
			int len = in.read(buf);
			
			String s = new String(buf,0,len);
			
			System.out.println("s="+s);
			in.close();
		} catch (Exception e) {
			// TODO: handle exception
		}
		
	}
}
class Output implements Runnable{
	private PipedOutputStream out;
	Output(PipedOutputStream out){
		this.out = out;
	}
	public void run(){
		try {
			Thread.sleep(5000);
			out.write("hi，管道来了！".getBytes());
		} catch (Exception e) {
			// TODO: handle exception
		}
	}
}
```
### 06-05-06 DataStream
操作基本数据类型的流对象

```
public class DataSteamDemo {
	/**
	 * @param args
	 * @throws IOException 
	 */
	public static void main(String[] args) throws IOException {
//		writeData();
		readData();
		
	}
	public static void readData() throws IOException {
		DataInputStream dis = new DataInputStream(new FileInputStream("data.txt"));
		
		String str = dis.readUTF();
		
		System.out.println(str);
	}
	public static void writeData() throws IOException {
		DataOutputStream dos = new DataOutputStream(new FileOutputStream("data.txt"));
		
		dos.writeUTF("你好");
		
		dos.close();
	}
}
```
### 06-05-07 操作数组的流
操作字节数组的流

- ByteArrayStream
    - ByteArrayInputStream
    - ByteArrayOutputStream

操作字符数组的流

- CharArrayReader
- CharArrayWriter

操作字符串

- StringReader
- StreamWriter

#### ByteArrayStream

```
public class ByteArrayStreamDemo {
	/**
	 * @param args
	 * @throws IOException 
	 */
	public static void main(String[] args) {
		ByteArrayInputStream bis = new ByteArrayInputStream("abcedf".getBytes());
		
		ByteArrayOutputStream bos = new ByteArrayOutputStream();
		
		int ch = 0;
		
		while((ch=bis.read())!=-1){
			bos.write(ch);
		}
		System.out.println(bos.toString());
	}
}
```
### 06-05-08 编码表

#### 常见的编码表
- ASCII：美国标准信息交换码
    - 用一个字节的7位可以表示
- ISO8859-1：欧洲码表
    - 用一个字节的8位表示
- GB2312：中国的中文编码表
- GBK：中国的中文编码表，融合了更多的中文符号
- Unicode：国际标准码表
    - 所有文字都用两个字节来表示，Java语言就是用的Unicode
- UTF-8：8-bit Unicode Transformation Format最多用**三个字节**表示一个字符

#### 简单的编码解码
- 字符串 --> 字节数组 编码
- 字节数组 --> 字符串 解码

```
public class EncodeDemo {
    public static void main(String[] args) {
        String str = "你好";
        //你好：GBK -60 -29 -70 -61
        //你好：UTF-8 -28 -67 -96 -27 -91 -67
        //编码
        byte[] buf = str.getBytes(“utf-8”);
        printBytes(buf);
        //解码
        String s1 = new String(buf);
    }
    
    private static vodi printBytes(byte[] buf) {
        for(byte b : buf) {
            System.out.println(b);
        }
    }
}
```

```
public class EncodeDemo {
    public static void main(String[] args) throws IOException {
	        /*
	         * 字符串 --> 字节数组：编码。
		 * 字节数组 --> 字符串：解码。
		 * 
		 * 你好：GBK:  -60 -29 -70 -61
		 * 
		 * 你好: utf-8: -28 -67 -96 -27 -91 -67 
		 * 
		 * 如果你编错了，解不出来。
		 * 如果编对了，解错了，有可能有救。
		 */
		String str = "谢谢";
		
		byte[] buf = str.getBytes("GBK");//用GBK编码
		String s1 = new String(buf,"UTF-8");//用UTF-8解码
		System.out.println("s1="+s1);//解码失败，用特殊编码表示原来的编码
		byte[] buf2 = s1.getBytes("UTF-8");//获取源字节.
		printBytes(buf2);
		
		String s2 = new String(buf2,"GBK");//用GBK解码
		System.out.println("s2="+s2);//有可能可以解码
//		encodeDemo(str);
	}
	/**
	 * @param str
	 * @throws UnsupportedEncodingException
	 */
	public static void encodeDemo(String str)
			throws UnsupportedEncodingException {
		//编码；
		byte[] buf = str.getBytes("UTF-8");
//		printBytes(buf);
		//解码：
		String s1 = new String(buf,"UTF-8");
		System.out.println("s1="+s1);
	}
	private static void printBytes(byte[] buf) {
		for(byte b : buf){
			System.out.print(b +" ");
		}
	}
}
```
**联通问题**  
联通这两个字的UTF-8和GBK的编码一样，所以导致GBK编码的联通系统会自动用UTF-8解码，导致乱码
```
public class LianTong {
    public static void main(String[] args) throws IOException {
	String str = "联通";
	/*
	11000001
	10101010
	11001101
	10101000
	*/
	byte[] buf = str.getBytes("gbk");
	for(byte b :buf){
	    System.out.println(Integer.toBinaryString(b&255));
	}
    }
}
```
**按字节截取字符串**  

在java中，字符串“abcd”与字符串“ab你好”的长度是一样，都是四个字符。但对应的字节数不同，一个汉字占两个字节。  
**定义一个方法**，按照最大的字节数来取子串。如：对于“ab你好”，如果取三个字节，那么子串就是ab与“你”字的半个，那么半个就要舍弃。如果去四个字节就是“ab你”，取五个字节还是“ab你”.

```
public class Test {
	/**
	 * @param args
	 * @throws IOException 
	 */
	public static void main(String[] args) throws IOException {
		String str = "ab你好cd谢谢";
//		str = "ab琲琲cd琲琲";
//		int len = str.getBytes("gbk").length;		
//		for(int x=0; x<len; x++){
//			System.out.println("截取"+(x+1)+"个字节结果是："+cutStringByByte(str, x+1));
//		}
		int len = str.getBytes("utf-8").length;		
		for(int x=0; x<len; x++){
			System.out.println("截取"+(x+1)+"个字节结果是："+cutStringByU8Byte(str, x+1));
		}
//		String str = "琲";
//		byte[] buf = str.getBytes("gbk");
//		for(byte b : buf){
//			System.out.println(b);//-84  105 
//		}
	}
	/*
	  	
	 */
	public static String cutStringByU8Byte(String str, int len) throws IOException {
		byte[] buf = str.getBytes("utf-8");
		int count = 0;
		for(int x=len-1; x>=0; x--){
			if(buf[x]<0)
				count++;
			else
				break;
		}
		if(count%3==0)
			return new String(buf,0,len,"utf-8");
		else if(count%3==1)
			return new String(buf,0,len-1,"utf-8");
		else 
			return new String(buf,0,len-2,"utf-8");
		
	}
	public static String cutStringByByte(String str,int len) throws IOException{
		
		byte[] buf = str.getBytes("gbk");
		
		int count = 0;
		for(int x=len-1; x>=0; x--){
			if(buf[x]<0)
				count++;
			else
				break;
		}
		if(count%2==0)
			return new String(buf,0,len,"gbk");
		else
			return new String(buf,0,len-1,"gbk");
	}
}

```
# 07 Java SE GUI

## 07-01 GUI概述
GUI

- Graphical User Interface（图形用户接口）
- 特点：
    - 更直观

CLI

- Command Line User Interface（命令行用户接口）
- 特点
    - 不直观

Java为GUI提供对象的两个包

- java.awt
    - Abstract Window Toolkit：抽象窗口工具包，调用本地系统方法实现功能
    - 重量级控件
- javax.swing
    - 完全由Java实现，提供更多组件，移植性强
    - 轻量级控件

### 继承关系

- Component：组件
    - Container：容器
        - Window：窗体，可以独立存在
            - Frame：框架
            - Dialog：对话框
                - FileDialog：文件对话框
        - Panel：面板，窗体中的一部分，不可以独立存在
    - Button：按钮
    - Label：标签
    - Checkbox：复选框
    - TextComponent：文本组件
        - TextArea：文本区域
        - TextField：文本框

Container：为容器，一个特殊组件，通过add方法添加其他组件  

### 布局  

- FlowLayout（流式布局）
    - 从左到右顺序排列
    - Panel默认的布局
- BorderLayout（边界布局）
    - 东南西北中
    - Frame默认的布局
- GridLayout（网格布局）
    - 规则的矩阵
- CardLayout（卡片布局）
    - 选项卡
- GridBagLayout（网络包布局）
    - 非规则的矩阵

### Frame演示

```
public class FrameDemo {
    public static void main(String[] args) {
        Frame f = new Frame("my frame");
        
        //f.setSize(500, 400);
        //f.setLocation(400, 200);
        f.setBounds(400, 200, 500, 400);
        
        f.setLayout(new FlowLayout());//设置流式布局
        
        Button but = new Button("一个按钮");
        f.add(but);
        
        f.setVisible(true);
        System.out.println("over");
    }
}
```
## 07-02 事件监听

- 事件源（组件）
- 事件（Event）
- 监听器（Listener）
- 事件处理（引发事件后的处理方式）

监听器

- WindowListener
    - windowClosing() 关闭窗口
- ActionListener
    - actionPerformed()
- MouseListener
    - mouseEntered() 鼠标移到按钮就触发，不需要点击
    - mouseClicked() 鼠标单击触发
- KeyListener
    - keyPressed()

**AWT**
```
public class FrameDemo {
    public static void main(String[] args) {
        Frame f = new Frame("my frame");
        
        //f.setSize(500, 400);
        //f.setLocation(400, 200);
        f.setBounds(400, 200, 500, 400);
        f.setLayout(new FlowLayout());//设置流式布局
        
        TextFiled tf = new TextField(35);
        Button but = new Button("一个按钮");
        f.add(tf);
        f.add(but);
        //窗口上加一个监听
        f.addWindowListener(new WindowAdapter() {
            @Override
            public void windowClosing(WindowEvent e) {
                super.windowClosing(e);//处理方式
                System.exit(0);
            }
        });
        //按钮上加一个监听
        buf.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(Action e) {
                System.out.println("Run");
            }
        })
        //按钮上加一个鼠标监听
        buf.addMouseListener(new MouseListener() {
            /*
            @Override
            public void MouseEntered(MouseEvent e) {
               System.out.println("Run");//鼠标移到按钮上就会触发
            }
            */
            @Override
            public void mouseClicked(MouseEvent e) {
                if(e.getClickCount()==2) {
                    tf.setText("double click"+count++);
                }
            }
        })
        //文本框添加键盘监听
        tf.addKeyListener(new KeyAdapter() {
            public void keyPressed(KeyEvent e) {
                System.out.println("key run");
                
            }
        })
        f.setVisible(true);
        System.out.println("over");
    }
}
```
**SWING**

```
public class MySwing extends javax.swing.JFrame {
	private JButton jButton1;

	/**
	* Auto-generated main method to display this JFrame
	*/
	public static void main(String[] args) {
		SwingUtilities.invokeLater(new Runnable() {
			public void run() {
				MySwing inst = new MySwing();
				inst.setLocationRelativeTo(null);
				inst.setVisible(true);
			}
		});
	}
	
	public MySwing() {
		super();
		initGUI();
	}
	
	private void initGUI() {
		try {
			getContentPane().setLayout(null);
			setDefaultCloseOperation(WindowConstants.DISPOSE_ON_CLOSE);
			{
				jButton1 = new JButton();
				getContentPane().add(jButton1);
				jButton1.setText("\u9000\u51fa");
				jButton1.setBounds(142, 26, 103, 48);
				jButton1.addActionListener(new ActionListener() {
					public void actionPerformed(ActionEvent evt) {
						jButton1ActionPerformed(evt);
					}
				});
			}
			pack();
			setSize(400, 300);
		} catch (Exception e) {
		    //add your error handling code here
			e.printStackTrace();
		}
	}
	
	private void jButton1ActionPerformed(ActionEvent evt) {
//		System.out.println("jButton1.actionPerformed, event="+evt);
		//TODO add your code for jButton1.actionPerformed
		
		System.exit(0);
	}

}

```
**菜单练习**

```
public class MyMenu extends javax.swing.JFrame {
	private static final String LINE_SEPARATOR = System.getProperty("line.separator");
	private JMenuBar jMenuBar1;
	private JScrollPane jScrollPane1;
	private JMenuItem jMenuItem2;
	private JTextArea jTextArea1;
	private JMenuItem jMenuItem1;
	private JMenu jMenu1;
	private JFileChooser chooser;
	private JDialog dialog;

	/**
	* Auto-generated main method to display this JFrame
	*/
	public static void main(String[] args) {
		SwingUtilities.invokeLater(new Runnable() {
			public void run() {
				MyMenu inst = new MyMenu();
				inst.setLocationRelativeTo(null);
				inst.setVisible(true);
			}
		});
	}
	
	public MyMenu() {
		super();
		initGUI();
	}
	
	private void initGUI() {
		try {
			setDefaultCloseOperation(WindowConstants.EXIT_ON_CLOSE);
			{
				jScrollPane1 = new JScrollPane();
				getContentPane().add(jScrollPane1, BorderLayout.CENTER);
				{
					jTextArea1 = new JTextArea();
					jScrollPane1.setViewportView(jTextArea1);
				}
			}
			{
				jMenuBar1 = new JMenuBar();
				setJMenuBar(jMenuBar1);
				{
					jMenu1 = new JMenu();
					jMenuBar1.add(jMenu1);
					jMenu1.setText("\u6587\u4ef6");
					{
						jMenuItem1 = new JMenuItem();
						jMenu1.add(jMenuItem1);
						jMenuItem1.setText("\u6253\u5f00");
						jMenuItem1.addActionListener(new ActionListener() {
							public void actionPerformed(ActionEvent evt) {
								try {
									jMenuItem1ActionPerformed(evt);
								} catch (IOException e) {
									
									e.printStackTrace();
								}
							}
						});
					}
					{
						jMenuItem2 = new JMenuItem();
						jMenu1.add(jMenuItem2);
						jMenuItem2.setText("\u4fdd\u5b58");
						jMenuItem2.addActionListener(new ActionListener() {
							public void actionPerformed(ActionEvent evt) {
								try {
									jMenuItem2ActionPerformed(evt);
								} catch (IOException e) {
									
									e.printStackTrace();
								}
							}
						});
					}
				}
			}
			pack();
			this.setSize(610, 402);
		} catch (Exception e) {
		    //add your error handling code here
			e.printStackTrace();
		}
	}
	
	private void jMenuItem1ActionPerformed(ActionEvent evt) throws IOException {
		
		
		chooser = new JFileChooser();
	
//		    FileNameExtensionFilter filter = new FileNameExtensionFilter(
//		        "JPG & GIF Images", "jpg", "gif");
//		    chooser.setFileFilter(filter);
		    
		    
		int returnVal = chooser.showOpenDialog(this);
		if(returnVal == JFileChooser.CANCEL_OPTION){
			System.out.println("没有选取文件，取消了");
			return;
		}
		    
		File file = chooser.getSelectedFile();
		
		
		
		BufferedReader bufr = new BufferedReader(new FileReader(file));
			
		String line = null;
		while((line=bufr.readLine())!=null){
			jTextArea1.append(line+LINE_SEPARATOR);
		}
			
		bufr.close();

	}
	
	private void jMenuItem2ActionPerformed(ActionEvent evt) throws IOException {
		
		chooser = new JFileChooser();
		int returnVal = chooser.showSaveDialog(this);
		if(returnVal == JFileChooser.CANCEL_OPTION){
			System.out.println("没有指定文件，取消了");
			return;
		}
		
		File file = chooser.getSelectedFile();
		
		String text = jTextArea1.getText();
		
		BufferedWriter bufw = new BufferedWriter(new FileWriter(file));
		bufw.write(text);
		bufw.close();
		
	}

}

```
# 08 Java SE 网络编程

## 08-01 网络模型概述

**网络模型**

- OSI（Open System Interconnection）开放系统互联参考模型
    - 应用层
        - 终端应用
    - 表示层
        - 把计算机能识别的东西表示成人能识别的东西
    - 会话层
        - 在系统之间发起会话，会话请求
    - 传输层
        - 定义传输协议和端口号
            - TCP（传输控制协议）
                - 传输效率低
                - 可靠性强
                - 传输数据量大的数据
            - UDP（用户数据报协议）
                - 可靠性低
                - 传输数据量小的数据
        - 这一层数据叫：段
    - 网络层
        - IP地址的封装和解封装
        - 这一层数据叫：数据包
        - 这一层设备是：路由器
    - 数据链路层
        - MAC地址的封装和解封装
        - 这一层数据叫：帧
        - 这一层设备是：交换机
    - 物理层
        - 定义物理设备标准
        - 作用是传输比特流
        - 这一层数据叫：比特

- TCP/IP参考模型
    - 应用层：数据段
    - 传输层：数据包
    - 网际互连层：数据帧
    - 网络接入层：比特

**网络通讯要素**

- IP地址
    - 网络中设备的标识
    - 本地回环地址：127.0.0.1   主机名：localhost
- 端口号
    - 用于标识进程的逻辑地址
    - 有效端口：0 - 65535
    - 系统保留端口：0 - 1024
- 传输协议
    - 通讯的规则
    - 常见协议
        - TCP（传输控制协议）
            - 建立链接，形成传输数据的通道
            - 在连接中进行大数据量传输
            - 通过三次握手完成连接，所以**可靠**
                - Client：Server 帮个忙噻
                - Server：干什么噻
                - Client：那就谢谢了
            - 因为要连接，所以**速度慢**
            - 类似**电话**
        - UDP（用户数据报协议）
            - 数据和源目封装成数据包，不需要建立连接
            - 每个数据报文限制在64k内
            - 因为无连接，所以**不可靠**
            - 因为无连接，所以**速速快**
            - 类似**对讲机**

**InetAddress类**  

**作用**：InetAddress类表示互联网协议（IP）地址


```
public class IPDemo {
    public static void main(String[] args) {
        //获取本地主机ip地址对象
        InetAddress ip = InetAddress.getLocalHost();
        //获取其他主机ip地址对象
        ip = InetAddress.getByName("192.168.1.100");
        
        System.out.println(ip.getHostAddress());
        System.out.println(ip.getHostName());
        
    }
}
```

## 08-02 TCP和UDP协议

**Socket** 

- Socket就是为网络服务提供的一种机制
- 通信的两段都有Socket
- 网络通信其实就是Socket间的通信
- 数据在两个Socket间通过IO传输

### UDP协议

**UDP协议发送端**  

创建UDP发送端思路
- 建立UDP的socket服务
- 将要发送的数据封装到数据包中
- 通过UDP的socket服务将数据包发送出去
- 关闭socket服务
```
public class UDPSendDemo {
    public static void main(String[] args) {
        //1.建立UDP的socket服务
        DatagramSocket ds = new DatagramSocket();
        //2.将要发送的数据封装到数据包中
        String str = "UDP transmitting";
            //用DatagramPacket将数据封装到该对象中
        byte[] buf = str.getBytes();
        DatagramPacket dp = new DatagramPacket(buf,buf.length,InetAddress.getByName("192.168.0.100"),10000);
        //3.通过UDP的Socket服务将数据包发送出去
        ds.send(dp);
        //4.关闭socket服务
        ds.close();
    }
}
```
**UDP协议接收端**  

创建UDP接收端思路：

- 建立UDP的socket服务，必须明确端口号
- 将要接受的数据存储到数据包中
- 用socket的receive方法接收数据，存储到数据包中
- 通过数据包的方法解析数据包中的数据
- 关闭socket服务
```
public class UDPReceiveDemo {
    public static void main(String[] args) {
        //1.建立UDP的socket服务
        DatagramSocket ds = new DatagramSocket(10000);
        //2.创建数据包
        byte[] buf = new byte[1024];
        DatagramPacket dp = new DatagramPacket(buf, buf.length);
        //3.使用接收方法将数据存储到数据包中
        ds.receive(dp);  
        //4.通过数据包方法解析数据
        String ip = dp.getAddress().getHostAddress();
        int port = dp.getPort();
        String text = new String(dp.getData(),0,dp.getLength());
        
        System.out.println(ip+":"+port+":"+text);
        //5.关闭资源
        ds.close();
}
```
**聊天程序**
```
public class UDPSendDemo {
    public static void main(String[] args) {
        //1.建立UDP的socket服务
        DatagramSocket ds = new DatagramSocket(8888);
        //2.将要发送的数据封装到数据包中
        //String str = "UDP transmitting";
        BufferedReader bufr = new BufferedReader(new InputStreamReader(System.in));
        String line = null;
        
        while((line=bufr.readLine())!=null) {
            if("over".equals(line))
                break;
            byte[] buf = line.getBytes();
            //用DatagramPacket将数据封装到该对象中
            DatagramPacket dp = new DatagramPacket(buf,buf.length,InetAddress.getByName("192.168.0.100"),10000);
            //3.通过UDP的Socket服务将数据包发送出去
            ds.send(dp);
        }
        
        //4.关闭socket服务
        ds.close();
    }
}
```
```
public class UDPReceiveDemo {
    public static void main(String[] args) {
        //1.建立UDP的socket服务
        DatagramSocket ds = new DatagramSocket(10000);
        while(true) { //持续接收数据
            byte[] buf = new byte[1024];
            DatagramPacket dp = new DatagramPacket(buf, buf.length);
            //3.使用接收方法将数据存储到数据包中
            ds.receive(dp);  
            //4.通过数据包方法解析数据
            String ip = dp.getAddress().getHostAddress();
            int port = dp.getPort();
            String text = new String(dp.getData(),0,dp.getLength());
            
            System.out.println(ip+":"+port+":"+text);
        }
        //2.创建数据包

        //5.关闭资源
        //ds.close();
}
```
多线程实现的聊天程序
```
public class ChatDemo {
	/**
	 * @param args
	 * @throws IOException 
	 */
	public static void main(String[] args) throws IOException {
		DatagramSocket send = new DatagramSocket();
		DatagramSocket rece = new DatagramSocket(10001);
		new Thread(new Send(send)).start();
		new Thread(new Rece(rece)).start();
	}
}
public class Rece implements Runnable {
	private DatagramSocket ds;
	public Rece(DatagramSocket ds) {
		this.ds = ds;
	}
	@Override
	public void run() {
		try {
			while (true) {

				byte[] buf = new byte[1024];
				DatagramPacket dp = new DatagramPacket(buf, buf.length);

				ds.receive(dp);

				String ip = dp.getAddress().getHostAddress();
				int port = dp.getPort();
				String text = new String(dp.getData(), 0, dp.getLength());
				
				System.out.println(ip + "::" + text);
				if(text.equals("886")){
					System.out.println(ip+"");
				}
			}
		} catch (Exception e) { }
	}
}
public class Send implements Runnable {
	private DatagramSocket ds;
	public Send(DatagramSocket ds){
		this.ds = ds;
	}
	@Override
	public void run() {
		try {
			BufferedReader bufr = new BufferedReader(new InputStreamReader(System.in));
			String line = null;
			while((line=bufr.readLine())!=null){
				byte[] buf = line.getBytes();
				DatagramPacket dp = new DatagramPacket(buf,buf.length,InetAddress.getByName("192.168.1.255"),10001);
				ds.send(dp);
				if("886".equals(line))
					break;
			}
			ds.close();
		} catch (Exception e) {}
	}
}
```
### TCP协议

**概述**

- Socket和ServerSocket
- 建立客户端和服务端
- 建立连接后，通过Socket中的IO流进行数据的传输
- 关闭Socket

**客户端**  

建立客户端思路
- 创建TCP客户端Socket服务
    - 使用Socket对象
    - 建议该对象已创建就明确目的地，要连接的主机
- 如果连接建立成功，说明数据传输通道已建立
    - 通道就是Socket流，包含输入输出
    - 通过Socket来获取输入输出对象
    - 通过getOutputStream()和getInputStream()来获取输入输出字节流
- 使用输出流，发送到服务器
- 关闭资源
```
public class ClientDemo {
    public static void main(String[] args) {
        //1.创建客户端socket服务
        Socket socket = new Socket("192.168.1.100", 10002);
        //2.获取socket流中的输出流
        OutputStream out = socket.getOutputStream();
        //3.使用输出流将制定的数据写出去
        out.write("TCP transmitting".getBytes());
        //4.关闭资源
        socket.close();
    }
}
```
**服务端**  

建立服务端思路
- 创建TCP服务端Socket服务
    - 使用ServerSocket对象
        - 服务端必须对外提供一个端口，否则客户端无法连接
- 获取连接过来的客户端对象
- 通过客户端对象获取socket流读取客户端发来的数据
- 关闭资源（客户端，服务端资源都要关闭）
```
public class ServerDemo {
    public static void main(String[] args) {
        //1.创建服务端socket服务
        ServerSocket ss = new ServerSocket(10002);
        //2.获取连接过来的客户端对象
        Socket s = ss.accept();
        String ip = s.getInetAddress().getHoustAddress();
        //3.通过Socket对象读取输入流，读取客户端发来的数据
        InputStream in = s.getInputStream();
        byte[] buf = new byte[1024];
        int len = in.read(buf);
        String text = new String(buf,0,len);
        System.out.println("server:"+text);
        //4.关闭客户端，关闭服务端
        s.close();
        ss.close();
    }
}
```

**客户端服务端交互**

```
public class ClientDemo {
    public static void main(String[] args) {

        //1.创建客户端socket服务
        Socket socket = new Socket("192.168.1.100", 10002);
        //2.获取socket流中的输出流
        OutputStream out = socket.getOutputStream();
        //3.使用输出流将制定的数据写出去
        out.write("TCP transmitting".getBytes());
        //读取服务端返回的数据，使用socket读取流
        InputStream in = socket.getInputsStream();
        byte[] buf = new byte[1024];
        int len = in.read(buf);
        String text = new String(buf,0,len);
        System.out.println(text);
        //4.关闭资源
        socket.close();
    }
}
```
```
public class ServerDemo {
    public static void main(String[] args) {
        //1.创建服务端socket服务
        ServerSocket ss = new ServerSocket(10002);
        //2.获取连接过来的客户端对象
        Socket s = ss.accept();
        String ip = s.getInetAddress().getHoustAddress();
        //3.通过Socket对象读取输入流，读取客户端发来的数据
        InputStream in = s.getInputStream();
        byte[] buf = new byte[1024];
        int len = in.read(buf);
        String text = new String(buf,0,len);
        System.out.println(ip+":"+text);
        //使用客户端Socket对象的输出流给客户端返回数据
        OutputStream out = s.getOutpuStream();
        out.write("Roger that".getBytes());
        //4.关闭客户端，关闭服务端
        s.close();
        ss.close();
    }
}
```
**文本转换**  

客户端思路

- 创建socket客户端对象
- 获取键盘录入
- 将录入的信息发送给socket输出流

```
public class TransClient {
    public static void main(String[] args) {
        //1.创建socket客户端对象
        Socket s = new Socket("192.168.1.100",10004);
        //2.获取键盘输入
        BufferedReader bufr = new BufferedReader(new InputStreamReader(System.in));
        //3.socket输出流
        //new BufferedWriter(new OutputStreamWriter(s.getOutputStream));
        PrintWriter out = new PrintWriter(s.getOutputStream(),true);
        //4.socket输入流，读取服务端返回的大写数据
        BufferedReader bufIn  = new BufferedReader(new InputStreamReader(s.getInputStream()));
        String line = null;
        while((line=bufr.readLine())!=null) {
            if("over".equals(line))
                break;
            out.println(line);
            //读取服务器发回的一行大写数据
            String upperStr = bufIn.readLine();
            System.out.println(upperStr);
        }
        s.close();
    }
}
```
服务端思路

- ServerSocket服务
- 获取Socket对象
- 源：socket，读取客户端发过来的需要转换的数据
- 目的：显示在控制台上
- 转换成大写发送给客户端
```
public class TransServer {
    public static void main(String[] args) {
        //1.ServerSocket服务
        ServerSocket ss = new ServerSocket(10004);
        //2.获取socket对象
        Socket s = ss.accept();
        //获取IP
        String ip = s.getInetAddress().getHostAddress();
        System.out.println(ip+"......connected");
        //3.获取socket读取流并装饰
        BufferedReader bufIn = new BufferedReader(new InputStreamReader(s.getInputStream()));
        //4.获取socket输出流并装饰
        PrintWriter out = new PrintWriter(s.getOutputStream(),true);
        
        String line = null;
        while((line=bufIn.readLine())!=null){
            System.out.println(line);
            out.println(line.toUpperCase());
            //out.print(line.toUpperCase()+"\r\n");
            //out.flush();
    }
    s.close();
    ss.close();
}
```
**上传文本文件**

```
public class UploadClient {
    public static void main(String[] args) {
        Socket s = new Socket("192.168.1.100",10005);
        BufferedReader bufr = new BufferedReader(new FileReader("client.txt"));
        PrintWriter out = new PrintWriter(s.getOutputStream(),true);
        String line = null;
        while((line=bufr.readLine())!=null) {
            out.println(line);
        }
        //告诉服务端，客户端写完了
        s.shutdownOutput();
        //out.println("over");
        BufferedRedaer bufIn = new BufferedReader(new InputStreamReader(s.getInputStream()));
        String str = bufIn.readLine();
        System.out.println(str);
        
        bufr.close();
        s.close();
    }
}
```
```
public class UploadServer {
    public static void main(String[] args) {
        ServerSocket ss = new ServerSocket(10005);
        Socket s = ss.accept();
        System.out.println(s.getInetAddress().getHostAddress()+"...connected");
        BufferedReader bufIn = new BufferedReader(new InputStreamReader(s.getInputStream()));
        
        BufferedWriter bufw = new BufferedWriter(new FileWriter("server.txt"));
        
        String line = null;
        while((line=bufIn.readLine())!=null) {
            if("over".equals(line))
                break
            bufw.write(line);
            bufw.newLine();
            bufw.flush();
        }
        PrintWriter out = new PrintWriter(s.getOutputStream(),true);
        out.println("upload complete");
        
        bufw.close();
        s.close();
        ss.close();
    }
}
```
**上传图片**

```
public class UploadPicClient {
    public static void main(String[] args) throws UnknownHostException, IOException {
        //1,创建客户端socket。
        Socket s = new Socket("192.168.1.100",10006);
        //2,读取客户端要上传的图片文件。
        FileInputStream fis = new FileInputStream("c:\\0.bmp");
        //3,获取socket输出流，将读到图片数据发送给服务端。
        OutputStream out = s.getOutputStream();
        byte[] buf = new byte[1024];
        int len = 0;
        while((len=fis.read(buf))!=-1){
            out.write(buf,0,len);
        }
        //告诉服务端说：这边的数据发送完毕。让服务端停止读取。
        s.shutdownOutput();
        //读取服务端发回的内容。
        InputStream in  = s.getInputStream();
        byte[] bufIn = new byte[1024];
        int lenIn = in.read(buf);
        String text = new String(buf,0,lenIn);
        System.out.println(text);
        fis.close();
        s.close();
	}
}
```

```
public class UploadPicServer {
    public static void main(String[] args) throws IOException {
        //创建tcp的socket服务端。
        ServerSocket ss = new ServerSocket(10006);
        //获取客户端
        while(true) {
            Socket s = ss.accept();
            new Thread(new UploadTask(s)).start();
        }
        

        //ss.close();
    }
}

public class UploadTask implements Runnable {
    private Socket s;
    private UploadTask(Socket s) {
        this.s = s;
}
    @Override
    public void run() {
        int count = 0;
        String ip = s.getInetAddress().getHostAddress();
        System.out.println(ip+"...connected");
        //读取客户端发来的数据
        try {
            InputStream in = s.getInputStream();
            //将读取到数据存储到一个文件中
            File dir = new File("c:\\pic");
            if(!dir.exists()) {
                dir.mkdirs();
            }
            File file = new File(dir,ip+".jpg");
            if(file.exists()) {
                file = new File(dir,ip+"("+(++count)+").jpg");
            }
            FileOutputStream fos = new FileOutputStream(file);
            byte[] buf = new byte[1024];
            
            int len = 0;
            
            while((len=in.read(buf)!=-1)) {
                fos.write(buf,0,len);
            }
            //获取socket输出流，把文件发送给客户端
            OutputStream out = s.getOutputStream();
            out.wirte("upload complete".getBytes());
            
            fos.close();
            s.close();
        } catch (IOException e) {}

    }
}
```
## 08-03 网络编程其他

### 常见客户端和服务端

常见的客户端

- 浏览器
    - Chrome，Edge，Firefox

常见的服务端

- 服务器
    - Tomcat

### 自定义客户端和服务端

**自定义服务端**

- 自定义服务端，使用已有的客户端IE，了解客户端给服务器端发了什么请求

```
public class MyTomcat {
    public static void main(String[] args) throws IOException {
    ServerSocket ss = new ServerSocket(9090);
    Socket s = ss.accept();
    System.out.println(s.getInetAddress().getHostAddress()+".....connected");
    
    InputStream in = s.getInputStream();
    byte[] buf = new byte[1024];
    int len = in.read(buf);
    String text = new String(buf,0,len);
    System.out.println(text);
    
    //给客户端一个反馈信息。
    PrintWriter out = new PrintWriter(s.getOutputStream(),true);
    out.println("<font color='red' size='7'>欢迎光临</font>");
    
    s.close()；
    ss.close()；
    }
}
```
服务端获取的信息如下：  

请求行 请求方式  
**GET / HTTP/1.1 /myweb/1.html** 请求的资源路径 http协议版本  
请求消息头，属性名：属性值  
**Accept: \*/\*  
Accept-Language: zh-cn, zu;q=0.5  
Accept-Encoding:gzip, deflate  
User-Agent: Mozilla/4.0  
Host: 192.168.1.105:9090  
Connection: Keep-Alive**  
//空行（请求头和请求体之间有空行）  
请求体  
......

**自定义客户端**

```
public class MyBrowser {
    public static void main(String[] args) throws UnknownHostException, IOException {
        Socket s = new Socket("192.168.1.100",8080);
        //模拟浏览器，给tomcat服务端发送符合http协议的请求消息。
        PrintWriter out = new PrintWriter(s.getOutputStream(),true);
        out.println("GET /myweb/1.html HTTP/1.1");
        out.println("Accept: */*");
        out.println("Host: 192.168.1.100:8080");
        out.println("Connection: close");
        out.println();
        out.println();
        
        InputStream in = s.getInputStream();
        byte[] buf = new byte[1024];
        int len = in.read(buf);
        String str =new String(buf,0,len);
        System.out.println(str);
        s.close();
        //http://192.168.1.100:8080/myweb/1.html
    }
}
```
**浏览器获取的信息如下：** 
 
**HTTP/1.1 200 OK** //应答行：http的协议版本  应答状态码  应答状态描述信息  

应答消息头  属性名：属性值  
**Server: Apache-Coyote/1.1  
Etag: W/"199-1323480176984"  
Last-Modified: Sat, 10 Dec 2011 01:22:56 GMT  
Content-Type:text/html  
Content-Length: 100
Date: Fri, 11 May 2012 07:51:39 GMT  
Connection: close**  
//空行  
应答体  

```
<html>
    <head>
        <title></title>
    </head>
    <body>
        <h1>欢迎光临</h1>
        <font size="5" color="red"> html网页 </font>
    </body>
</html>
```



应答状态码 | 应答状态描述信息
---|---
200 | OK
404 | not found

### URL&URL Connection

```
public class URLDemo {
    public static void main(String[] args) throws MalformedURLException {
        String str_url = "http://192.168.1.100:8080/myweb/1.html?name=lisi";
        
        URL url = new URL(str_url);
        
        /*
        System.out.println(""+url.getProtocol());
        System.out.println(""+url.getHost());
        System.out.println(""+url.getPort());
        System.out.println(""+url.getFile());
        System.out.println(""+url.getPath());
        System.out.println(""+url.getQuery());
        */
        //InputStream in = url.openStream();
        //获取url对象的url连接器对象，将连接封装成了对象
        //Java中内置的可以解析的具体协议的对象+socket
        URLConnection conn = url.openConnection();
        //System.out.println(conn);
        InputStream in = conn.getInputStream();
        
        byte[] buf = new byte[1024];
        int len = in.read(buf);
        String text = new String(buf,0,len);
        System.out.println(text);
        in.close();
        
    }
}
```
### 常见网络架构

- C/S (Client/Server)
    - 缺点
        - 客户端服务端都需要开发
        - 开发成本高，维护麻烦
    - 优点
        - 客户端在本地可以分担运算
- B/S (Browser/Server)
    - 优点
        - 服务端需要开发，客户端不需要开发，直接用浏览器
        - 开发成本相对C/S低，维护简单
    - 缺点
        - 所有运算都在服务端完成

# 09 Java SE 反射

**定义**：反射机制是在**运行状态中**，对于任意一个**类**（class文件），都能知道这个类的所有**方法**和**属性**。对于任意一个对象都能调用它的**任意**一个**方法**和**属性**。

Tomcat例

- Tomcat App提供 Servlet接口
- MyServlet类实现Servlet接口
- 编写MyServlet类配置文件
- Tomcat直接读取配置文件来动态获取MyServlet类中的方法和属性
    - Tomcat通过Class类来获取MyServlet类字节码文件中的内容（想要对MyServlet文件进行内容获取，第一步要获取该类的字节码文件对象即可）
        - 获取Class类中的对象（字节码文件对象）
            - Tomcat通过Class类中的forName()方法获取MyServlet类字节码文件对象
        - 获取Class类中的构造方法
            - 通过newInstance()获取该类空构造方法对象
            - 通过getConstructor获取构造方法对象
                - 再通过构造方法对象newInstance();方法来创建非空参对象
        - 获取Class类中的字段
        - 获取Class类中的方法

```
class Person {
    name;
    age;
}

Person p1 = new Person(Leo, 20);
Person P2 = new Person(Kylo, 28);
```
```
//描述字节码文件的类
class Class {
    提供可以获取字节码文件的内容（字段，构造方法，一般方法）
}
class Demo {
    int a = 6;
    Demo() {}
    void show() {}
}
class Test {
    int b = 9;
    Test() {}
    void abc() {}
}
```
## 获取Class对象
**三种方式**
- 方式三：Object类中的getClass()方法
    - 必须明确具体的类并且创建对象
- 方式二：任何数据类型都具备一个静态的属性.class来获取其对应的class对象
    - 要明确类中的静态成员
- 方式三：通过给定的类的字符串名称就可以获取该类
    - Class类中的forName()方法
```
public class ReflectDemo {
    public static void main(String[] args) {
        //方式一：Object类中的getClass()方法
        public static void getClassObject_1() {
            Person p = new Person();
            Class clazz = p.getClass();
            
            Person p1 = ne Person();
            Class clazz1 = p1.getClass();
            
            System.out.println(clazz==clazz1);//true
        }
        //方式二
        public static void getClassObject_2() {
            Class clazz = Person.class;
            Class clazz1 = Person.class;
            System.out.println(clazz==clazz1);//true
        }
        //方式三
        public static void getClassObject_3() throws ClassNotFoundException {
            String className ="Person";
            Class class = Class.forName(className);
            System.out.println(clazz);
        }
    }
}
public class Person {
    private int age;
    private String name;
    
    public Person(int age, String name) {
        super();
        this.age = age;
        this.name = name;
        System.out.println(personParam run"");
    }
    public Person() {
        super;
        System.out.println(person run"");
    }
    public void show() {
        System.out.println(name+"..."+age);
    }
    private void method() {
        System.out.println("method run");
    }
    public void paraMethod(String str, int num) {
        System.out.println("paramMethod run"+str+":"+num);
    }
    public static void staticMethod() {
        System.out.println("staticMethod run");
    }
}
```
## 获取Class中的构造方法
- 早期创建对象
    - new的时候，先根据被new的类的名称找寻该类的字节码文件，并加载进内创建该字节码文件对象，然后创建该字节文件的对应Person对象
- 反射创建对象
    - 只要知道类名，通过Class来创建该类字节码文件对象
        - 通过newInstance()获取该类空构造方法对象
        - 通过getConstructor获取构造方法对象
            - 再通过构造方法对象newInstance();方法来创建非空参对象
```
public class ReflectDemo2 {
    public static void main(String[] args) {
        createNewObject_1();
        createNewObject_2();
    }
    //空参数构造方法
    public static void createNewObject_1() {
        //以前
        Person p = new Person();
        //反射
        String name = "Person";
        Class clazz = Clazz.forName(name);//获取Person类字节码文件对象
        Object obj = clazz.newInstance();//产生Person类对象
    }
    //非空参数构造方法
    public static void createNewObject_2() {

        String name = "Person";
        Class clazz = Clazz.forName(name);//获取Person类字节码文件对象
        //获取指定构造函数的对象
        Constructor constructor = clazz.getConstructor(String.class, int.class);
        Object obj = constructor.newInstance("Kylo", 29);
    }
}
```
## 获取Class中的字段

```
public class ReflectDemo3 {
    public static void main(String[] args) {
        createNewObject_1();
        createNewObject_2();
    }
    //空参数构造方法
    public static void getFieldDemo() {
        Class clazz = Class.forName("Person");
        Field field = clazz.getField("age");//获取公有的
        field = clazz.getDeclaredField("age");//获取本类，包含私有
        //对私有字段的访问取消权限检查，强制访问
        field.setAccessible(true);
        Object obj = clazz.newInstance();
        field.set(obj,20);
        Object o = field.get(obj);
        System.out.println(o);
        
    }
}
```
## 获取Class中的方法

```
public class ReflectDemo4 {
    public static void main(String[] args) throws Exception {
        getMethodDemo_3();
    }
    //获取有参方法
    public static void getMethodDemo_3() throws Exception {
        Class clazz = Class.forName("cn.itcast.bean.Person");
        Method method = clazz.getMethod("paramMethod", String.class,int.class);
        Object obj = clazz.newInstance();
        method.invoke(obj, "小强",89);
    }
    //获取无参方法
    public static void getMethodDemo_2() throws Exception {
        Class clazz = Class.forName("cn.itcast.bean.Person");
        Method method = clazz.getMethod("show", null);//获取空参数一般方法。
        //Object obj = clazz.newInstance();
        Constructor constructor = clazz.getConstructor(String.class,int.class);
        Object obj = constructor.newInstance("小明",37);
        method.invoke(obj, null);
    }
    //获取指定Class中的所有公共方法
    public static void getMethodDemo() throws Exception {
        Class clazz = Class.forName("cn.itcast.bean.Person");
        Method[] methods  = clazz.getMethods();//获取的都是公有的方法。 
        methods = clazz.getDeclaredMethods();//只获取本类中所有方法，包含私有。 
        for(Method method : methods){
            System.out.println(method);
        }
    }
}

```
## 反射练习

```
public class Mainboard {
    public void run() {
        System.out.println("main board run....");
    }
    public void usePCI(PCI p) {//PCI p = new SouncCard();
        if (p != null) {
            p.open();
            p.close();
        }
    }
}
public class SoundCard implements PCI {
    public void open(){
        System.out.println("sound open");
    }
    public void close(){
        System.out.println("sound close");
    }
}
public class NetCard implements PCI {
    @Override
    public void open() {
        System.out.println("net open");
    }
    @Override
    public void close() {
        System.out.println("net close");
    }
}
public interface PCI {
    public void open();
    public void close();
}
/*
 * 电脑运行。 
 */
public class ReflectTest {
    public static void main(String[] args) throws Exception {
        Mainboard mb = new Mainboard();
        mb.run();
        //每次添加一个设备都需要修改代码传递一个新创建的对象
        //mb.usePCI(new SoundCard());
        //能不能不修改代码就可以完成这个动作。
        //不用new来完成，而是只获取其class文件。在内部实现创建对象的动作。 
        File configFile = new File("pci.properties");
        
        Properties prop = new Properties();
        FileInputStream fis = new FileInputStream(configFile);
        
        prop.load(fis);
        
        for(int x=0; x<prop.size(); x++){
            String pciName = prop.getProperty("pci"+(x+1));
            Class clazz = Class.forName(pciName);//用Class去加载这个pci子类。
            PCI p = (PCI)clazz.newInstance();
            
            mb.usePCI(p);
        }
        fis.close();
    }
}
pci.properties文件
pci1=cn.itcast.reflect.test.SoundCard
pci2=cn.itcast.reflect.test.NetCard
```
# 10 Java SE 正则表达式

## 概述

**作用**：操作字符串数据

```
public class RegexDemo {
    public static void main(String[] args) {
        String qq = "303043149";
        //第一位1到9
        //第二位0到9
        //第二位0到9出现4到14次
        String regex = "[1-9][0-9]{4,14}";//正则表达式
        boolean b = qq.matches(regex);
        System.out.println(qq+b);
    }
    public static void checkQQ(String qq) {
        int len = qq.length();
        if(len>=5 %% len<=15) {
            if(!qq.startsWith("0")) {
                try {
                    long l Long.parseLong(qq);
                } catch(NumberFormatException e) {
                    System.out.println("非法字符");
                }
            } else {
                System.out.println(qq+":不能0开头");
            }
        } else {
            System.out.println(qq+"长度错误");
        }
    }
}
```

## 常见的规则

字符类 | 含义
---|---
[abc] | a、b 或 c（简单类）
[^abc] | 任何字符，除了 a、b 或 c（否定）
[a-zA-Z] | a 到 z 或 A 到 Z，两头的字母包括在内（范围）
[a-d[m-p]] | a 到 d 或 m 到 p：[a-dm-p]（并集）
[a-z&&[def]] | d、e 或 f（交集）
[a-z&&[^bc]] | a 到 z，除了 b 和 c：[ad-z]（减去）
[a-z&&[^m-p]] | a 到 z，而非 m 到 p：[a-lq-z]（减去）

预定义字符类 | 含义
---|---
. | 任何字符（与行结束符可能匹配也可能不匹配）
\d | 数字：[0-9]
\D | 非数字： [^0-9]
\s | 空白字符：[ \t\n\x0B\f\r]
\S | 非空白字符：[^\s]
\w | 单词字符：[a-zA-Z_0-9]
\W | 非单词字符：[^\w]

边界匹配器 | 含义
---|---
^ | 行的开头
$ | 行的结尾
\b | 单词边界
\B | 非单词边界
\A | 输入的开头
\G | 上一个匹配的结尾
\Z | 输入的结尾，仅用于最后的结束符（如果有的话）
\z | 输入的结尾

Greedy | 数量词
---|---
X? | X 一次或一次也没有
X* | X 零次或多次
X+ | X 一次或多次
X{n} | X 恰好 n 次
X{n,} | X 至少 n 次
X{n,m} | 至少 n 次，但是不超过 m 次

Logical 运算符 | 含义
---|---
XY | X 后跟 Y
X|Y | X 或 Y
(X) | X，作为捕获组

Back 引用 | 含义
---|---
\n | 任何匹配的 n^th 捕获组

**组的概念**  

（（A）（B（C）））  
1    	((A)(B(C)))  
2    	\A  
3    	(B(C))  
4    	(C)  
组零始终代表整个表达式
## 常见功能

正则表达式对字符串的常见操作
- 匹配
    - 使用String类中的matches方法
- 切割
    - 使用String类中的split方法
- 替换
    - 使用String类中的replaceAll方法
- 获取
    - 将正则表达式封装成对象
        - Pattern p = Pattern.compile("a*b");
    - 通过正则对象的matcher方法字符串相关联。获取要对字符串操作的匹配器对象Matcher
        - Matcher m = p.matcher("aaaaab");
    - 通过Matcher匹配其对象的方法对字符串进行操作
        - boolean b = m.matches();

```
public class RegexDemo2 {
    public static void main(String[] args) {
        functionDemo_4();
    }
    /*获取

    */
    public  static void functionDemo_4() {
        String str = "da jia hao,ming tian bu fang jia!";
        /*
        获取三个字母的单词[a-z]{3}
        
        */
        String regex = "\\b[a-z]{3}\\b";
        //把正则封装成对象
        Pattern p = Pattern.compile(regex);
        //通过正则对象获取匹配器对象
        Matcher m = p.matcher(str);
        
        //使用Matcher对象的方法对字符串进行操作
        //要获取三个字母组成的单词，用find()方法
        System.out.println(str);
        while(m.find()) {
            System.out.println(m.group());//获取匹配的子序列
            System.out.println(m.start()+":"+m.end());//获取字母开始和结束位置，包头不包尾
        }
    }
    //替换
    public static void functionDemo_3() {
        String str = "zhangsanttttxiaoqiangmmmmmmzhaoliu";
        /*
        把.用()封装成组(.)
        组的编号为\\1
        编号为1的组出现过一次或者多次所以(.)\\1+
        获取编号1组里的字母并且替换$1
        */
        str = str.replaceAll("(.)\\1+", "$1");
        System.out.println(str);
        
        String tel = "15800001111";//158****1111;
        /*
        前三个数封装成编号为1的组(\\d{3})
        末四个数封装成编号为2的组(\\d{4})
        */
        tel = tel.replaceAll("(\\d{3})\\d{4}(\\d{4})", "$1****$2");
        
        System.out.println(tel);
    }
    //切割
    public static void functionDemo_2(){
        String str = "zhangsan    xiaoqiang   zhaoliu";
        String[] names = str.split(" +");//一次或多次空格
        
        String str = "zhangsan.xiaoqiang.zhaoliu";
        String[] names = str.split("\\.");//用.来切，\\转义
        
        String str = "zhangsanttttxiaoqiangmmmmmmzhaoliu";
        /*
        把.用()封装成组(.)
        组的编号为\\1
        编号为1的组出现过一次或者多次所以(.)\\1+
        */
        String[] names = str.split("(.)\\1+");/
        
        for(String name : names){
            System.out.println(name);
        }
    }
    //匹配
    public static void functionDemo_1(){
        //匹配手机号码是否正确
        String tel = "15800001111";
        /*
        第一位固定1
        第二位是3，5，8中的一个[358]
        第三位开始[0-9]用预定义字符类表示\\d重复9次
        */
        String regex = "1[358]\\d{9}";
        boolean b = tel.matches(regex);
        System.out.println(tel+":"+b);
    }
}
```
## 正则表达式练习

练习一
- 过滤信息
    - We....neeeeeed..baa...aaack......uuu..up
- ip地址排序
    - 192.168.10.34 127.0.0.1 3.3.3.3 105.70.11.55
- 邮件地址校验
```
public class RegexTest {
    public static void main(String[] args) {
        test_1();
    }
    public static void test_1 {
        String str = "We....neeeeeed..baa...aaack......uuu..up";
        //去掉...
        str = str.replaceAll("\\.+"," ");
        //替换叠词
        str = str.replaceAall("(.)\\1+","$1");
        System.out.println(str);
    }
    public static void test_2 {
        String ip_str = "192.168.10.34 127.0.0.1 3.3.3.3 105.70.11.55";
        //为了让ip可以按照字符串顺序比较，只要让ip的每一段的位数相同
        //补零，每一段加2个0
        ip_str = ip_str.replaceAll("(\\d+)","00$1");
        //00192.168.10.34 00127.0.0.1 003.3.3.3 00105.70.11.55
        System.out.println(ip_str);
        //每一段保留数字三位
        ip_str = ip_str.replaceAll("0*(\\d{3})","$1");
        //192.168.10.34 127.0.0.1 003.3.3.3 105.70.11.55
        System.out.println(ip_str);
        
        //把ip地址切出
        str = str.split(" +");
        
        TreeSet<String> ts = new TreeSet<String>();
        
        for(String ip : ips) {
            ts.add(ip);
        }
        for(String ip : ts) {
            //0没有或者多次后跟着连续数字
            //用连续的数字替换带0的那部分
            System.out.println(ip.replaceAll("0*(\\d+)", "$1"));
        }
        public static void test_3 {
        String mail = "abc@sina.com";
        /*
        第一部分大小写字母数字下划线都可以一个或者多个[a-zA-Z0-9_]+
        第二部分固定@
        第三部分大小写字母数字都可以一个或者多个[a-zA-Z0-9]+
        第四部分（\\.字母出现1到3次）出现一次或者多次（\\.[a-zA-Z]{1,3})+
        */
        String regex = "[a-zA-Z0-9_]+@[a-zA-Z0-9]+\\.[a-zA-Z]{1,3})+";
        regex = "\\w+@\\w+(\\.\\w+)+";
        boolean b = mail.matches(regex);
        System.out.println(mail+":"+b);
        }
    }
}
```
## 网页爬虫
定义：在互联网中获取符合指定规则数据的程序

```
public class RegexTest2 {
    public static void main(String[] args) throws IOException {
        List<String> list = getMailsByWeb();
        for(String mail : list){
            System.out.println(mail);
        }
    }
    public static List<String> getMailsByWeb() throws IOException {
        //1, 读取源文件
        //BufferedReader bufr = new BufferedReader(new FileReader("c:\\mail.html"));
        URL url = new URL("http://192.168.1.100:8080/myweb/mail.html");
        BufferedReader bufIn = new BufferedReader(new InputStreamReader(url.openStream()));
        //2，对读取的数据进行规则的匹配，从中获取符合规则的数据
        String mail_regex = "\\w+@\\w+(\\.\\w+)+";
        List<String> list = new ArrayList<String>();
        Pattern p = Pattern.compile(mail_regex);
        String line = null;
        while((line=bufIn.readLine())!=null){
            Matcher m = p.matcher(line);
            while(m.find()){
                //3，符合规则的数据存储到集合中
                list.add(m.group());
            }
        }
        return list;
    }
    public static List<String>  getMails() throws IOException{
        //1, 读取源文件
        BufferedReader bufr = new BufferedReader(new FileReader("c:\\mail.html"));
        //2，对读取的数据进行规则的匹配，从中获取符合规则的数据
        String mail_regex = "\\w+@\\w+(\\.\\w+)+";
        List<String> list = new ArrayList<String>();
        Pattern p = Pattern.compile(mail_regex);
        String line = null;
        while((line=bufr.readLine())!=null){
            Matcher m = p.matcher(line);
            while(m.find()){
                //3，符合规则的数据存储到集合中
                list.add(m.group());
            }
        }
        return list;
    }
}
```
