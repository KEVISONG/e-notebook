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
	- [02-09 iterable 类型](#02-09-iterable-%E7%B1%BB%E5%9E%8B)
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
**方法一**：直接把代码放到`<head>`里
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
**方法二**：把代码放到单独.js文件，用`<script src="..."> </script>`导入
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
**`length`获取数组长度**
```
var arr = [1, 2, 3.14, 'Hello', null, true];
arr.length; // 6
```
> 给length赋新值会导致数组大小改变

```
var arr = [1, 2, 3];
arr.length; // 3
arr.length = 6;
arr; // arr变为[1, 2, 3, undefined, undefined, undefined]
arr.length = 2;
arr; // arr变为[1, 2]
```
**修改元素值**
```
var arr = ['A', 'B', 'C'];
arr[1] = 99;
arr; // arr现在变为['A', 99, 'C']
```
> 越界访问会引起Array大小的变化

```
var arr = [1, 2, 3];
arr[5] = 'x';
arr; // arr变为[1, 2, 3, undefined, undefined, 'x']
```

**`indxOf()`搜索指定元素位置**
```
var arr = [10, 20, '30', 'xyz'];
arr.indexOf(10); // 元素10的索引为0
arr.indexOf(30); // 元素30没有找到，返回-1
```

**`slice()`截取数组**
```
var arr = ['A', 'B', 'C', 'D', 'E', 'F', 'G'];
arr.slice(0, 3); // 从索引0开始，到索引3结束，但不包括索引3: ['A', 'B', 'C']
arr.slice(3); // 从索引3开始到结束: ['D', 'E', 'F', 'G']
```
> 不传参数则复制一个一模一样的数组

```
var arr = ['A', 'B', 'C', 'D', 'E', 'F', 'G'];
var aCopy = arr.slice();
aCopy; // ['A', 'B', 'C', 'D', 'E', 'F', 'G']
aCopy === arr; // false
```
**`push()`和`pop()`末尾增减**

`push()`向数组的末尾添加元素，`pop()`把数组的最后一个元素删除掉：
```
var arr = [1, 2];
arr.push('A', 'B'); // 返回Array新的长度: 4
arr; // [1, 2, 'A', 'B']
arr.pop(); // pop()返回'B'
arr; // [1, 2, 'A']
arr.pop(); arr.pop(); arr.pop(); // 连续pop 3次
arr; // []
arr.pop(); // 空数组继续pop不会报错，而是返回undefined
arr; // []
```
**`unshift()`和`shift()`头部增减**
`unshift()`向数组的头部添加元素，`shift()`把数组的第一个元素删掉：
```
var arr = [1, 2];
arr.unshift('A', 'B'); // 返回Array新的长度: 4
arr; // ['A', 'B', 1, 2]
arr.shift(); // 'A'
arr; // ['B', 1, 2]
arr.shift(); arr.shift(); arr.shift(); // 连续shift 3次
arr; // []
arr.shift(); // 空数组继续shift不会报错，而是返回undefined
arr; // []
```
**`sort()`排序**
```
var arr = ['B', 'C', 'A'];
arr.sort();
arr; // ['A', 'B', 'C']
```
**`reverse()`逆序**
```
var arr = ['one', 'two', 'three'];
arr.reverse(); 
arr; // ['three', 'two', 'one']
```
**`splice()`万能方法**

- 第一个参数 起始删除索引
- 第二个参数 删除元素个数
- 其他参数 需要增加的元素

```
var arr = ['Microsoft', 'Apple', 'Yahoo', 'AOL', 'Excite', 'Oracle'];
// 从索引2开始删除3个元素,然后再添加两个元素:
arr.splice(2, 3, 'Google', 'Facebook'); // 返回删除的元素 ['Yahoo', 'AOL', 'Excite']
arr; // ['Microsoft', 'Apple', 'Google', 'Facebook', 'Oracle']
// 只删除,不添加:
arr.splice(2, 2); // ['Google', 'Facebook']
arr; // ['Microsoft', 'Apple', 'Oracle']
// 只添加,不删除:
arr.splice(2, 0, 'Google', 'Facebook'); // 返回[],因为没有删除任何元素
arr; // ['Microsoft', 'Apple', 'Google', 'Facebook', 'Oracle']
```
**`concat()`连接两个数组**
```
var arr = ['A', 'B', 'C'];
var added = arr.concat([1, 2, 3]);
added; // ['A', 'B', 'C', 1, 2, 3]
```
> `concat()`方法并没有修改当前Array，而是返回了一个新的Array

**`join()`连接数组中的元素**

把当前Array的每个元素都用指定的字符串连接起来，然后返回连接后的字符串
```
var arr = ['A', 'B', 'C', 1, 2, 3];
arr.join('-'); // 'A-B-C-1-2-3'
```
> 如果Array的元素不是字符串，将自动转换为字符串后再连接

**多维数组**

如果数组的某个元素又是一个Array，则可以形成多维数组
```
var arr = [[1, 2, 3], [400, 500, 600], '-'];
```
## 02-05 对象

JavaScript的对象是一种无序的集合数据类型

- 用一个`{...}`表示一个对象
- 键值对以`xxx: xxx`形式申明
    - 键都是字符串
    - 值可以是任意类型
- 用`,`隔开

```
var xiaoming = {
    name: '小明',
    birth: 1990,
    school: 'No.1 Middle School',
    height: 1.70,
    weight: 65,
    score: null
};
```
> 如果属性名包含特殊字符，就必须用`''`括起来
> 如果属性名包含特殊字符，就必须用`['xxx']`访问

```
var xiaohong = {
    name: '小红',
    'middle-school': 'No.1 Middle School'
};
xiaohong['middle-school']; // 'No.1 Middle School'
xiaohong['name']; // '小红'
xiaohong.name; // '小红'
```
**给对象添加或删除属性**

```
var xiaoming = {
    name: '小明'
};
xiaoming.age; // undefined
xiaoming.age = 18; // 新增一个age属性
xiaoming.age; // 18
delete xiaoming.age; // 删除age属性
xiaoming.age; // undefined
delete xiaoming['name']; // 删除name属性
xiaoming.name; // undefined
delete xiaoming.school; // 删除一个不存在的school属性也不会报错
```
`in`检查是否拥有属性

```
var xiaoming = {
    name: '小明',
    birth: 1990,
    school: 'No.1 Middle School',
    height: 1.70,
    weight: 65,
    score: null
};
'name' in xiaoming; // true
'grade' in xiaoming; // false
```
> 如果in判断一个属性存在，这个属性不一定是xiaoming的，它可能是xiaoming继承得到的

要判断一个属性是否是xiaoming自身拥有的，而不是继承得到的，可以用`hasOwnProperty()`

```
var xiaoming = {
    name: '小明'
};
xiaoming.hasOwnProperty('name'); // true
xiaoming.hasOwnProperty('toString'); // false
```

## 02-06 条件判断
`if () { ... } else { ... }`来进行条件判断

```
var age = 20;
if (age >= 18) { // 如果age >= 18为true，则执行if语句块
    alert('adult');
} else { // 否则执行else语句块
    alert('teenager');
}
```
**多行条件判断**

```
var age = 3;
if (age >= 18) {
    alert('adult');
} else if (age >= 6) {
    alert('teenager');
} else {
    alert('kid');
}
```

## 02-07 循环

**`for`循环**

```
for (初始条件; 判断条件; 循环后条件) {
    语句
}
```

```
var x = 0;
var i;
for (i=1; i<=10000; i++) {
    x = x + i;
}
x; // 50005000
```
> 支持 `for ... in` 和python一样

**`while`循环**

```
var x = 0;
var n = 99;
while (n > 0) {
    x = x + n;
    n = n - 2;
}
x; // 2500
```

**`do...while`循环**
```
var n = 0;
do {
    n = n + 1;
} while (n < 100);
n; // 100
```
> 循环体至少执行一次

## 02-08 Map和Set

**Map 键值对的键可以是任意类型**


```
var m = new Map([['Michael', 95], ['Bob', 75], ['Tracy', 85]]);
m.get('Michael'); // 95
```
初始化Map需要一个二维数组，或者直接初始化一个空Map。Map具有以下方法：

```
var m = new Map(); // 空Map
m.set('Adam', 67); // 添加新的key-value
m.set('Bob', 59);
m.has('Adam'); // 是否存在key 'Adam': true
m.get('Adam'); // 67
m.delete('Adam'); // 删除key 'Adam'
m.get('Adam'); // undefined
```
一个key只能对应一个value，所以，多次对一个key放入value，后面的值会把前面的值冲掉：

```
var m = new Map();
m.set('Adam', 67);
m.set('Adam', 88);
m.get('Adam'); // 88
```
**Set 没有重复值**
```
var s = new Set([1, 2, 3, 3, '3']);
s; // Set {1, 2, 3, "3"}
```
**`add()`添加元素**
```
s.add(4);
s; // Set {1, 2, 3, 4}
```
**`delete()`删除元素**
```
var s = new Set([1, 2, 3]);
s; // Set {1, 2, 3}
s.delete(3);
s; // Set {1, 2}
```
## 02-09 iterable 类型
Array、Map和Set都属于iterable类型

具有iterable类型的集合可以通过新的`for ... of`循环来遍历
```
var a = ['A', 'B', 'C'];
var s = new Set(['A', 'B', 'C']);
var m = new Map([[1, 'x'], [2, 'y'], [3, 'z']]);
for (var x of a) { // 遍历Array
    console.log(x);
}
for (var x of s) { // 遍历Set
    console.log(x);
}
for (var x of m) { // 遍历Map
    console.log(x[0] + '=' + x[1]);
```
**`for ... of`循环和`for ... in`循环的区别**

`for ... in`循环会把数组对象的额外属性循环出来
```
var a = ['A', 'B', 'C'];
a.name = 'Hello';
for (var x in a) {
    console.log(x); // '0', '1', '2', 'name'
}
```
`for ... of`只会循环集合本身元素

```
var a = ['A', 'B', 'C'];
a.name = 'Hello';
for (var x of a) {
    console.log(x); // 'A', 'B', 'C'
}
```


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