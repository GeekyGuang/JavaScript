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



