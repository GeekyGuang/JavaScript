0. ctrl + shift + J 打开Console
   ctrl + L         clear console
   shift + Enter    换行
   Enter            运行

1. 1995年5月，Brendan Eich 只用了10天，就设计完成了这种语言的第一版。它是一个大杂烩，语法有多个来源。

基本语法：借鉴 C 语言和 Java 语言。
数据结构：借鉴 Java 语言，包括将值分成原始值和对象两大类。
函数的用法：借鉴 Scheme 语言和 Awk 语言，将函数当作第一等公民，并引入闭包。
原型继承模型：借鉴 Self 语言（Smalltalk 的一种变种）。
正则表达式：借鉴 Perl 语言。
字符串和数组处理：借鉴 Python 语言。

2. 2009年，Node.js 项目诞生，创始人为 Ryan Dahl，它标志着 JavaScript 可以用于服务器端编程，从此网站的前端和后端可以使用同一种语言开发。并且，Node.js 可以承受很大的并发流量，使得开发某些互联网大规模的实时应用变得容易。

3. 2014年11月，由于对 Joyent 公司垄断 Node 项目、以及该项目进展缓慢的不满，一部分核心开发者离开了 Node.js，创造了 io.js 项目，这是一个更开放、更新更频繁的 Node.js 版本，很短时间内就发布到了2.0版。三个月后，Joyent 公司宣布放弃对 Node 项目的控制，将其转交给新成立的开放性质的 Node 基金会。随后，io.js 项目宣布回归 Node，两个版本将合并。

4. 变量提升，必须加分号，下面两段代码的结果是不同的
```
console.log(a)
var a = 1
// 1
```
```
console.log(a);
var a = 1;
// undifined
```

5. NaN(Not a Number)不是独立的数据类型，而是一个特殊数值，它的数据类型依然属于Number
```
typeof NaN // 'number'
```
NaN不等于任何值，包括它本身。
```
NaN === NaN // false
0 / 0 // NaN
```

6. JS区分大小写
```
number(null);  // error
Number(null);  // 0
Number(NULL);  // error
```

7. undefined
```
Number(undefined) // NaN
5 + undefined     // NaN
```

8. JavaScript 内部，所有数字都是以64位浮点数形式储存，即使整数也是如此。
```
0.3 - 0.2 
// 0.09999999999999998
```

9. Inifinity
Infinity大于一切数值（除了NaN），-Infinity小于一切数值（除了NaN）
Infinity与NaN比较，总是返回false

10. 与数值相关的全局方法
```
parseInt()    // 字符串转整数
parseFloat()  // 字符串转浮点数
isNaN()       // 判断是否是NaN，只对数字有效，若传入字符串则返回true
isNaN('hello') // true
isFinite()    // 判断是否是正常的数值
```

11. 字符串
由于 HTML 语言的属性值使用双引号，所以很多项目约定 JavaScript 语言的字符串只使用单引号
```
// 用\将字符串拆分多行
var longString = 'Long \
long \
long \
string';

longString
--> "Long long long string"
```
```
// 字符串的连接
var longString = 'Long'
+ 'long'
+ 'long'
+ 'string';

longString
--> "Longlonglongstring"
```

12. 字符串和数组的关系(仅此而已)
```
var s = 'hello';
s[0] // "h"
s[1] // "e"
s[4] // "o"

// 直接对字符串使用方括号运算符
'hello'[1] // "e"
```

13. length属性
```
var s = 'hello';
s.length // 5
```
14. JavaScript 使用 Unicode 字符集。JavaScript 引擎内部，所有字符都用 Unicode 表示。
每个字符在 JavaScript 内部都是以16位（即2个字节）的 UTF-16 格式储存。

15. Base64转码(仅适用ASCII码)
```
btoa()：任意值转为 Base64 编码
atob()：Base64 编码转为原来的值
```
16. 对象object
```
// 对象就是一组“键值对”（key-value）的集合，是一种无序的复合数据集合。
var obj = {
  foo: 'Hello',
  bar: 'world'
};

// 对象的所有键名都是字符串（ES6 又引入了 Symbol 值也可以作为键名），所以加不加引号都可以。数值会自动转换为字符串。
var obj = {
  'foo': 'Hello',
  'bar': 'World', //最后一行的逗号可以有也可以没有
};
```

17. 对象的引用
如果不同的变量名指向同一个对象，那么它们都是这个对象的引用，也就是说指向同一个内存地址。修改其中一个变量，会影响到其他所有变量。
```
var o1 = {};
var o2 = o1;

o1.a = 1;
o2.a // 1

o2.b = 2;
o1.b // 2
```

18. 
