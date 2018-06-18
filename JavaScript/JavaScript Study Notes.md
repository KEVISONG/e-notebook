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

`<input type="file">`上传文件

> 当表单包含`<input type="file">`时，表单的`enctype`必须指定为`multipart/form-data`，`method`必须指定为`post`，浏览器才能正确编码并以`multipart/form-data`格式发送表单的数据

出于安全考虑，浏览器只允许用户点击`<input type="file">`来选择本地文件，用JavaScript对`<input type="file">`的`value`赋值没有任何效果的。

当用户选择了上传某个文件后，JavaScript也无法获得该文件的真实路径

在提交表单时对文件扩展名做检查

```
var f = document.getElementById('test-file-upload');
var filename = f.value; // 'C:\fakepath\test.png'
if (!filename || !(filename.endsWith('.jpg') || filename.endsWith('.png') || filename.endsWith('.gif'))) {
    alert('Can only upload image file.');
    return false;
}
```

**File API**

HTML5新增的File API允许JavaScript读取文件内容

File API提供两个主要对象

- `File`获得文件信息
- `FileReader`读取文件

读取用户选取的图片文件，并在一个`<div>`中预览图像：

```
var
    fileInput = document.getElementById('test-image-file'),
    info = document.getElementById('test-file-info'),
    preview = document.getElementById('test-image-preview');
// 监听change事件:
fileInput.addEventListener('change', function () {
    // 清除背景图片:
    preview.style.backgroundImage = '';
    // 检查文件是否选择:
    if (!fileInput.value) {
        info.innerHTML = '没有选择文件';
        return;
    }
    // 获取File引用:
    var file = fileInput.files[0];
    // 获取File信息:
    info.innerHTML = '文件: ' + file.name + '<br>' +
                     '大小: ' + file.size + '<br>' +
                     '修改: ' + file.lastModifiedDate;
    if (file.type !== 'image/jpeg' && file.type !== 'image/png' && file.type !== 'image/gif') {
        alert('不是有效的图片文件!');
        return;
    }
    // 读取文件:
    var reader = new FileReader();
    reader.onload = function(e) {
        var
            data = e.target.result; // 'data:image/jpeg;base64,/9j/4AAQSk...(base64编码)...'            
        preview.style.backgroundImage = 'url(' + data + ')';
    };
    // 以DataURL的形式读取文件:
    reader.readAsDataURL(file);
});
```

## 06-05 AJAX

Asynchronous JavaScript and XML

**传统Web原理**：一次HTTP请求对应一个页面

**AJAX作用原理**：

- 用户停留在页面中
- JavaScript发送新请求并且接受服务端数据
- JavaScript动态更新页面内容
- 用户不用刷新页面就可以更新页面

```
function success(text) {
    var textarea = document.getElementById('test-response-text');
    textarea.value = text;
}

function fail(code) {
    var textarea = document.getElementById('test-response-text');
    textarea.value = 'Error code: ' + code;
}

var request = new XMLHttpRequest(); // 新建XMLHttpRequest对象

request.onreadystatechange = function () { // 状态发生变化时，函数被回调
    if (request.readyState === 4) { // 成功完成
        // 判断响应结果:
        if (request.status === 200) {
            // 成功，通过responseText拿到响应的文本:
            return success(request.responseText);
        } else {
            // 失败，根据响应码判断失败原因:
            return fail(request.status);
        }
    } else {
        // HTTP请求还在继续...
    }
}

// 发送请求:
request.open('GET', '/api/categories');//open()方法有3个参数，第一个参数指定是GET还是POST，第二个参数指定URL地址，第三个参数指定是否使用异步，默认是true
request.send();

alert('请求已发送，请等待响应...');
```

第一步：创建`XMLHttpRequest`对象后先设置`onreadystatechange`的回调函数

- 在回调函数中通过`readyState === 4`判断请求是否完成
    - 如果完成，根据`status === 200`判断是否是一个成功的响应

第二步：`XMLHttpRequest`对象的`open()`方法有3个参数

 - 第一个参数指定是`GET`还是`POST`
 - 第二个参数指定URL地址
 - 第三个参数指定是否使用异步，默认是true

> 千万不要把第三个参数指定为`false`，否则浏览器将停止响应，直到AJAX请求完成

第三步：`send()`方法才真正发送请求。`GET`请求不需要参数，`POST`请求需要把body部分以字符串或者`FormData`对象传进去

**安全限制**

`open()`的URL使用的是**相对路径**：默认情况下，JavaScript在发送AJAX请求时，URL的域名必须和当前页面完全一致

完全一致：

- 域名要相同（`www.example.com`和`example.com`不同）
- 协议要相同（`http`和`https`不同）
- 端口号要相同

**用JavaSCript请求其他网站的URL**

方法一：通过Flash插件发送HTTP请求，这种方式可以绕过浏览器的安全限制，但必须安装Flash，并且跟Flash交互。不过Flash用起来麻烦

方法二：通过在同源域名下架设一个代理服务器来转发，JavaScript负责把请求发送到代理服务器：
```
'/proxy?url=http://www.sina.com.cn'
```
方法三：JSONP，有个限制，只能用GET请求，并且要求返回JavaScript。这种方式跨域实际上是利用了浏览器允许跨域引用JavaScript资源：

```
<html>
<head>
    <script src="http://example.com/abc.js"></script>
    ...
</head>
<body>
...
</body>
</html>
```

JSONP通常以函数调用的形式返回，例如，返回JavaScript内容如下：

```
foo('data');
```
这样一来，我们如果在页面中先准备好`foo()`然后给页面动态加一个`<script>`节点，相当于动态读取外域的JavaScript资源，最后就等着接收回调了

**CORS（Cross-Origin Resource Sharing）**

- Origin：本域向外域发起请求
- 外域检查`Access-Control-Allow-Origin`是否包含本域
    - 包含：跨域请求成功
    - 不包含：跨域请求失败，无法获取响应数据

![image](https://cdn.liaoxuefeng.com/cdn/files/attachments/00143640805071744d58164a40e42ef92b9973824451595000/l)

PUT、DELETE以及其他类型如`application/json`的POST请求，在发送AJAX请求之前，浏览器会先发送一个OPTIONS请求（称为preflighted请求）到这个URL上，询问目标服务器是否接受：

```
OPTIONS /path/to/resource HTTP/1.1
Host: bar.com
Origin: http://my.com
Access-Control-Request-Method: POST
```

服务器必须响应并明确指出允许的Method：

```
HTTP/1.1 200 OK
Access-Control-Allow-Origin: http://my.com
Access-Control-Allow-Methods: POST, GET, PUT, OPTIONS
Access-Control-Max-Age: 86400
```

[W3C文档](https://www.w3.org/TR/cors/)

## 06-06 Promise

JavaScript不支持多线程，只能通过回调函数实现异步

```
function callback() {
    console.log('Done');
}
console.log('before setTimeout()');
setTimeout(callback, 1000); // 1秒钟后调用callback函数
console.log('after setTimeout()');
```
输出：
```
before setTimeout()
after setTimeout()
(等待1秒后)
Done
```
**Promise对象**：承诺将来会执行的对象

```
function test(resolve, reject) {
    var timeOut = Math.random() * 2;
    log('set timeout to: ' + timeOut + ' seconds.');
    setTimeout(function () {
        if (timeOut < 1) {
            log('call resolve()...');
            resolve('200 OK');
        }
        else {
            log('call reject()...');
            reject('timeout in ' + timeOut + ' seconds.');
        }
    }, timeOut * 1000);
}
```
`test()`函数有两个参数，这两个参数都是函数，如果执行成功将调用`resolve('200 OK')`，如果执行失败将调用`reject('timeout in ' + timeOut + ' seconds.')`

`test()`函数只关心自身的逻辑，并不关心具体的`resolve`和`reject`将如何处理结果

```
var p1 = new Promise(test);
// 如果成功，执行这个函数：
var p2 = p1.then(function (result) {
    console.log('成功：' + result);
});
// 如果失败，执行这个函数：
var p3 = p2.catch(function (reason) {
    console.log('失败：' + reason);
});
```
代码可以简化为：

```
new Promise(test).then(function (result) {
    console.log('成功：' + result);
}).catch(function (reason) {
    console.log('失败：' + reason);
});
```
Promise异步执行
```
new Promise(function (resolve, reject) {
    log('start new Promise...');
    var timeOut = Math.random() * 2;
    log('set timeout to: ' + timeOut + ' seconds.');
    setTimeout(function () {
        if (timeOut < 1) {
            log('call resolve()...');
            resolve('200 OK');
        }
        else {
            log('call reject()...');
            reject('timeout in ' + timeOut + ' seconds.');
        }
    }, timeOut * 1000);
}).then(function (r) {
    log('Done: ' + r);
}).catch(function (reason) {
    log('Failed: ' + reason);
});
```
![image](https://cdn.liaoxuefeng.com/cdn/files/attachments/001436512391628944d5da9a5654a35b0ace38246f30b9c000/l)

Promise简化异步处理

```
// ajax函数将返回Promise对象:
function ajax(method, url, data) {
    var request = new XMLHttpRequest();
    return new Promise(function (resolve, reject) {
        request.onreadystatechange = function () {
            if (request.readyState === 4) {
                if (request.status === 200) {
                    resolve(request.responseText);
                } else {
                    reject(request.status);
                }
            }
        };
        request.open(method, url);
        request.send(data);
    });
}
var log = document.getElementById('test-promise-ajax-result');
var p = ajax('GET', '/api/categories');
p.then(function (text) { // 如果AJAX成功，获得响应内容
    log.innerText = text;
}).catch(function (status) { // 如果AJAX失败，获得响应代码
    log.innerText = 'ERROR: ' + status;
});
```

## 06-07 Canvas

HTML5新增组件，JS无需与Flash交互就可以进行绘制


```
<canvas id="test-canvas" width="300" height="200"></canvas>
```
`getContext('2d')`方法获取一个`CanvasRenderingContext2D`对象，所有的绘图操作都需要通过这个对象完成

```
var ctx = canvas.getContext('2d');
```
> 绘制3D图形：`gl = canvas.getContext("webgl");`


```
ctx.clearRect(0, 0, 200, 200); // 擦除(0,0)位置大小为200x200的矩形，擦除的意思是把该区域变为透明
ctx.fillStyle = '#dddddd'; // 设置颜色
ctx.fillRect(10, 10, 130, 130); // 把(10,10)位置大小为130x130的矩形涂色
// 利用Path绘制复杂路径:
var path=new Path2D();
path.arc(75, 75, 50, 0, Math.PI*2, true);
path.moveTo(110,75);
path.arc(75, 75, 35, 0, Math.PI, false);
path.moveTo(65, 65);
path.arc(60, 65, 5, 0, Math.PI*2, true);
path.moveTo(95, 65);
path.arc(90, 65, 5, 0, Math.PI*2, true);
ctx.strokeStyle = '#0000ff';
ctx.stroke(path);
```

**绘制文本**

```
ctx.clearRect(0, 0, canvas.width, canvas.height);
ctx.shadowOffsetX = 2;
ctx.shadowOffsetY = 2;
ctx.shadowBlur = 2;
ctx.shadowColor = '#666666';
ctx.font = '24px Arial';
ctx.fillStyle = '#333333';
ctx.fillText('带阴影的文字', 20, 40);
```

# 07 JavaScript jQuery

使用jQuery：在`<head>`引入jQuery文件

```
<html>
<head>
    <script src="//code.jquery.com/jquery-1.11.3.min.js"></script>
    ...
</head>
<body>
    ...
</body>
</html>
```

jQuery符号$：jQuery把所有功能全部封装在一个全局变量`jQuery`中，而$也是一个合法的变量名，是变量jQuery的别名

$本质上就是一个函数

## 07-01 选择器

### 基本选择器
JavaScript选择节点：**返回DOM对象**
```
// 按ID查找：
var a = document.getElementById('dom-id');

// 按tag查找：
var divs = document.getElementsByTagName('div');

// 查找<p class="red">：
var ps = document.getElementsByTagName('p');
// 过滤出class="red":
// TODO:

// 查找<table class="green">里面的所有<tr>：
var table = ...
for (var i=0; i<table.children; i++) {
    // TODO: 过滤出<tr>
}
```
jQuery选择节点：**返回jQuery对象**（一个数组）

**按ID查找`$('#ID')`**

```
// 查找<div id="abc">:
var div = $('#abc');
```
如果`id`为`abc`的`<div>`存在，返回jQuery对象

```
[<div id="abc">...</div>]
```

如果`id`为`abc`的`<div>`不存在

```
[]
```

jQuery对象和DOM对象转换

```
var div = $('#abc'); // jQuery对象
var divDom = div.get(0); // 假设存在div，获取第1个DOM元素
var another = $(divDom); // 重新把DOM包装为jQuery对象
```

**按tag查找`$('TAGNAME')`**

```
var ps = $('p'); // 返回所有<p>节点
ps.length; // 数一数页面有多少个<p>节点
```
**按class查找`$('.CLASS')`**

```
var a = $('.red'); // 所有节点包含`class="red"`都将返回
// 例如:
// <div class="red">...</div>
// <p class="green red">...</p>
```

有的节点有多个class，查找同时包含`red`和`green`的节点：

```
var a = $('.red.green'); // 注意没有空格！
// 符合条件的节点：
// <div class="red green">...</div>
// <div class="blue green red">...</div>
```

**按属性查找`$('属性名=属性值')`**

```
var email = $('[name=email]'); // 找出<xxx name="email">
var passwordInput = $('[type=password]'); // 找出<xxx type="password">
var a = $('[items="A B"]'); // 找出<xxx items="A B">
```
前缀查找
```
var icons = $('[name^=icon]'); // 找出所有name属性值以icon开头的DOM
// 例如: name="icon-1", name="icon-2"
```
后缀查找
```
var names = $('[name$=with]'); // 找出所有name属性值以with结尾的DOM
// 例如: name="startswith", name="endswith"
```
class也是一种属性，可以class属性查找
```
var icons = $('[class^="icon-"]'); // 找出所有class包含至少一个以`icon-`开头的DOM
// 例如: class="icon-clock", class="abc icon-home"
```
**标签和属性组合查找`$('标签名[属性名=属性值]')`**

```
var emailInput = $('input[name=email]'); // 不会找出<div name="email">
```

**标签和类组合查找`$('标签名.CLASS]')`**

```
var tr = $('tr.red'); // 找出<tr class="red ...">...</tr>
```

**多项选择器：`,`隔开**

```
$('p,div'); // 把<p>和<div>都选出来
$('p.red,p.green'); // 把<p class="red">和<p class="green">都选出来
```

### 层级选择器（Descendant Selector）

**层级选择器`$('ancestor descendant')`**

```
<!-- HTML结构 -->
<div class="testing">
    <ul class="lang">
        <li class="lang-javascript">JavaScript</li>
        <li class="lang-python">Python</li>
        <li class="lang-lua">Lua</li>
    </ul>
</div>
```

```
$('ul.lang li.lang-javascript'); // [<li class="lang-javascript">JavaScript</li>]
$('div.testing li.lang-javascript'); // [<li class="lang-javascript">JavaScript</li>]
```
> 优点：缩小了选择范围，首先要定位父节点，再选择相应的子节点，避免了页面其他不相关的元素

**子选择器`$('parent>child')`**

限定了层级关系必须是父子关系，`<child>`节点必须是`<parent>`节点的直属子节点

```
$('ul.lang>li.lang-javascript'); // 可以选出[<li class="lang-javascript">JavaScript</li>]
$('div.testing>li.lang-javascript'); // [], 无法选出，因为<div>和<li>不构成父子关系
```

**过滤器`：`**

附加在选择器上使用
```
$('ul.lang li'); // 选出JavaScript、Python和Lua 3个节点

$('ul.lang li:first-child'); // 仅选出JavaScript
$('ul.lang li:last-child'); // 仅选出Lua
$('ul.lang li:nth-child(2)'); // 选出第N个元素，N从1开始
$('ul.lang li:nth-child(even)'); // 选出序号为偶数的元素
$('ul.lang li:nth-child(odd)'); // 选出序号为奇数的元素
```

表单相关特殊的选择器：

- `:input`：可以选择`<input>`，`<textarea>`，`<select>`和`<button>`；
- `:file`：可以选择`<input type="file">`，和`input[type=file]`一样；
- `:checkbox`：可以选择复选框，和`input[type=checkbox]`一样；
- `:radio`：可以选择单选框，和`input[type=radio]`一样；
- `:focus`：可以选择当前输入焦点的元素，例如把光标放到一个`<input>`上，用`$('input:focus')`就可以选出；
- `:checked`：选择当前勾上的单选框和复选框，用这个选择器可以立刻获得用户选择的项目，如`$('input[type=radio]:checked')`；
- `:enabled`：可以选择可以正常输入的`<input>`、`<select>`等，也就是没有灰掉的输入；
- `:disabled`：和`:enabled`正好相反，选择那些不能输入的。


选出可见的或隐藏的元素：

```
$('div:visible'); // 所有可见的div
$('div:hidden'); // 所有隐藏的div
```
### 查找和过滤

**`find()`查找**

```
<!-- HTML结构 -->
<ul class="lang">
    <li class="js dy">JavaScript</li>
    <li class="dy">Python</li>
    <li id="swift">Swift</li>
    <li class="dy">Scheme</li>
    <li name="haskell">Haskell</li>
</ul>
```

`find()`查找：

```
var ul = $('ul.lang'); // 获得<ul>
var dy = ul.find('.dy'); // 获得JavaScript, Python, Scheme
var swf = ul.find('#swift'); // 获得Swift
var hsk = ul.find('[name=haskell]'); // 获得Haskell
```

`parent()`从当前节点开始向上查找

```
var swf = $('#swift'); // 获得Swift
var parent = swf.parent(); // 获得Swift的上层节点<ul>
var a = swf.parent('.red'); // 获得Swift的上层节点<ul>，同时传入过滤条件。如果ul不符合条件，返回空jQuery对象
```

`next()`和`prev()`方法获取同一层级的节点

```
var swift = $('#swift');

swift.next(); // Scheme
swift.next('[name=haskell]'); // 空的jQuery对象，因为Swift的下一个元素Scheme不符合条件[name=haskell]

swift.prev(); // Python
swift.prev('.dy'); // Python，因为Python同时符合过滤器条件.dy
```

**filter()过滤**

```
var langs = $('ul.lang li'); // 拿到JavaScript, Python, Swift, Scheme和Haskell
var a = langs.filter('.dy'); // 拿到JavaScript, Python, Scheme
```
传入一个函数

```
var langs = $('ul.lang li'); // 拿到JavaScript, Python, Swift, Scheme和Haskell
langs.filter(function () {
    return this.innerHTML.indexOf('S') === 0; // 返回S开头的节点
}); // 拿到Swift, Scheme
```

**`map()`方法** 把一个jQuery对象包含的若干DOM节点转化为其他对象：

```
var langs = $('ul.lang li'); // 拿到JavaScript, Python, Swift, Scheme和Haskell
var arr = langs.map(function () {
    return this.innerHTML;
}).get(); // 用get()拿到包含string的Array：['JavaScript', 'Python', 'Swift', 'Scheme', 'Haskell']
```

## 07-02 操作DOM

**修改Text和HTML**

`text()`无参获取节点文本  
`html()`无参获取原始HTML文本

```
<!-- HTML结构 -->
<ul id="test-ul">
    <li class="js">JavaScript</li>
    <li name="book">Java &amp; JavaScript</li>
</ul>
```
分别获取文本和HTML：
```
$('#test-ul li[name=book]').text(); // 'Java & JavaScript'
$('#test-ul li[name=book]').html(); // 'Java &amp; JavaScript'
```

`text()`无参获取节点文本  
`html()`无参获取原始HTML文本

```
var j1 = $('#test-ul li.js');
var j2 = $('#test-ul li[name=book]');
j1.html('<span style="color: red">JavaScript</span>');
j2.text('JavaScript & ECMAScript');
```

**`css('name', 'value')`修改CSS**

```
<!-- HTML结构 -->
<ul id="test-css">
    <li class="lang dy"><span>JavaScript</span></li>
    <li class="lang"><span>Java</span></li>
    <li class="lang dy"><span>Python</span></li>
    <li class="lang"><span>Swift</span></li>
    <li class="lang dy"><span>Scheme</span></li>
</ul>
```
链式调用
```
$('#test-css li.dy>span').css('background-color', '#ffd351').css('color', 'red');
```
`css()`用法：

```
var div = $('#test-div');
div.css('color'); // '#000033', 获取CSS属性
div.css('color', '#336699'); // 设置CSS属性
div.css('color', ''); // 清除CSS属性
```
修改`class`属性

```
var div = $('#test-div');
div.hasClass('highlight'); // false， class是否包含highlight
div.addClass('highlight'); // 添加highlight这个class
div.removeClass('highlight'); // 删除highlight这个class
```
**`show()`显示和`hide()`隐藏DOM**

```
var a = $('a[target=_blank]');
a.hide(); // 隐藏
a.show(); // 显示
```
> 隐藏DOM节点并未改变DOM树的结构，它只影响DOM节点的显示。和删除DOM节点不同

**`width()`和`height()`获取设置宽高**

```
// 浏览器可视窗口大小:
$(window).width(); // 800
$(window).height(); // 600

// HTML文档大小:
$(document).width(); // 800
$(document).height(); // 3500

// 某个div的大小:
var div = $('#test-div');
div.width(); // 600
div.height(); // 300
div.width(400); // 设置CSS属性 width: 400px，是否生效要看CSS是否有效
div.height('200px'); // 设置CSS属性 height: 200px，是否生效要看CSS是否有效
```
**`attr()`和`removeAttr()`操作DOM节点的属性**

```
// <div id="test-div" name="Test" start="1">...</div>
var div = $('#test-div');
div.attr('data'); // undefined, 属性不存在
div.attr('name'); // 'Test'
div.attr('name', 'Hello'); // div的name属性变为'Hello'
div.removeAttr('name'); // 删除name属性
div.attr('name'); // undefined
```
`val()`方法获取和设置表单中对应的value属性

```
/*
    <input id="test-input" name="email" value="">
    <select id="test-select" name="city">
        <option value="BJ" selected>Beijing</option>
        <option value="SH">Shanghai</option>
        <option value="SZ">Shenzhen</option>
    </select>
    <textarea id="test-textarea">Hello</textarea>
*/
var
    input = $('#test-input'),
    select = $('#test-select'),
    textarea = $('#test-textarea');

input.val(); // 'test'
input.val('abc@example.com'); // 文本框的内容已变为abc@example.com

select.val(); // 'BJ'
select.val('SH'); // 选择框已变为Shanghai

textarea.val(); // 'Hello'
textarea.val('Hi'); // 文本区域已更新为'Hi'
```
**`append()`添加DOM到最后**

```
<div id="test-div">
    <ul>
        <li><span>JavaScript</span></li>
        <li><span>Python</span></li>
        <li><span>Swift</span></li>
    </ul>
</div>
```

```
var ul = $('#test-div>ul');
ul.append('<li><span>Haskell</span></li>');
```
**`prepend()`添加到DOM开头**

**`remove()`移除DOM节点**

```
var li = $('#test-div>ul>li');
li.remove(); // 所有<li>全被删除
```

## 07-03 事件

因为JavaScript在浏览器中以单线程运行，所以页面加载完所有的JavaScript代码并且执行后，只能依赖**触发事件**来执行JavaScript代码

> jQuery屏蔽了不同浏览器的差异，写一种代码，所有浏览器都能支持

**触发事件方法一：`on(事件名, 处理函数)`方法绑定事件**

```
/* HTML:
 *
 * <a id="test-link" href="#0">点我试试</a>
 *
 */

// 获取超链接的jQuery对象:
var a = $('#test-link');
a.on('click', function () {
    alert('Hello!');
});
```
**触发事件方法二：直接调用`click()`方法**

```
a.click(function () {
    alert('Hello!');
});
```
> 两者完全等价，第二种常用

**事件大全：**

- 鼠标事件
    - `click`：鼠标单击触发
    - `dblclick`：鼠标双击触发
    - `mouseenter`：鼠标进入时触发
    - `mouseleave`：鼠标移出时触发
    - `mousemove`：鼠标在DOM内部移动时触发
    - `hover`：鼠标进入和退出时触发两个函数，相当于`mouseenter`加上`mouseleave`
- 键盘事件
    - `keydown`：键盘按下时触发
    - `keyup`：键盘松开时触发
    - `keypress`：按一次键后触发
- 其他事件
    - `focus`：当DOM获得焦点时触发
    - `blur`：当DOM失去焦点时触发
    - `change`：当`<input>`、`<select>`或`<textarea>`的内容改变时触发
    - `submit`：当`<form>`提交时触发
    - `ready`：当页面被载入并且DOM树完成初始化后触发

> `ready`仅作用于`document`对象

> `ready`事件在DOM完成初始化后触发，且只触发一次，非常适合用来写其他的初始化代码

给`<form>`表单绑定`submit`事件：错误演示

```
<html>
<head>
    <script>
        // 代码有误:
        $('#testForm).on('submit', function () {
            alert('submit!');
        });
    </script>
</head>
<body>
    <form id="testForm">
        ...
    </form>
</body>
```
> JavaScript在此执行的时候，`<form>`尚未载入浏览器，所以`$('#testForm)`返回`[]`，并没有绑定事件到任何DOM上

给`<form>`表单绑定`submit`事件：正确方法，加载完再绑定方法

```
<html>
<head>
    <script>
        $(document).on('ready', function () {
            $('#testForm).on('submit', function () {
                alert('submit!');
            });
        });
    </script>
</head>
<body>
    <form id="testForm">
        ...
    </form>
</body>
```
可以这样简化：
```
$(document).ready(function () {
    // on('submit', function)也可以简化:
    $('#testForm).submit(function () {
        alert('submit!');
    });
});
```
再简化：
```
$(function () {
    // init...
});
```
> 最为常见的形式：`$(function () {...})`，牢记这是`document`对象的`ready`事件处理函数

可以反复绑定事件处理函数，它们会依次执行：
```
$(function () {
    console.log('init A...');
});
$(function () {
    console.log('init B...');
});
$(function () {
    console.log('init C...');
});
```
**事件参数**

事件如`mousemove`和`keypress`，需要获取鼠标位置和按键的值，所有事件都会传入`Event`对象作为参数，可以从`Event`对象上获取到更多的信息：

```
$(function () {
    $('#testMouseMoveDiv').mousemove(function (e) {
        $('#testMouseMoveSpan').text('pageX = ' + e.pageX + ', pageY = ' + e.pageY);
    });
});
```
**`off(事件名, 处理函数)`方法取消绑定事件**

```
function hello() {
    alert('hello!');
}

a.click(hello); // 绑定事件

// 10秒钟后解除绑定:
setTimeout(function () {
    a.off('click', hello);
}, 10000);
```
**事件触发条件**

一个需要注意的问题是，事件的触发总是由用户操作引发的。例如，我们监控文本框的内容改动：

```
var input = $('#test-input');
input.change(function () {
    console.log('changed...');
});
```

当用户在文本框中输入时，就会触发`change`事件。但是，如果用JavaScript代码去改动文本框的值，将不会触发`change`事件：

```
var input = $('#test-input');
input.val('change it!'); // 无法触发change事件
```

有些时候，我们希望用代码触发change事件，可以直接调用无参数的`change()`方法来触发该事件：

```
var input = $('#test-input');
input.val('change it!');
input.change(); // 触发change事件
```


`input.change()`相当于`input.trigger('change')`，是`trigger()`方法的简写。

**浏览器安全限制**

在浏览器中，有些JavaScript代码只有在用户触发下才能执行，例如，`window.open()`函数：

```
// 无法弹出新窗口，将被浏览器屏蔽:
$(function () {
    window.open('/');
});
```


## 07-04 动画

JavaScript实现动画原理：以固定的时间间隔（例如，0.1秒），每次把DOM元素的CSS样式修改一点（例如，高宽各增加10%）

jQuery内置动画样式

- `show()`/`hide()`
- `slideUp()`/`slideDown()`
- `fadeIn()`/`fadeOut()`
- `animate()`

**`show()`/`hide()`**

无参调用：显示和隐藏DOM元素

有参调用：动态显示和隐藏DOM元素

```
var div = $('#test-show-hide');
div.hide(3000); // 在3秒钟内逐渐消失
```

> `toggle()`方法则根据当前状态决定是`show()`还是`hide()`

**`slideUp()`/`slideDown()`**

`slideUp()`和`slideDown()`则是在垂直方向逐渐展开或收缩

```
var div = $('#test-slide');
div.slideUp(3000); // 在3秒钟内逐渐向上消失
```

> `slideToggle()`则根据元素是否可见来决定下一步动作

**`fadeIn()`/`fadeOut()` 淡入淡出**

> 设置DOM元素的opacity属性来实现

```
var div = $('#test-fade');
div.fadeOut('slow'); // 在0.6秒内淡出
```
> `fadeToggle()`则根据元素是否可见来决定下一步动作

**`animate()`自定义动画**

参数就是DOM元素最终的CSS状态和时间，jQuery在时间段内不断调整CSS直到达到我们设定的值
```
var div = $('#test-animate');
div.animate({
    opacity: 0.25,
    width: '256px',
    height: '256px'
}, 3000); // 在3秒钟内CSS过渡到设定值
```
`animate()`还可以再传入一个函数，当动画结束时，该函数将被调用：

```
var div = $('#test-animate');
div.animate({
    opacity: 0.25,
    width: '256px',
    height: '256px'
}, 3000, function () {
    console.log('动画已结束');
    // 恢复至初始状态:
    $(this).css('opacity', '1.0').css('width', '128px').css('height', '128px');
});
```
**`delay()`串行动画**


```
var div = $('#test-animates');
// 动画效果：slideDown - 暂停 - 放大 - 暂停 - 缩小
div.slideDown(2000)
   .delay(1000)
   .animate({
       width: '256px',
       height: '256px'
   }, 2000)
   .delay(1000)
   .animate({
       width: '128px',
       height: '128px'
   }, 2000);
}
```
## 07-05 AJAX

jQuery的全局对象`jQuery`绑定了`ajax()`函数，用来处理AJAX请求

`ajax(url, settings)`函数接受一个URL和一个可选的`settings`对象



- async：是否异步执行AJAX请求，默认为`true`，千万不要指定为`false`
- method：发送的Method，缺省为`'GET'`，可指定为`'POST'`、`'PUT'`等；
- contentType：发送POST请求的格式，默认值为`'application/x-www-form-urlencoded; charset=UTF-8'`，也可以指定为`text/plain`、`application/json`；
- data：发送的数据，可以是字符串、数组或object。如果是GET请求，data将被转换成query附加到URL上，如果是POST请求，根据contentType把data序列化成合适的格式；
- headers：发送的额外的HTTP头，必须是一个object；
- dataType：接收的数据格式，可以指定为`'html'`、`'xml'`、`'json'`、`'text'`等，缺省情况下根据响应的`Content-Type`猜测。

发送一个GET请求，并返回一个JSON格式的数据：

```
var jqxhr = $.ajax('/api/categories', {
    dataType: 'json'
});
```
jQuery的jqXHR对象类似一个Promise对象，我们可以用链式写法来处理各种回调：


```
'use strict';

function ajaxLog(s) {
    var txt = $('#test-response-text');
    txt.val(txt.val() + '\n' + s);
}

$('#test-response-text').val('');

var jqxhr = $.ajax('/api/categories', {
    dataType: 'json'
}).done(function (data) {
    ajaxLog('成功, 收到的数据: ' + JSON.stringify(data));
}).fail(function (xhr, status) {
    ajaxLog('失败: ' + xhr.status + ', 原因: ' + status);
}).always(function () {
    ajaxLog('请求完成: 无论成功或失败都会调用');
});
```

AJAX常用操作已经封装好，直接使用

**`get()`**

```
var jqxhr = $.get('/path/to/resource', {
    name: 'Bob Lee',
    check: 1
});
```

第二个参数如果是object，jQuery自动把它变成query string然后加到URL后面，实际的URL是：

```
/path/to/resource?name=Bob%20Lee&check=1
```

**`post()`**

`post()`和`get()`类似，但是传入的第二个参数默认被序列化为`application/x-www-form-urlencoded：`


```
var jqxhr = $.post('/path/to/resource', {
    name: 'Bob Lee',
    check: 1
});
```


实际构造的数据`name=Bob%20Lee&check=1作为POST的body`被发送。

**`getJSON()`**

`getJSON()`方法来快速通过GET获取一个JSON对象：


```
var jqxhr = $.getJSON('/path/to/resource', {
    name: 'Bob Lee',
    check: 1
}).done(function (data) {
    // data已经被解析为JSON对象了
});
```



## 07-06 扩展


```
$('span.hl').css('backgroundColor', '#fffceb').css('color', '#d85030');
$('p a.hl').css('backgroundColor', '#fffceb').css('color', '#d85030');
```

字定义highlight()方法

```
$.fn.highlight1 = function () {
    // this已绑定为当前jQuery对象:
    this.css('backgroundColor', '#fffceb').css('color', '#d85030');
    return this;
}
```
```
$('span.hl').highlight();
$('p a.hl').highlight();
```

带参数的`highlight2()：`

```
$.fn.highlight2 = function (options) {
    // 要考虑到各种情况:
    // options为undefined
    // options只有部分key
    var bgcolor = options && options.backgroundColor || '#fffceb';
    var color = options && options.color || '#d85030';
    this.css('backgroundColor', bgcolor).css('color', color);
    return this;
}
```


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