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
**定义函数方式一：**
```
function abs(x) {
    if (x >= 0) {
        return x;
    } else {
        return -x;
    }
}
```

- `function`关键字定义函数
- `abs`函数名
- `(x)`函数参数
- `{...}`函数体

> 没有`return`语句的函数返回`undefined`

**定义函数方式二：**
```
var abs = function (x) {
    if (x >= 0) {
        return x;
    } else {
        return -x;
    }
};
```
`function (x) { ... }`是一个匿名函数，它没有函数名。但是，这个匿名函数赋值给了变量`abs`，所以，通过变量`abs`就可以调用该函数

> 第二种方式按照完整语法需要在函数体末尾加一个`;`

> 传入参数太多也没事儿

```
abs(10, 'blablabla'); // 返回10
abs(-9, 'haha', 'hehe', null); // 返回9
```
> 传入参数太少也没事儿，此时abs(x)函数的参数x将收到undefined，计算结果为NaN


```
abs(); // 返回NaN
```

**`arguments`关键字**

`arguments`可以获得调用者传入的所有参数。也就是说，即使函数不定义任何参数，还是可以拿到参数的值：
```
function abs() {
    if (arguments.length === 0) {
        return 0;
    }
    var x = arguments[0];
    return x >= 0 ? x : -x;
}

abs(); // 0
abs(10); // 10
abs(-9); // 9
```
**`rest`关键字**

`rest`表示剩下的参数

```
function foo(a, b, ...rest) {
    console.log('a = ' + a);
    console.log('b = ' + b);
    console.log(rest);
}

foo(1, 2, 3, 4, 5);
// 结果:
// a = 1
// b = 2
// Array [ 3, 4, 5 ]

foo(1);
// 结果:
// a = 1
// b = undefined
// Array []
```

## 03-02 变量作用域和解构赋值

**函数内部声明的变量作用域在函数内部**

```
function foo() {
    var x = 1;
    x = x + 1;
}
x = x + 2; // ReferenceError! 无法在函数体外引用变量x
```
**变量提升**

JavaScript函数定义时，自动扫描函数体并且把声明的变量提升到顶部

```
function foo() {
    var x = 'Hello, ' + y;
    console.log(x);
    var y = 'Bob';
}
foo();
```
相当于如下

```
function foo() {
    var y; // 提升变量y的申明，此时y为undefined
    var x = 'Hello, ' + y;
    console.log(x);
    y = 'Bob';
}
```
**全局作用域**

不在任何函数内定义的变量就具有**全局作用域**

JavaScript默认有一个全局对象`window`，全局作用域的变量实际上被绑定到`window`的一个属性：

```
var course = 'Learn JavaScript';
alert(course); // 'Learn JavaScript'
alert(window.course); // 'Learn JavaScript'
```
由于函数定义有两种方式，以变量方式`var foo = function () {}`定义的函数实际上也是一个全局变量，因此，顶层函数的定义也被视为一个全局变量，并绑定到`window`对象：

```
function foo() {
    alert('foo');
}

foo(); // 直接调用foo()
window.foo(); // 通过window.foo()调用
```
> 同理`alert()`也是window的一个变量

**名字空间**

不同的JavaScript文件使用相同的全局变量会造成命名冲突

解决方案：把所有变量和函数绑定到一个全局变量

```
// 唯一的全局变量MYAPP:
var MYAPP = {};

// 其他变量:
MYAPP.name = 'myapp';
MYAPP.version = 1.0;

// 其他函数:
MYAPP.foo = function () {
    return 'foo';
};
```
> 许多著名的JavaScript库都是这么干的：jQuery，YUI，underscore等

**局部作用域**

`for`循环等语句块中无法定义局部变量

```
function foo() {
    for (var i=0; i<100; i++) {
        //
    }
    i += 100; // 仍然可以引用变量i
}
```
解决方案：ES6新关键字`let`，代替`var`申明一个块级作用域的变量

```
function foo() {
    var sum = 0;
    for (let i=0; i<100; i++) {
        sum += i;
    }
    // SyntaxError:
    i += 1;
}
```
**常量**

定义方式一：全大写

```
var PI = 3.14;
```

定义方式二：ES6新关键字`const`

```
const PI = 3.14;
PI = 3; // 某些浏览器不报错，但是无效果！
PI; // 3.14
```

**解构赋值**

传统方法一个数组的元素分别赋值给几个变量：

```
var array = ['hello', 'JavaScript', 'ES6'];
var x = array[0];
var y = array[1];
var z = array[2];
```
ES6新特性解构赋值，多个变量用`[...]`括起来

```
var [x, y, z] = ['hello', 'JavaScript', 'ES6'];
```
嵌套型解构赋值

```
let [x, [y, z]] = ['hello', ['JavaScript', 'ES6']];
x; // 'hello'
y; // 'JavaScript'
z; // 'ES6'

```
忽略元素的解构赋值

```
let [, , z] = ['hello', 'JavaScript', 'ES6']; // 忽略前两个元素，只对z赋值第三个元素
z; // 'ES6'
```
对象的解构赋值

```
var person = {
    name: '小明',
    age: 20,
    gender: 'male',
    passport: 'G-12345678',
    school: 'No.4 middle school',
    address: {
        city: 'Beijing',
        street: 'No.1 Road',
        zipcode: '100001'
    }
};
var {name, address: {city, zip}} = person;
name; // '小明'
city; // 'Beijing'
zip; // undefined, 因为属性名是zipcode而不是zip
// 注意: address不是变量，而是为了让city和zip获得嵌套的address对象的属性:
address; // Uncaught ReferenceError: address is not defined
```
> 如果对应的属性不存在，变量将被赋值为`undefined`

如果要使用的变量名和属性名不一致

```
var person = {
    name: '小明',
    age: 20,
    gender: 'male',
    passport: 'G-12345678',
    school: 'No.4 middle school'
};

// 把passport属性赋值给变量id:
let {name, passport:id} = person;
name; // '小明'
id; // 'G-12345678'
// 注意: passport不是变量，而是为了让变量id获得passport属性:
passport; // Uncaught ReferenceError: passport is not defined
```
**解构赋值应用**

交换两个变量x和y的值
```
var x=1, y=2;
[x, y] = [y, x]
```

快速获取当前页面的域名和路径

```
var {hostname:domain, pathname:path} = location;
```
## 03-03 方法
**给对象绑定方法**

```
var xiaoming = {
    name: '小明',
    birth: 1990,
    age: function () {
        var y = new Date().getFullYear();
        return y - this.birth;
    }
};
```
> `this`指向当前对象

特殊情况：函数写在方法外面并且被方法调用

```
function getAge() {
    var y = new Date().getFullYear();
    return y - this.birth;
}

var xiaoming = {
    name: '小明',
    birth: 1990,
    age: getAge
};

xiaoming.age(); // 25, 正常结果
getAge(); // NaN
```
> 此时this指向window，所以返回NaN

> `strict`模式下，`this`指向`undefined`

**`apply()`指定this指向**

- 参数一：需要绑定的`this`变量
- 参数二：一个数组，包含函数本身参数
```
function getAge() {
    var y = new Date().getFullYear();
    return y - this.birth;
}

var xiaoming = {
    name: '小明',
    birth: 1990,
    age: getAge
};

xiaoming.age(); // 25
getAge.apply(xiaoming, []); // 25, this指向xiaoming, 参数为空
```

`call()`和`apply()`差不多，唯一区别是：

- `apply()`把参数打包成`Array`再传入；
- `call()`把参数按顺序传入。


```
Math.max.apply(null, [3, 5, 4]); // 5
Math.max.call(null, 3, 5, 4); // 5
```
**装饰器**

统计一下代码一共调用了多少次parseInt()
```
var count = 0;
var oldParseInt = parseInt; // 保存原函数

window.parseInt = function () {
    count += 1;
    return oldParseInt.apply(null, arguments); // 调用原函数
};
```
## 03-04 高阶函数

高阶函数：参数是函数的函数

```
function add(x, y, f) {
    return f(x) + f(y);
}
```
**`map()`函数**

`map()`方法定义在JavaScript的`Array`中，调用Array的`map()`方法时传入一个函数，就得到了一个新的Array作为结果

```
var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9];
arr.map(String); // ['1', '2', '3', '4', '5', '6', '7', '8', '9']
```

**`reduce()`函数**

```
[x1, x2, x3, x4].reduce(f) = f(f(f(x1, x2), x3), x4)
```
数组求和

```
var arr = [1, 3, 5, 7, 9];
arr.reduce(function (x, y) {
    return x + y;
}); // 25
```
**`filter()`函数**

用于把`Array`的某些元素根据返回值是`true`还是`false`过滤掉，然后返回剩下的元素

Array中，删掉偶数，只保留奇数：

```
var arr = [1, 2, 4, 5, 6, 9, 10, 15];
var r = arr.filter(function (x) {
    return x % 2 !== 0;
});
r; // [1, 5, 9, 15]
```
**`sort()`函数**

`String`排序
```
// apple排在了最后:
['Google', 'apple', 'Microsoft'].sort(); // ['Google', 'Microsoft", 'apple']
```

`Number`排序
```
// 无法理解的结果:
[10, 20, 1, 2].sort(); // [1, 10, 2, 20]
```
> `Array`的`sort()`方法默认把所有元素先转换为String再排序

按照数字大小排序：

```
var arr = [10, 20, 1, 2];
arr.sort(function (x, y) {
    if (x < y) {
        return -1;
    }
    if (x > y) {
        return 1;
    }
    return 0;
});
console.log(arr); // [1, 2, 10, 20]
```

## 03-05 闭包

对Array求和的函数：

```
function sum(arr) {
    return arr.reduce(function (x, y) {
        return x + y;
    });
}

sum([1, 2, 3, 4, 5]); // 15
```

不想立即求和，返回求和函数：

```
function lazy_sum(arr) {
    var sum = function () {
        return arr.reduce(function (x, y) {
            return x + y;
        });
    }
    return sum;
}
var f = lazy_sum([1, 2, 3, 4, 5]); // function sum()
f(); // 15
```
闭包：当`lazy_sum()`返回函数`sum()`时，相关参数和变量都保存在返回的函数中的这种程序结构

## 03-06 箭头函数

ES6新增箭头函数

```
x => x * x
```
相当于

```
function (x) {
    return x * x;
}
```

包含多条语句的箭头函数

```
x => {
    if (x > 0) {
        return x * x;
    }
    else {
        return - x * x;
    }
}
```
包含多个参数的箭头函数

```
// 两个参数:
(x, y) => x * x + y * y

// 无参数:
() => 3.14

// 可变参数:
(x, y, ...rest) => {
    var i, sum = x + y;
    for (i=0; i<rest.length; i++) {
        sum += rest[i];
    }
    return sum;
}
```
返回对象的箭头函数

```
// ok:
x => ({ foo: x })
```
> 箭头函数类似匿名函数

## 03-07 generator

ES6新增的类似Python的generator的特性

由`function*`定义

```
function* foo(x) {
    yield x + 1;
    yield x + 2;
    return x + 3;
}
var x = foo(3)
x.next()
x.next()
x.next()
```

# 04 JavaScript 标准对象

`typeof`关键字判断对象类型

```
typeof 123; // 'number'
typeof NaN; // 'number'
typeof 'str'; // 'string'
typeof true; // 'boolean'
typeof undefined; // 'undefined'
typeof Math.abs; // 'function'
typeof null; // 'object'
typeof []; // 'object'
typeof {}; // 'object'
```
**包装对象**

类似Java里`int`和`Integer`的关系，JavaScript中有

```
var n = new Number(123); // 123,生成了新的包装类型
var b = new Boolean(true); // true,生成了新的包装类型
var s = new String('str'); // 'str',生成了新的包装类型
```
> 虽然包装对象看上去和原来的值一模一样，显示出来也是一模一样，但他们的类型已经变为object

包装对象和原始值用===比较会返回false：

```
typeof new Number(123); // 'object'
new Number(123) === 123; // false

typeof new Boolean(true); // 'object'
new Boolean(true) === true; // false

typeof new String('str'); // 'object'
new String('str') === 'str'; // false
```
## 04-01 Date

**`Date`对象用来表示日期和时间**

获取系统当前时间
```
var now = new Date();
now; // Wed Jun 24 2015 19:49:22 GMT+0800 (CST)
now.getFullYear(); // 2015, 年份
now.getMonth(); // 5, 月份，注意月份范围是0~11，5表示六月
now.getDate(); // 24, 表示24号
now.getDay(); // 3, 表示星期三
now.getHours(); // 19, 24小时制
now.getMinutes(); // 49, 分钟
now.getSeconds(); // 22, 秒
now.getMilliseconds(); // 875, 毫秒数
now.getTime(); // 1435146562875, 以number形式表示的时间戳
```
第一种方法：创建一个指定日期和时间的Date对象
```
var d = new Date(2015, 5, 19, 20, 15, 30, 123);
d; // Fri Jun 19 2015 20:15:30 GMT+0800 (CST)
```
> JavaScript的Date对象月份值从0开始，0=1月，1=2月，2=3月，……，11=12月。 

第二种方法：创建一个指定日期和时间的Date对象：解析一个符合ISO 8601格式的字符串

```
var d = Date.parse('2015-06-24T19:49:22.875+08:00');
d; // 1435146562875
```
返回的不是Date对象，而是一个时间戳。不过有时间戳就可以很容易地把它转换为一个Date：
```
var d = new Date(1435146562875);
d; // Wed Jun 24 2015 19:49:22 GMT+0800 (CST)
d.getMonth(); // 5
```
**时区转换**

时区


```
var d = new Date(1435146562875);
d.toLocaleString(); // '2015/6/24 下午7:49:22'，本地时间（北京时区+8:00），显示的字符串与操作系统设定的格式有关
d.toUTCString(); // 'Wed, 24 Jun 2015 11:49:22 GMT'，UTC时间，与本地时间相差8小时
```
## 04-02 RegExp

创建正则表达式对象方式一：

```
var re1 = /ABC\-001/;
```
创建正则表达式对象方式二：

```
var re2 = new RegExp('ABC\\-001');
```
**`test()`测试字符串是否match**
```
var re = /^\d{3}\-\d{3,8}$/;
re.test('010-12345'); // true
re.test('010-1234x'); // false
re.test('010 12345'); // false
```
**`split()`切分字符串**

```
'a b   c'.split(' '); // ['a', 'b', '', '', 'c']
```
**`exec()`提取子串**

- `exec()`匹配成功返回一个Array，第一个元素是正则表达式匹配到的整个字符串，后面的字符串表示匹配成功的子串
- `exec()`匹配失败返回null

```
var re = /^(\d{3})-(\d{3,8})$/;
re.exec('010-12345'); // ['010-12345', '010', '12345']
re.exec('010 12345'); // null
```

**贪婪匹配**

正则匹配默认是贪婪匹配

```
var re = /^(\d+)(0*)$/;
re.exec('102300'); // ['102300', '102300', '']
```
非贪婪匹配需要加`?`

```
var re = /^(\d+?)(0*)$/;
re.exec('102300'); // ['102300', '1023', '00']
```

## 04-03 JSON

JSON是JavaScript Object Notation的缩写，它是一种数据交换格式。

JSON数据类型：

- number：和JavaScript的`number`完全一致；
- boolean：就是JavaScript的`true`或`false`；
- string：就是JavaScript的`string`；
- null：就是JavaScript的`null`；
- array：就是JavaScript的Array表示方式——`[]`；
- object：就是JavaScript的`{ ... }`表示方式。

**序列化**

把小明这个对象序列化成JSON格式的字符串：

```
'use strict';

var xiaoming = {
    name: '小明',
    age: 14,
    gender: true,
    height: 1.65,
    grade: null,
    'middle-school': '\"W3C\" Middle School',
    skills: ['JavaScript', 'Java', 'Python', 'Lisp']
};
JSON.stringify(xiaoming, null, '  ');
```
结果
```
{
  "name": "小明",
  "age": 14,
  "gender": true,
  "height": 1.65,
  "grade": null,
  "middle-school": "\"W3C\" Middle School",
  "skills": [
    "JavaScript",
    "Java",
    "Python",
    "Lisp"
  ]
}
```
- 第一个参数：对象名
- 第二个参数：控制删选对象的键值，以输出指定属性
```
JSON.stringify(xiaoming, ['name', 'skills'], '  ');
```

结果：

```
{
  "name": "小明",
  "skills": [
    "JavaScript",
    "Java",
    "Python",
    "Lisp"
  ]
}
```
精确控制序列化小明，可以给`xiaoming`定义一个`toJSON()`的方法，直接返回JSON应该序列化的数据：

```
var xiaoming = {
    name: '小明',
    age: 14,
    gender: true,
    height: 1.65,
    grade: null,
    'middle-school': '\"W3C\" Middle School',
    skills: ['JavaScript', 'Java', 'Python', 'Lisp'],
    toJSON: function () {
        return { // 只输出name和age，并且改变了key：
            'Name': this.name,
            'Age': this.age
        };
    }
};

JSON.stringify(xiaoming); // '{"Name":"小明","Age":14}'
```

**反序列化**

拿到一个JSON格式的字符串，我们直接用`JSON.parse()`把它变成一个JavaScript对象：
```
JSON.parse('[1,2,3,true]'); // [1, 2, 3, true]
JSON.parse('{"name":"小明","age":14}'); // Object {name: '小明', age: 14}
JSON.parse('true'); // true
JSON.parse('123.45'); // 123.45

```

# 05 JavaScript 面向对象编程

**`__proto__`改变对象原型**

```
var Student = {
    name: 'Robot',
    height: 1.2,
    run: function () {
        console.log(this.name + ' is running...');
    }
};

var xiaoming = {
    name: '小明'
};

xiaoming.__proto__ = Student;
```

`xiaoming`可以`run()`

```
xiaoming.name; // '小明'
xiaoming.run(); // 小明 is running...
```
新建一个鸟对象
```
var Bird = {
    fly: function () {
        console.log(this.name + ' is flying...');
    }
};

xiaoming.__proto__ = Bird;
```
现在`xiaoming`已经无法`run()`了，他已经变成了一只鸟：

```
xiaoming.fly(); // 小明 is flying...
```
## 05-01 创建对象
JavaScript对每个创建的对象都会设置一个**原型**，指向它的**原型对象**。
Array对象：
```
var arr = [1, 2, 3];
```
原型链是：
```
arr ----> Array.prototype ----> Object.prototype ----> null
```
`Array.prototype`定义了`indexOf()`、`shift()`等方法，因此可以在所有的Array对象上直接调用这些方法

**构造函数**

```
function Student(name) {
    this.name = name;
    this.hello = function () {
        alert('Hello, ' + this.name + '!');
    }
}
```

用关键字`new`来调用这个函数，并返回一个对象：

```
var xiaoming = new Student('小明');
xiaoming.name; // '小明'
xiaoming.hello(); // Hello, 小明!
```
> 如果不写`new`，这就是一个普通函数，它返回`undefined`。

> 如果写了`new`，它就变成了一个构造函数，它绑定的`this`指向新创建的对象，并默认返`this`，不需要在最后写`return this`;

原型链
```
xiaoming ↘
xiaohong → Student.prototype ----> Object.prototype ----> null
xiaojun  ↗
```
> 用`new Student()`创建的对象还从原型上获得了一个`constructor`属性，它指向函数`Student`本身

![image](https://cdn.liaoxuefeng.com/cdn/files/attachments/00143529922671163eebb527bc14547ac11363bf186557d000/l)

给对象的原型添加方法可以被所有对象共享

```
function Student(name) {
    this.name = name;
}

Student.prototype.hello = function () {
    alert('Hello, ' + this.name + '!');
};
```
![image](https://cdn.liaoxuefeng.com/cdn/files/attachments/001435299854512faf32868f60348be878982909b5a5d04000/l)

**防止忘记写`new`**

编写一个createStudent()函数，在内部封装所有的new操作

```
function Student(props) {
    this.name = props.name || '匿名'; // 默认值为'匿名'
    this.grade = props.grade || 1; // 默认值为1
}

Student.prototype.hello = function () {
    alert('Hello, ' + this.name + '!');
};

function createStudent(props) {
    return new Student(props || {})
}
```
`createStudent()`优点

- 不需要`new`
- 参数灵活，可以不传，也可以这样传

```
var xiaoming = createStudent({
    name: '小明'
});

xiaoming.grade; // 1
```

## 05-02 原型继承

`Student`构造函数

```
function Student(props) {
    this.name = props.name || 'Unnamed';
}

Student.prototype.hello = function () {
    alert('Hello, ' + this.name + '!');
}
```
`Student`的原型链

![image](https://cdn.liaoxuefeng.com/cdn/files/attachments/001439872136313496e60e07ed143bda40a0200b12d8cc3000/l)

基于`Student`扩展出`PrimaryStudent`

```
function PrimaryStudent(props) {
    // 调用Student构造函数，绑定this变量:
    Student.call(this, props);
    this.grade = props.grade || 1;
}
```
`PrimaryStudent`的原型链

```
new PrimaryStudent() ----> PrimaryStudent.prototype ----> Object.prototype ----> null
```
想办法把原型链修改为：
```
new PrimaryStudent() ----> PrimaryStudent.prototype ----> Student.prototype ----> Object.prototype ----> null
```
**原型继承`inherits()`**

```
function inherits(Child, Parent) {
    var F = function () {};
    F.prototype = Parent.prototype;
    Child.prototype = new F();
    Child.prototype.constructor = Child;
}
```
原型继承实现方式：

- 定义新的构造函数，并在内部用`call()`调用希望“继承”的构造函数，并绑定`this`；
- 借助中间函数`F`实现原型链继承，最好通过封装的`inherits`函数完成；
- 继续在新的构造函数的原型上定义新方法

```
function Student(props) {
    this.name = props.name || 'Unnamed';
}

Student.prototype.hello = function () {
    alert('Hello, ' + this.name + '!');
}

function PrimaryStudent(props) {
    Student.call(this, props);
    this.grade = props.grade || 1;
}

// 实现原型继承链:
inherits(PrimaryStudent, Student);

// 绑定其他方法到PrimaryStudent原型:
PrimaryStudent.prototype.getGrade = function () {
    return this.grade;
};
```

## 05-03 class继承

**`function`定义类**

```
function Student(name) {
    this.name = name;
}

Student.prototype.hello = function () {
    alert('Hello, ' + this.name + '!');
}
```

**`class`定义类**

```
class Student {
    constructor(name) {
        this.name = name;
    }

    hello() {
        alert('Hello, ' + this.name + '!');
    }
}
```
**`class`继承**

```
class PrimaryStudent extends Student {
    constructor(name, grade) {
        super(name); // 记得用super调用父类的构造方法!
        this.grade = grade;
    }

    myGrade() {
        alert('I am at grade ' + this.grade);
    }
}
```
> ES6引入`class`关键字，不是所有浏览器都支持

# 06 JavaScript 浏览器
## 06-01 浏览器对象

**`window`对象**

`window`对象不但充当**全局作用域**，而且表示**浏览器窗口**

`window`对象属性：

- `innerWidth`和`innerHeight`获取浏览器窗口的内部宽高（除去菜单栏、工具栏、边框等）
- `outerWidth`和`outerHeight`获取浏览器窗口整个宽高


```
var a = window.innerWidth;
var b = window.innerHeight;
var c = window.outerWidth;
var d = window.outerHeight;
```

**`navigator`对象**

`navigator`对象表示浏览器的信息

`navigator`对象属性：

- `navigator.appName`: 浏览器名称
- `navigator.appVersion`: 浏览器版本
- `navigator.language`: 浏览器设置的语言
- `navigator.platform`: 操作系统类型
- `navigator.userAgent`: 浏览器谁当的`User-Agent`字符串

> navigator的信息可以很容易地被用户修改，所以JavaScript读取的值不一定正确

**`screen`对象**

`screen`对象表示屏幕的信息

`screen`对象的属性：

- `screen.width`：屏幕宽度，以像素为单位
- `screen.height`：屏幕高度，以像素为单位
- `screen.colorDepth`：返回颜色位数

**`location`对象**

`location`对象表示当前页面的URL信息


```
location.href; //http://www.example.com:8080/path/index.html?a=1&b=2#TOP
location.protocol; // 'http'
location.host; // 'www.example.com'
location.port; // '8080'
location.pathname; // '/path/index.html'
location.search; // '?a=1&b=2'
location.hash; // 'TOP'
```

- `location.assign()`：加载新页面
- `location.reload()`：重新加载当前页面

**`document`对象**

`document`对象表示当前页面

- `title`属性从`<title>xxx</title>`读取，而且可以动态改变

```
document.title = '努力学习JavaScript!';
```

> HTML在浏览器中以DOM形式表示为树形结构，`document`对象就是整个DOM树的根节点

- `document.getElementById()`：按ID获得一个DOM节点
- `document.getElementByTagName()`：按Tag名获得一组DOM节点

```
<dl id="drink-menu" style="border:solid 1px #ccc;padding:6px;">
    <dt>摩卡</dt>
    <dd>热摩卡咖啡</dd>
    <dt>酸奶</dt>
    <dd>北京老酸奶</dd>
    <dt>果汁</dt>
    <dd>鲜榨苹果汁</dd>
</dl>
```
```
var menu = document.getElementById('drink-menu');
menu.tagName; // 'DL'

var drinks = document.getElementsByTagName('dt');
s = '提供的饮料有:';
for (i=0; i<drinks.length; i++) {
    s = s + drinks[i].innerHTML + ',';
}
```

- `document.cookie`获得当前页面Cookie

```
document.cookie; // 'v=123; remember=true; prefer=zh'
```

> Cookie是由服务器发送的key-value标示符。因为HTTP协议是无状态的，但是服务器要区分到底是哪个用户发过来的请求，就可以用Cookie来区分。当一个用户成功登录后，服务器发送一个Cookie给浏览器，例如user=ABC123XYZ(加密的字符串)...，此后，浏览器访问该网站时，会在请求头附上这个Cookie，服务器根据Cookie即可区分出用户

Cookie的安全隐患：

- JavaScript可以读取到包含用户登陆信息的Cookie
- 设置Cookie时坚持使用`httpOnly`
- 设置了`httpOnly`的Cookie不能被JavaScript读取

**`history`对象**

`history`对象保存了浏览器的历史记录

- history.back()：后退
- history.forward()：前进

> 现代页面含有大量AJAX和交互，不应该使用`history`

## 06-02 操作DOM

DOM节点操作类型：

- 更新：更新该DOM节点内容，相当于更新该节点表示的HTML内容
- 遍历：遍历该DOM节点下的子节点
- 添加：在该DOM节点下新增一个子节点，相当于动态增加了一个HTML节点
- 删除：将该节点从HTML中删除，相当于删掉了该DOM节点以及所有子节点

**获取DOM节点方法一**：

- `document.getElementById()`：按ID获取一个DOM节点
- `document.getElementByTagName()`：按Tag名获取一组DOM节点
- `document.getElementsByClassName()`：按CSS选择器获取一组DOM节点

```
// 返回ID为'test'的节点：
var test = document.getElementById('test');

// 先定位ID为'test-table'的节点，再返回其内部所有tr节点：
var trs = document.getElementById('test-table').getElementsByTagName('tr');

// 先定位ID为'test-div'的节点，再返回其内部所有class包含red的节点：
var reds = document.getElementById('test-div').getElementsByClassName('red');

// 获取节点test下的所有直属子节点:
var cs = test.children;

// 获取节点test下第一个、最后一个子节点：
var first = test.firstElementChild;
var last = test.lastElementChild;
```
**获取节点方法二**：

- `querySelector()`
- `querySelectorAll()`

```
// 通过querySelector获取ID为q1的节点：
var q1 = document.querySelector('#q1');

// 通过querySelectorAll获取q1节点内的符合条件的所有节点：
var ps = q1.querySelectorAll('div.highlighted > p');
```
> 这里的DOM节点是指`Element`，但是DOM节点实际上是`Node`，在HTML中，`Node`包括`Element`、`Comment`、`CDATA_SECTION`等很多种，以及根节点`Document`类型，但是只用关心`Element`，也就是实际控制页面结构的`Node`，其他类型的`Node`忽略即可

**更新DOM**

修改节点文本方法一：`innerHTML`

```
// 获取<p id="p-id">...</p>
var p = document.getElementById('p-id');
// 设置文本为abc:
p.innerHTML = 'ABC'; // <p id="p-id">ABC</p>
// 设置HTML:
p.innerHTML = 'ABC <span style="color:red">RED</span> XYZ';
// <p>...</p>的内部结构已修改
```
修改节点文本方法二：`innerText`和`textContent`

```
// 获取<p id="p-id">...</p>
var p = document.getElementById('p-id');
// 设置文本:
p.innerText = '<script>alert("Hi")</script>';
// HTML被自动编码，无法设置一个<script>节点:
// <p id="p-id">&lt;script&gt;alert("Hi")&lt;/script&gt;</p>
```
> 区别在于读取属性时，`innerText`不返回隐藏元素的文本，而`textContent`返回所有文本。IE<9不支持`textContent`

修改CSS

```
// 获取<p id="p-id">...</p>
var p = document.getElementById('p-id');
// 设置CSS:
p.style.color = '#ff0000';
p.style.fontSize = '20px';
p.style.paddingTop = '2em';
```

**插入DOM**

如果DOM节点是空的：直接用`innerHTML`

如果DOM节点不是空的：用`innerHTML`会替换掉原来的所有子节点。应该用`appendChild`

```
<!-- HTML结构 -->
<p id="js">JavaScript</p>
<div id="list">
    <p id="java">Java</p>
    <p id="python">Python</p>
    <p id="scheme">Scheme</p>
</div>
```
把`<p id="js">JavaScript</p>`添加到`<div id="list">`的最后一项：

```
var
    js = document.getElementById('js'),
    list = document.getElementById('list');
list.appendChild(js);
```
先创建新节点再插入

```
var
    list = document.getElementById('list'),
    haskell = document.createElement('p');
haskell.id = 'haskell';
haskell.innerText = 'Haskell';
list.appendChild(haskell);
```
insertBefore

把子节点插入到指定的位置用`parentElement.insertBefore(newElement, referenceElement);`，子节点会插入到`referenceElement`之前。


```
<!-- HTML结构 -->
<div id="list">
    <p id="java">Java</p>
    <p id="python">Python</p>
    <p id="scheme">Scheme</p>
</div>
```

可以这么写：

```
var
    list = document.getElementById('list'),
    ref = document.getElementById('python'),
    haskell = document.createElement('p');
haskell.id = 'haskell';
haskell.innerText = 'Haskell';
list.insertBefore(haskell, ref);
```
新的HTML结构如下：

```
<!-- HTML结构 -->
<div id="list">
    <p id="java">Java</p>
    <p id="haskell">Haskell</p>
    <p id="python">Python</p>
    <p id="scheme">Scheme</p>
</div>
```
**删除DOM**

要删除一个节点，首先要获得该节点本身以及它的父节点，然后，调用父节点的`removeChild`把自己删掉：

```
// 拿到待删除节点:
var self = document.getElementById('to-be-removed');
// 拿到父节点:
var parent = self.parentElement;
// 删除:
var removed = parent.removeChild(self);
removed === self; // true
```


## 06-03 操作表单

表单输入控件：

- 文本框，`<input type="text">`，用于输入文本
- 口令框，`<input type="password">`，用于输入口令
- 单选框，`<input type="radio">`，用于选择一项
- 复选框，`<input type="checkbox">`，用于选择多项
- 下拉框，`<select>`，用于选择一项
- 隐藏文本，`<input type="hidden">`，用户不可见，但是表单提交时会发送到服务器

**获取值**

`value`属性获取`text`, `password`, `hidden`, `select`值

```
// <input type="text" id="email">
var input = document.getElementById('email');
input.value; // '用户输入的值'
```

`checked`属性获取`radio`和`checkbox`的值

```
// <label><input type="radio" name="weekday" id="monday" value="1"> Monday</label>
// <label><input type="radio" name="weekday" id="tuesday" value="2"> Tuesday</label>
var mon = document.getElementById('monday');
var tue = document.getElementById('tuesday');
mon.value; // '1'
tue.value; // '2'
mon.checked; // true或者false
tue.checked; // true或者false
```

**设置值**

`value`属性设置`text`, `password`, `hidden`, `select`值

```
// <input type="text" id="email">
var input = document.getElementById('email');
input.value = 'test@example.com'; // 文本框的内容已更新
```
`checked`属性设置`radio`和`checkbox`的值

**HTML5**

HTML5针对`<input>`标签增加了`date`, `datetime`, `datetime-local`, `color`等

```
<input type="date" value="2015-07-01">
```
```
<input type="color" value="#ff0000">
```

**提交表单**

方式一：通过`<form>`元素的`submit()`方法提交表单

```
<!-- HTML -->
<form id="test-form">
    <input type="text" name="test">
    <button type="button" onclick="doSubmitForm()">Submit</button>
</form>

<script>
function doSubmitForm() {
    var form = document.getElementById('test-form');
    // 可以在此修改form的input...
    // 提交form:
    form.submit();
}
</script>
```
> 缺点：扰乱了浏览器对`form`的正常提交。浏览器默认点击`<button type="submit">`时提交表单，或者用户在最后一个输入框按回车键

方式二：响应`<form>`本身的`onsubmit`事件

```
<!-- HTML -->
<form id="test-form" onsubmit="return checkForm()">
    <input type="text" name="test">
    <button type="submit">Submit</button>
</form>

<script>
function checkForm() {
    var form = document.getElementById('test-form');
    // 可以在此修改form的input...
    // 继续下一步:
    return true;
}
</script>
```

> `return true`来告诉浏览器继续提交，如果`return false`，浏览器将不会继续提交form

MD5提交口令

```
<!-- HTML -->
<form id="login-form" method="post" onsubmit="return checkForm()">
    <input type="text" id="username" name="username">
    <input type="password" id="password" name="password">
    <button type="submit">Submit</button>
</form>

<script>
function checkForm() {
    var pwd = document.getElementById('password');
    // 把用户输入的明文变为MD5:
    pwd.value = toMD5(pwd.value);
    // 继续下一步:
    return true;
}
</script>
```
> 潜在问题：输入口令提交时，口令框的显示会突然从几个`*`变成32个`*`（因为MD5有32个字符）

利用`<input type="hidden">`实现优化表单提交

```
<!-- HTML -->
<form id="login-form" method="post" onsubmit="return checkForm()">
    <input type="text" id="username" name="username">
    <input type="password" id="input-password">//接收用户输入，不会被提交
    <input type="hidden" id="md5-password" name="password">//获取上面的用户输入并且转化成md5后提交
    <button type="submit">Submit</button>
</form>

<script>
function checkForm() {
    var input_pwd = document.getElementById('input-password');
    var md5_pwd = document.getElementById('md5-password');
    // 把用户输入的明文变为MD5:
    md5_pwd.value = toMD5(input_pwd.value);
    // 继续下一步:
    return true;
}
</script>
```
> 没有`name`属性的`<input>`的数据不会被提交

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