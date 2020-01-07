# 入门篇

## 导论

ctrl + shift + J 或 F12 或 右键'检查' ctrl + shift + I 打开Console三种方式
ctrl + L         clear console
shift + Enter    换行
Enter            运行
F5               重启console

## 基本语法

如果只是声明变量而没有赋值，则该变量的值是`undefined`。

JavaScript 是一种动态类型语言，也就是说，变量的类型没有限制，变量可以随时更改类型。

变量提升hoisting
```javascript
console.log(a);
var a = 1; 

// 等价于
var a;
console.log(a); // undefined
a = 1; 
```

`switch`语句后面的表达式，与`case`语句后面的表示式比较运行结果时，采用的是严格相等运算符（`===`），而不是相等运算符（`==`），这意味着比较时不会发生类型转换。

`for`语句的三个部分（initialize、test、increment），可以省略任何一个，也可以全部省略(死循环)。

标签

```javascript
top: // 给循环加top标签
  for (var i = 0; i < 3; i++){
    for (var j = 0; j < 3; j++){
      if (i === 1 && j === 1) break top; // 跳出top循环
      console.log('i=' + i + ', j=' + j);
    }
  }

// 给代码块加标签
foo: {
  console.log(1);
  break foo;
  console.log('本行不会输出');
}
console.log(2);
```

## 数据类型

`typeof`运算符可以返回一个值的数据类型

```javascript
typeof 123 // "number"
typeof '123' // "string"
typeof false // "boolean"
typeof null // "object" 历史原因造成的 
typeof undefined // "undefined"
```

`null`是一个表示“空”的对象，转为数值时为`0`；`undefined`是一个表示"此处无定义"的原始值，转为数值时为`NaN`。

#### 布尔值

```javascript
if ('') {
  console.log('true');
}
// 没有任何输出

// 空数组（[]）和空对象（{}）对应的布尔值，都是true
if ([]) {
  console.log('true');
}
// true

if ({}) {
  console.log('true');
}
// true
```

JavaScript 内部，所有数字都是以64位浮点数形式储存，即使整数也是如此。

#### NaN

`NaN`不是独立的数据类型，而是一个特殊数值，它的数据类型依然属于`Number`.

NaN是用来表示不是数值的数值

```javascript
0 / 0 // NaN
Boolean(NaN) // false
```

#### Infinity

```javascript
0 * Infinity // NaN
0 / Infinity // 0
Infinity / 0 // Infinity
```

#### 数值方法

```javascript
parseInt() //字符串转换为整数
parseInt('1000') // 1000
// 等同于
parseInt('1000', 10) // 1000 


//字符串转换为浮点数
parseFloat('3.14') // 3.14 

isNaN(NaN) // true
isNaN(123) // false

NaN !== NaN

isFinite(Infinity) // false
isFinite(-Infinity) // false
isFinite(NaN) // false
isFinite(undefined) // false
isFinite(null) // true
isFinite(-1) // true
```








