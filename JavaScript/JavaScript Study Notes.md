# JavaScript Study Notes
> By Kevin Song

<!-- MarkdownTOC autolink='true' -->

- [01 JavaScript 简介](#01-javascript-%E7%AE%80%E4%BB%8B)
- [02 JavaScript 基础](#02-javascript-%E5%9F%BA%E7%A1%80)
  - [02-01 基本语法](#02-01-%E5%9F%BA%E6%9C%AC%E8%AF%AD%E6%B3%95)
  - [02-02 数据类型和变量](#02-02-%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B%E5%92%8C%E5%8F%98%E9%87%8F)
  - [02-03 字符串](#02-03-%E5%AD%97%E7%AC%A6%E4%B8%B2)
  - [02-04 数组](#02-04-%E6%95%B0%E7%BB%84)
  - [02-05 对象](#02-05-%E5%AF%B9%E8%B1%A1)
  - [02-06 条件判断](#02-06-%E6%9D%A1%E4%BB%B6%E5%88%A4%E6%96%AD)
  - [02-07 循环](#02-07-%E5%BE%AA%E7%8E%AF)
  - [02-08 Map和Set](#02-08-map%E5%92%8Cset)
  - [02-09 iterable](#02-09-iterable)
- [03 JavaScript 函数](#03-javascript-%E5%87%BD%E6%95%B0)
  - [03-01 函数定义和调用](#03-01-%E5%87%BD%E6%95%B0%E5%AE%9A%E4%B9%89%E5%92%8C%E8%B0%83%E7%94%A8)
  - [03-02 变量作用域和解构赋值](#03-02-%E5%8F%98%E9%87%8F%E4%BD%9C%E7%94%A8%E5%9F%9F%E5%92%8C%E8%A7%A3%E6%9E%84%E8%B5%8B%E5%80%BC)
  - [03-03 方法](#03-03-%E6%96%B9%E6%B3%95)
  - [03-04 高阶函数](#03-04-%E9%AB%98%E9%98%B6%E5%87%BD%E6%95%B0)
  - [03-05 闭包](#03-05-%E9%97%AD%E5%8C%85)
  - [03-06 箭头函数](#03-06-%E7%AE%AD%E5%A4%B4%E5%87%BD%E6%95%B0)
  - [03-07 generator](#03-07-generator)
- [04 JavaScript 标准对象](#04-javascript-%E6%A0%87%E5%87%86%E5%AF%B9%E8%B1%A1)
  - [04-01 Date](#04-01-date)
  - [04-02 RegExp](#04-02-regexp)
  - [04-03 JSON](#04-03-json)
- [05 JavaScript 面向对象编程](#05-javascript-%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E7%BC%96%E7%A8%8B)
  - [05-01 创建对象](#05-01-%E5%88%9B%E5%BB%BA%E5%AF%B9%E8%B1%A1)
  - [05-02 原型继承](#05-02-%E5%8E%9F%E5%9E%8B%E7%BB%A7%E6%89%BF)
  - [05-03 class继承](#05-03-class%E7%BB%A7%E6%89%BF)
- [06 JavaScript 浏览器](#06-javascript-%E6%B5%8F%E8%A7%88%E5%99%A8)
  - [06-01 浏览器对象](#06-01-%E6%B5%8F%E8%A7%88%E5%99%A8%E5%AF%B9%E8%B1%A1)
  - [06-02 操作DOM](#06-02-%E6%93%8D%E4%BD%9Cdom)
  - [06-03 操作表单](#06-03-%E6%93%8D%E4%BD%9C%E8%A1%A8%E5%8D%95)
  - [06-04 操作文件](#06-04-%E6%93%8D%E4%BD%9C%E6%96%87%E4%BB%B6)
  - [06-05 AJAX](#06-05-ajax)
  - [06-06 Promise](#06-06-promise)
  - [06-07 Canvas](#06-07-canvas)
- [07 JavaScript jQuery](#07-javascript-jquery)
  - [07-01 选择器](#07-01-%E9%80%89%E6%8B%A9%E5%99%A8)
  - [07-02 操作DOM](#07-02-%E6%93%8D%E4%BD%9Cdom)
  - [07-03 事件](#07-03-%E4%BA%8B%E4%BB%B6)
  - [07-04 动画](#07-04-%E5%8A%A8%E7%94%BB)
  - [07-05 AJAX](#07-05-ajax)
  - [07-06 扩展](#07-06-%E6%89%A9%E5%B1%95)
- [08 JavaScript 错误处理](#08-javascript-%E9%94%99%E8%AF%AF%E5%A4%84%E7%90%86)
  - [08-01 错误传播](#08-01-%E9%94%99%E8%AF%AF%E4%BC%A0%E6%92%AD)
  - [08-02 异步错误处理](#08-02-%E5%BC%82%E6%AD%A5%E9%94%99%E8%AF%AF%E5%A4%84%E7%90%86)
- [09 JavaScript underscore](#09-javascript-underscore)
  - [09-01 Collections](#09-01-collections)
  - [09-02 Arrays](#09-02-arrays)
  - [09-03 Functions](#09-03-functions)
  - [09-04 Objects](#09-04-objects)
  - [09-05 Chaining](#09-05-chaining)
- [10 JavaScript Nodejs](#10-javascript-nodejs)
  - [10-01 安装Nodejs和npm](#10-01-%E5%AE%89%E8%A3%85nodejs%E5%92%8Cnpm)
  - [10-02 第一个Node程序](#10-02-%E7%AC%AC%E4%B8%80%E4%B8%AAnode%E7%A8%8B%E5%BA%8F)
  - [10-03 搭建Node开发环境](#10-03-%E6%90%AD%E5%BB%BAnode%E5%BC%80%E5%8F%91%E7%8E%AF%E5%A2%83)
  - [10-04 模块介绍](#10-04-%E6%A8%A1%E5%9D%97%E4%BB%8B%E7%BB%8D)
  - [10-05 基本模块](#10-05-%E5%9F%BA%E6%9C%AC%E6%A8%A1%E5%9D%97)
  - [10-06 Web开发](#10-06-web%E5%BC%80%E5%8F%91)
  - [10-07 自动化工具](#10-07-%E8%87%AA%E5%8A%A8%E5%8C%96%E5%B7%A5%E5%85%B7)

<!-- /MarkdownTOC -->


# 01 JavaScript 简介

**JavaScript 历史**

1995年 Netscape公司让Brendan Eich兄弟10天设计出JavaScript。当时Java火，Netscape想蹭热度所以取名JavaScript，除了语法有点像之外没有什么关系

**ECMAScript**

几个公司联合ECMA（European Computer Manufacturers Association）制定了JavaScript标准，称为**ECMAScript**

JavaScript是Netscape对ECMAScript标准的**一种实现**

**JavaScript 版本**

ECMAScript 6标准（ES6）在2015年6月发布，所谓JavaScript版本就是说它实现了ECMAScript的哪个标准

浏览器发布时就确定了JavaScript的版本，比如IE6不支持ES6。

# 02 JavaScript 基础
**方法一**：直接把代码放到\<head\>里
```
<html>
<head>
  <script>
    alert('Hello, world');
  </script>
</head>
<body>
  ...
</body>
</html>
```
**方法二**：把代码放到单独.js文件，用<script src="..."></script>导入
```
<html>
<head>
  <script src="/static/js/abc.js"></script>
</head>
<body>
  ...
</body>
</html>

```
## 02-01 基本语法
JavaScript的语法和Java语言类似，每个语句以`;`结束，语句块用`{...}`

完整赋值语句

```
var x = 1;
```

完整字符串语句

```
'Hello, world';
```
```{...}```语句块嵌套
```
if (2 > 1) {
    x = 1;
    y = 2;
    z = 3;
    if (x < y) {
        z = 4;
    }
    if (x > y) {
        z = 5;
    }
}
```

**行注释**

```
// 这是一行注释
alert('hello'); // 这也是注释

```

**块注释**

```
/* 
仍然是注释
仍然是注释
*/
```

## 02-02 数据类型和变量

**Number**

```
//整数
123;
//浮点数
0.456
//非数字
NaN;
//无穷大
Infinity;
```
**字符串**

单引号和双引号都能表示字符串：```'abc', "xyz"```

**布尔值**

- true
- false

```&&``` 与运算

```
true && true; // 这个&&语句计算结果为true
true && false; // 这个&&语句计算结果为false
```
```||``` 或运算
```
false || false; // 这个||语句计算结果为false
true || false; // 这个||语句计算结果为true
```
```!``` 非运算
```
! true; // 结果为false
! false; // 结果为true
```

> **两种比较运算符**

- `\=\=`（不推荐使用）：自动转换数据类型再比较
- `\=\=\=`（推荐使用）：不会自动转换数据类型再比较，如果数据类型不一致则返回false

> **NaN和所有其他值都不相等，包括自己**

```
NaN === NaN; // false
```

唯一能判断`NaN`的方法是通过`isNaN()`函数：
```
isNaN(NaN); // true
```
**数组**

创建数组方式一

```
var arr = [1, 2, 3.14, 'Hello', null, true];
```
创建数组方式二

```
var arr = new Array(1, 2, 3);
```
**对象**

JavaScript的对象是一组键（字符串类型）值（任意类型）对组成的无序集合

```
var person = {
    name: 'Bob',
    age: 20,
    tags: ['js', 'web', 'mobile'],
    city: 'Beijing',
    hasCar: true,
    zipcode: null
};

person.name; // 'Bob'
person.zipcode; // null
```

**变量**
```
var a; // 申明了变量a，此时a的值为undefined
var $b = 1; // 申明了变量$b，同时给$b赋值，此时$b的值为1
var s_007 = '007'; // s_007是一个字符串
var Answer = true; // Answer是一个布尔值true
var t = null; // t的值是null
```
**strict模式**
不用var申明那么该变量自动成为全局变量
```
i = 10; // i现在是全局变量
```
启用strict模式：强制通过var申明变量，未使用var申明变量就使用的，将导致运行错误

启用strict模式的方法是在JavaScript代码的第一行写上：
```
'use strict';
```
## 02-03 字符串
转义字符：`\`

ASCII字符用`\x##`表示：

```
'\x41'; // 完全等同于 'A'
```

Unicode字符用`\u####`表示：

```
'\u4e2d\u6587'; // 完全等同于 '中文'
```

**多行字符串**

用`\n`写起来麻烦，ES6标准新增反引号\` ... \`表示
```
`这是一个
多行
字符串`;
```
**模板字符串**

多个字符串连接使用`+`
```
var name = '小明';
var age = 20;
var message = '你好, ' + name + ', 你今年' + age + '岁了!';
alert(message);
```
如果有很多变量需要连接，推荐用ES6新增的模板字符串，表示方法和上面的多行字符串一样，但是它会自动替换字符串中的变量：

```
var name = '小明';
var age = 20;
var message = `你好, ${name}, 你今年${age}岁了!`;
alert(message);
```
**操作字符串**

`length`返回字符串长度

```
var s = 'Hello, world!';
s.length; // 13
```

`toUpperCase()`把一个字符串全部变为大写

```
var s = 'Hello';
s.toUpperCase(); // 返回'HELLO'
```

`toLowerCase()`把一个字符串全部变为小写：

```
var s = 'Hello';
var lower = s.toLowerCase(); // 返回'hello'并赋值给变量lower
lower; // 'hello'
```

`indexOf()`会搜索指定字符串出现的位置：

```
var s = 'hello, world';
s.indexOf('world'); // 返回7
s.indexOf('World'); // 没有找到指定的子串，返回-1
```

`substring()`返回指定索引区间的子串：

```
var s = 'hello, world'
s.substring(0, 5); // 从索引0开始到5（不包括5），返回'hello'
s.substring(7); // 从索引7开始到结束，返回'world'
```




## 02-04 数组
## 02-05 对象
## 02-06 条件判断
## 02-07 循环
## 02-08 Map和Set
## 02-09 iterable
# 03 JavaScript 函数
## 03-01 函数定义和调用
## 03-02 变量作用域和解构赋值
## 03-03 方法
## 03-04 高阶函数
## 03-05 闭包
## 03-06 箭头函数
## 03-07 generator
# 04 JavaScript 标准对象
## 04-01 Date
## 04-02 RegExp
## 04-03 JSON
# 05 JavaScript 面向对象编程
## 05-01 创建对象
## 05-02 原型继承
## 05-03 class继承
# 06 JavaScript 浏览器
## 06-01 浏览器对象
## 06-02 操作DOM
## 06-03 操作表单
## 06-04 操作文件
## 06-05 AJAX
## 06-06 Promise
## 06-07 Canvas
# 07 JavaScript jQuery
## 07-01 选择器
## 07-02 操作DOM
## 07-03 事件
## 07-04 动画
## 07-05 AJAX
## 07-06 扩展
# 08 JavaScript 错误处理
## 08-01 错误传播
## 08-02 异步错误处理
# 09 JavaScript underscore
## 09-01 Collections
## 09-02 Arrays
## 09-03 Functions
## 09-04 Objects
## 09-05 Chaining
# 10 JavaScript Nodejs
## 10-01 安装Nodejs和npm
## 10-02 第一个Node程序
## 10-03 搭建Node开发环境
## 10-04 模块介绍
## 10-05 基本模块
## 10-06 Web开发
## 10-07 自动化工具