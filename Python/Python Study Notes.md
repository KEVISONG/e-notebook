# Python Study Notes
> By Kevin Song

<!-- MarkdownTOC autolink='true' -->

- [01 Python 简介](#01-python-%E7%AE%80%E4%BB%8B)
	- [01-01 Python 简介](#01-01-python-%E7%AE%80%E4%BB%8B)
	- [01-02 Python 解释器\(CPython, IPython, PyPy, Jython, IronPython\)](#01-02-python-%E8%A7%A3%E9%87%8A%E5%99%A8cpython-ipython-pypy-jython-ironpython)
	- [01-03 第一个Python程序](#01-03-%E7%AC%AC%E4%B8%80%E4%B8%AApython%E7%A8%8B%E5%BA%8F)
	- [01-04 输入和输出](#01-04-%E8%BE%93%E5%85%A5%E5%92%8C%E8%BE%93%E5%87%BA)
- [02 Python 基础](#02-python-%E5%9F%BA%E7%A1%80)
	- [02-01 数据类型和变量\(整数, 浮点数, 字符串, 布尔值, 空值\)](#02-01-%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B%E5%92%8C%E5%8F%98%E9%87%8F%E6%95%B4%E6%95%B0-%E6%B5%AE%E7%82%B9%E6%95%B0-%E5%AD%97%E7%AC%A6%E4%B8%B2-%E5%B8%83%E5%B0%94%E5%80%BC-%E7%A9%BA%E5%80%BC)
	- [02-02 字符串转换\(ord(\), chr\(\))和编码\(encode(\), decode\(\), len\(\))](#02-02-%E5%AD%97%E7%AC%A6%E4%B8%B2%E8%BD%AC%E6%8D%A2ord-chr%E5%92%8C%E7%BC%96%E7%A0%81encode-decode-len)
	- [02-03 list和tuple](#02-03-list%E5%92%8Ctuple)
	- [02-04 判断语句\(if, if else, elif\)](#02-04-%E5%88%A4%E6%96%AD%E8%AF%AD%E5%8F%A5if-if-else-elif)
	- [02-05 循环语句\(for, while\)](#02-05-%E5%BE%AA%E7%8E%AF%E8%AF%AD%E5%8F%A5for-while)
	- [02-06 dict和set](#02-06-dict%E5%92%8Cset)
- [03 Python 函数](#03-python-%E5%87%BD%E6%95%B0)
	- [03-01 调用函数\(内置函数, 数据类型转换\)](#03-01-%E8%B0%83%E7%94%A8%E5%87%BD%E6%95%B0%E5%86%85%E7%BD%AE%E5%87%BD%E6%95%B0-%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2)
	- [03-02 定义函数\(空函数, 多返回值\)](#03-02-%E5%AE%9A%E4%B9%89%E5%87%BD%E6%95%B0%E7%A9%BA%E5%87%BD%E6%95%B0-%E5%A4%9A%E8%BF%94%E5%9B%9E%E5%80%BC)
	- [03-03 函数的参数\(位置参数, 默认参数, 可变参数, 关键字参数\)](#03-03-%E5%87%BD%E6%95%B0%E7%9A%84%E5%8F%82%E6%95%B0%E4%BD%8D%E7%BD%AE%E5%8F%82%E6%95%B0-%E9%BB%98%E8%AE%A4%E5%8F%82%E6%95%B0-%E5%8F%AF%E5%8F%98%E5%8F%82%E6%95%B0-%E5%85%B3%E9%94%AE%E5%AD%97%E5%8F%82%E6%95%B0)
	- [03-04 递归函数](#03-04-%E9%80%92%E5%BD%92%E5%87%BD%E6%95%B0)
- [04 Python 高级特性\(切片, 迭代, 生成器, 迭代器\)](#04-python-%E9%AB%98%E7%BA%A7%E7%89%B9%E6%80%A7%E5%88%87%E7%89%87-%E8%BF%AD%E4%BB%A3-%E7%94%9F%E6%88%90%E5%99%A8-%E8%BF%AD%E4%BB%A3%E5%99%A8)
	- [04-01 切片](#04-01-%E5%88%87%E7%89%87)
	- [04-02 迭代](#04-02-%E8%BF%AD%E4%BB%A3)
	- [04-03 列表生成式\(List Comprehensions\)](#04-03-%E5%88%97%E8%A1%A8%E7%94%9F%E6%88%90%E5%BC%8Flist-comprehensions)
	- [04-04 生成器\((\)实现, 函数实现)](#04-04-%E7%94%9F%E6%88%90%E5%99%A8%E5%AE%9E%E7%8E%B0-%E5%87%BD%E6%95%B0%E5%AE%9E%E7%8E%B0)
	- [04-05 迭代器](#04-05-%E8%BF%AD%E4%BB%A3%E5%99%A8)
- [05 Python 函数式编程](#05-python-%E5%87%BD%E6%95%B0%E5%BC%8F%E7%BC%96%E7%A8%8B)
	- [05-01 高阶函数\(map(\), reduce\(\), filter\(\), sorted\(\))](#05-01-%E9%AB%98%E9%98%B6%E5%87%BD%E6%95%B0map-reduce-filter-sorted)
	- [05-02 返回函数](#05-02-%E8%BF%94%E5%9B%9E%E5%87%BD%E6%95%B0)
	- [05-03 匿名函数](#05-03-%E5%8C%BF%E5%90%8D%E5%87%BD%E6%95%B0)
	- [05-04 装饰器\(Decorator\)](#05-04-%E8%A3%85%E9%A5%B0%E5%99%A8decorator)
	- [05-05 偏函数\(Partial function\)](#05-05-%E5%81%8F%E5%87%BD%E6%95%B0partial-function)
- [06 Python 模块](#06-python-%E6%A8%A1%E5%9D%97)
	- [06-01 使用模块](#06-01-%E4%BD%BF%E7%94%A8%E6%A8%A1%E5%9D%97)
	- [06-02 安装第三方模块](#06-02-%E5%AE%89%E8%A3%85%E7%AC%AC%E4%B8%89%E6%96%B9%E6%A8%A1%E5%9D%97)
- [07 Python OOP](#07-python-oop)
	- [07-01 类\(Class\)和实例\(Instance\)](#07-01-%E7%B1%BBclass%E5%92%8C%E5%AE%9E%E4%BE%8Binstance)
	- [07-02 访问限制](#07-02-%E8%AE%BF%E9%97%AE%E9%99%90%E5%88%B6)
	- [07-03 继承和多态](#07-03-%E7%BB%A7%E6%89%BF%E5%92%8C%E5%A4%9A%E6%80%81)
	- [07-04 获取对象信息\(type(\), isinstance\(\), dir\(\))](#07-04-%E8%8E%B7%E5%8F%96%E5%AF%B9%E8%B1%A1%E4%BF%A1%E6%81%AFtype-isinstance-dir)
	- [07-05 实例属性和类属性](#07-05-%E5%AE%9E%E4%BE%8B%E5%B1%9E%E6%80%A7%E5%92%8C%E7%B1%BB%E5%B1%9E%E6%80%A7)
- [08 Python 面向对象高级编程\(OOP Advanced Features\)](#08-python-%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E9%AB%98%E7%BA%A7%E7%BC%96%E7%A8%8Boop-advanced-features)
	- [08-01 \_\_slots__](#08-01-slots__)
	- [08-02 @property](#08-02-property)
	- [08-03 多重继承](#08-03-%E5%A4%9A%E9%87%8D%E7%BB%A7%E6%89%BF)
	- [08-04 定制类\(str, repr, iter, getattr, call\)](#08-04-%E5%AE%9A%E5%88%B6%E7%B1%BBstr-repr-iter-getattr-call)
	- [08-05 枚举类](#08-05-%E6%9E%9A%E4%B8%BE%E7%B1%BB)
	- [08-06 元类](#08-06-%E5%85%83%E7%B1%BB)
- [09 Python 错误调试测试](#09-python-%E9%94%99%E8%AF%AF%E8%B0%83%E8%AF%95%E6%B5%8B%E8%AF%95)
	- [09-01 错误处理\(不同类型错误, 调用堆栈, 记录错误, 抛出错误\)](#09-01-%E9%94%99%E8%AF%AF%E5%A4%84%E7%90%86%E4%B8%8D%E5%90%8C%E7%B1%BB%E5%9E%8B%E9%94%99%E8%AF%AF-%E8%B0%83%E7%94%A8%E5%A0%86%E6%A0%88-%E8%AE%B0%E5%BD%95%E9%94%99%E8%AF%AF-%E6%8A%9B%E5%87%BA%E9%94%99%E8%AF%AF)
	- [09-02 调试\(直接打印, 断言assert, logging, pdb, \)](#09-02-%E8%B0%83%E8%AF%95%E7%9B%B4%E6%8E%A5%E6%89%93%E5%8D%B0-%E6%96%AD%E8%A8%80assert-logging-pdb-)
	- [09-03 单元测试](#09-03-%E5%8D%95%E5%85%83%E6%B5%8B%E8%AF%95)
	- [09-04 文档测试](#09-04-%E6%96%87%E6%A1%A3%E6%B5%8B%E8%AF%95)
- [10 Python IO](#10-python-io)
	- [10-01 文件读写](#10-01-%E6%96%87%E4%BB%B6%E8%AF%BB%E5%86%99)
	- [10-02 StringIO和BytesIO](#10-02-stringio%E5%92%8Cbytesio)
	- [10-03 操作文件和目录](#10-03-%E6%93%8D%E4%BD%9C%E6%96%87%E4%BB%B6%E5%92%8C%E7%9B%AE%E5%BD%95)
	- [10-04 序列化\(pickling\)和JSON](#10-04-%E5%BA%8F%E5%88%97%E5%8C%96pickling%E5%92%8Cjson)
- [11 Python 进程和线程](#11-python-%E8%BF%9B%E7%A8%8B%E5%92%8C%E7%BA%BF%E7%A8%8B)
	- [11-01 多进程\(Multiprocessing\)](#11-01-%E5%A4%9A%E8%BF%9B%E7%A8%8Bmultiprocessing)
	- [11-02 多线程](#11-02-%E5%A4%9A%E7%BA%BF%E7%A8%8B)
	- [11-03 ThreadLocal](#11-03-threadlocal)
	- [11-04 进程vs线程](#11-04-%E8%BF%9B%E7%A8%8Bvs%E7%BA%BF%E7%A8%8B)
	- [11-05 分布式进程](#11-05-%E5%88%86%E5%B8%83%E5%BC%8F%E8%BF%9B%E7%A8%8B)
- [12 Python 正则表达式](#12-python-%E6%AD%A3%E5%88%99%E8%A1%A8%E8%BE%BE%E5%BC%8F)
	- [12-01 正则基础](#12-01-%E6%AD%A3%E5%88%99%E5%9F%BA%E7%A1%80)
	- [12-02 re模块](#12-02-re%E6%A8%A1%E5%9D%97)
	- [12-03 正则进阶\(切分字符串, 分组, 贪婪匹配, 编译\)](#12-03-%E6%AD%A3%E5%88%99%E8%BF%9B%E9%98%B6%E5%88%87%E5%88%86%E5%AD%97%E7%AC%A6%E4%B8%B2-%E5%88%86%E7%BB%84-%E8%B4%AA%E5%A9%AA%E5%8C%B9%E9%85%8D-%E7%BC%96%E8%AF%91)
- [13 Python 常用内建模块](#13-python-%E5%B8%B8%E7%94%A8%E5%86%85%E5%BB%BA%E6%A8%A1%E5%9D%97)
	- [13-01 datetime\(timestamp转换, str转换, datetime加减, 时区转换\)](#13-01-datetimetimestamp%E8%BD%AC%E6%8D%A2-str%E8%BD%AC%E6%8D%A2-datetime%E5%8A%A0%E5%87%8F-%E6%97%B6%E5%8C%BA%E8%BD%AC%E6%8D%A2)
	- [13-02 collections\(namedtuple, deque, defaultdict, OrderedDict, Counter\)](#13-02-collectionsnamedtuple-deque-defaultdict-ordereddict-counter)
	- [13-03 base64](#13-03-base64)
	- [13-04 struct](#13-04-struct)
	- [13-05 hashlib\(MD5, SHA1, 摘要算法\)](#13-05-hashlibmd5-sha1-%E6%91%98%E8%A6%81%E7%AE%97%E6%B3%95)
	- [13-06 itertools\(count(\), cycle\(\), repeat\(\), chain\(\), groupby\(\))](#13-06-itertoolscount-cycle-repeat-chain-groupby)
	- [13-07 contextlib\(@contextmanager, @closing\)](#13-07-contextlibcontextmanager-closing)
	- [13-08 XML](#13-08-xml)
	- [13-09 HTMLParser](#13-09-htmlparser)
	- [13-10 urllib\(Get, Post, Handler\)](#13-10-urllibget-post-handler)
- [14 Python GUI](#14-python-gui)
- [15 Python 网络](#15-python-%E7%BD%91%E7%BB%9C)
	- [15-01 TCP/IP](#15-01-tcpip)
	- [15-02 TCP 编程\(客户端, 服务端\)](#15-02-tcp-%E7%BC%96%E7%A8%8B%E5%AE%A2%E6%88%B7%E7%AB%AF-%E6%9C%8D%E5%8A%A1%E7%AB%AF)
	- [15-03 UDP 编程\(服务端, 客户端\)](#15-03-udp-%E7%BC%96%E7%A8%8B%E6%9C%8D%E5%8A%A1%E7%AB%AF-%E5%AE%A2%E6%88%B7%E7%AB%AF)
	- [15-04 电子邮件原理](#15-04-%E7%94%B5%E5%AD%90%E9%82%AE%E4%BB%B6%E5%8E%9F%E7%90%86)
	- [15-05 SMTP发送邮件\(纯文本邮件, HTML邮件, 发送附件, 加密SMTP\)](#15-05-smtp%E5%8F%91%E9%80%81%E9%82%AE%E4%BB%B6%E7%BA%AF%E6%96%87%E6%9C%AC%E9%82%AE%E4%BB%B6-html%E9%82%AE%E4%BB%B6-%E5%8F%91%E9%80%81%E9%99%84%E4%BB%B6-%E5%8A%A0%E5%AF%86smtp)
	- [15-06 POP3收取邮件](#15-06-pop3%E6%94%B6%E5%8F%96%E9%82%AE%E4%BB%B6)
- [16 Python 数据库](#16-python-%E6%95%B0%E6%8D%AE%E5%BA%93)
	- [16-01 使用SQLite](#16-01-%E4%BD%BF%E7%94%A8sqlite)
	- [16-02 使用MySQL](#16-02-%E4%BD%BF%E7%94%A8mysql)
	- [16-03 使用SQLAlchemy\(ORM, SQLAlchemy\)](#16-03-%E4%BD%BF%E7%94%A8sqlalchemyorm-sqlalchemy)
- [17 Python Web](#17-python-web)
	- [17-01 HTTP协议简介\(HTTP请求, HTTP格式\)](#17-01-http%E5%8D%8F%E8%AE%AE%E7%AE%80%E4%BB%8Bhttp%E8%AF%B7%E6%B1%82-http%E6%A0%BC%E5%BC%8F)
	- [17-02 HTML简介](#17-02-html%E7%AE%80%E4%BB%8B)
	- [17-03 WSGI接口](#17-03-wsgi%E6%8E%A5%E5%8F%A3)
	- [17-04 使用Web框架\(FLASK\)](#17-04-%E4%BD%BF%E7%94%A8web%E6%A1%86%E6%9E%B6flask)
	- [17-05 使用模板\(MVC\)](#17-05-%E4%BD%BF%E7%94%A8%E6%A8%A1%E6%9D%BFmvc)
- [18 Python 异步IO](#18-python-%E5%BC%82%E6%AD%A5io)
	- [18-01 协程\(Coroutine\)](#18-01-%E5%8D%8F%E7%A8%8Bcoroutine)
	- [18-02 asyncio](#18-02-asyncio)
	- [18-03 async/await](#18-03-asyncawait)
	- [18-04 aiohttp](#18-04-aiohttp)

<!-- /MarkdownTOC -->


# 01 Python 简介

## 01-01 Python 简介
Python应用场景

- 网络应用，包括网站、后台服务等等；
- 日常需要的小工具，包括系统管理员需要的脚本任务等等；
- 把其他语言开发的程序再包装起来，方便使用。

## 01-02 Python 解释器(CPython, IPython, PyPy, Jython, IronPython)
Python解释器用来执行.py文件

**CPython**

- Python官方解释器
- 由C语言开发
- 命令行下运行python就是启动CPython解释器

CPython是使用最广的Python解释器  

CPython用 **>>>** 作为提示符

**IPython**

- 基于CPython
- 只是在交互方式上有所增强
- 执行代码的功能和CPython完全一样

Python用 **In [序号]:** 作为提示符

**PyPy**

- 执行速度快
- 采用JIT技术
- 对Python代码进行动态编译

绝大部分Python代码都可以在PyPy下运行，但是PyPy和CPython有一些是不同的，这就导致相同的Python代码在两种解释器下执行可能会有不同的结果。

**Jython**

- 运行在Java平台上的Python解释器
- 可以直接把Python代码编译成Java字节码执行

**IronPython**

- 运行在微软.Net平台上的Python解释器
- 可以直接把Python代码编译成.Net的字节码

## 01-03 第一个Python程序

- 交互式环境
- 文本编辑环境

**交互式环境**

命令行下输入 **python** 进入交互式环境
```
>>> 100+200
300
```
```
>>> print('hello, world')
hello, world
```
exit()退出Python

**文本编辑器**

hello.py
```
print('hello, world')
```
命令行操作运行.py文件
```
C:\work>python hello.py
hello, world
```
## 01-04 输入和输出

**输出**

print()会依次打印每个字符串，遇到逗号“,”会输出一个空格  

下例两句输出相同
```
>>> print('hello world')
>>> print('hello', 'world')
```

**输入**

input()，可以让用户输入字符串，并存放到一个变量里

交互式环境
```
>>> name = input()
Michael
>>> name
'Michael'
```
文本编辑环境
```
name = input('please enter your name: ')
print('Hello,', name)
```
```
C:\Workspace> python hello.py
please enter your name: Kevin
Hello, Kevin
```
# 02 Python 基础

## 02-01 数据类型和变量(整数, 浮点数, 字符串, 布尔值, 空值)

**整数**  

Python可已处理任意大小的整数

**浮点数**

按照科学记数法表示时，小数点位置可变：1.23x10^9 = 12.3x10^8

对于很大或者很小的浮点数采用科学记数法：1.23x10^9 = 1.23e9

**字符串**  

单引号 **' '** 或双引号 **" "** 括起来的任意文本：'abc'，"xyz"

如果 **' '** 本身也是一个字符，那就可以用 **" "** 括起来

```
a = "I'm OK"
```

输出：I'm OK

如果字符串内部既包含 **' '** 又包含 **" "** ，用转义字符\来标识

```
a = 'I\'m \"OK\"!'
```

输出：I'm "OK"!

**转义字符**

**r''** ： **' '** 内部字符串默认不转义

```
>>> print(r'\\\t\\')
\\\t\\
```

**'''...'''** ： 表示多行内容  

交互式

```
>>> print('''line1
... line2
... line3''')
line1
line2
line3
```

编辑器

```
print('''line1
line2
line3''')
```
**布尔值**  

- Ture
- False

布尔值运算符

- and
- or
- not

```
>>> True and True
True
>>> True and False
False
>>> False and False
False
>>> 5 > 3 and 3 > 1
True
```

**空值**

空值是Python里一个特殊的值，用None表示

**变量**

动态语言 Python

```
a = 123 # a是整数
print(a)
a = 'ABC' # a变为字符串
print(a)
```

动态语言 Java

```
int a = 123; // a是整数类型变量
a = "ABC"; // 错误：不能把字符串赋给整型变量
```

## 02-02 字符串转换(ord(), chr())和编码(encode(), decode(), len())

字符串 转 整数 ：ord()

```
>>> ord('A')
65
>>> ord('中')
20013
```

整数 转 字符串 ：chr()

```
>>> chr(66)
'B'
>>> chr(25991)
'文'
```

**bytes类型**

把str变为以字节为单位的bytes  

bytes类型的数据用带b前缀的单引号或双引号表示：

```
x = b'ABC'
```

**'ABC'** 和 **b'ABC'**，前者是str，后者虽然内容显示得和前者一样，但bytes的每个字符都只占用一个字节。

**encode()**

以Unicode表示的str编码为bytes，通过encode()方法

```
>>> 'ABC'.encode('ascii')
b'ABC'
>>> '中文'.encode('utf-8')
b'\xe4\xb8\xad\xe6\x96\x87'
>>> '中文'.encode('ascii')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
UnicodeEncodeError: 'ascii' codec can't encode characters in position 0-1: ordinal not in range(128)
```

**decode()**

bytes解码为str，通过decode()方法

```
>>> b'ABC'.decode('ascii')
'ABC'
>>> b'\xe4\xb8\xad\xe6\x96\x87'.decode('utf-8')
'中文'
```

**len()**

- 计算的是str的字符数
- 计算的是bytes的字节数

```
>>> len('ABC')
3
>>> len('中文')
2
>>> len(b'ABC')
3
>>> len('中文'.encode('utf-8'))
6
```

**格式化**

常见占位符
- %d	整数
- %f	浮点数
- %s	字符串
- %x	十六进制整数

```
>>> 'Hi, %s, you have %d RMB.' % ('Kevin', 1000000)
'Hi, Kevin, you have 1000000 RMB.'
```
```
>>> 'growth rate: %d %%' % 7
'growth rate: 7 %'
```
## 02-03 list和tuple

**list**

Python内置的一种数据类型是列表：list

```
>>> justice = ['Kevin', 'Cyborg', 'Flash']
>>> justice
['Kevin', 'Cyborg', 'Flash']
```

获取长度

```
>>> len(justice)
3
```
常用函数：
- cmp(list1, list2)：比较两个列表的元素
- len(list)：列表元素个数
- max(list)：返回列表元素最大值
- min(list)：返回列表元素最小值
- list(seq)：将元组转换为列表 

常用方法：

- list.append(obj)：在列表末尾添加新的对象
- list.count(obj)：统计某个元素在列表中出现的次数
- list.extend(seq)：在列表末尾一次性追加另一个序列中的多个值（用新列表扩展原来的列表）
- list.index(obj)：从列表中找出某个值第一个匹配项的索引位置
- list.insert(index, obj)：将对象插入列表
- list.pop(obj=list[-1])：移除列表中的一个元素（默认最后一个元素），并且返回该元素的值
- list.remove(obj)：移除列表中某个值的第一个匹配项
- list.reverse()：反向列表中元素
- list.sort([func])：对原列表进行排序

查改

```
>>> justice[0]
'Kevin'
>>> justice[-1]
'Flash'
>>> justice[2] = 'Superman'
```
list元素的数据类型可以不同
```
>>> L = ['Apple', 123, True]
```
list元素也可以是另一个list
```
>>> s = ['python', 'java', ['asp', 'php'], 'javascript']
>>> len(s)
4
```
**tuple**

元组：tuple一旦初始化就不能修改

```
>>> justice = ('Kevin', 'Cyborg', 'Flash')
```
没有append()，insert()这样的方法。其他获取元素的方法和list一样

定义只有一个元素的tuple，加一个逗号
```
>>> t = (1,)
>>> t
(1,)
```
tuple里的list可变
```
>>> t = ('a', 'b', ['A', 'B'])
>>> t[2][0] = 'X'
>>> t[2][1] = 'Y'
>>> t
('a', 'b', ['X', 'Y'])
```
## 02-04 判断语句(if, if else, elif)

**if 语句**

- 如果if语句判断是True，就执行缩进的两行print语句
- 否则，什么也不做

```
age = 20
if age >= 18:
    print('your age is', age)
    print('adult')
```
**if else 语句**
```
age = 3
if age >= 18:
    print('your age is', age)
    print('adult')
else:
    print('your age is', age)
    print('teenager')
```
**elif 语句**

其实就是else if
```
age = 3
if age >= 18:
    print('adult')
elif age >= 6:
    print('teenager')
else:
    print('kid')
```

例

```
s = input('birth: ')
birth = int(s)
if birth < 2000:
    print('00前')
else:
    print('00后')
```
## 02-05 循环语句(for, while)

**for in 循环**

```
names = ['Michael', 'Bob', 'Tracy']
for name in names:
    print(name)
```
range()函数生成整数序列
```
sum = 0
for x in range(101):
    sum = sum + x
print(sum)
```

**while 循环**

计算100以内所有奇数之和

```
sum = 0
n = 99
while n > 0:
    sum = sum + n
    n = n - 2
print(sum)
```
## 02-06 dict和set
**dict**

使用键值对存储数据
```
>>> d = {'Kevin': 95, 'Cyborg': 75, 'Flash': 85}
>>> d['Kevin']
95
```
判断是否存在

```
>>> 'Superman' in d
False
```
获取删除

```
>>> d.get('Superman')
>>> d.get('Superman', -1)
-1
>>> d.pop('Cyborg')
75
```
dict

- 查找和插入的速度极快，不会随着key的增加而变慢；
- 需要占用大量的内存，内存浪费多。

list

- 查找和插入的时间随着元素的增加而增加；
- 占用空间小，浪费内存很少。

所以，dict是用空间来换取时间的一种方法

> dict的key必须是不可变对象（str，int）

**set**

- 没有重复的key
- 没有value
- 需要提供一个list作为输入集合

```
>>> s = set([1, 1, 2, 2, 3, 3])
>>> s
{1, 2, 3}
```
常用方法

- add() 可以重复添加，但不会有效果
- remove(key) 删除

两个set取交集并集
```
>>> s1 = set([1, 2, 3])
>>> s2 = set([2, 3, 4])
>>> s1 & s2
{2, 3}
>>> s1 | s2
{1, 2, 3, 4}
```

**不可变对象**

可变对象：list

```
>>> a = ['c', 'b', 'a']
>>> a.sort()
>>> a
['a', 'b', 'c']
```
不可变对象：很多  

比如：str

```
>>> a = 'abc'
>>> a.replace('a', 'A')
'Abc'
>>> a
'abc'
```
# 03 Python 函数

## 03-01 调用函数(内置函数, 数据类型转换)

**内置函数**

[内置函数官方文档](https://docs.python.org/3/library/functions.html#abs)

可以在交互式环境输入 help() 来查询内置函数的作用
```
>>> help(len)
Help on built-in function len in module builtins:

len(obj, /)
    Return the number of items in a container.
```

**数据类型转换**

- int()
- float()
- str()
- bool()
```
>>> int('123')
123
>>> int(12.34)
12
>>> float('12.34')
12.34
>>> str(100)
'100'
>>> bool(1)
True
>>> bool('')
False
```
函数名可以赋值给一个变量

```
>>> a = abs # 变量a指向abs函数
>>> a(-1) # 所以也可以通过a调用abs函数
1
```
## 03-02 定义函数(空函数, 多返回值)
格式
```
def my_abs(): 
    if x >= 0:
        return x
    else:
        return -x
```

**空函数**

```
def nop():
    pass
```
缺少了pass，代码运行就会有语法错误

**多返回值**

```
import math

def move(x, y, step, angle=0):
    nx = x + step * math.cos(angle)
    ny = y - step * math.sin(angle)
    return nx, ny
```
```
>>> x, y = move(100, 100, 60, math.pi / 6)
>>> print(x, y)
151.96152422706632 70.0
```
其实返回的任然是单一值，只不过是个tuple
```
>>> r = move(100, 100, 60, math.pi / 6)
>>> print(r)
(151.96152422706632, 70.0)
```
在语法上，返回一个tuple可以省略括号，而多个变量可以同时接收一个tuple，按位置赋给对应的值
## 03-03 函数的参数(位置参数, 默认参数, 可变参数, 关键字参数)

**位置参数**

一个位置参数
```
def power(x):
    return x * x
```
```
>>> power(5)
25
```
两个位置参数
```
def power(x, n):
    s = 1
    while n > 0:
        n = n - 1
        s = s * x
    return s
```
```
>>> power(5, 2)
25
>>> power(5)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: power() missing 1 required positional argument: 'n'
```

**默认参数**

为了避免报错，使用默认参数
```
def power(x, n=2):
    s = 1
    while n > 0:
        n = n - 1
        s = s * x
    return s
```
```
>>> power(5)
25
>>> power(5, 2)
25
```
默认参数注意：

1. 必选参数在前，默认参数在后，否则Python的解释器会报错
2. 函数有多个参数时，把变化大的参数放前面，变化小的参数放后面。变化小的参数就可以作为默认参数

默认参数问题：
```
def add_end(L=[]):
    L.append('END')
    return L
```
```
>>> add_end()
['END']
>>> add_end()
['END', 'END']
```
Python函数在定义的时候，默认参数L的值就被计算出来了，即 **[ ]** ，因为默认参数L也是一个变量，它指向对象 **[ ]** ，每次调用该函数，如果改变了L的内容，则下次调用时，默认参数的内容就变了，不再是函数定义时的 **[ ]** 

> 默认参数必须指向不变对象

```
def add_end(L=None):
    if L is None:
        L = []
    L.append('END')
    return L
```
```
>>> add_end()
['END']
>>> add_end()
['END']
```
**可变参数**

可变参数允许传入0个或任意个参数，这些可变参数在函数调用时自动组装为一个tuple。

list或tuple参数
```
def calc(numbers):
    sum = 0
    for n in numbers:
        sum = sum + n * n
    return sum
```
```
>>> calc([1, 2, 3])
14
```
可变参数
```
def calc(*numbers):
    sum = 0
    for n in numbers:
        sum = sum + n * n
    return sum
```
```
>>> calc(1, 2, 3)
14
```
list或tuple调用可变参数函数
```
>>> nums = [1, 2, 3]
>>> calc(*nums)
14
```

**关键字参数**

关键字参数允许传入0个或任意个含参数名的参数，这些关键字参数在函数内部自动组装为一个dict

```
def person(name, age, **kw):
    print('name:', name, 'age:', age, 'other:', kw)
```
```
>>> person('Michael', 30)
name: Michael age: 30 other: {}
>>> person('Bob', 35, city='Beijing')
name: Bob age: 35 other: {'city': 'Beijing'}
>>> person('Adam', 45, gender='M', job='Engineer')
name: Adam age: 45 other: {'gender': 'M', 'job': 'Engineer'}
```
dict调用关键字参数函数
```
>>> extra = {'city': 'Beijing', 'job': 'Engineer'}
>>> person('Jack', 24, **extra)
name: Jack age: 24 other: {'city': 'Beijing', 'job': 'Engineer'}
```
**命名关键字参数**  

限制关键字参数的名字，就可以用命名关键字参数，例如，只接收city和job作为关键字参数
```
def person(name, age, *, city, job):
    print(name, age, city, job)
```
和关键字参数 \*\*kw不同，命名关键字参数需要一个特殊分隔符 *，* 后面的参数被视为命名关键字参数。
```
>>> person('Jack', 24, city='Beijing', job='Engineer')
Jack 24 Beijing Engineer
```

**参数组合**

参数定义的顺序**必须**是：必选参数、默认参数、可变参数、命名关键字参数和关键字参数
```
def f1(a, b, c=0, *args, **kw):
    print('a =', a, 'b =', b, 'c =', c, 'args =', args, 'kw =', kw)

def f2(a, b, c=0, *, d, **kw):
    print('a =', a, 'b =', b, 'c =', c, 'd =', d, 'kw =', kw)
```
```
>>> f1(1, 2)
a = 1 b = 2 c = 0 args = () kw = {}
>>> f1(1, 2, c=3)
a = 1 b = 2 c = 3 args = () kw = {}
>>> f1(1, 2, 3, 'a', 'b')
a = 1 b = 2 c = 3 args = ('a', 'b') kw = {}
>>> f1(1, 2, 3, 'a', 'b', x=99)
a = 1 b = 2 c = 3 args = ('a', 'b') kw = {'x': 99}
>>> f2(1, 2, d=99, ext=None)
a = 1 b = 2 c = 0 d = 99 kw = {'ext': None}
```
## 03-04 递归函数
递归计算阶乘n! = 1 x 2 x 3 x ... x n

```
def fact(n):
    if n==1:
        return 1
    return n * fact(n - 1)
```
```
>>> fact(1)
1
>>> fact(5)
120
```
计算过程
```
===> fact(5)
===> 5 * fact(4)
===> 5 * (4 * fact(3))
===> 5 * (4 * (3 * fact(2)))
===> 5 * (4 * (3 * (2 * fact(1))))
===> 5 * (4 * (3 * (2 * 1)))
===> 5 * (4 * (3 * 2))
===> 5 * (4 * 6)
===> 5 * 24
===> 120
```
尾递归：在函数返回的时候，调用自身本身，并且，return语句不能包含表达式
```
def fact(n):
    return fact_iter(n, 1)

def fact_iter(num, product):
    if num == 1:
        return product
    return fact_iter(num - 1, num * product)
```
计算过程
```
===> fact_iter(5, 1)
===> fact_iter(4, 5)
===> fact_iter(3, 20)
===> fact_iter(2, 60)
===> fact_iter(1, 120)
===> 120
```
# 04 Python 高级特性(切片, 迭代, 生成器, 迭代器)

## 04-01 切片
取前三个元素
```
>>> L = ['Michael', 'Sarah', 'Tracy', 'Bob', 'Jack']
```
传统方法
```
>>> [L[0], L[1], L[2]]
['Michael', 'Sarah', 'Tracy']
```
**切片**

**L[a:b]**：从 **a** 号位取到 **b-1** 号位，如果a为0可以省略

```
>>> L[0:3]
['Michael', 'Sarah', 'Tracy']
```
倒数切片：倒数第一个元素的索引是-1
```
>>> L[-2:]
['Bob', 'Jack']
>>> L[-2:-1]
['Bob']
```
**示例：**
创建一个0-99的数列
```
>>> L = list(range(100))
>>> L
[0, 1, 2, 3, ..., 99]
```
前10个数
```
>>> L[:10]
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```
后10个数
```
>>> L[-10:]
[90, 91, 92, 93, 94, 95, 96, 97, 98, 99]
```
前10个数，每两个取一个：
```
>>> L[:10:2]
[0, 2, 4, 6, 8]
```
所有数，每5个取一个：
```
>>> L[::5]
[0, 5, 10, 15, 20, 25, 30, 35, 40, 45, 50, 55, 60, 65, 70, 75, 80, 85, 90, 95]
```
复制一个list：
```
>>> L[:]
[0, 1, 2, 3, ..., 99]
```
- 切list：同上
- 切tuple：
```
>>> (0, 1, 2, 3, 4, 5)[:3]
(0, 1, 2)
```
- 切str：
```
>>> 'ABCDEFG'[:3]
'ABC'
>>> 'ABCDEFG'[::2]
'ACEG'
```

## 04-02 迭代

for...in可以迭代任何可迭代对象

**迭代list和tuple**

```
>>> l = [1, 2, 3]
>>> for a in l:
...     print(a)
...
1
2
3
>>> t = (1, 2, 3)
>>> for b in t:
...     print(b)
...
1
2
3
```
**迭代dict的key**
```
>>> d = {'a': 1, 'b': 2, 'c': 3}
>>> for key in d:
...     print(key)
...
a
c
b
```
**迭代dict的value**
```
>>> d = {'a': 1, 'b': 2, 'c': 3}
>>> for value in d.values()
...     print(key)
...
1
2
3
```
**同时迭代key和value**
```
>>> d = {'a': 1, 'b': 2, 'c': 3}
>>> for k, v in d.items()
...     print(key)
...
```
**迭代str**
```
>>> for ch in 'ABC':
...     print(ch)
...
A
B
C
```
**判断是可迭代对象**
```
>>> from collections import Iterable
>>> isinstance('abc', Iterable) # str是否可迭代
True
>>> isinstance([1,2,3], Iterable) # list是否可迭代
True
>>> isinstance(123, Iterable) # 整数是否可迭代
False
```
enumerate函数可以把一个list变成索引-元素对
```
>>> for i, value in enumerate(['A', 'B', 'C']):
...     print(i, value)
...
0 A
1 B
2 C
```
双变量for in
```
>>> for x, y in [(1, 1), (2, 4), (3, 9)]:
...     print(x, y)
...
1 1
2 4
3 9
```
## 04-03 列表生成式(List Comprehensions)
**格式：** 对 **容器** 中的 **变量** 进行 **表达式** 处理
```
[表达式 for 变量 in 容器]
```

生成list [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```
>>> list(range(1, 11))
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```
生成list [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```
>>> [x * x for x in range(1, 11)]
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```
生成list [4, 16, 36, 64, 100]
```
>>> [x * x for x in range(1, 11) if x % 2 == 0]
[4, 16, 36, 64, 100]
```
生成全排列list ['AX', 'AY', 'AZ', 'BX', 'BY', 'BZ', 'CX', 'CY', 'CZ']
```
>>> [m + n for m in 'ABC' for n in 'XYZ']
['AX', 'AY', 'AZ', 'BX', 'BY', 'BZ', 'CX', 'CY', 'CZ']
```
两个变量生成list
```
>>> d = {'x': 'A', 'y': 'B', 'z': 'C' }
>>> [k + '=' + v for k, v in d.items()]
['y=B', 'x=A', 'z=C']
```
## 04-04 生成器(()实现, 函数实现)
列表生成式一次性生成整个列表，太占内存，于是就有了一边循环一边计算的机制，生成器
**\( \)实现生成器**
```
>>> L = [x * x for x in range(10)]
>>> L
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
>>> g = (x * x for x in range(10))
>>> g
<generator object <genexpr> at 0x1022ef630>
```
通过next()函数获得generator的下一个返回值

```
>>> next(g)
0
```
generator保存的是算法，每次调用next(g)，就计算出g的下一个元素的值
for循环遍历
```
>>> g = (x * x for x in range(10))
>>> for n in g:
...     print(n)
... 
0
1
4
9
16
25
36
49
64
81
```

**函数实现生成器**

打印斐波拉契数列
```
def fib(max):
    n, a, b = 0, 0, 1
    while n < max:
        print(b)
        a, b = b, a + b
        # t = (b, a + b)  t是一个tuple
        # a = t[0]
        # b = t[1]
        n = n + 1
    return 'done'
```
```
>>> fib(6)
1
1
2
3
5
8
'done'
```
斐波拉契数列生成器仅仅是把 **print(b)** 改为 **yield b**

```
def fib(max):
    n, a, b = 0, 0, 1
    while n < max:
        yield b
        a, b = b, a + b
        n = n + 1
    return 'done'
```
```
>>> f = fib(6)
>>> f
<generator object fib at 0x104feaaa0>
```
打印生成器内容
```
>>> for n in fib(6):
...     print(n)
...
1
1
2
3
5
8
```
generator和函数的执行流程不一样

- 函数是顺序执行，遇到return语句或者最后一行函数语句就返回
- generator的函数，在每次调用next()的时候执行，遇到yield语句返回，再次执行时从上次返回的yield语句处继续执行

## 04-05 迭代器

- 可以直接作用于 **for** 循环的对象统称为可迭代对象：**Iterable**
    - 一类是集合数据类型，如list、tuple、dict、set、str等；
    - 一类是generator，包括生成器和带yield的generator function。
- 可以被 **next()** 函数调用并不断返回下一个值的对象称为迭代器：**Iterator**


小结

- 生成器是Iterator对象
- list、dict、str等Iterable可以使用 **iter()** 函数变成Iterator对象

Python的Iterator对象表示的是一个**数据流**，这个数据流是一个有序序列，但不知道序列的长度，只能不断通过next()函数实现按需计算下一个数据，所以Iterator的计算是**惰性**的，只有在需要返回下一个数据时它才会计算

Python的for循环本质上就是通过不断调用next()函数实现的

```
for x in [1, 2, 3, 4, 5]:
    pass

```
等价于
```
# 首先获得Iterator对象:
it = iter([1, 2, 3, 4, 5])
# 循环:
while True:
    try:
        # 获得下一个值:
        x = next(it)
    except StopIteration:
        # 遇到StopIteration就退出循环
        break

```
# 05 Python 函数式编程

函数式编程：一种抽象程度很高的编程范式

特点：允许把函数本身作为参数传入另一个函数，返回一个函数

## 05-01 高阶函数(map(), reduce(), filter(), sorted())

**变量可以指向函数**  

函数调用
```
>>> abs(-10)
10
```
函数本身
```
>>> abs
<built-in function abs>
```
函数返回值 赋给 变量
```
>>> x = abs(-10)
>>> x
10
```
函数本身 赋给 变量
```
>>> f = abs
>>> f
<built-in function abs>
```
**函数名也是变量**

**abs()** 中函数名 **abs** 也是变量，它指向一个可以计算绝对值的函数

把abs指向10后，就无法通过abs(-10)调用该函数，因为abs这个变量已经不指向求绝对值函数而是指向一个整数10
```
>>> abs = 10
>>> abs(-10)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'int' object is not callable
```

**高阶函数定义**

高阶函数： 一个函数作为参数传递给另一个函数

```
def add(x, y, f):
    return f(x) + f(y)
```
```
>>> add(-5, 6, abs)
11
```
计算过程
```
x = -5
y = 6
f = abs
f(x) + f(y) ==> abs(-5) + abs(6) ==> 11
return 11
```
**map() 函数**

- **map()** 函数接收两个参数，一个是函数，一个是Iterable
- map将传入的函数依次作用到序列的每个元素，并把结果作为新的惰性序列Iterator返回

```
>>> def f(x):
...     return x * x
...
>>> r = map(f, [1, 2, 3, 4, 5, 6, 7, 8, 9])
>>> list(r)
[1, 4, 9, 16, 25, 36, 49, 64, 81]
```

把这个list所有数字转为字符串

```
>>> list(map(str, [1, 2, 3, 4, 5, 6, 7, 8, 9]))
['1', '2', '3', '4', '5', '6', '7', '8', '9']
```

**reduce() 函数**

- **reduce()** 函数接收两个参数，一个是接收两个参数的函数，一个是Iterable
- reduce 把第一第二个元素的计算结果继续和序列的下一个元素做计算

```
reduce(f, [x1, x2, x3, x4]) = f(f(f(x1, x2), x3), x4)
```

把序列[1, 3, 5, 7, 9]变换成整数13579

```
>>> from functools import reduce
>>> def fn(x, y):
...     return x * 10 + y
...
>>> reduce(fn, [1, 3, 5, 7, 9])
13579

```

**map()和reduce()组合**

把str转换为int的函数
```
>>> from functools import reduce
>>> def fn(x, y):
...     return x * 10 + y
...
>>> def char2num(s):
...     return {'0': 0, '1': 1, '2': 2, '3': 3, '4': 4, '5': 5, '6': 6, '7': 7, '8': 8, '9': 9}[s]
...
>>> reduce(fn, map(char2num, '13579'))
13579
```
**filter()函数**

- **filter()** 函数接收两个参数，一个是函数，一个是Iterable
- map将传入的函数依次作用到序列的每个元素，并把结果作为新的惰性序列Iterator返回

在一个list中，删掉偶数，只保留奇数

```
def is_odd(n):
    return n % 2 == 1

list(filter(is_odd, [1, 2, 4, 5, 6, 9, 10, 15]))
# 结果: [1, 5, 9, 15]
```
一个序列中的空字符串删掉
```
def not_empty(s):
    return s and s.strip()

list(filter(not_empty, ['A', '', 'B', None, 'C', '  ']))
# 结果: ['A', 'B', 'C']
```

**sorted()函数**

sorted()函数也是一个高阶函数

数字list排序
```
>>> sorted([36, 5, -12, 9, -21])
[-21, -12, 5, 9, 36]
```
数字list按绝对值大小排序
```
>>> sorted([36, 5, -12, 9, -21], key=abs)
[5, 9, -12, -21, 36]
```
字符串list排序
```
>>> sorted(['bob', 'about', 'Zoo', 'Credit'])
['Credit', 'Zoo', 'about', 'bob']
```
字符串list忽略大小写排序
```
>>> sorted(['bob', 'about', 'Zoo', 'Credit'], key=str.lower)
['about', 'bob', 'Credit', 'Zoo']
```
字符串list忽略大小写反向排序
```
>>> sorted(['bob', 'about', 'Zoo', 'Credit'], key=str.lower, reverse=True)
['Zoo', 'Credit', 'bob', 'about']
```
## 05-02 返回函数

**函数作为返回值**

可变参数的求和：返回和
```
def calc_sum(*args):
    ax = 0
    for n in args:
        ax = ax + n
    return ax
```
```
>>> calc_sum(1, 3, 5, 7, 9)
25
```
可变参数的求和：返回求和的函数
```
def lazy_sum(*args):
    def sum():
        ax = 0
        for n in args:
            ax = ax + n
        return ax
    return sum
```

```
>>> f = lazy_sum(1, 3, 5, 7, 9)
>>> f
<function lazy_sum.<locals>.sum at 0x101c6ed90>
>>> f()
25
```

## 05-03 匿名函数

**计算f(x)=x^2**

函数
```
>>> def f(x):
...     return x * x
...
>>> r = map(f, [1, 2, 3, 4, 5, 6, 7, 8, 9])
>>> list(r)
[1, 4, 9, 16, 25, 36, 49, 64, 81]
```
匿名函数
```
>>> list(map(lambda x: x * x, [1, 2, 3, 4, 5, 6, 7, 8, 9]))
[1, 4, 9, 16, 25, 36, 49, 64, 81]
```
关键字lambda表示匿名函数，冒号前面的x表示函数参数

---
```
lambda x: x * x
```
相当于
```
def f(x):
    return x * x
```
---
特点

- 只能有一个表达式，不用写return，返回值就是该表达式的结果
- 函数没有名字，不必担心函数名冲突
- 匿名函数也是一个函数对象，也可以把匿名函数赋值给一个变量，再利用变量来调用该函数

```
->>> f = lambda x: x * x
>>> f
<function <lambda> at 0x101c6ef28>
>>> f(5)
25
```

- 匿名函数可以作为返回值返回

```
def build(x, y):
    return lambda: x * x + y * y
```

## 05-04 装饰器(Decorator)

作用：增强函数的功能

**示例：在函数调用前打印函数名**
定义装饰器
```
def log(func):
    def wrapper(*args, **kw):
        print(func.__name__)
        return func(*args, **kw)
    return wrapper
```
定义函数
```
@log
def now():
    print('2017-9-6')
```
调用函数
```
>>> now()
now():
2017-9-6
```
把@log放到now()函数的定义处，相当于执行了语句：
```
now = log(now)
```
## 05-05 偏函数(Partial function)
int()可以把字符串转换成整数
```
>>> int('12345')
12345
>>> int('12345', base=8)
5349
```
定义一个int2()的函数，默认把base=2传进去

```
def int2(x, base=2):
    return int(x, base)
```

```
>>> int2('1000000')
64
>>> int2('1010101')
85
```
用 **偏函数** 创建 **int2( )**
```
>>> import functools
>>> int2 = functools.partial(int, base=2)
>>> int2('1000000')
64
>>> int2('1010101')
85

```
作用：把一个函数的某些参数给固定住（也就是设置默认值），返回一个新的函数，调用这个新函数会更简单
# 06 Python 模块
一个 **.py** 文件就称之为一个 **模块（Module）**

模块的优点：

- 提高了代码的可维护性，代码不必从零开始，可以直接引用已经编写好的模块
- 避免函数名和变量名冲突

为了避免模块名冲突，可以用 **包（Package）** 来区分

- 每一个包目录下面都会有一个__init__.py的文件，这个文件必须存在，否则，Python就把这个目录当成普通目录，而不是一个包

## 06-01 使用模块
以内建的sys模块为例 自己编写hello模块
```
# -*- coding: utf-8 -*-

' a test module '

__author__ = 'Kevin Song'

import sys

def test():
    args = sys.argv
    if len(args)==1:
        print('Hello, world!')
    elif len(args)==2:
        print('Hello, %s!' % args[1])
    else:
        print('Too many arguments!')

if __name__=='__main__':
    test()
```
命令行
```
$ python3 hello.py
Hello, world!
$ python hello.py Kevin
Hello, Kevin!
```
交互环境
```
$ python3
Python 3.4.3 (v3.4.3:9b73f1c3e601, Feb 23 2015, 02:52:03) 
[GCC 4.2.1 (Apple Inc. build 5666) (dot 3)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> import hello
>>>
>>> hello.test()
Hello, world!
```

1. **\# \-\*\- coding: utf-8 \-\*\-**：注释，.py文件本身使用标准UTF-8编码
2. **' a test module '**：字符串，模块的文档注释，模块代码的第一个字符串都被视为模块的文档注释
3. **\_\_author__ = 'Kevin Song'**：作者名
4. **import sys：** 导入sys模块
5. sys模块有一个argv变量，用list存储了命令行的所有参数。argv至少有一个元素，因为第一个参数永远是该.py文件的名称
    - 运行python3 hello.py获得的sys.argv就是['hello.py']
    - 运行python3 hello.py Michael获得的sys.argv就是['hello.py', 'Michael]
6. **if \_\_name__=='\_\_main__':**：运行hello模块文件时，Python解释器把一个特殊变量__name__置为__main__，而如果在其他地方导入该hello模块时，if判断将失败，因此，这种if测试可以让一个模块通过命令行运行时执行一些额外的代码，最常见的就是运行测试

**权限**

- 公开变量&函数（public）：什么也不加
    - abc，x123，PI
- 特殊变量："__" 可以被直接引用，但是有特殊用途
    - \_\_author__，\_\_name__
- 私有变量&函数（private）："_" 不应该被直接引用
    - \_abc 虽然可以被访问，但是视为私有变量，不要随意访问
    - \_\_abc   可以强制访问（强烈不建议）。Python解释器对外把变量改成 **_类名__abc**

```
def _private_1(name):
    return 'Hello, %s' % name

def _private_2(name):
    return 'Hi, %s' % name

def greeting(name):
    if len(name) > 3:
        return _private_1(name)
    else:
        return _private_2(name)
```

## 06-02 安装第三方模块

包管理工具pip安装第三方模块

命令行安装第三方模块
```
pip install Pillow
```
使用第三方模块
```
>>> from PIL import Image
>>> im = Image.open('test.png')
>>> print(im.format, im.size, im.mode)
PNG (400, 300) RGB
>>> im.thumbnail((200, 100))
>>> im.save('thumb.jpg', 'JPEG')
```

**模块搜索路径**

试图加载一个模块时，Python会在指定的路径下搜索对应的.py文件，如果找不到，就会报错

```
>>> import mymodule
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ImportError: No module named mymodule
```
Python解释器会搜索当前目录、所有已安装的内置模块和第三方模块，搜索路径存放在sys模块的path变量中：
```
>>> import sys
>>> sys.path
['', '/Library/Frameworks/Python.framework/Versions/3.4/lib/python34.zip', '/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4', '/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4/plat-darwin', '/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4/lib-dynload', '/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4/site-packages']
```
添加自己的搜索目录的两种方法
1. 修改sys.path，添加要搜索的目录，运行时修改，运行结束后失效
```
>>> import sys
>>> sys.path.append('/Users/michael/my_py_scripts')
```
2. 设置环境变量PYTHONPATH，该环境变量的内容会被自动添加到模块搜索路径中

# 07 Python OOP

**面向过程** 的程序设计把计算机程序视为一系列的命令集合，即一组函数的顺序执行。为了简化程序设计，面向过程把函数继续切分为子函数，即把大块函数通过切割成小块函数来降低系统的复杂度

**面向对象** 的程序设计把计算机程序视为一组对象的集合，而每个对象都可以接收其他对象发过来的消息，并处理这些消息，计算机程序的执行就是一系列消息在各个对象之间传递


## 07-01 类(Class)和实例(Instance)
Python定义类（Class）
```
class Student(object):

    def __init__(self, name, score):
        self.name = name
        self.score = score

    def print_score(self):
        print('%s: %s' % (self.name, self.score))
```
Python创建对象并调用内部函数访问参数
```
kevin = Student('Kevin', 86)
kevin.print_score1()
```

**数据封装**

函数内部方法，除了第一个参数是self外，其他和普通函数一样。要调用一个方法，只需要在实例变量上直接调用，除了self不用传递，其他参数正常传入
```
class Student(object):
    ...

    def get_grade(self):
        if self.score >= 90:
            return 'A'
        elif self.score >= 60:
            return 'B'
        else:
            return 'C'
```
```
>>> kevin.get_grade()
'B'
```
外部函数访问参数
```
>>> def print_score(std):
...     print('%s: %s' % (std.name, std.score))
...
>>> print_score(kevin)
kevin: 86
```
## 07-02 访问限制
为了让内部name和score属性不被外部访问，需要通过两个下划线 **"__"** 私有化属性
```
class Student(object):

    def __init__(self, name, score):
        self.__name = name
        self.__score = score

    def print_score(self):
        print('%s: %s' % (self.__name, self.__score))
    def get_name(self):
        return self.__name
    def get_score(self):
        return self.__score
    def set_score(self, score):
        self.__score = score
```
**私有变量（private）**，只有内部可以访问，外部不能访问
```
>>> kevin = Student('Kevin', 86)
>>> kevin.__name
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'Student' object has no attribute '__name'
```
私有变量的好处：可以对参数做检查，避免传入无效的参数
```
def set_score(self, score):
        if 0 <= score <= 100:
            self.__score = score
        else:
            raise ValueError('bad score')
```

- \_\_xxx__     
    - 特殊变量，可以直接访问
- xxx           
    - 公开变量，可以直接访问
- _xxx
    - 私有变量，可以直接访问，但是按照规定，请不要随意访问
- \_\_xxx
    - 私有变量，不可以直接访问，可以通过_类名__xxx强制访问（不建议）

## 07-03 继承和多态

- 子类Dog和Cat **继承** 父类Animal
- 子类Dog和Cat **重写** 父类run方法

```
class Animal(object):
    def run(self):
        print('Animal is running...')
        
class Dog(Animal):
    def run(self):
        print('Dog is running...')

class Cat(Animal):
    def run(self):
        print('Cat is running...')
```
```
>>> dog = Dog()
>>> dog.run()
Dog is running...
>>> cat = Cat()
>>> cat.run()
Cat is running...
```
- **多态：** dog是Dog也是Animal 

多态的优点：新增一个Animal的子类，不必对run_twice()做任何修改，就会自动调用实际类型的run()方法

```
def run_twice(animal):
    animal.run()
    animal.run()
```
```
>>> run_twice(Dog())
Dog is running...
Dog is running...
>>> run_twice(Cat())
Cat is running...
Cat is running...
```
**“开闭”原则：**

对扩展开放：允许新增Animal子类；

对修改封闭：不需要修改依赖Animal类型的run_twice()等函数。

**静态语言 vs 动态语言**

静态语言（Java）：如果需要传入Animal类型，则传入的对象必须是Animal类型或者它的子类，否则，将无法调用run()方法

动态语言（Python）：不一定需要传入Animal类型。我们只需要保证传入的对象有一个run()方法就行，因此继承不是必须的

比如Timer也可以传入run_twice()方法
```
class Timer(object):
    def run(self):
        print('Start...')
```
这就是动态语言的“鸭子类型”，它并不要求严格的继承体系，一个对象只要“看起来像鸭子，走起路来像鸭子”，那它就可以被看做是鸭子

## 07-04 获取对象信息(type(), isinstance(), dir())

- type()
    - 返回对应Class类型
- isinstance()
    - 返回布尔类型
- dir()
    - 返回包含字符串的list

**使用type()**

判断对象类型
```
>>> type(123)
<class 'int'>
>>> type('str')
<class 'str'>
>>> type(None)
<type(None) 'NoneType'>
```
判断方法类型
```
>>> type(abs)
<class 'builtin_function_or_method'>
```
判断类类型
```
>>> type(a)
<class '__main__.Animal'>
```
type()函数返回的是对应的Class类型
```
>>> type(123)==type(456)
True
>>> type(123)==int
True
>>> type('abc')==type('123')
True
>>> type('abc')==str
True
>>> type('abc')==type(123)
False
```

**使用isinstance()**

```
>>> a = Animal()
>>> d = Dog()
>>> h = Husky()
```
```
>>> isinstance(h, Husky)
True
>>> isinstance(h, Animal)
True
```
判断一个变量是否是某些类型中的一种
```
>>> isinstance([1, 2, 3], (list, tuple))
True
>>> isinstance((1, 2, 3), (list, tuple))
True
```

**使用dir()**

```
>>> dir('ABC')
['__add__', '__class__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__gt__', '__hash__', '__init__', '__iter__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmod__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', 'capitalize', 'casefold', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'format_map', 'index', 'isalnum', 'isalpha', 'isdecimal', 'isdigit', 'isidentifier', 'islower', 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'maketrans', 'partition', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']
```
调用len()函数试图获取一个对象的长度时，实际上len()函数内部自动去调用该对象的__len__()方法

下面代码等价
```
>>> len('ABC')
3
>>> 'ABC'.__len__()
3

```

**直接操作对象状态**

- getattr(对象,'属性')
- setattr(对象,'属性')
- hasattr(对象,'属性')

```
>>> class MyObject(object):
...     def __init__(self):
...         self.x = 9
...     def power(self):
...         return self.x * self.x
...
>>> obj = MyObject()
```

```
>>> hasattr(obj, 'x') # 有属性'x'吗？
True
>>> obj.x
9
>>> hasattr(obj, 'y') # 有属性'y'吗？
False
>>> setattr(obj, 'y', 19) # 设置一个属性'y'
>>> hasattr(obj, 'y') # 有属性'y'吗？
True
>>> getattr(obj, 'y') # 获取属性'y'
19
>>> obj.y # 获取属性'y'
19
```

**注意**

如果可以直接写
```
sum = obj.x + obj.y
```
就不要写
```
sum = getattr(obj, 'x') + getattr(obj, 'y')
```
原因
```
def readImage(fp):
    if hasattr(fp, 'read'):
        return readData(fp)
    return None
```
从文件流fp中读取图像，首先判断该fp对象是否存在read方法

- 如果存在，则该对象是一个流
- 如果不存在，则无法读取。

## 07-05 实例属性和类属性
给实例绑定属性：通过self变量
```
class Student(object):
    def __init__(self, name):
        self.name = name

s = Student('Bob')
s.score = 90
```
给类绑定属性：直接在class中定义属性
```
class Student(object):
    name = 'Student'
```
测试
```
>>> class Student(object):
...     name = 'Student'
...
>>> s = Student() # 创建实例s
>>> print(s.name) # 打印name属性，因为实例并没有name属性，所以会继续查找class的name属性
Student
>>> print(Student.name) # 打印类的name属性
Student
>>> s.name = 'Michael' # 给实例绑定name属性
>>> print(s.name) # 由于实例属性优先级比类属性高，因此，它会屏蔽掉类的name属性
Michael
>>> print(Student.name) # 但是类属性并未消失，用Student.name仍然可以访问
Student
>>> del s.name # 如果删除实例的name属性
>>> print(s.name) # 再次调用s.name，由于实例的name属性没有找到，类的name属性就显示出来了
Student
```
**注意：**

不要把实例属性和类属性使用相同的名字，因为相同名称的实例属性将屏蔽掉类属性，但是当删除实例属性后，再使用相同的名称，访问到的将是类属性

# 08 Python 面向对象高级编程(OOP Advanced Features)

## 08-01 \_\_slots__

**给对象绑定属性和方法**

```
class Student(object):
    pass
```
给对象绑定属性
```
>>> s = Student()
>>> s.name = 'Kevin' # 动态给实例绑定一个属性
>>> print(s.name)
Kevin
```
给对象绑定方法
```
>>> def set_age(self, age): # 定义一个函数作为实例方法
...     self.age = age
...
>>> from types import MethodType
>>> s.set_age = MethodType(set_age, s) # 给实例绑定一个方法
>>> s.set_age(25) # 调用实例方法
>>> s.age # 测试结果
25
```
给实例绑定方法，对另一个实例不起作用
```
>>> s2 = Student() # 创建新的实例
>>> s2.set_age(25) # 尝试调用方法
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'Student' object has no attribute 'set_age'
```
给class绑定方法，所有实例都可用
```
>>> def set_score(self, score):
...     self.score = score
...
>>> Student.set_score = set_score
>>> s.set_score(100)
>>> s.score
100
>>> s2.set_score(99)
>>> s2.score
99
```

**限制给对象绑定属性和方法**

定义class的时候，定义一个特殊的 **\_\_slots\_\_** 变量，来限制该class实例能添加的属性
```
class Student(object):
    __slots__ = ('name', 'age') # 用tuple定义允许绑定的属性名称
```
只能绑定name和age
```
>>> s = Student() # 创建新的实例
>>> s.name = 'Michael' # 绑定属性'name'
>>> s.age = 25 # 绑定属性'age'
>>> s.score = 99 # 绑定属性'score'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'Student' object has no attribute 'score'
```
**注意：** \_\_slots__定义的属性仅对当前类实例起作用，对继承的子类不起作用
```
>>> class GraduateStudent(Student):
...     pass
...
>>> g = GraduateStudent()
>>> g.score = 9999
```
## 08-02 @property
直接修改属性，因为可以直接修改，所以不符合逻辑
```
s = Student()
s.score = 9999
```
为了限制score范围，可以用 **set_score()** 方法设置成绩，用 **get_score()** 获取成绩
```
class Student(object):

    def get_score(self):
         return self._score

    def set_score(self, value):
        if not isinstance(value, int):
            raise ValueError('score must be an integer!')
        if value < 0 or value > 100:
            raise ValueError('score must between 0 ~ 100!')
        self._score = value
```
```
>>> s = Student()
>>> s.set_score(60) # ok!
>>> s.get_score()
60
>>> s.set_score(9999)
Traceback (most recent call last):
  ...
ValueError: score must between 0 ~ 100!
```
上面的调用方法略显复杂，没有直接用属性这么直接简单，所以用 **@property** 装饰器把 **方法** 变成**属性**
```
class Student(object):

    @property
    def score(self):
        return self._score

    @score.setter
    def score(self, value):
        if not isinstance(value, int):
            raise ValueError('score must be an integer!')
        if value < 0 or value > 100:
            raise ValueError('score must between 0 ~ 100!')
        self._score = value
```

- @property：把一个getter方法变成属性
- @score.setter：把一个setter方法变成属性

```
>>> s = Student()
>>> s.score = 60 # OK，实际转化为s.set_score(60)
>>> s.score # OK，实际转化为s.get_score()
60
>>> s.score = 9999
Traceback (most recent call last):
  ...
ValueError: score must between 0 ~ 100!
```
还可以定义只读属性，只定义getter方法，不定义setter方法就是一个只读属性：
```
class Student(object):

    @property
    def birth(self):
        return self._birth

    @birth.setter
    def birth(self, value):
        self._birth = value

    @property
    def age(self):
        return 2015 - self._birth
```
## 08-03 多重继承
```
class Animal(object):
    pass

# 大类:
class Mammal(Animal):
    pass

class Bird(Animal):
    pass

# 各种动物:
class Dog(Mammal):
    pass

class Bat(Mammal):
    pass

class Parrot(Bird):
    pass

class Ostrich(Bird):
    pass

```
定义好Runnable和Flyable的类
```
class Runnable(object):
    def run(self):
        print('Running...')

class Flyable(object):
    def fly(self):
        print('Flying...')
```
给Dog加上Runnable，给Bat加上Flyable
```
class Dog(Mammal, Runnable):
    pass
class Bat(Mammal, Flyable):
    pass
```

**MixIn**

为了更好地看出继承关系：**Runnable** 和 **Flyable** 改为 **RunnableMixIn** 和 **FlyableMixIn**
```
class Dog(Mammal, RunnableMixIn, CarnivorousMixIn):
    pass
```
## 08-04 定制类(str, repr, iter, getattr, call)

**打印自定义信息：\_\_str\_\_**

定义Student类，打印实例
```
>>> class Student(object):
...     def __init__(self, name):
...         self.name = name
...
>>> print(Student('Michael'))
<__main__.Student object at 0x109afb190>
```

用 **\_\_str__** 打印自定义实例信息

```
>>> class Student(object):
...     def __init__(self, name):
...         self.name = name
...     def __str__(self):
...         return 'Student object (name: %s)' % self.name
...
>>> print(Student('Michael'))
Student object (name: Michael)
```

**直接显示变量自定义信息：\_\_repr__()**

```
>>> class Student(object):
...     def __init__(self, name):
...         self.name = name
...     def __str__(self):
...         return 'Student object (name: %s)' % self.name
...     __repr__ = __str__
...
>>> s = Student('Michael')
>>> s
Student object (name: Michael)
```
**\_\_iter\_\_**

如果一个类想被用于for ... in循环，类似list或tuple那样，就必须实现一个__iter__()方法，该方法返回一个迭代对象  

for循环就会不断调用该迭代对象的__next__()方法拿到循环的下一个值，直到遇到StopIteration错误时退出循环
```
class Fib(object):
    def __init__(self):
        self.a, self.b = 0, 1 # 初始化两个计数器a，b

    def __iter__(self):
        return self # 实例本身就是迭代对象，故返回自己

    def __next__(self):
        self.a, self.b = self.b, self.a + self.b # 计算下一个值
        if self.a > 100000: # 退出循环的条件
            raise StopIteration()
        return self.a # 返回下一个值
```

**\_\_getattr\_\_**

调用类的方法或属性时，如果不存在，就会报错
```
class Student(object):

    def __init__(self):
        self.name = 'Michael'

```
```
>>> s = Student()
>>> print(s.name)
Michael
>>> print(s.score)
Traceback (most recent call last):
  ...
AttributeError: 'Student' object has no attribute 'score'

```
要避免这个错误，写一个__getattr__()方法，动态返回一个属性

```
class Student(object):

    def __init__(self):
        self.name = 'Michael'

    def __getattr__(self, attr):
        if attr=='score':
            return 99
```
当调用不存在的属性时，比如score，Python解释器会试图调用__getattr__(self, 'score')来尝试获得属性
```
>>> s = Student()
>>> s.name
'Michael'
>>> s.score
99
```
> 只有在没有找到属性的情况下，才调用__getattr__，已有的属性，比如name，不会在__getattr__中查找

返回函数也完全可以

```
class Student(object):

    def __getattr__(self, attr):
        if attr=='age':
            return lambda: 25
```
```
>>> s.age()
25
```


**\_\_call\_\_**

直接对实例进行调用

```
class Student(object):
    def __init__(self, name):
        self.name = name

    def __call__(self):
        print('My name is %s.' % self.name)
```
```
>>> s = Student('Kevin')
>>> s() # self参数不要传入
My name is Kevin.
```
判断一个对象是否能被调用（是否是Callable对象）

```
>>> callable(Student())
True
>>> callable(max)
True
>>> callable([1, 2, 3])
False
>>> callable(None)
False
>>> callable('str')
False
```
## 08-05 枚举类
用大写变量定义的常量任然是变量
```
JAN = 1
FEB = 2
MAR = 3
```
解决方案：Enum类（为这样的枚举类型定义一个class类型，然后，每个常量都是class的一个唯一实例）

```
from enum import Enum

Month = Enum('Month', ('Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'))
```
直接使用Month.Jan来引用一个常量
```
>>> Month.Jan
<Month.Jan: 1>
```
枚举所有成员
```
>>> for name, member in Month.__members__.items():
... 	print(name, '=>', member, ',', member.value)
... 
Jan => Month.Jan , 1
Feb => Month.Feb , 2
Mar => Month.Mar , 3
Apr => Month.Apr , 4
May => Month.May , 5
Jun => Month.Jun , 6
Jul => Month.Jul , 7
Aug => Month.Aug , 8
Sep => Month.Sep , 9
Oct => Month.Oct , 10
Nov => Month.Nov , 11
Dec => Month.Dec , 12
>>> 
```
更精确地控制枚举类型，可以从Enum派生出自定义类
```
from enum import Enum, unique

@unique
class Weekday(Enum):
    Sun = 0 # Sun的value被设定为0
    Mon = 1
    Tue = 2
    Wed = 3
    Thu = 4
    Fri = 5
    Sat = 6
```
@unique装饰器可以帮助我们检查保证没有重复值

访问这些枚举类型可以有若干种方法
```
>>> day1 = Weekday.Mon
>>> print(day1)
Weekday.Mon
>>> print(Weekday.Tue)
Weekday.Tue
>>> print(Weekday['Tue'])
Weekday.Tue
>>> print(Weekday.Tue.value)
2
>>> print(day1 == Weekday.Mon)
True
>>> print(day1 == Weekday.Tue)
False
>>> print(Weekday(1))
Weekday.Mon
>>> print(day1 == Weekday(1))
True
>>> Weekday(7)
Traceback (most recent call last):
  ...
ValueError: 7 is not a valid Weekday
>>> for name, member in Weekday.__members__.items():
...     print(name, '=>', member)
...
Sun => Weekday.Sun
Mon => Weekday.Mon
Tue => Weekday.Tue
Wed => Weekday.Wed
Thu => Weekday.Thu
Fri => Weekday.Fri
Sat => Weekday.Sat
```
## 08-06 元类
**type() 作用一：** 查看一个类型或变量的类型

定义一个Hello的class
```
class Hello(object):
    def hello(self, name='world'):
        print('Hello, %s.' % name)
```

```
>>> from hello import Hello
>>> h = Hello()
>>> h.hello()
Hello, world.
>>> print(type(Hello))
<class 'type'>
>>> print(type(h))
<class 'hello.Hello'>
```
- Hello是一个class，它的类型就是type
- h是一个实例，它的类型就是class Hello

**type() 作用二：** 创建一个class对象

- type()函数依次传入3个参数
    1. class的名称
    2. 继承的父类集合（Python支持多重继承，如果只有一个父类，需要用tuple的单元素写法）
    3. class的方法名称与函数绑定

```
>>> def fn(self, name='world'): # 先定义函数
...     print('Hello, %s.' % name)
...
>>> Hello = type('Hello', (object,), dict(hello=fn)) # 创建Hello class
>>> h = Hello()
>>> h.hello()
Hello, world.
>>> print(type(Hello))
<class 'type'>
>>> print(type(h))
<class '__main__.Hello'>
```

**元类（metaclass）**

定义：类的类（类看做元类的实例）
作用：控制类的创建行为

# 09 Python 错误调试测试

## 09-01 错误处理(不同类型错误, 调用堆栈, 记录错误, 抛出错误)
**try...except...finally...**
```
try:
    print('try...')
    r = 10 / 0
    print('result:', r)
except ZeroDivisionError as e:
    print('except:', e)
finally:
    print('finally...')
print('END')
```
```
try...
except: division by zero
finally...
END
```

- 执行try内语句，如果出错，后续代码不会继续执行，直接跳转至except
- 执行except
- 执行finally

**多种类型的错误**

多个except捕获不同类型的错误

```
try:
    print('try...')
    r = 10 / int('a')
    print('result:', r)
except ValueError as e:
    print('ValueError:', e)
except ZeroDivisionError as e:
    print('ZeroDivisionError:', e)
finally:
    print('finally...')
print('END')
```
如果没有错误发生，可以在except语句块后面加一个else，当没有错误发生时，会自动执行else语句
```
try:
    print('try...')
    r = 10 / int('2')
    print('result:', r)
except ValueError as e:
    print('ValueError:', e)
except ZeroDivisionError as e:
    print('ZeroDivisionError:', e)
else:
    print('no error!')
finally:
    print('finally...')
print('END')
```

所有的错误类型都继承自 **BaseException**：https://docs.python.org/3/library/exceptions.html#exception-hierarchy

下面代码第二个except永远也捕获不到UnicodeError，因为UnicodeError是ValueError的子类，如果有，也被第一个except给捕获了

```
try:
    foo()
except ValueError as e:
    print('ValueError')
except UnicodeError as e:
    print('UnicodeError')
```

优点：不需要在每个可能出错的地方去捕获错误，只要在合适的层次去捕获错误就可以了

```
def foo(s):
    return 10 / int(s)

def bar(s):
    return foo(s) * 2

def main():
    try:
        bar('0')
    except Exception as e:
        print('Error:', e)
    finally:
        print('finally...')
```

**调用堆栈**

如果错误没有被捕获，它就会一直往上抛，最后被Python解释器捕获，打印一个错误信息，然后程序退出

```
# err.py:
def foo(s):
    return 10 / int(s)

def bar(s):
    return foo(s) * 2

def main():
    bar('0')

main()
```
```
$ python3 err.py
Traceback (most recent call last):
  File "err.py", line 11, in <module>
    main()
  File "err.py", line 9, in main
    bar('0')
  File "err.py", line 6, in bar
    return foo(s) * 2
  File "err.py", line 3, in foo
    return 10 / int(s)
ZeroDivisionError: division by zero
```

**记录错误**

Python内置的logging模块可以非常容易地记录错误信息

```
# err_logging.py

import logging

def foo(s):
    return 10 / int(s)

def bar(s):
    return foo(s) * 2

def main():
    try:
        bar('0')
    except Exception as e:
        logging.exception(e)

main()
print('END')
```
同样是出错，但程序打印完错误信息后会继续执行，并正常退出：
```
$ python3 err_logging.py
ERROR:root:division by zero
Traceback (most recent call last):
  File "err_logging.py", line 13, in main
    bar('0')
  File "err_logging.py", line 9, in bar
    return foo(s) * 2
  File "err_logging.py", line 6, in foo
    return 10 / int(s)
ZeroDivisionError: division by zero
END
```
**抛出错误**

- 定义错误的class
- 选择继承关系
- raise抛出一个错误的实例

```
# err_raise.py
class FooError(ValueError):
    pass

def foo(s):
    n = int(s)
    if n==0:
        raise FooError('invalid value: %s' % s)
    return 10 / n

foo('0')
```

一层一层抛出

```
# err_reraise.py

def foo(s):
    n = int(s)
    if n==0:
        raise ValueError('invalid value: %s' % s)
    return 10 / n

def bar():
    try:
        foo('0')
    except ValueError as e:
        print('ValueError!')
        raise

bar()
```

> raise语句如果不带参数，就会把当前错误原样抛出

在except中raise一个Error，可以把一种类型的错误转化成另一种类型

```
try:
    10 / 0
except ZeroDivisionError:
    raise ValueError('input error!')
```

注意：转换必须合理，不应该把一个IOError转换成毫不相干的ValueError

## 09-02 调试(直接打印, 断言assert, logging, pdb, )

**调试方法一：直接打印**

```
def foo(s):
    n = int(s)
    print('>>> n = %d' % n)
    return 10 / n

def main():
    foo('0')

main()
```
```
$ python3 err.py
>>> n = 0
Traceback (most recent call last):
  ...
ZeroDivisionError: integer division or modulo by zero
```
缺点：调试完毕需要手动删除print

**调试方法二：断言（assert）**

格式：assert 表达式1, 表达式2

- 表达式1：返回布尔型
- 表达式2：断言失败时输出的失败消息的字符串
```
def foo(s):
    n = int(s)
    assert n != 0, 'n is zero!'
    return 10 / n

def main():
    foo('0')
```

断言失败

```
$ python3 err.py
Traceback (most recent call last):
  ...
AssertionError: n is zero!
```
启动Python解释器时可以用-O参数来关闭assert，关闭后，所有的assert相当于pass

**调试方法三：logging**

和assert比，logging不会抛出错误，而且可以输出到文件

```
import logging
logging.basicConfig(level=logging.INFO)

s = '0'
n = int(s)
logging.info('n = %d' % n)
print(10 / n)
```
记录信息的级别

- debug
- info：level=logging.INFO
- warning
- error

**调试方法四：pdb**

作用：让程序以单步方式运行，可以随时查看运行状态

```
# err.py
s = '0'
n = int(s)
print(10 / n)
```
启动pdb
```
$ python3 -m pdb err.py
> /Users/michael/Github/learn-python3/samples/debug/err.py(2)<module>()
-> s = '0'

```
输入命令 **l** 查看代码

```
(Pdb) l
  1     # err.py
  2  -> s = '0'
  3     n = int(s)
  4     print(10 / n)
```
输入命令 **n** 单步执行代码
```
(Pdb) n
> /Users/michael/Github/learn-python3/samples/debug/err.py(3)<module>()
-> n = int(s)
(Pdb) n
> /Users/michael/Github/learn-python3/samples/debug/err.py(4)<module>()
-> print(10 / n)
```
输入命令 **p** 变量名 查看变量

```
(Pdb) p s
'0'
(Pdb) p n
0
```
输入命令 **q** 结束调试

```
(Pdb) q
```
**调试方法五：pdb.set_trace()**

不需要单步执行的pdb

- import pdb
- 在可能出错的地方放一个pdb.set_trace()（设置断点）
```
# err.py
import pdb

s = '0'
n = int(s)
pdb.set_trace() # 运行到这里会自动暂停
print(10 / n)
```
程序会自动在pdb.set_trace()暂停并进入pdb调试环境，可以用命令p查看变量，或者用命令c继续运行
```
$ python3 err.py 
> /Users/michael/Github/learn-python3/samples/debug/err.py(7)<module>()
-> print(10 / n)
(Pdb) p n
0
(Pdb) c
Traceback (most recent call last):
  File "err.py", line 7, in <module>
    print(10 / n)
ZeroDivisionError: division by zero
```
## 09-03 单元测试
类似于Codewars的attempt

定义：用来对一个模块、一个函数或者一个类来进行正确性检验的测试工作

编写Dict类：mydict.py
```
class Dict(dict):

    def __init__(self, **kw):
        super().__init__(**kw)

    def __getattr__(self, key):
        try:
            return self[key]
        except KeyError:
            raise AttributeError(r"'Dict' object has no attribute '%s'" % key)

    def __setattr__(self, key, value):
        self[key] = value
```
编写mydict_test.py
```
import unittest

from mydict import Dict

class TestDict(unittest.TestCase):

    def test_init(self):
        d = Dict(a=1, b='test')
        self.assertEqual(d.a, 1)
        self.assertEqual(d.b, 'test')
        self.assertTrue(isinstance(d, dict))

    def test_key(self):
        d = Dict()
        d['key'] = 'value'
        self.assertEqual(d.key, 'value')

    def test_attr(self):
        d = Dict()
        d.key = 'value'
        self.assertTrue('key' in d)
        self.assertEqual(d['key'], 'value')

    def test_keyerror(self):
        d = Dict()
        with self.assertRaises(KeyError):
            value = d['empty']

    def test_attrerror(self):
        d = Dict()
        with self.assertRaises(AttributeError):
            value = d.empty
```
每一类测试都需要编写一个test_xxx()方法，unittest.TestCase提供了很多内置的条件判断，调用这些方法就可以断言输出结果

**相等断言：assertEqual()**
```
self.assertEqual(abs(-1), 1) # 断言函数返回的结果与1相等
```
**抛出指定类型的Error断言：assertRaises()**

通过d['empty']访问不存在的key时，断言会抛出KeyError
```
with self.assertRaises(KeyError):
    value = d['empty']
```
通过d.empty访问不存在的key时，期待抛出AttributeError
```
with self.assertRaises(AttributeError):
    value = d.empty
```

**运行单元测试**

**方法一：** 在mydict_test.py的最后加上两行代码：
```
if __name__ == '__main__':
    unittest.main()
```
```
$ python3 mydict_test.py
```
**方法二：** 在命令行通过参数-m unittest直接运行单元测试
```
$ python3 -m unittest mydict_test
.....
----------------------------------------------------------------------
Ran 5 tests in 0.000s

OK

```
**setUp与tearDown**

setUp与tearDown这两个方法会分别在每调用一个测试方法的前后分别被执行

示例：测试需要启动一个数据库，这时，就可以在setUp()方法中连接数据库，在tearDown()方法中关闭数据库，这样，不必在每个测试方法中重复相同的代码：
```
class TestDict(unittest.TestCase):

    def setUp(self):
        print('setUp...')

    def tearDown(self):
        print('tearDown...')
```
## 09-04 文档测试
自动执行写在注释中的代码

```
# mydict2.py
class Dict(dict):
    '''
    Simple dict but also support access as x.y style.

    >>> d1 = Dict()
    >>> d1['x'] = 100
    >>> d1.x
    100
    >>> d1.y = 200
    >>> d1['y']
    200
    >>> d2 = Dict(a=1, b=2, c='3')
    >>> d2.c
    '3'
    >>> d2['empty']
    Traceback (most recent call last):
        ...
    KeyError: 'empty'
    >>> d2.empty
    Traceback (most recent call last):
        ...
    AttributeError: 'Dict' object has no attribute 'empty'
    '''
    def __init__(self, **kw):
        super(Dict, self).__init__(**kw)

    def __getattr__(self, key):
        try:
            return self[key]
        except KeyError:
            raise AttributeError(r"'Dict' object has no attribute '%s'" % key)

    def __setattr__(self, key, value):
        self[key] = value

if __name__=='__main__':
    import doctest
    doctest.testmod()
```
运行python3 mydict2.py：
```
$ python3 mydict2.py
```
什么输出也没有。说明编写的doctest运行都是正确的。如果程序有问题，比如把__getattr__()方法注释掉，再运行就会报错：
```
$ python3 mydict2.py
**********************************************************************
File "/Users/michael/Github/learn-python3/samples/debug/mydict2.py", line 10, in __main__.Dict
Failed example:
    d1.x
Exception raised:
    Traceback (most recent call last):
      ...
    AttributeError: 'Dict' object has no attribute 'x'
**********************************************************************
File "/Users/michael/Github/learn-python3/samples/debug/mydict2.py", line 16, in __main__.Dict
Failed example:
    d2.c
Exception raised:
    Traceback (most recent call last):
      ...
    AttributeError: 'Dict' object has no attribute 'c'
**********************************************************************
1 items had failures:
   2 of   9 in __main__.Dict
***Test Failed*** 2 failures.
```
当模块正常导入时，doctest不会被执行。只有在命令行直接运行时，才执行doctest。所以，不必担心doctest会在非测试环境下执行

# 10 Python IO

Output

- 浏览器 发送请求给 服务器
- 内存 写入 硬盘

Input

- 服务器 返回请求给 浏览器
- 内存 读取 硬盘

**CPU和硬盘速度不匹配**

- 同步IO
    - CPU 等待数据写入磁盘后，继续执行后续代码
- 异步IO
    - CPU 不等待数据写入磁盘，直接执行后续代码

现实案例：去McDonald买汉堡，汉堡要现做，需要等待五分钟

- 同步IO
    - 站在收银台前等了5分钟，拿到汉堡再去逛商场
- 异步IO
    - 先去逛商场
        - 服务员跑来找到我（回调模式）
        - 服务员发短信通知我（轮询模式）

## 10-01 文件读写

**读文件**

格式
```
f = open('文件名', '标示符')
```
1. **打开文件**
```
>>> f1 = open('/Users/kevin/test.txt', 'r')
```
标示符'r'表示打开文本文件 
```
>>> f2 = open('/Users/michael/test.jpg', 'rb')
```
标示符'rb'表示打开二进制文件（图片、视频等等）
```
>>> f3 = open('/Users/michael/gbk.txt', 'r', encoding='gbk')
```
加入encoding参数打开非UTF-8编码的文本文件

2. **读取文件**
```
>>> f1.read()
'Hello, world!'
>>> f2.read()
b'\xff\xd8\xff\xe1\x00\x18Exif\x00\x00...' # 十六进制表示的字节
>>> f3.read()
'测试'
```
3. 关闭文件
```
>>> f1.close()
>>> f2.close()
>>> f3.close()
```
文件读写时都有可能产生IOError，一旦出错，后面的f.close()就不会调用。所以，为了保证无论是否出错都能正确地关闭文件，使用try ... finally来实现：
```
try:
    f = open('/path/to/file', 'r')
    print(f.read())
finally:
    if f:
        f.close()
```
用with语句简化代码
```
with open('/path/to/file', 'r') as f:
    print(f.read())
```

- read()：读取较小的文件
- read(size)：读取不确定大小的文件
- readlines()：读取配置文件

```
for line in f.readlines():
    print(line.strip()) # 把末尾的'\n'删掉
```

> file-like Object：有read()方法的对象（file，内存的字节流，网络流，自定义流等等）

**写文件**
写文件和读文件是一样的，唯一区别是调用open()函数时，传入标识符'w'或者'wb'表示写文本文件或写二进制文件
```
>>> f = open('/Users/michael/test.txt', 'w')
>>> f.write('Hello, world!')
>>> f.close()
```
> 调用write()时不会立刻把数据写入磁盘，而是存放在内存中，只有调用close()方法时才会全部写入磁盘。

用with语句保险

```
with open('/Users/michael/test.txt', 'w') as f:
    f.write('Hello, world!')
```
要写入特定编码的文本文件，请给open()函数传入encoding参数，将字符串自动转换成指定编码。

## 10-02 StringIO和BytesIO

**StringIO**

在内存中读写str
```
>>> from io import StringIO
>>> f = StringIO()
>>> f.write('hello')
5
>>> f.write(' ')
1
>>> f.write('world!')
6
>>> print(f.getvalue())
hello world!
```
getvalue()方法用于获得写入后的str。

带初始化值的 StringIO
```
>>> from io import StringIO
>>> f = StringIO('Hello!\nHi!\nGoodbye!')
>>> while True:
...     s = f.readline()
...     if s == '':
...         break
...     print(s.strip())
...
Hello!
Hi!
Goodbye!
```

**BytesIO**

在内存中读写二进制数据
```
>>> from io import BytesIO
>>> f = BytesIO()
>>> f.write('中文'.encode('utf-8'))
6
>>> print(f.getvalue())
b'\xe4\xb8\xad\xe6\x96\x87'
```
带初始化值的 BytesIO
```
>>> from io import BytesIO
>>> f = BytesIO(b'\xe4\xb8\xad\xe6\x96\x87')
>>> f.read()
b'\xe4\xb8\xad\xe6\x96\x87'
```

## 10-03 操作文件和目录

os模块可以直接调用操作系统提供的接口函数

```
>>> import os
>>> os.name # 操作系统类型
'nt'
```

- posix：Linux、Unix、Mac OS X
- nt：Windows

uname()函数：获取详细的系统信息
```
>>> os.uname()
posix.uname_result(sysname='Darwin', nodename='MichaelMacPro.local', release='14.3.0', version='Darwin Kernel Version 14.3.0: Mon Mar 23 11:59:05 PDT 2015; root:xnu-2782.20.48~5/RELEASE_X86_64', machine='x86_64')
```
os.environ：操作系统中定义的环境变量
```
>>> os.environ
environ({'VERSIONER_PYTHON_PREFER_32_BIT': 'no', 'TERM_PROGRAM_VERSION': '326', 'LOGNAME': 'michael', 'USER': 'michael', 'PATH': '/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin:/opt/X11/bin:/usr/local/mysql/bin', ...})
```
os.environ.get('key')：获取某个环境变量的值
```
>>> os.environ.get('PATH')
'/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin:/opt/X11/bin:/usr/local/mysql/bin'
>>> os.environ.get('x', 'default')
'default'
```
**操作目录**

- 查看目录
    - 当前目录绝对路径：os.path.abspath('.')
- 创建目录
    1. 先把新目录的完整路径表示出来：os.path.join('/Users/michael', 'testdir')
    2. 创建新目录：os.mkdir('/Users/michael/testdir')
- 删除目录
    - os.rmdir('/Users/michael/testdir')
```
# 查看当前目录的绝对路径:
>>> os.path.abspath('.')
'/Users/michael'
# 在某个目录下创建一个新目录，首先把新目录的完整路径表示出来:
>>> os.path.join('/Users/michael', 'testdir')
'/Users/michael/testdir'
# 然后创建一个目录:
>>> os.mkdir('/Users/michael/testdir')
# 删掉一个目录:
>>> os.rmdir('/Users/michael/testdir')
```
拆分路径：os.path.split()
```
>>> os.path.split('/Users/michael/testdir/file.txt')
('/Users/michael/testdir', 'file.txt')
```

**操作文件**

拆分扩展名：os.path.splitext('文件名')
```
>>> os.path.splitext('/path/to/file.txt')
('/path/to/file', '.txt')
```
文件重命名：os.rename('原文件名', '新文件名')
```
>>> os.rename('test.txt', 'test.py')
```
文件删除：os.remove('文件名')
```
>>> os.remove('test.py')
```
os模块没有复制文件的函数。但是shutil函数有 **copyfile()** 函数

**过滤文件**

列出当前目录下的所有目录
```
>>> [x for x in os.listdir('.') if os.path.isdir(x)]
['.lein', '.local', '.m2', '.npm', '.ssh', '.Trash', '.vim', 'Applications', 'Desktop', ...]
```
列出所有的.py文件
```
>>> [x for x in os.listdir('.') if os.path.isfile(x) and os.path.splitext(x)[1]=='.py']
['apis.py', 'config.py', 'models.py', 'pymonitor.py', 'test_db.py', 'urls.py', 'wsgiapp.py']
```
## 10-04 序列化(pickling)和JSON

**序列化**

- 序列化：内存写入磁盘
- 反序列化：磁盘读取到内存

pickle模块实现**序列化**
```
>>> import pickle
>>> d = dict(name='Bob', age=20, score=88)
>>> pickle.dumps(d)
b'\x80\x03}q\x00(X\x03\x00\x00\x00ageq\x01K\x14X\x05\x00\x00\x00scoreq\x02KXX\x04\x00\x00\x00nameq\x03X\x03\x00\x00\x00Bobq\x04u.'
```
1. pickle.dumps()方法把任意对象序列化成一个bytes，
2. 写入磁盘
    - 方法一：pickle.dumps()把bytes写入文件
    - 方法二：方法pickle.dump()直接把对象序列化后写入一个file-like Object

```
>>> f = open('dump.txt', 'wb')
>>> pickle.dump(d, f)
>>> f.close()
```
pickle模块实现**反序列化**

1. open('文件名', 'rb')
2. 读入内存
    - pickle.loads()方法反序列化出对象
    - pickle.load()方法从一个file-like Object中直接反序列化出对象
```
>>> f = open('dump.txt', 'rb')
>>> d = pickle.load(f)
>>> f.close()
>>> d
{'age': 20, 'score': 88, 'name': 'Bob'}
```

**JSON**

JSON和Python内置的数据类型对应

JSON类型 | Python类型
---|---
{} | dict
[] | list
"string" | str
1234.56 | int或float
true/false | True/False
null | None

**Python对象变成一个JSON：**
```
>>> import json
>>> d = dict(name='Bob', age=20, score=88)
>>> json.dumps(d)
'{"age": 20, "score": 88, "name": "Bob"}'
```

- dumps()：方法返回一个str，内容就是标准的JSON。
- dump()：方法可以直接把JSON写入一个file-like Object。

**JSON变成一个Python对象：**
```
>>> json_str = '{"age": 20, "score": 88, "name": "Bob"}'
>>> json.loads(json_str)
{'age': 20, 'score': 88, 'name': 'Bob'}
```

- loads()：方法把JSON的字符串反序列化
- load()：从file-like Object中读取字符串并反序列化

**自定义对象转换成JSON**

```
import json

class Student(object):
    def __init__(self, name, age, score):
        self.name = name
        self.age = age
        self.score = score

s = Student('Kevin', 20, 88)
```
为Student专门写一个转换函数
```
def student2dict(std):
    return {
        'name': std.name,
        'age': std.age,
        'score': std.score
    }
```
Student实例首先被student2dict()函数转换成dict，然后再被顺利序列化为JSON：
```
>>> print(json.dumps(s, default=student2dict))
{"age": 20, "name": "Bob", "score": 88}
```
**JSON转换成自定义对象**
loads()方法首先转换出一个dict对象，然后，我们传入的object_hook函数负责把dict转换为Student实例：
```
def dict2student(d):
    return Student(d['name'], d['age'], d['score'])
```

```
>>> json_str = '{"age": 20, "score": 88, "name": "Bob"}'
>>> print(json.loads(json_str, object_hook=dict2student))
<__main__.Student object at 0x10cd3c190>
```
# 11 Python 进程和线程

进程（Process）：操作系统中执行的任务  

线程（Thread）：每个任务需要同时处理子任务

Python执行多任务解决方案

- 多进程：多个进程，每个进程运行一个线程
- 多线程：一个进程，这个进程运行多个线程
- 多进程+多线程：多个进程，每个进程运行多个线程（模型复杂，很少采用）

**多进程和多线程的区别：**

- 多进程：同一个变量，各自有一份拷贝存在于每个进程中，互不影响
- 多线程：所有变量都由所有线程共享，任何一个变量都可以被任何一个线程修改

## 11-01 多进程(Multiprocessing)

**Unix/Linux**

Unix/Linux操作系统提供了一个 **fork()** 系统调用，fork()调用一次，返回两次，操作系统自动把当前进程（**父进程**）复制了一份（**子进程**），然后，分别在父进程和子进程内返回

- 子进程返回0
- 父进程返回子进程的ID：os.getpid()
- 父进程的ID：getppid()
```
import os

print('Process (%s) start...' % os.getpid())
# Only works on Unix/Linux/Mac:
pid = os.fork()
if pid == 0:
    print('I am child process (%s) and my parent is %s.' % (os.getpid(), os.getppid()))
else:
    print('I (%s) just created a child process (%s).' % (os.getpid(), pid))
```
```
Process (876) start...
I (876) just created a child process (877).
I am child process (877) and my parent is 876.

```

**Windows**

multiprocessing模块提供了一个Process类来代表一个进程对象
```
from multiprocessing import Process
import os

# 子进程要执行的代码
def run_proc(name):
    print('Run child process %s (%s)...' % (name, os.getpid()))

if __name__=='__main__':
    print('Parent process %s.' % os.getpid())
    p = Process(target=run_proc, args=('test',))
    print('Child process will start.')
    p.start()
    p.join()
    print('Child process end.')
```
```
Parent process 928.
Process will start.
Run child process test (929)...
Process end.
```

创建子进程方式：p = Process(target=run_proc, args=('test',))

1. 创建一个Process实例
2. 传入一个执行函数和函数的参数
3. start()启动
4. join()方法可以等待子进程结束后再继续往下运行，通常用于进程间的同步

**Pool：批量创建子进程**

用进程池批量创建子进程：
```
from multiprocessing import Pool
import os, time, random

def long_time_task(name):
    print('Run task %s (%s)...' % (name, os.getpid()))
    start = time.time()
    time.sleep(random.random() * 3)
    end = time.time()
    print('Task %s runs %0.2f seconds.' % (name, (end - start)))

if __name__=='__main__':
    print('Parent process %s.' % os.getpid())
    p = Pool(4)
    for i in range(5):
        p.apply_async(long_time_task, args=(i,))
    print('Waiting for all subprocesses done...')
    p.close()
    p.join()
    print('All subprocesses done.')
```
```
Parent process 669.
Waiting for all subprocesses done...
Run task 0 (671)...
Run task 1 (672)...
Run task 2 (673)...
Run task 3 (674)...
Task 2 runs 0.14 seconds.
Run task 4 (673)...
Task 1 runs 0.27 seconds.
Task 3 runs 0.86 seconds.
Task 0 runs 1.41 seconds.
Task 4 runs 1.91 seconds.
All subprocesses done.
```
对Pool对象调用join()方法会等待所有子进程执行完毕，调用join()之前必须先调用close()，调用close()之后就不能继续添加新的Process了

**子进程**

用subprocess模块 **启动** 并且 **控制** 子进程的 **输入** 和 **输出**

运行命令nslookup www.python.org
```
import subprocess

print('$ nslookup www.python.org')
r = subprocess.call(['nslookup', 'www.python.org'])
print('Exit code:', r)
```
运行结果：
```
$ nslookup www.python.org
Server:        192.168.19.4
Address:    192.168.19.4#53

Non-authoritative answer:
www.python.org    canonical name = python.map.fastly.net.
Name:    python.map.fastly.net
Address: 199.27.79.223

Exit code: 0
```
communicate()方法输入：
```
import subprocess

print('$ nslookup')
p = subprocess.Popen(['nslookup'], stdin=subprocess.PIPE, stdout=subprocess.PIPE, stderr=subprocess.PIPE)
output, err = p.communicate(b'set q=mx\npython.org\nexit\n')
print(output.decode('utf-8'))
print('Exit code:', p.returncode)
```
运行结果：
```
$ nslookup
Server:        192.168.19.4
Address:    192.168.19.4#53

Non-authoritative answer:
python.org    mail exchanger = 50 mail.python.org.

Authoritative answers can be found from:
mail.python.org    internet address = 82.94.164.166
mail.python.org    has AAAA address 2001:888:2000:d::a6


Exit code: 0
```
**进程间通信**

multiprocessing模块包装了底层的机制，提供了Queue、Pipes等多种方式来交换数据

父进程中创建两个子进程，一个往Queue里写数据，一个从Queue里读数据：

```
from multiprocessing import Process, Queue
import os, time, random

# 写数据进程执行的代码:
def write(q):
    print('Process to write: %s' % os.getpid())
    for value in ['A', 'B', 'C']:
        print('Put %s to queue...' % value)
        q.put(value)
        time.sleep(random.random())

# 读数据进程执行的代码:
def read(q):
    print('Process to read: %s' % os.getpid())
    while True:
        value = q.get(True)
        print('Get %s from queue.' % value)

if __name__=='__main__':
    # 父进程创建Queue，并传给各个子进程：
    q = Queue()
    pw = Process(target=write, args=(q,))
    pr = Process(target=read, args=(q,))
    # 启动子进程pw，写入:
    pw.start()
    # 启动子进程pr，读取:
    pr.start()
    # 等待pw结束:
    pw.join()
    # pr进程里是死循环，无法等待其结束，只能强行终止:
    pr.terminate()
```
```
Process to write: 50563
Put A to queue...
Process to read: 50564
Get A from queue.
Put B to queue...
Get B from queue.
Put C to queue...
Get C from queue.
```

## 11-02 多线程

一个进程里的多个线程实现多任务

Python的标准库提供了两个模块

- \_thread（低级模块）
- threading（高级模块）：对_thread进行了封装

启动一个线程就是把一个函数传入并创建Thread实例，然后调用start()开始执行：

格式：

```
t = threading.Thread(target='需要运行的方法名', args=('方法参数,'), name='自定义线程名称')
t.start()
t.join()
```

示例：
```
import time, threading

# 新线程执行的代码:
def loop():
    print('thread %s is running...' % threading.current_thread().name)
    n = 0
    while n < 5:
        n = n + 1
        print('thread %s >>> %s' % (threading.current_thread().name, n))
        time.sleep(1)
    print('thread %s ended.' % threading.current_thread().name)

print('thread %s is running...' % threading.current_thread().name)
t = threading.Thread(target=loop, name='LoopThread')
t.start()
t.join()
print('thread %s ended.' % threading.current_thread().name)
```
```
thread MainThread is running...
thread LoopThread is running...
thread LoopThread >>> 1
thread LoopThread >>> 2
thread LoopThread >>> 3
thread LoopThread >>> 4
thread LoopThread >>> 5
thread LoopThread ended.
thread MainThread ended.
```

- threading 模块
    - threading.current_thread()：返回当前线程实例
        - threading.current_thread().name：返回当前线程实例的name

**Lock**
不加Lock的多线程在操作同一数据时会把数据改乱

```
import time, threading

# 假定这是你的银行存款:
balance = 0

def change_it(n):
    # 先存后取，结果应该为0:
    global balance
    balance = balance + n
    balance = balance - n

def run_thread(n):
    for i in range(100000):
        change_it(n)

t1 = threading.Thread(target=run_thread, args=(5,))
t2 = threading.Thread(target=run_thread, args=(8,))
t1.start()
t2.start()
t1.join()
t2.join()
print(balance)
```

数据改乱根本原因：

- 线程交替运行
- 操作同一变量（balance）

```
初始值 balance = 0

t1: x1 = balance + 5  # x1 = 0 + 5 = 5

t2: x2 = balance + 8  # x2 = 0 + 8 = 8
t2: balance = x2      # balance = 8

t1: balance = x1      # balance = 5
t1: x1 = balance - 5  # x1 = 5 - 5 = 0
t1: balance = x1      # balance = 0

t2: x2 = balance - 8  # x2 = 0 - 8 = -8
t2: balance = x2   # balance = -8

结果 balance = -8
```

**threading.Lock()：** 拿到锁的线程才可以运行方法

```
balance = 0
lock = threading.Lock()

def run_thread(n):
    for i in range(100000):
        # 先要获取锁:
        lock.acquire()
        try:
            # 放心地改吧:
            change_it(n)
        finally:
            # 改完了一定要释放锁:
            lock.release()
```

- lock.acquire()获取锁
- 用try-finally确保锁一定可以释放，否则造成死锁

**多核CPU**

- 多核CPU中，一个死循环线程会导致100%占用一个CPU
- 两个死循环线程，在多核CPU中，可以监控到会占用200%的CPU
- 以此类推

死循环示例

```
import threading, multiprocessing

def loop():
    x = 0
    while True:
        x = x ^ 1

for i in range(multiprocessing.cpu_count()):
    t = threading.Thread(target=loop)
    t.start()
```

- C、C++或Java来改写相同的死循环，直接可以把全部核心跑满，4核就跑到400%，8核就跑到800%
- Python最多102%
    - 解释器执行代码时，有一个GIL锁：Global Interpreter Lock。任何Python线程执行前，必须先获得GIL锁，然后，每执行100条字节码，解释器就自动释放GIL锁，让别的线程有机会执行。

所以，多线程在Python中只能交替执行，即使100个线程跑在100核CPU上，也只能用到1个核

## 11-03 ThreadLocal

局部变量优点：全局变量的修改必须加锁，因此一个线程使用自己的局部变量比使用全局变量好  

局部变量缺点：函数调用的时候，传递起来很麻烦，如下

```
def process_student(name):
    std = Student(name)
    # std是局部变量，但是每个函数都要用它，因此必须传进去：
    do_task_1(std)
    do_task_2(std)

def do_task_1(std):
    do_subtask_1(std)
    do_subtask_2(std)

def do_task_2(std):
    do_subtask_2(std)
    do_subtask_2(std)
```

解决方案：ThreadLocal

```
import threading

# 创建全局ThreadLocal对象:
local_school = threading.local()

def process_student():
    # 获取当前线程关联的student:
    std = local_school.student
    print('Hello, %s (in %s)' % (std, threading.current_thread().name))

def process_thread(name):
    # 绑定ThreadLocal的student:
    local_school.student = name
    process_student()

t1 = threading.Thread(target= process_thread, args=('Alice',), name='Thread-A')
t2 = threading.Thread(target= process_thread, args=('Bob',), name='Thread-B')
t1.start()
t2.start()
t1.join()
t2.join()
```
```
Hello, Alice (in Thread-A)
Hello, Bob (in Thread-B)
```

全局变量local_school就是一个ThreadLocal对象。Thread对它都可以读写student属性，但互不影响。

- local_school相当于全局变量
- local_school.student都是线程的局部变量

## 11-04 进程vs线程

Master-Worker模式

- Master负责分配任务（一）
- Worker负责执行任务（多）

实现Master-Worker

- 多进程实现Master-Worker，主进程就是Master，其他进程就是Worker
- 多线程实现Master-Worker，主线程就是Master，其他线程就是Worker

优缺点

- 多进程
    - 优点：稳定性高
        - 子进程崩溃了不会影响主进程和其他子进程
    - 缺点：创建代价大
        - Unix/Linux系统下用fork调用还行
        - Windows下创建进程开销巨大
        - 操作系统能同时运行的进程数也是有限

- 多线程
    - 优点：速度比多进程快（只快一点点）
    - 缺点：稳定性差
        - 一个线程挂掉都可能直接造成整个进程崩溃

**线程切换**

单任务模型（批处理任务模型）

- 处理完 **A任务** 处理 **B任务**
- 处理完 **B任务** 处理 **C任务**
- 处理完 **C任务** 结束

多任务模型

- 处理 **A任务** 1秒
    - 保存现场：保存 **A任务** CPU寄存器状态、内存页等
    - 准备新环境：恢复 **B任务** 的寄存器状态，切换内存页等
- 处理 **B任务** 1秒
    - 保存现场：保存 **B任务** CPU寄存器状态、内存页等
    - 准备新环境：恢复 **C任务** 的寄存器状态，切换内存页等
- 处理 **C任务** 1秒
    - 保存现场：保存 **C任务** CPU寄存器状态、内存页等
    - 准备新环境：恢复 **B任务** 的寄存器状态，切换内存页等
- 处理 **B任务** 1秒
- ...

切换过程虽然很快，但需要耗费时间。如果有几千个任务同时进行，操作系统可能就主要忙着切换任务，根本没有多少时间去执行任务，这种情况最常见的就是硬盘狂响，点窗口无反应，系统处于假死状态

**计算密集型任务**

- 进行大量的计算，消耗CPU资源，比如计算圆周率、对视频进行高清解码等等，全靠CPU的运算能力
- 任务越多，花在任务切换的时间就越多，CPU执行任务的效率就越低
- 最高效地利用CPU，计算密集型任务同时进行的数量应当等于CPU的核心数
计算密集型任务由于主要消耗CPU资源，因此，代码运行效率至关重要。Python这样的脚本语言运行效率很低，完全不适合计算密集型任务。对于计算密集型任务，最好用C语言编写。

**IO密集型**

- CPU消耗很少，任务的大部分时间都在等待IO操作完成（因为IO的速度远远低于CPU和内存的速度）
- 任务越多，CPU效率越高，但也有一个限度

IO密集型任务执行期间，99%的时间都花在IO上，花在CPU上的时间很少，因此，用运行速度极快的C语言替换用Python这样运行速度极低的脚本语言，完全无法提升运行效率。对于IO密集型任务，最合适的语言就是开发效率最高（代码量最少）的语言，脚本语言是首选，C语言最差。

**异步IO**

多进程模型或者多线程模型来支持多任务并发执行

## 11-05 分布式进程

- Process更稳定，可以分布到多台机器上
- Thread最多只能分布到同一台机器的多个CPU上

Python的multiprocessing模块的managers子模块支持把多进程分布到多台机器上。一个服务进程可以作为调度者，将任务分布到其他多个进程中，依靠网络通信

服务进程负责启动Queue，把Queue注册到网络上，然后往Queue里面写入任务：

```
# task_master.py

import random, time, queue
from multiprocessing.managers import BaseManager

# 发送任务的队列:
task_queue = queue.Queue()
# 接收结果的队列:
result_queue = queue.Queue()

# 从BaseManager继承的QueueManager:
class QueueManager(BaseManager):
    pass

# 把两个Queue都注册到网络上, callable参数关联了Queue对象:
QueueManager.register('get_task_queue', callable=lambda: task_queue)
QueueManager.register('get_result_queue', callable=lambda: result_queue)
# 绑定端口5000, 设置验证码'abc':
manager = QueueManager(address=('', 5000), authkey=b'abc')
# 启动Queue:
manager.start()
# 获得通过网络访问的Queue对象:
task = manager.get_task_queue()
result = manager.get_result_queue()
# 放几个任务进去:
for i in range(10):
    n = random.randint(0, 10000)
    print('Put task %d...' % n)
    task.put(n)
# 从result队列读取结果:
print('Try get results...')
for i in range(10):
    r = result.get(timeout=10)
    print('Result: %s' % r)
# 关闭:
manager.shutdown()
print('master exit.')
```
另一台机器上启动任务进程（本机上启动也可以）：

```
# task_worker.py

import time, sys, queue
from multiprocessing.managers import BaseManager

# 创建类似的QueueManager:
class QueueManager(BaseManager):
    pass

# 由于这个QueueManager只从网络上获取Queue，所以注册时只提供名字:
QueueManager.register('get_task_queue')
QueueManager.register('get_result_queue')

# 连接到服务器，也就是运行task_master.py的机器:
server_addr = '127.0.0.1'
print('Connect to server %s...' % server_addr)
# 端口和验证码注意保持与task_master.py设置的完全一致:
m = QueueManager(address=(server_addr, 5000), authkey=b'abc')
# 从网络连接:
m.connect()
# 获取Queue的对象:
task = m.get_task_queue()
result = m.get_result_queue()
# 从task队列取任务,并把结果写入result队列:
for i in range(10):
    try:
        n = task.get(timeout=1)
        print('run task %d * %d...' % (n, n))
        r = '%d * %d = %d' % (n, n, n*n)
        time.sleep(1)
        result.put(r)
    except Queue.Empty:
        print('task queue is empty.')
# 处理结束:
print('worker exit.')
```
启动task_master.py服务进程：
```
$ python3 task_master.py 
Put task 3411...
Put task 1605...
Put task 1398...
Put task 4729...
Put task 5300...
Put task 7471...
Put task 68...
Put task 4219...
Put task 339...
Put task 7866...
Try get results...
```
task_master.py进程发送完任务后，开始等待result队列的结果。现在启动task_worker.py进程：

```
$ python3 task_worker.py
Connect to server 127.0.0.1...
run task 3411 * 3411...
run task 1605 * 1605...
run task 1398 * 1398...
run task 4729 * 4729...
run task 5300 * 5300...
run task 7471 * 7471...
run task 68 * 68...
run task 4219 * 4219...
run task 339 * 339...
run task 7866 * 7866...
worker exit.

```
这就是一个简单但真正的分布式计算

Queue对象存储在task_master.py进程中

而Queue之所以能通过网络访问，就是通过QueueManager实现的。由于QueueManager管理的不止一个Queue，所以，要给每个Queue的网络调用接口起个名字，比如get_task_queue。

authkey有什么用？这是为了保证两台机器正常通信，不被其他机器恶意干扰。如果task_worker.py的authkey和task_master.py的authkey不一致，肯定连接不上。

# 12 Python 正则表达式

## 12-01 正则基础

作用：匹配字符串

设计思想：用描述性的语言给字符串定义一个规则

- 符合规则，则“匹配”
- 不符合规则，则不“匹配”

匹配精确字符

- **\d**：匹配一个数字
    - **'00\d'** 可以匹配 **'007'**，但无法匹配 **'00A'**；
    - **'\d\d\d'** 可以匹配 **'010'**；
- **\w**：匹配一个字母或数字
    - **'\w\w\d'** 可以匹配 **'py3'**
- **\s**：匹配一个空格
- **.** ：匹配任意字符
    - **'py.'** 可以匹配'pyc'、'pyo'、'py!'

匹配变长字符

- **\*** ：表示任意个字符（包括0个）
- **+** ：表示至少一个字符
- **?** ：表示0个或1个字符
- **{ n }**：表示n个字符
- **{ n, m }** ：表示n-m个字符

**例**：任意个空格隔开的带区号的电话号码：\d{3}\s+\d{3,8}

- \d{3}表示匹配3个数字，例如'010'；
- \s可以匹配一个空格（也包括Tab等空白符），所以\s+表示至少有一个空格，例如匹配' '，' '等；
- \d{3,8}表示3-8个数字，例如'1234567'

**[ ]** 表示范围

- **[0-9a-zA-Z\\_]** 可以匹配一个数字、字母或者下划线；
- **[0-9a-zA-Z\\_]+** 可以匹配至少由一个数字、字母或者下划线组成的字符串，比如'a100'，'0_Z'，'Py3000'等等；
- **[a-zA-Z\\_][0-9a-zA-Z\\_]*\** 可以匹配由字母或下划线开头，后接任意个由一个数字、字母或者下划线组成的字符串，也就是Python合法的变量；
- **[a-zA-Z\\_][0-9a-zA-Z\\_]{0, 19}**更精确地限制了变量的长度是1-20个字符（前面1个字符+后面最多19个字符）

或

- **A|B** 可以匹配A或B，所以(P|p)ython可以匹配'Python'或者'python'。
- **^** 表示行的开头，^\d表示必须以数字开头。
- **$** 表示行的结束，\d$表示必须以数字结束。

re模块

## 12-02 re模块

re模块的match()方法判断是否匹配

- 匹配成功，返回一个Match对象
- 匹配失败，返回None
```
>>> import re
>>> re.match(r'^\d{3}\-\d{3,8}$', '010-12345')
<_sre.SRE_Match object; span=(0, 9), match='010-12345'>
>>> re.match(r'^\d{3}\-\d{3,8}$', '010 12345')
>>>
```
常见的判断方法：
```
test = '用户输入的字符串'
if re.match(r'正则表达式', test):
    print('ok')
else:
    print('failed')
```

## 12-03 正则进阶(切分字符串, 分组, 贪婪匹配, 编译)

**切分字符串**

正常用**空格**切分
```
>>> 'a b   c'.split(' ')
['a', 'b', '', '', 'c']
```
正则用**空格**切分
```
>>> re.split(r'\s+', 'a b   c')
['a', 'b', 'c']
```
正则用**空格**和 **，** 切分
```
>>> re.split(r'[\s\,]+', 'a,b, c  d')
['a', 'b', 'c', 'd']
```
正则用**空格**和 **，** 和 **;** 切分
```
>>> re.split(r'[\s\,\;]+', 'a,b;; c  d')
['a', 'b', 'c', 'd']
```

**分组（Group）**

^(\d{3})-(\d{3,8})$分别定义了两个组，可以直接从匹配的字符串中提取出区号和本地号码：
```
>>> m = re.match(r'^(\d{3})-(\d{3,8})$', '010-12345')
>>> m
<_sre.SRE_Match object; span=(0, 9), match='010-12345'>
>>> m.group(0)
'010-12345'
>>> m.group(1)
'010'
>>> m.group(2)
'12345'
```

**贪婪匹配**

正则匹配默认**贪婪匹配**

```
>>> re.match(r'^(\d+)(0*)$', '102300').groups()
('102300', '')
```
由于\d+采用贪婪匹配，直接把后面的0全部匹配了，结果0*只能匹配空字符串

必须让\d+采用非贪婪匹配（也就是尽可能少匹配），才能把后面的0匹配出来，加个?就可以让\d+采用非贪婪匹配：

```
>>> re.match(r'^(\d+?)(0*)$', '102300').groups()
('1023', '00')
```

**编译**

Python中使用正则表达式时，re模块内部会干两件事情：

- 编译正则表达式，如果正则表达式的字符串本身不合法，会报错；
- 用编译后的正则表达式去匹配字符串。

出于效率的考虑，预编译该正则表达式，重复使用时不需要编译
```
>>> import re
# 编译:
>>> re_telephone = re.compile(r'^(\d{3})-(\d{3,8})$')
# 使用：
>>> re_telephone.match('010-12345').groups()
('010', '12345')
>>> re_telephone.match('010-8086').groups()
('010', '8086')
```
# 13 Python 常用内建模块

## 13-01 datetime(timestamp转换, str转换, datetime加减, 时区转换)
datetime是Python处理日期和时间的标准库

**获取当前日期和时间**
```
>>> from datetime import datetime
>>> now = datetime.now() # 获取当前datetime
>>> print(now)
2015-05-18 16:28:07.198690
>>> print(type(now))
<class 'datetime.datetime'>
```
datetime.now()返回当前日期和时间，其类型是datetime

**获取指定日期和时间**
```
>>> from datetime import datetime
>>> dt = datetime(2015, 4, 19, 12, 20) # 用指定日期时间创建datetime
>>> print(dt)
2015-04-19 12:20:00
```
**datetime & timestamp**
```
timestamp = 0 = 1970-1-1 00:00:00 UTC+0:00
```
对应的北京时间是：
```
timestamp = 0 = 1970-1-1 08:00:00 UTC+8:00
```
**datetime转换为timestamp**

调用 **timestamp()** 方法：
```
>>> from datetime import datetime
>>> dt = datetime(2015, 4, 19, 12, 20) # 用指定日期时间创建datetime
>>> dt.timestamp() # 把datetime转换为timestamp
1429417200.0
```
**timestamp转换为datetime**

调用 **fromtimestamp()** 方法：
```
>>> from datetime import datetime
>>> t = 1429417200.0
>>> print(datetime.fromtimestamp(t)) # 本地时间
2015-04-19 12:20:00
>>> print(datetime.utcfromtimestamp(t)) # UTC时间
2015-04-19 04:20:00
```
**str转换为datetime**

调用 **datetime.strptime()** 方法：
```
>>> from datetime import datetime
>>> cday = datetime.strptime('2015-6-1 18:19:59', '%Y-%m-%d %H:%M:%S')
>>> print(cday)
2015-06-01 18:19:59
```
**datetime转换为str**

调用 **strftime()** 方法：
```
>>> from datetime import datetime
>>> now = datetime.now()
>>> print(now.strftime('%a, %b %d %H:%M'))
Mon, May 05 16:28
```

**datetime加减**

```
>>> from datetime import datetime, timedelta
>>> now = datetime.now()
>>> now
datetime.datetime(2015, 5, 18, 16, 57, 3, 540997)
>>> now + timedelta(hours=10)
datetime.datetime(2015, 5, 19, 2, 57, 3, 540997)
>>> now - timedelta(days=1)
datetime.datetime(2015, 5, 17, 16, 57, 3, 540997)
>>> now + timedelta(days=2, hours=12)
datetime.datetime(2015, 5, 21, 4, 57, 3, 540997)
```

**时区转换**

```
# 拿到UTC时间，并强制设置时区为UTC+0:00:
>>> utc_dt = datetime.utcnow().replace(tzinfo=timezone.utc)
>>> print(utc_dt)
2015-05-18 09:05:12.377316+00:00
# astimezone()将转换时区为北京时间:
>>> bj_dt = utc_dt.astimezone(timezone(timedelta(hours=8)))
>>> print(bj_dt)
2015-05-18 17:05:12.377316+08:00
# astimezone()将转换时区为东京时间:
>>> tokyo_dt = utc_dt.astimezone(timezone(timedelta(hours=9)))
>>> print(tokyo_dt)
2015-05-18 18:05:12.377316+09:00
# astimezone()将bj_dt转换时区为东京时间:
>>> tokyo_dt2 = bj_dt.astimezone(timezone(timedelta(hours=9)))
>>> print(tokyo_dt2)
2015-05-18 18:05:12.377316+09:00
```
## 13-02 collections(namedtuple, deque, defaultdict, OrderedDict, Counter)
Python内建的一个集合模块，提供了许多有用的集合类

**amedtuple**

namedtuple函数：创建一个自定义的tuple对象，并且规定了tuple元素的个数，并可以用属性而不是索引来引用tuple的某个元素

定义二维坐标：
```
>>> from collections import namedtuple
>>> Point = namedtuple('Point', ['x', 'y'])
>>> p = Point(1, 2)
>>> p.x
1
>>> p.y
2
```
定义一个圆：
```
# namedtuple('名称', [属性list]):
Circle = namedtuple('Circle', ['x', 'y', 'r'])
```

**deque**

高效实现插入和删除操作的双向列表，适合用于队列和栈：
```
>>> from collections import deque
>>> q = deque(['a', 'b', 'c'])
>>> q.append('x')
>>> q.appendleft('y')
>>> q
deque(['y', 'a', 'b', 'c', 'x'])
```

- append()
- pop()
- appendleft()
- popleft()

可以非常高效地往头部添加或删除元素。

**defaultdict**

defaultdict：key不存在时，不会抛出KeyError，返回一个默认值
```
>>> from collections import defaultdict
>>> dd = defaultdict(lambda: 'N/A')
>>> dd['key1'] = 'abc'
>>> dd['key1'] # key1存在
'abc'
>>> dd['key2'] # key2不存在，返回默认值
'N/A'
```

**OrderedDict**

Key有顺序的dict

```
>>> from collections import OrderedDict
>>> d = dict([('a', 1), ('b', 2), ('c', 3)])
>>> d # dict的Key是无序的
{'a': 1, 'c': 3, 'b': 2}
>>> od = OrderedDict([('a', 1), ('b', 2), ('c', 3)])
>>> od # OrderedDict的Key是有序的
OrderedDict([('a', 1), ('b', 2), ('c', 3)])
```
OrderedDict实现一个FIFO（先进先出）的dict，当容量超出限制时，先删除最早添加的Key：
```
from collections import OrderedDict

class LastUpdatedOrderedDict(OrderedDict):

    def __init__(self, capacity):
        super(LastUpdatedOrderedDict, self).__init__()
        self._capacity = capacity

    def __setitem__(self, key, value):
        containsKey = 1 if key in self else 0
        if len(self) - containsKey >= self._capacity:
            last = self.popitem(last=False)
            print('remove:', last)
        if containsKey:
            del self[key]
            print('set:', (key, value))
        else:
            print('add:', (key, value))
        OrderedDict.__setitem__(self, key, value)
```

**Counter**

计数器，统计字符出现的个数：
```
>>> from collections import Counter
>>> c = Counter()
>>> for ch in 'programming':
...     c[ch] = c[ch] + 1
...
>>> c
Counter({'g': 2, 'm': 2, 'r': 2, 'a': 1, 'i': 1, 'o': 1, 'n': 1, 'p': 1})
```

## 13-03 base64
Base64是一种用64个字符来表示任意二进制数据的方法

原理：

- 包含64个字符的数组：
```
['A', 'B', 'C', ... 'a', 'b', 'c', ... '0', '1', ... '+', '/']
```
- 对二进制数据进行处理，每3个字节一组，一共是3x8=24bit，划为4组，每组正好6个bit
- 得到4个数字作为索引，然后查表，获得相应的4个字符，就是编码后的字符串

Base64编码会把3字节的二进制数据编码为4字节的文本数据，长度增加33%，好处是编码后的文本数据可以在邮件正文、网页等直接显示

> 当要编码的二进制数据不是3的倍数，最后会剩下1个或2个字节时，Base64用\x00字节在末尾补足后，再在编码的末尾加上1个或2个=号，表示补了多少字节，解码的时候，会自动去掉

```
>>> import base64
>>> base64.b64encode(b'binary\x00string')
b'YmluYXJ5AHN0cmluZw=='
>>> base64.b64decode(b'YmluYXJ5AHN0cmluZw==')
b'binary\x00string'
```
url safe"的base64编码（把字符+和/分别变成-和_）
```
>>> base64.b64encode(b'i\xb7\x1d\xfb\xef\xff')
b'abcd++//'
>>> base64.urlsafe_b64encode(b'i\xb7\x1d\xfb\xef\xff')
b'abcd--__'
>>> base64.urlsafe_b64decode('abcd--__')
b'i\xb7\x1d\xfb\xef\xff'

```


## 13-04 struct

把一个32位无符号整数变成字节（也就是4个长度的bytes）
```
>>> n = 10240099
>>> b1 = (n & 0xff000000) >> 24
>>> b2 = (n & 0xff0000) >> 16
>>> b3 = (n & 0xff00) >> 8
>>> b4 = n & 0xff
>>> bs = bytes([b1, b2, b3, b4])
>>> bs
b'\x00\x9c@c'
```
Python提供了一个struct模块来解决bytes和其他二进制数据类型的转换

**pack函数把任意数据类型变成bytes：**
```
>>> import struct
>>> struct.pack('>I', 10240099)
b'\x00\x9c@c'
```
- 第一个参数是处理指令：'>I'
    - \>表示字节顺序是big-endian，也就是网络序
    - I表示4字节无符号整数

**unpack把bytes变成相应的数据类型：**
```
>>> struct.unpack('>IH', b'\xf0\xf0\xf0\xf0\x80\x80')
(4042322160, 32896)
```
- I：4字节无符号整数
- H：2字节无符号整数

## 13-05 hashlib(MD5, SHA1, 摘要算法)
hashlib提供了常见的摘要算法（又名哈希算法、散列算法）

哈希算法：通过一个函数，把任意长度的数据转换为一个长度固定的数据串（通常用16进制的字符串表示）

**MD5**

**计算出一个字符串的MD5值：**
```
import hashlib

md5 = hashlib.md5()
md5.update('how to use md5 in python hashlib?'.encode('utf-8'))
print(md5.hexdigest())
```
计算结果如下：
```
d26a53750bc40b38b65a520292f69306
```
分块多次调用update()，计算结果一样：
```
import hashlib

md5 = hashlib.md5()
md5.update('how to use md5 in '.encode('utf-8'))
md5.update('python hashlib?'.encode('utf-8'))
print(md5.hexdigest())
```

**SHA1**

```
import hashlib

sha1 = hashlib.sha1()
sha1.update('how to use sha1 in '.encode('utf-8'))
sha1.update('python hashlib?'.encode('utf-8'))
print(sha1.hexdigest())
```

**摘要算法应用**

数据库表中存储用户登录的用户名和口令  

name | password  
---|---
michael | 123456 
bob | abc999  
lice   | alice2008  

正确的保存口令的方式是不存储用户的明文口令，而是存储用户口令的摘要，比如MD5：

username | password
---|---
michael  | e10adc3949ba59abbe56e057f20f883e
bob      | 878ef96e86145580c38c87f0410ad153
alice    | 99b1c2188db85afee403b1536010c2c9

当用户登录时，首先计算用户输入的明文口令的MD5，然后和数据库存储的MD5对比，如果一致，说明口令输入正确，如果不一致，口令肯定错误。
## 13-06 itertools(count(), cycle(), repeat(), chain(), groupby())

**count()**

创建一个无限的迭代器，根本停不下来，只能Ctrl+C退出
```
>>> import itertools
>>> cs = itertools.cycle('ABC') # 注意字符串也是序列的一种
>>> for c in cs:
...     print(c)
...
'A'
'B'
'C'
'A'
'B'
'C'
...
```

**cycle()**

无限重复序列
```
>>> import itertools
>>> cs = itertools.cycle('ABC') # 注意字符串也是序列的一种
>>> for c in cs:
...     print(c)
...
'A'
'B'
'C'
'A'
'B'
'C'
...
```

**repeat()**

重复序列n次
```
>>> ns = itertools.repeat('A', 3)
>>> for n in ns:
...     print(n)
...
A
A
A
```

**chain()**

把一组迭代对象串联起来，形成一个更大的迭代器：
```
>>> for c in itertools.chain('ABC', 'XYZ'):
...     print(c)
# 迭代效果：'A' 'B' 'C' 'X' 'Y' 'Z'
```

**groupby()**

把迭代器中相邻的重复元素挑出来放在一起：
```
>>> for key, group in itertools.groupby('AAABBBCCAAA'):
...     print(key, list(group))
...
A ['A', 'A', 'A']
B ['B', 'B', 'B']
C ['C', 'C']
A ['A', 'A', 'A']
```
实际上挑选规则是通过函数完成的，只要作用于函数的两个元素返回的值相等，这两个元素就被认为是在一组的，而函数返回值作为组的key。如果我们要忽略大小写分组，就可以让元素'A'和'a'都返回相同的key：
```
>>> for key, group in itertools.groupby('AaaBBbcCAAa', lambda c: c.upper()):
...     print(key, list(group))
...
A ['A', 'a', 'a']
B ['B', 'B', 'b']
C ['c', 'C']
A ['A', 'A', 'a']
```
## 13-07 contextlib(@contextmanager, @closing)
读写文件这样的资源要在使用完毕后用try...finally正确关闭它们
```
try:
    f = open('/path/to/file', 'r')
    f.read()
finally:
    if f:
        f.close()
```
with语句简化为：
```
with open('/path/to/file', 'r') as f:
    f.read()
```
实现上下文管理就可以用于with语句，是通过__enter__和__exit__这两个方法实现

```
class Query(object):

    def __init__(self, name):
        self.name = name

    def __enter__(self):
        print('Begin')
        return self

    def __exit__(self, exc_type, exc_value, traceback):
        if exc_type:
            print('Error')
        else:
            print('End')

    def query(self):
        print('Query info about %s...' % self.name)
```
这样我们就可以把自己写的资源对象用于with语句：
```
with Query('Bob') as q:
    q.query()
```

**@contextmanager**

contextlib提供了@contextmanager这个decorator更简单

```
from contextlib import contextmanager

class Query(object):

    def __init__(self, name):
        self.name = name

    def query(self):
        print('Query info about %s...' % self.name)

@contextmanager
def create_query(name):
    print('Begin')
    q = Query(name)
    yield q
    print('End')
```
@contextmanager这个decorator接受一个generator，用yield语句把with ... as var把变量输出出去，然后，with语句就可以正常地工作了：
```
with create_query('Bob') as q:
    q.query()
```
用@contextmanager实现某段代码执行前后自动执行特定代码

```
@contextmanager
def tag(name):
    print("<%s>" % name)
    yield
    print("</%s>" % name)

with tag("h1"):
    print("hello")
    print("world")
```
上述代码执行结果为：
```
<h1>
hello
world
</h1>
```
代码的执行顺序是：

1. with语句首先执行yield之前的语句，因此打印出<h1>；
2. yield调用会执行with语句内部的所有语句，因此打印出hello和world；
3. 最后执行yield之后的语句，打印出</h1>。

**@closing**

如果一个对象没有实现上下文，我们就不能把它用于with语句。这个时候，可以用closing()来把该对象变为上下文对象。例如，用with语句使用urlopen()：

```
from contextlib import closing
from urllib.request import urlopen

with closing(urlopen('https://www.python.org')) as page:
    for line in page:
        print(line)
```
closing也是一个经过@contextmanager装饰的generator，这个generator编写起来其实非常简单：
```
@contextmanager
def closing(thing):
    try:
        yield thing
    finally:
        thing.close()
```
它的作用就是把任意对象变为上下文对象，并支持with语句。
## 13-08 XML
操作XML有两种方法：

- DOM
    - 把整个XML读入内存，解析为树，因此占用内存大，解析慢
    - 优点：可以任意遍历树的节点
- SAX
    - 流模式，边读边解析，占用内存小，解析快
    - 缺点：需要自己处理事件

优先考虑SAX，DOM太占内存

当SAX解析器读到一个节点时：
```
<a href="/">python</a>
```
会产生3个事件：

1. start_element事件，在读取\<a href="/">时
2. char_data事件，在读取python时
3. end_element事件，在读取</a>时

```
from xml.parsers.expat import ParserCreate

class DefaultSaxHandler(object):
    def start_element(self, name, attrs):
        print('sax:start_element: %s, attrs: %s' % (name, str(attrs)))

    def end_element(self, name):
        print('sax:end_element: %s' % name)

    def char_data(self, text):
        print('sax:char_data: %s' % text)

xml = r'''<?xml version="1.0"?>
<ol>
    <li><a href="/python">Python</a></li>
    <li><a href="/ruby">Ruby</a></li>
</ol>
'''

handler = DefaultSaxHandler()
parser = ParserCreate()
parser.StartElementHandler = handler.start_element
parser.EndElementHandler = handler.end_element
parser.CharacterDataHandler = handler.char_data
parser.Parse(xml)
```
注意：读取一大段字符串时，CharacterDataHandler可能被多次调用，所以需要自己保存起来，在EndElementHandler里面再合并

生成XML
```
L = []
L.append(r'<?xml version="1.0"?>')
L.append(r'<root>')
L.append(encode('some & data'))
L.append(r'</root>')
return ''.join(L)
```
## 13-09 HTMLParser
搜索引擎

- 第一步：用爬虫把目标网站的页面抓下来
- 第二步：解析该HTML页面，看看里面的内容到底是新闻、图片还是视频

HTMLParser解析HTML：可以把网页中的文本、图像等解析出来
```
from html.parser import HTMLParser
from html.entities import name2codepoint

class MyHTMLParser(HTMLParser):

    def handle_starttag(self, tag, attrs):
        print('<%s>' % tag)

    def handle_endtag(self, tag):
        print('</%s>' % tag)

    def handle_startendtag(self, tag, attrs):
        print('<%s/>' % tag)

    def handle_data(self, data):
        print(data)

    def handle_comment(self, data):
        print('<!--', data, '-->')

    def handle_entityref(self, name):
        print('&%s;' % name)

    def handle_charref(self, name):
        print('&#%s;' % name)

parser = MyHTMLParser()
parser.feed('''<html>
<head></head>
<body>
<!-- test html parser -->
    <p>Some <a href=\"#\">html</a> HTML&nbsp;tutorial...<br>END</p>
</body></html>''')
```
feed()方法可以多次调用，也就是不一定一次把整个HTML字符串都塞进去，可以一部分一部分塞进去。

特殊字符有两种，一种是英文表示的\&nbsp;，一种是数字表示的\&#1234;，这两种字符都可以通过Parser解析出来

## 13-10 urllib(Get, Post, Handler)
urllib提供了一系列用于操作URL的功能

**Get**

urllib的request模块抓取URL内容：发送一个GET请求到指定的页面，然后返回HTTP的响应：
```
from urllib import request

with request.urlopen('https://api.douban.com/v2/book/2129650') as f:
    data = f.read()
    print('Status:', f.status, f.reason)
    for k, v in f.getheaders():
        print('%s: %s' % (k, v))
    print('Data:', data.decode('utf-8'))
```
HTTP响应的头和JSON数据：
```
Status: 200 OK
Server: nginx
Date: Tue, 26 May 2015 10:02:27 GMT
Content-Type: application/json; charset=utf-8
Content-Length: 2049
Connection: close
Expires: Sun, 1 Jan 2006 01:00:00 GMT
Pragma: no-cache
Cache-Control: must-revalidate, no-cache, private
X-DAE-Node: pidl1
Data: {"rating":{"max":10,"numRaters":16,"average":"7.4","min":0},"subtitle":"","author":["廖雪峰编著"],"pubdate":"2007-6","tags":[{"count":20,"name":"spring","title":"spring"}...}
```
模拟浏览器发送GET请求，就需要使用Request对象，通过往Request对象添加HTTP头，我们就可以把请求伪装成浏览器。例如，模拟iPhone 6去请求豆瓣首页：
```
from urllib import request

req = request.Request('http://www.douban.com/')
req.add_header('User-Agent', 'Mozilla/6.0 (iPhone; CPU iPhone OS 8_0 like Mac OS X) AppleWebKit/536.26 (KHTML, like Gecko) Version/8.0 Mobile/10A5376e Safari/8536.25')
with request.urlopen(req) as f:
    print('Status:', f.status, f.reason)
    for k, v in f.getheaders():
        print('%s: %s' % (k, v))
    print('Data:', f.read().decode('utf-8'))
```
这样豆瓣会返回适合iPhone的移动版网页：
```
...
    <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0">
    <meta name="format-detection" content="telephone=no">
    <link rel="apple-touch-icon" sizes="57x57" href="http://img4.douban.com/pics/cardkit/launcher/57.png" />
...
```

**Post**

把参数data以bytes形式传入
模拟一个微博登录，先读取登录的邮箱和口令，然后按照weibo.cn的登录页的格式以username=xxx&password=xxx的编码传入：
```
from urllib import request, parse

print('Login to weibo.cn...')
email = input('Email: ')
passwd = input('Password: ')
login_data = parse.urlencode([
    ('username', email),
    ('password', passwd),
    ('entry', 'mweibo'),
    ('client_id', ''),
    ('savestate', '1'),
    ('ec', ''),
    ('pagerefer', 'https://passport.weibo.cn/signin/welcome?entry=mweibo&r=http%3A%2F%2Fm.weibo.cn%2F')
])

req = request.Request('https://passport.weibo.cn/sso/login')
req.add_header('Origin', 'https://passport.weibo.cn')
req.add_header('User-Agent', 'Mozilla/6.0 (iPhone; CPU iPhone OS 8_0 like Mac OS X) AppleWebKit/536.26 (KHTML, like Gecko) Version/8.0 Mobile/10A5376e Safari/8536.25')
req.add_header('Referer', 'https://passport.weibo.cn/signin/login?entry=mweibo&res=wel&wm=3349&r=http%3A%2F%2Fm.weibo.cn%2F')

with request.urlopen(req, data=login_data.encode('utf-8')) as f:
    print('Status:', f.status, f.reason)
    for k, v in f.getheaders():
        print('%s: %s' % (k, v))
    print('Data:', f.read().decode('utf-8'))
```
如果登录成功，我们获得的响应如下：
```
Status: 200 OK
Server: nginx/1.2.0
...
Set-Cookie: SSOLoginState=1432620126; path=/; domain=weibo.cn
...
Data: {"retcode":20000000,"msg":"","data":{...,"uid":"1658384301"}}
```
如果登录失败，我们获得的响应如下：
```
...
Data: {"retcode":50011015,"msg":"\u7528\u6237\u540d\u6216\u5bc6\u7801\u9519\u8bef","data":{"username":"example@python.org","errline":536}}
```
**Handler**

如果还需要更复杂的控制，比如通过一个Proxy去访问网站，我们需要利用ProxyHandler来处理，示例代码如下：
```
proxy_handler = urllib.request.ProxyHandler({'http': 'http://www.example.com:3128/'})
proxy_auth_handler = urllib.request.ProxyBasicAuthHandler()
proxy_auth_handler.add_password('realm', 'host', 'username', 'password')
opener = urllib.request.build_opener(proxy_handler, proxy_auth_handler)
with opener.open('http://www.example.com/login.html') as f:
    pass
```
# 14 Python GUI

Python支持多种图形界面的第三方库，包括：

- Tkinter（Python自带）
- wxWidgets
- Qt
- GTK

**第一个GUI程序**

第一步是导入Tkinter包的所有内容：
```
from tkinter import *
```
第二步是从Frame派生一个Application类，这是所有Widget的父容器：
```
class Application(Frame):
    def __init__(self, master=None):
        Frame.__init__(self, master)
        self.pack()
        self.createWidgets()

    def createWidgets(self):
        self.helloLabel = Label(self, text='Hello, world!')
        self.helloLabel.pack()
        self.quitButton = Button(self, text='Quit', command=self.quit)
        self.quitButton.pack()
```
每个Button、Label、输入框等，都是一个Widget。Frame则是可以容纳其他Widget的Widget，所有的Widget组合起来就是一棵树。

pack()方法把Widget加入到父容器中，并实现布局。pack()是最简单的布局，grid()可以实现更复杂的布局。


第三步，实例化Application，并启动消息循环：
```
app = Application()
# 设置窗口标题:
app.master.title('Hello World')
# 主消息循环:
app.mainloop()
```

**输入文本**

我们再对这个GUI程序改进一下，加入一个文本框，让用户可以输入文本，然后点按钮后，弹出消息对话框。
```
from tkinter import *
import tkinter.messagebox as messagebox

class Application(Frame):
    def __init__(self, master=None):
        Frame.__init__(self, master)
        self.pack()
        self.createWidgets()

    def createWidgets(self):
        self.nameInput = Entry(self)
        self.nameInput.pack()
        self.alertButton = Button(self, text='Hello', command=self.hello)
        self.alertButton.pack()

    def hello(self):
        name = self.nameInput.get() or 'world'
        messagebox.showinfo('Message', 'Hello, %s' % name)

app = Application()
# 设置窗口标题:
app.master.title('Hello World')
# 主消息循环:
app.mainloop()
```
当用户点击按钮时，触发hello()，通过self.nameInput.get()获得用户输入的文本后，使用tkMessageBox.showinfo()可以弹出消息对话框
# 15 Python 网络

**网络通信** 是两台计算机上的 **两个进程** 之间的通信

## 15-01 TCP/IP

**IP协议**：把数据从一台计算机通过网络发送到另一台计算机

特点：

- 按块发送
- 途径多个路由
- 不保证能到达
- 不保证顺序到达

**TCP协议**：负责在两台计算机之间建立可靠连接，保证数据包按顺序到达

特点：

- 握手建立连接
- 对每个IP包编号
- 确保对方按顺序收到
- 如果丢包自动重发

IP包：包含要传输的数据，源IP地址和目标IP地址，源端口和目标端口

## 15-02 TCP 编程(客户端, 服务端)

**Socket** 表示打开了一个网络链接，打开一个Socket需要知道目标计算机的IP地址和端口号，再指定协议类型

创建TCP连接

- 主动发起连接的叫客户端
- 被动响应连接的叫服务器

**客户端**

```
# 导入socket库:
import socket

# 创建一个socket:
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
# 建立连接:
s.connect(('www.sina.com.cn', 80))
# 发送数据:
s.send(b'GET / HTTP/1.1\r\nHost: www.sina.com.cn\r\nConnection: close\r\n\r\n')
```

1. 创建Socket对象
    - AF_INET指定使用IPv4协议
        - AF_INET6指定使用IPv6协议
    - SOCK_STREAM指定使用面向流的TCP协议
2. 发起TCP连接（参数是一个tuple）
    - 服务器的IP地址
    - 端口号
3. 发送请求，要求返回首页的内容
    - s.send(b'GET / HTTP/1.1\r\nHost: www.sina.com.cn\r\nConnection: close\r\n\r\n')
4. 接收新浪服务器返回的数据
    - recv(max)方法指定一次最多接收的字节数
    - while循环反复接收
        - d不为空：加入buffer
        - d为空：接收完毕
    - close()关闭连接

```
# 接收数据:
buffer = []
while True:
    # 每次最多接收1k字节:
    d = s.recv(1024)
    if d:
        buffer.append(d)
    else:
        break
data = b''.join(buffer)
# 关闭连接:
s.close()
```
5. 打印HTTP头网页内容保存到文件
```
header, html = data.split(b'\r\n\r\n', 1)
print(header.decode('utf-8'))
# 把接收的数据写入文件:
with open('sina.html', 'wb') as f:
    f.write(html)
```
**服务器**

- 绑定一个端口监听来自客户端的连接
- 区分Socket连接和哪个客户端绑定（依靠服务器地址、服务器端口、客户端地址、客户端端口）
- 每个连接都需要一个新的进程或者新的线程来处理

示例：接收客户端连接，把客户端发过来的字符串加上Hello再发回去

```
# 导入socket库:
import socket

# 创建一个socket:
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
# 监听端口:
s.bind(('127.0.0.1', 9999))

s.listen(5)
print('Waiting for connection...')
```

1. 创建Socket对象
    - AF_INET指定使用IPv4协议
        - AF_INET6指定使用IPv6协议
    - SOCK_STREAM指定使用面向流的TCP协议
2. 绑定监听地址和端口
    - 地址
        - 绑定到某一块网卡的IP地址上
        - 用0.0.0.0绑定到所有的网络地址
        - 用127.0.0.1绑定到本机地址（特殊IP地址：表示本机地址，如果绑定到这个地址，客户端必须同时在本机运行才能连接外部计算机无法连接）
    - 端口
        - 标准服务：小于1024的端口号（必须要有管理员权限才能绑定）
        - 非标准服务
3. listen()方法开始监听端口，传入的参数指定等待连接的最大数量
4. 接受来自客户端的连接，accept()会等待并返回一个客户端的连接:
```
while True:
    # 接受一个新连接:
    sock, addr = s.accept()
    # 创建新线程来处理TCP连接:
    t = threading.Thread(target=tcplink, args=(sock, addr))
    t.start()
```
5. 每个连接都必须创建新线程（或进程）来处理
    - 连接建立后，服务器首先发一条欢迎消息，然后等待客户端数据，并加上Hello再发送给客户端。如果客户端发送了exit字符串，就直接关闭连接。
```
def tcplink(sock, addr):
    print('Accept new connection from %s:%s...' % addr)
    sock.send(b'Welcome!')
    while True:
        data = sock.recv(1024)
        time.sleep(1)
        if not data or data.decode('utf-8') == 'exit':
            break
        sock.send(('Hello, %s!' % data.decode('utf-8')).encode('utf-8'))
    sock.close()
    print('Connection from %s:%s closed.' % addr)
```
对应的客户端程序
```
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
# 建立连接:
s.connect(('127.0.0.1', 9999))
# 接收欢迎消息:
print(s.recv(1024).decode('utf-8'))
for data in [b'Michael', b'Tracy', b'Sarah']:
    # 发送数据:
    s.send(data)
    print(s.recv(1024).decode('utf-8'))
s.send(b'exit')
s.close()
```

## 15-03 UDP 编程(服务端, 客户端)

UDP：面向无连接的协议

特点：

- 不需要建立连接
- 只需要知道对方的IP地址和端口号
- 速度快

**服务端**

```
s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
# 绑定端口:
s.bind(('127.0.0.1', 9999))
```

1. 创建Socket对象
    - AF_INET指定使用IPv4协议
        - AF_INET6指定使用IPv6协议
    - SOCK_DGRAM指定使用面向流的UDP协议
2. 绑定监听地址和端口
    - 地址
        - 绑定到某一块网卡的IP地址上
        - 用0.0.0.0绑定到所有的网络地址
        - 用127.0.0.1绑定到本机地址（特殊IP地址：表示本机地址，如果绑定到这个地址，客户端必须同时在本机运行才能连接外部计算机无法连接）
    - 端口
        - 标准服务：小于1024的端口号（必须要有管理员权限才能绑定）
        - 非标准服务
3. 接受来自客户端的连接
    - recvfrom()方法返回数据和客户端的地址与端口
    - 服务器收到数据后，直接调用sendto()就可以把数据用UDP发给客户端

```
print('Bind UDP on 9999...')
while True:
    # 接收数据:
    data, addr = s.recvfrom(1024)
    print('Received from %s:%s.' % addr)
    s.sendto(b'Hello, %s!' % data, addr)
```

**客户端**

客户端使用UDP时，首先仍然创建基于UDP的Socket，然后，不需要调用connect()，直接通过sendto()给服务器发数据：
```
s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
for data in [b'Michael', b'Tracy', b'Sarah']:
    # 发送数据:
    s.sendto(data, ('127.0.0.1', 9999))
    # 接收数据:
    print(s.recv(1024).decode('utf-8'))
s.close()
```
## 15-04 电子邮件原理
运作流程：

```
graph LR
发件人 --> 发件人MUA
发件人MUA --> MTA
MTA --> 若干个MTA
若干个MTA --> MDA
MDA --> 收件人MUA
收件人MUA --> 收件人
```
发件人：me@163.com -> MUA -> MTA -> MTA -> 若干个MTA -> MDA \<\- MUA \<\- 收件人：friend@sina.com

- MUA 邮件用户代理（Mail User Agent）：编写邮件
- MTA 邮件传输代理（Mail Transfer Agent）：发送到网易MTA
- 网易MTA发送到新浪MTA
- MDA 邮件投递代理（Mail Delivery Agent）：新浪MTA发送到新浪MDA，长期保存
- 对方通过MUA从MDA上把邮件取到自己的电脑上

编写程序来发送和接收邮件，本质上就是：

- 编写MUA把邮件发到MTA
    - 发邮件时，MUA和MTA使用的协议就是SMTP：Simple Mail Transfer Protocol，后面的MTA到另一个MTA也是用SMTP协议
    - 配置SMTP服务器：指定发送到哪个MTA上，发件人是me@163.com的话就是smtp.163.com
    - 填写邮箱地址和邮箱口令
- 编写MUA从MDA上收邮件
    - 收邮件时，MUA和MDA使用的协议有两种
        - POP：Post Office Protocol，目前版本是3，俗称POP3
        - IMAP：Internet Message Access Protocol，目前版本是4，优点是不但能取邮件，还可以直接操作MDA上存储的邮件，比如从收件箱移到垃圾箱
    - 填写POP3或IMAP服务器地址、邮箱地址和口令
        - MUA才能顺利地通过POP或IMAP协议从MDA取到邮件

注意：目前大多数邮件服务商都需要手动打开SMTP发信和POP收信的功能，否则只允许在网页登录

## 15-05 SMTP发送邮件(纯文本邮件, HTML邮件, 发送附件, 加密SMTP)

SMTP是发送邮件的协议：可以发送纯文本邮件、HTML邮件以及带附件的邮件


**纯文本邮件：**

- 第一个参数：邮件正文
- 第二个参数：MIME的subtype（'plain'表示纯文本，最终的MIME就是'text/plain'）
- 第三个参数：utf-8编码

```
from email.mime.text import MIMEText
msg = MIMEText('hello, send by Python...', 'plain', 'utf-8')
```
通过SMTP发出去：

- set_debuglevel(1)打印出和SMTP服务器交互的所有信息
- login()方法用来登录SMTP服务器
- sendmail()方法就是发邮件，由于可以一次发给多个人，所以传入一个list
- 邮件正文是一个str，as_string()把MIMEText对象变成str
```
# 输入Email地址和口令:
from_addr = input('From: ')
password = input('Password: ')
# 输入收件人地址:
to_addr = input('To: ')
# 输入SMTP服务器地址:
smtp_server = input('SMTP server: ')

import smtplib
server = smtplib.SMTP(smtp_server, 25) # SMTP协议默认端口是25
server.set_debuglevel(1)
server.login(from_addr, password)
server.sendmail(from_addr, [to_addr], msg.as_string())
server.quit()
```
有三个问题：

- 邮件没有主题
- 收件人的名字没有显示为友好的名字，比如Mr Green <green@example.com>
- 明明收到了邮件，却提示不在收件人中

把From、To和Subject添加到MIMEText中
```
from email import encoders
from email.header import Header
from email.mime.text import MIMEText
from email.utils import parseaddr, formataddr

import smtplib

def _format_addr(s):
    name, addr = parseaddr(s)
    return formataddr((Header(name, 'utf-8').encode(), addr))

from_addr = input('From: ')
password = input('Password: ')
to_addr = input('To: ')
smtp_server = input('SMTP server: ')

msg = MIMEText('hello, send by Python...', 'plain', 'utf-8')
msg['From'] = _format_addr('Python爱好者 <%s>' % from_addr)
msg['To'] = _format_addr('管理员 <%s>' % to_addr)
msg['Subject'] = Header('来自SMTP的问候……', 'utf-8').encode()

server = smtplib.SMTP(smtp_server, 25)
server.set_debuglevel(1)
server.login(from_addr, password)
server.sendmail(from_addr, [to_addr], msg.as_string())
server.quit()
```
**HTML邮件**

- 构造MIMEText对象时，把HTML字符串传进去
- 第二个参数由plain变为html

```
msg = MIMEText('<html><body><h1>Hello</h1>' +
    '<p>send by <a href="http://www.python.org">Python</a>...</p>' +
    '</body></html>', 'html', 'utf-8')
```
**发送附件**

- 构造一个MIMEMultipart对象代表邮件本身
- 后往里面加上一个MIMEText作为邮件正文
- 再继续往里面加上表示附件的MIMEBase对象
```
# 邮件对象:
msg = MIMEMultipart()
msg['From'] = _format_addr('Python爱好者 <%s>' % from_addr)
msg['To'] = _format_addr('管理员 <%s>' % to_addr)
msg['Subject'] = Header('来自SMTP的问候……', 'utf-8').encode()

# 邮件正文是MIMEText:
msg.attach(MIMEText('send with file...', 'plain', 'utf-8'))

# 添加附件就是加上一个MIMEBase，从本地读取一个图片:
with open('/Users/michael/Downloads/test.png', 'rb') as f:
    # 设置附件的MIME和文件名，这里是png类型:
    mime = MIMEBase('image', 'png', filename='test.png')
    # 加上必要的头信息:
    mime.add_header('Content-Disposition', 'attachment', filename='test.png')
    mime.add_header('Content-ID', '<0>')
    mime.add_header('X-Attachment-Id', '0')
    # 把附件的内容读进来:
    mime.set_payload(f.read())
    # 用Base64编码:
    encoders.encode_base64(mime)
    # 添加到MIMEMultipart:
    msg.attach(mime)
```

如果构造一个MIMEText对象，就表示一个文本邮件对象，如果构造一个MIMEImage对象，就表示一个作为附件的图片，要把多个对象组合起来，就用MIMEMultipart对象，而MIMEBase可以表示任何对象。它们的继承关系如下：

Message

- MIMEBase
    - MIMEMultipart
    - MIMENonMultipart
        - MIMEMessage
        - MIMEText
        - MIMEImage

**加密SMTP**

使用标准的25端口连接SMTP服务器时，使用的是明文传输，发送邮件的整个过程可能会被窃听。要更安全地发送邮件，可以加密SMTP会话，实际上就是先创建SSL安全连接，然后再使用SMTP协议发送邮件。

某些邮件服务商，例如Gmail，提供的SMTP服务必须要加密传输。我们来看看如何通过Gmail提供的安全SMTP发送邮件。

Gmail的SMTP端口是587，因此，修改代码如下：

```
smtp_server = 'smtp.gmail.com'
smtp_port = 587
server = smtplib.SMTP(smtp_server, smtp_port)
server.starttls()
# 剩下的代码和前面的一模一样:
server.set_debuglevel(1)
...
```
只需要在创建SMTP对象后，立刻调用starttls()方法，就创建了安全连接。后面的代码和前面的发送邮件代码完全一样。

## 15-06 POP3收取邮件

Python内置poplib模块，实现了POP3协议，可以直接用来收邮件

收取邮件分两步：

- 第一步：用poplib把邮件的原始文本下载到本地
- 第二部：用email解析原始文本，还原为邮件对象
```
import poplib

# 输入邮件地址, 口令和POP3服务器地址:
email = input('Email: ')
password = input('Password: ')
pop3_server = input('POP3 server: ')

# 连接到POP3服务器:
server = poplib.POP3(pop3_server)
# 可以打开或关闭调试信息:
server.set_debuglevel(1)
# 可选:打印POP3服务器的欢迎文字:
print(server.getwelcome().decode('utf-8'))

# 身份认证:
server.user(email)
server.pass_(password)

# stat()返回邮件数量和占用空间:
print('Messages: %s. Size: %s' % server.stat())
# list()返回所有邮件的编号:
resp, mails, octets = server.list()
# 可以查看返回的列表类似[b'1 82923', b'2 2184', ...]
print(mails)

# 获取最新一封邮件, 注意索引号从1开始:
index = len(mails)
resp, lines, octets = server.retr(index)

# lines存储了邮件的原始文本的每一行,
# 可以获得整个邮件的原始文本:
msg_content = b'\r\n'.join(lines).decode('utf-8')
# 稍后解析出邮件:
msg = Parser().parsestr(msg_content)

# 可以根据邮件索引号直接从服务器删除邮件:
# server.dele(index)
# 关闭连接:
server.quit()
```

**解析邮件**

```
from email.parser import Parser
from email.header import decode_header
from email.utils import parseaddr

import poplib

msg = Parser().parsestr(msg_content)
```
但是这个Message对象本身可能是一个MIMEMultipart对象，即包含嵌套的其他MIMEBase对象，嵌套可能还不止一层。

所以递归地打印出Message对象的层次结构：
```
# indent用于缩进显示:
def print_info(msg, indent=0):
    if indent == 0:
        for header in ['From', 'To', 'Subject']:
            value = msg.get(header, '')
            if value:
                if header=='Subject':
                    value = decode_str(value)
                else:
                    hdr, addr = parseaddr(value)
                    name = decode_str(hdr)
                    value = u'%s <%s>' % (name, addr)
            print('%s%s: %s' % ('  ' * indent, header, value))
    if (msg.is_multipart()):
        parts = msg.get_payload()
        for n, part in enumerate(parts):
            print('%spart %s' % ('  ' * indent, n))
            print('%s--------------------' % ('  ' * indent))
            print_info(part, indent + 1)
    else:
        content_type = msg.get_content_type()
        if content_type=='text/plain' or content_type=='text/html':
            content = msg.get_payload(decode=True)
            charset = guess_charset(msg)
            if charset:
                content = content.decode(charset)
            print('%sText: %s' % ('  ' * indent, content + '...'))
        else:
            print('%sAttachment: %s' % ('  ' * indent, content_type))
```
邮件的Subject或者Email中包含的名字都是经过编码后的str，要正常显示，就必须decode：
```
def decode_str(s):
    value, charset = decode_header(s)[0]
    if charset:
        value = value.decode(charset)
    return value
```
文本邮件的内容也是str，还需要检测编码
```
def guess_charset(msg):
    charset = msg.get_charset()
    if charset is None:
        content_type = msg.get('Content-Type', '').lower()
        pos = content_type.find('charset=')
        if pos >= 0:
            charset = content_type[pos + 8:].strip()
    return charset
```
# 16 Python 数据库


付费的商用数据库：

- Oracle，典型的高富帅
- SQL Server，微软自家产品，Windows定制专款
- DB2，IBM的产品
- Sybase，曾经跟微软是好基友，后来关系破裂，现在家境惨淡

免费的开源数据库：

- MySQL，大家都在用，一般错不了
- PostgreSQL，学术气息有点重，其实挺不错，但知名度没有MySQL高
- sqlite，嵌入式数据库，适合桌面和移动应用

## 16-01 使用SQLite
SQLite的驱动内置在Python标准库中，所以可以直接操作SQLite数据库

特点

- 轻量级
- 可嵌入：体积很小，经常被集成到各种应用程序中（在iOS和Android的App中都可以集成）
- 不能承受高并发访问：适合桌面和移动应用

```
# 导入SQLite驱动:
>>> import sqlite3
# 连接到SQLite数据库
# 数据库文件是test.db
# 如果文件不存在，会自动在当前目录创建:
>>> conn = sqlite3.connect('test.db')
# 创建一个Cursor:
>>> cursor = conn.cursor()
# 执行一条SQL语句，创建user表:
>>> cursor.execute('create table user (id varchar(20) primary key, name varchar(20))')
<sqlite3.Cursor object at 0x10f8aa260>
# 继续执行一条SQL语句，插入一条记录:
>>> cursor.execute('insert into user (id, name) values (\'1\', \'Michael\')')
<sqlite3.Cursor object at 0x10f8aa260>
# 通过rowcount获得插入的行数:
>>> cursor.rowcount
1
# 关闭Cursor:
>>> cursor.close()
# 提交事务:
>>> conn.commit()
# 关闭Connection:
>>> conn.close()
```
查询记录：
```
>>> conn = sqlite3.connect('test.db')
>>> cursor = conn.cursor()
# 执行查询语句:
>>> cursor.execute('select * from user where id=?', ('1',))
<sqlite3.Cursor object at 0x10f8aa340>
# 获得查询结果集:
>>> values = cursor.fetchall()
>>> values
[('1', 'Michael')]
>>> cursor.close()
>>> conn.close()
```

- 使用Cursor对象执行insert，update，delete语句时，执行结果由rowcount返回影响的行数，就可以拿到执行结果。
- 使用Cursor对象执行select语句时，通过featchall()可以拿到结果集。结果集是一个list，每个元素都是一个tuple，对应一行记录

如果SQL语句带有参数，那么需要把参数按照位置传递给execute()方法，有几个?占位符就必须对应几个参数，例如：

```
cursor.execute('select * from user where name=? and pwd=?', ('abc', 'password'))
```

## 16-02 使用MySQL

Web世界中使用最广泛的数据库服务器

1. 安装MySQL
    - 输入root用户的口令（记不住就设置为password）
2. 安装MySQL驱动：mysql-connector-python
```
$ pip install mysql-connector-python --allow-external mysql-connector-python
```
如果安装失败，可以试另一个驱动：
```
$ pip install mysql-connector
```
Python连接到MySQL服务器的test数据库：
```
# 导入MySQL驱动:
>>> import mysql.connector
# 注意把password设为你的root口令:
>>> conn = mysql.connector.connect(user='root', password='password', database='test')
>>> cursor = conn.cursor()
# 创建user表:
>>> cursor.execute('create table user (id varchar(20) primary key, name varchar(20))')
# 插入一行记录，注意MySQL的占位符是%s:
>>> cursor.execute('insert into user (id, name) values (%s, %s)', ['1', 'Michael'])
>>> cursor.rowcount
1
# 提交事务:
>>> conn.commit()
>>> cursor.close()
# 运行查询:
>>> cursor = conn.cursor()
>>> cursor.execute('select * from user where id = %s', ('1',))
>>> values = cursor.fetchall()
>>> values
[('1', 'Michael')]
# 关闭Cursor和Connection:
>>> cursor.close()
True
>>> conn.close()
```
操作MySQL的数据库代码和SQLite类似

pymysql 版本
```
import pymysql

#建立连接
conn = pymysql.connect(host='10.104.120.24', user='root', password='123', database='test')
cursor = conn.cursor()
#创建表
cursor.execute('create table user (id varchar(20) primary key, name varchar(20))')
#插入数据
cursor.execute('insert into user (id, name) values (%s, %s)', ['1', 'Michael'])
#cursor.rowcount
#提交事务
conn.commit()
cursor.close()

cursor = conn.cursor()
#查询数据
cursor.execute('select * from user where id = %s', ('1',))
values = cursor.fetchall()
print(values)
#查询Mysql版本
cursor.execute('select version()')
v = cursor.fetchall()
print ("Database version : %s " % v)
cursor.close()
conn.close()
```
## 16-03 使用SQLAlchemy(ORM, SQLAlchemy)

**ORM技术（Object-Relational Mapping）**

数据库表是一个二维表

- 一个list表示多行
- list的每一个元素是tuple，表示一行记录
```
[
    ('1', 'Michael'),
    ('2', 'Bob'),
    ('3', 'Adam')
]
```
缺点：tuple表示一行很难看出表的结构

解决方案：关系数据库的表结构映射到对象上 - ORM（Object-Relational Mapping）
```
class User(object):
    def __init__(self, id, name):
        self.id = id
        self.name = name

[
    User('1', 'Michael'),
    User('2', 'Bob'),
    User('3', 'Adam')
]
```

**SQLAlchemy**

是一个ORM框架

安装SQLAlchemy：
```
$ pip install sqlalchemy
```
第一步，导入SQLAlchemy，并初始化DBSession：
```
# 导入:
from sqlalchemy import Column, String, create_engine
from sqlalchemy.orm import sessionmaker
from sqlalchemy.ext.declarative import declarative_base

# 创建对象的基类:
Base = declarative_base()

# 定义User对象:
class User(Base):
    # 表的名字:
    __tablename__ = 'user'

    # 表的结构:
    id = Column(String(20), primary_key=True)
    name = Column(String(20))

# 初始化数据库连接:
engine = create_engine('mysql+mysqlconnector://root:password@localhost:3306/test')
# 创建DBSession类型:
DBSession = sessionmaker(bind=engine)
```
如果有多个表，就继续定义其他class，例如School：
```
class School(Base):
    __tablename__ = 'school'
    id = ...
    name = ...
```
create_engine()用来初始化数据库连接。SQLAlchemy用一个字符串表示连接信息：
```
'数据库类型+数据库驱动名称://用户名:口令@机器地址:端口号/数据库名'
```
向数据库表中添加一行记录，可以视为**添加**一个User对象：
```
# 创建session对象:
session = DBSession()
# 创建新User对象:
new_user = User(id='5', name='Bob')
# 添加到session:
session.add(new_user)
# 提交即保存到数据库:
session.commit()
# 关闭session:
session.close()
```
查询数据，不再是tuple，而是User对象
```
# 创建Session:
session = DBSession()
# 创建Query查询，filter是where条件，最后调用one()返回唯一行，如果调用all()则返回所有行:
user = session.query(User).filter(User.id=='5').one()
# 打印类型和对象的name属性:
print('type:', type(user))
print('name:', user.name)
# 关闭Session:
session.close()
```
如果一个User拥有多个Book，就可以定义一对多关系如下：
```
class User(Base):
    __tablename__ = 'user'

    id = Column(String(20), primary_key=True)
    name = Column(String(20))
    # 一对多:
    books = relationship('Book')

class Book(Base):
    __tablename__ = 'book'

    id = Column(String(20), primary_key=True)
    name = Column(String(20))
    # “多”的一方的book表是通过外键关联到user表的:
    user_id = Column(String(20), ForeignKey('user.id'))
```
查询一个User对象时，该对象的books属性将返回一个包含若干个Book对象的list

# 17 Python Web

WEB开发经历阶段

1. 静态Web页面
2. CGI
3. ASP/JSP/PHP
4. MVC

## 17-01 HTTP协议简介(HTTP请求, HTTP格式)

- HTML是一种用来定义网页的文本，会HTML，就可以编写网页
- HTTP是在网络上传输HTML的协议，用于浏览器和服务器的通信

**HTTP请求**

HTTP请求的流程：

- 步骤1：浏览器首先向服务器发送HTTP请求，请求包括：
    - 方法：GET还是POST，GET仅请求资源，POST会附带用户数据
    - 路径：/full/url/path
    - 域名：由Host头指定：Host: www.sina.com.cn
    - 以及其他相关的Header
    - 如果是POST，那么请求还包括一个Body，包含用户数据
- 步骤2：服务器向浏览器返回HTTP响应，响应包括：
    - 响应代码：
        - 200表示成功
        - 3xx表示重定向
        - 4xx表示客户端发送的请求有错误
        - 5xx表示服务器端处理时发生了错误
    - 响应类型：由Content-Type指定；
    - 以及其他相关的Header
- 步骤3：如果浏览器还需要继续向服务器请求其他资源，比如图片，就再次发出HTTP请求，重复步骤1、2

**HTTP格式**

每个HTTP请求和响应都遵循相同的格式，一个HTTP包含Header和Body（可选）两部分

HTTP GET请求的格式：
```
GET /path HTTP/1.1
Header1: Value1
Header2: Value2
Header3: Value3
```
HTTP POST请求的格式：
```
POST /path HTTP/1.1
Header1: Value1
Header2: Value2
Header3: Value3

body data goes here...
```
当遇到连续两个\r\n时，Header部分结束，后面的数据全部是Body。

HTTP响应的格式：
```
200 OK
Header1: Value1
Header2: Value2
Header3: Value3

body data goes here...
```
Body的数据类型由Content-Type头来确定

- 如果是网页，Body就是文本
- 如果是图片，Body就是图片的二进制数据

## 17-02 HTML简介

[HTML学习笔记](https://github.com/KEVISONG/e-notebooks/blob/master/HTML/HTML%20Study%20Notes.md#html-study-notes)

## 17-03 WSGI接口

Web应用的本质：

- 浏览器发送一个HTTP请求
- 服务器收到请求，生成一个HTML文档
- 服务器把HTML文档作为HTTP响应的Body发送给浏览器
- 浏览器收到HTTP响应，从HTTP Body取出HTML文档并显示

WSGI接口：接受HTTP请求、解析HTTP请求、发送HTTP响应等由专门的服务器软件实现。WSGI接口连接底层和Python

响应HTTP请求，一个简单的Web版本的“Hello, web!”：

```
def application(environ, start_response):
    start_response('200 OK', [('Content-Type', 'text/html')])
    return [b'<h1>Hello, web!</h1>']
```
application()函数就是符合WSGI标准的一个HTTP处理函数，它接收两个参数：

- environ：一个包含所有HTTP请求信息的dict对象
- start_response：一个发送HTTP响应的函数

application()函数中，调用：
```
start_response('200 OK', [('Content-Type', 'text/html')])
```
start_response()函数接收两个参数

- 一个是HTTP响应码
- 一个是一组list表示的HTTP Header，每个Header用一个包含两个str的tuple表示
    - 通常情况下应该把Content-Type头发送给浏览器
    - 其他很多常用的HTTP Header也应该发送

**运行WSGI服务**

编写hello.py，实现Web应用程序的WSGI处理函数：
```
# hello.py

def application(environ, start_response):
    start_response('200 OK', [('Content-Type', 'text/html')])
    return [b'<h1>Hello, web!</h1>']
```
server.py，负责启动WSGI服务器，加载application()函数：
```
# server.py
# 从wsgiref模块导入:
from wsgiref.simple_server import make_server
# 导入我们自己编写的application函数:
from hello import application

# 创建一个服务器，IP地址为空，端口是8000，处理函数是application:
httpd = make_server('', 8000, application)
print('Serving HTTP on port 8000...')
# 开始监听HTTP请求:
httpd.serve_forever()
```
打开浏览器，输入http://localhost:8000/ 即可看到结果

**动态内容**

在地址栏输入用户名作为URL的一部分，将返回Hello, xxx!
```
# hello.py

def application(environ, start_response):
    start_response('200 OK', [('Content-Type', 'text/html')])
    body = '<h1>Hello, %s!</h1>' % (environ['PATH_INFO'][1:] or 'web')
    return [body.encode('utf-8')]
```
## 17-04 使用Web框架(FLASK)
**其实一个Web App，就是写一个WSGI的处理函数，针对每个HTTP请求进行响应**

笨方法处理不同的URL请求（GET，POST，PUT，DELETE等）：从environ变量里取出HTTP请求的信息，然后逐个判断：
```
def application(environ, start_response):
    method = environ['REQUEST_METHOD']
    path = environ['PATH_INFO']
    if method=='GET' and path=='/':
        return handle_home(environ, start_response)
    if method=='POST' and path='/signin':
        return handle_signin(environ, start_response)
```
框架作用：用一个函数处理一个URL时，实现URL到函数的映射

**FLASK 框架**

安装 FLASK
```
$ pip install flask
```
app. py，处理3个URL，分别是：

- GET /：首页，返回Home；
- GET /signin：登录页，显示登录表单；
- POST /signin：处理登录表单，显示登录结果

Flask通过Python的装饰器在内部自动地把URL和函数给关联起来：
```
from flask import Flask
from flask import request

app = Flask(__name__)

@app.route('/', methods=['GET', 'POST'])
def home():
    return '<h1>Home</h1>'

@app.route('/signin', methods=['GET'])
def signin_form():
    return '''<form action="/signin" method="post">
              <p><input name="username"></p>
              <p><input name="password" type="password"></p>
              <p><button type="submit">Sign In</button></p>
              </form>'''

@app.route('/signin', methods=['POST'])
def signin():
    # 需要从request对象读取表单内容：
    if request.form['username']=='admin' and request.form['password']=='password':
        return '<h3>Hello, admin!</h3>'
    return '<h3>Bad username or password.</h3>'

if __name__ == '__main__':
    app.run()
```
运行python app. py，Flask自带的Server在端口5000上监听：
```
$ python app.py 
 * Running on http://127.0.0.1:5000/
```
常见的Python Web框架还有：

- Django：全能型Web框架
- web. py：一个小巧的Web框架
- Bottle：和Flask类似的Web框架
- Tornado：Facebook的开源异步Web框架

## 17-05 使用模板(MVC)

模板：嵌入了变量和指令的特殊HTML文件

作用：传入不同的数据，替换后得到最终HTML发送给用户

**MVC**：Model-View-Controller（模型-视图-控制器）

1. 浏览器请求：GET /Kevin

2. app. py（C）

```
@app.route('/<name>')
def home(name):
    return render_template('home.html', name=name)
```
3. 模板（V）
```
<html>
<body>
<p>Hello, {{ name }}</p>
</body>
</html>
```
4. 用户看到的
```
<html>
<body>
<p>Hello, Kevin</p>
</body>
</html>
```
（M）：传给View的数据，上例是一个dict：{ 'name': 'Michael' }

**MVC模式改写FLASK框架代码**

```
from flask import Flask, request, render_template

app = Flask(__name__)

@app.route('/', methods=['GET', 'POST'])
def home():
    return render_template('home.html')

@app.route('/signin', methods=['GET'])
def signin_form():
    return render_template('form.html')

@app.route('/signin', methods=['POST'])
def signin():
    username = request.form['username']
    password = request.form['password']
    if username=='admin' and password=='password':
        return render_template('signin-ok.html', username=username)
    return render_template('form.html', message='Bad username or password', username=username)

if __name__ == '__main__':
    app.run()
```
原来代码直接return字符串，而MVC return **render_template('模板（网页.html）')**

Flask默认支持的模板是jinja2

```
$ pip install jinja2
```


用来显示首页的模板：home.html
```
<html>
<head>
  <title>Home</title>
</head>
<body>
  <h1 style="font-style:italic">Home</h1>
</body>
</html>
```
用来显示登录表单的模板：form.html
```
<html>
<head>
  <title>Please Sign In</title>
</head>
<body>
  {% if message %}
  <p style="color:red">{{ message }}</p>
  {% endif %}
  <form action="/signin" method="post">
    <legend>Please sign in:</legend>
    <p><input name="username" placeholder="Username" value="{{ username }}"></p>
    <p><input name="password" placeholder="Password" type="password"></p>
    <p><button type="submit">Sign In</button></p>
  </form>
</body>
</html>
```
登录成功的模板：signin-ok.html
```
<html>
<head>
  <title>Welcome, {{ username }}</title>
</head>
<body>
  <p>Welcome, {{ username }}!</p>
</body>
</html>
```
**MVC作用**：把Python代码和HTML代码最大限度地分离了

Jinja2模板

- 需要替换的变量：{ { name } }
- 指令：{ % ... % }
```
{% for i in page_list %}
    <a href="/page/{{ i }}">{{ i }}</a>
{% endfor %}
```

常见的模板：

- Mako：用 < % ... % > 和 ${xxx} 的一个模板；
- Cheetah：也是用 <% ... %> 和 ${xxx} 的一个模板；
- Django：Django是一站式框架，内置一个用 {% ... %} 和 {{ xxx }} 的模板

# 18 Python 异步IO

CPU运行快，IO设备龟速，导致：

- 同步IO：IO设备慢慢读写，CPU等待
    - 多进程/多线程：提升效率，但是不能无限增加线程，切换线程开销大，效率低
- 异步IO：IO设备慢慢读写，CPU不等待，直接执行其他代码。IO返回结果时，通知CPU处理

传统读写文件：无法实现异步IO
```
do_some_code()
f = open('/path/to/file', 'r')
r = f.read() # <== 线程停在此处等待IO操作结果
# IO操作完成后线程才能继续执行:
do_some_code(r)
```
消息循环：实现异步IO
```
loop = get_event_loop()
while True:
    event = loop.get_event()
    process_event(event)
```
消息循环中，主线程不断地重复“读取消息-处理消息”这一过程

**停止响应**

GUI程序使用消息模型：键盘、鼠标等消息都被发送到GUI程序的消息队列中，然后由GUI程序的主线程处理。GUI线程在一个消息处理的过程中遇到问题导致一次消息处理时间过长，整个GUI程序停止响应了，敲键盘、点鼠标都没有反应

**消息模型**

1. 代码中遇到IO操作
2. 代码发出IO请求，
    1. 不等待IO结果
    2. 直接结束本轮消息处理
    3. 进入下一轮消息处理过程
3. IO操作完成后，CPU收到IO完成消息，直接获取IO操作结果


异步IO优点：一个线程就可以同时处理多个IO请求，不用切换线程，IO密集型的应用程序，使用异步IO将大大提升系统的多任务处理能力

## 18-01 协程(Coroutine)

定义：执行过程中，在子程序内部可中断，然后转而执行别的子程序，在适当的时候再返回来接着执行

```
def A():
    print('1')
    print('2')
    print('3')

def B():
    print('x')
    print('y')
    print('z')
```

协程执行，在执行A的过程中，可以随时中断，去执行B，B也可能在执行过程中中断再去执行A：

```
1
2
x
y
3
z
```
有点像多线程，不同的是协程是一个线程执行，优点

- 极高的执行效率：子程序切换不是线程切换，没有线程切换的开销
- 不需要多线程的锁机制，只有一个线程，不存在同时写变量冲突

发挥多核最大性能：多进程+协程（充分利用多核，又充分发挥协程的高效率）

**generator实现协程**

示例：协程实现生产者-消费者模型
```
生产者生产消息后，直接通过yield跳转到消费者开始执行，待消费者执行完毕后，切换回生产者继续生产，效率极高：

def consumer():
    r = ''
    while True:
        n = yield r
        if not n:
            return
        print('[CONSUMER] Consuming %s...' % n)
        r = '200 OK'

def produce(c):
    c.send(None)
    n = 0
    while n < 5:
        n = n + 1
        print('[PRODUCER] Producing %s...' % n)
        r = c.send(n)
        print('[PRODUCER] Consumer return: %s' % r)
    c.close()

c = consumer()
produce(c)
```
执行结果：
```
[PRODUCER] Producing 1...
[CONSUMER] Consuming 1...
[PRODUCER] Consumer return: 200 OK
[PRODUCER] Producing 2...
[CONSUMER] Consuming 2...
[PRODUCER] Consumer return: 200 OK
[PRODUCER] Producing 3...
[CONSUMER] Consuming 3...
[PRODUCER] Consumer return: 200 OK
[PRODUCER] Producing 4...
[CONSUMER] Consuming 4...
[PRODUCER] Consumer return: 200 OK
[PRODUCER] Producing 5...
[CONSUMER] Consuming 5...
[PRODUCER] Consumer return: 200 OK
```
consumer函数是一个generator，把一个consumer传入produce后：

1. 首先调用c.send(None)启动生成器
2. 然后，一旦生产了东西，通过c.send(n)切换到consumer执行
3. consumer通过yield拿到消息，处理，又通过yield把结果传回
4. produce拿到consumer处理的结果，继续生产下一条消息
5. produce决定不生产了，通过c.close()关闭consumer，整个过程结束

整个流程无锁，由一个线程执行，produce和consumer协作完成任务，所以称为“协程”，而非线程的抢占式多任务


## 18-02 asyncio
内置异步IO支持库
```
import asyncio

@asyncio.coroutine
def hello():
    print("Hello world!")
    # 异步调用asyncio.sleep(1):
    r = yield from asyncio.sleep(1)
    print("Hello again!")

# 获取EventLoop:
loop = asyncio.get_event_loop()
# 执行coroutine
loop.run_until_complete(hello())
loop.close()
```

- @asyncio.coroutine把一个generator标记为coroutine类型
- 然后把这个coroutine扔到EventLoop中执行

运行流程

1. hello()首先打印出Hello world!
2. yield from语法可以让我们方便地调用另一个generator
3. asyncio.sleep()也是一个coroutine，所以线程不会等待asyncio.sleep()，而是直接中断并执行下一个消息循环
4. 当耗时1秒的IO操作asyncio.sleep()返回时，线程就可以从yield from拿到返回值（此处是None），然后接着执行下一行语句

用Task封装两个coroutine：
```
import threading
import asyncio

@asyncio.coroutine
def hello():
    print('Hello world! (%s)' % threading.currentThread())
    yield from asyncio.sleep(1)
    print('Hello again! (%s)' % threading.currentThread())

loop = asyncio.get_event_loop()
tasks = [hello(), hello()]
loop.run_until_complete(asyncio.wait(tasks))
loop.close()
```
观察执行过程：
```
Hello world! (<_MainThread(MainThread, started 140735195337472)>)
Hello world! (<_MainThread(MainThread, started 140735195337472)>)
(暂停约1秒)
Hello again! (<_MainThread(MainThread, started 140735195337472)>)
Hello again! (<_MainThread(MainThread, started 140735195337472)>)
```

两个coroutine是由同一个线程并发执行的

如果把asyncio.sleep()换成真正的IO操作，则多个coroutine就可以由一个线程并发执行

用asyncio的异步网络连接来获取sina、sohu和163的网站首页：

```
import asyncio

@asyncio.coroutine
def wget(host):
    print('wget %s...' % host)
    connect = asyncio.open_connection(host, 80)
    reader, writer = yield from connect
    header = 'GET / HTTP/1.0\r\nHost: %s\r\n\r\n' % host
    writer.write(header.encode('utf-8'))
    yield from writer.drain()
    while True:
        line = yield from reader.readline()
        if line == b'\r\n':
            break
        print('%s header > %s' % (host, line.decode('utf-8').rstrip()))
    # Ignore the body, close the socket
    writer.close()

loop = asyncio.get_event_loop()
tasks = [wget(host) for host in ['www.sina.com.cn', 'www.sohu.com', 'www.163.com']]
loop.run_until_complete(asyncio.wait(tasks))
loop.close()
```
执行结果如下：
```
wget www.sohu.com...
wget www.sina.com.cn...
wget www.163.com...
(等待一段时间)
(打印出sohu的header)
www.sohu.com header > HTTP/1.1 200 OK
www.sohu.com header > Content-Type: text/html
...
(打印出sina的header)
www.sina.com.cn header > HTTP/1.1 200 OK
www.sina.com.cn header > Date: Wed, 20 May 2015 04:56:33 GMT
...
(打印出163的header)
www.163.com header > HTTP/1.0 302 Moved Temporarily
www.163.com header > Server: Cdn Cache Server V2.0
...
```

## 18-03 async/await
用asyncio提供的@asyncio.coroutine可以把一个generator标记为coroutine类型，然后在coroutine内部用yield from调用另一个coroutine实现异步操作

为了简化并更好地标识异步IO，从Python 3.5开始引入了新的语法async和await，可以让coroutine的代码更简洁易读

两步简单的替换：
- 把@asyncio.coroutine替换为async
- 把yield from替换为await

原代码：
```
@asyncio.coroutine
def hello():
    print("Hello world!")
    r = yield from asyncio.sleep(1)
    print("Hello again!")
```
用新语法重新编写如下：
```
async def hello():
    print("Hello world!")
    r = await asyncio.sleep(1)
    print("Hello again!")
```

## 18-04 aiohttp

asyncio可以实现单线程并发IO操作

- 用在客户端，威力不大
- 用在服务端，血妈爆炸
    - HTTP连接（IO操作），所以可以用单线程+coroutine实现多用户的高并发支持

aiohttp

- asyncio实现了TCP、UDP、SSL等协议
- aiohttp是基于asyncio实现的HTTP框架

安装aiohttp：
```
pip install aiohttp
```
编写一个HTTP服务器，分别处理以下URL：

- \/ - 首页返回b\'\<h1>Index\</h1>'
- \/hello/{name} - 根据URL参数返回文本hello, %s!

代码如下：
```
import asyncio

from aiohttp import web

async def index(request):
    await asyncio.sleep(0.5)
    return web.Response(body=b'<h1>Index</h1>')

async def hello(request):
    await asyncio.sleep(0.5)
    text = '<h1>hello, %s!</h1>' % request.match_info['name']
    return web.Response(body=text.encode('utf-8'))

async def init(loop):
    app = web.Application(loop=loop)
    app.router.add_route('GET', '/', index)
    app.router.add_route('GET', '/hello/{name}', hello)
    srv = await loop.create_server(app.make_handler(), '127.0.0.1', 8000)
    print('Server started at http://127.0.0.1:8000...')
    return srv

loop = asyncio.get_event_loop()
loop.run_until_complete(init(loop))
loop.run_forever()
```
注意：aiohttp的初始化函数init()也是一个coroutine，loop.create_server()则利用asyncio创建TCP服务