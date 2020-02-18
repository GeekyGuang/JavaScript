- 不加var是全局变量
```javascript
var message = "hi",   // 定义多个变量用，分隔
    found = false,
    age = 29;
```
- typeof是操作符，不是函数，可以不加括号
```javascript
var message='hello'
typeof message
typeof null
typeof NaN
typeof(null)
```
- null是空对象指针
  如果定义的变量准备在将来用于保存对象，那么最好将该变量初始化为 null 而不是其他值
```javascript
var car = null; //用于保存对象，则初始化为null
typeof car // object
```
- Boolean()函数
```javascript
var message = 'hello';
Boolean(message); // true 将message转换为boolean值输出，但不会改变message本身
```
- Number
```javascript
Number.MIN_VALUE
5e-324
Number.MAX_VALUE
1.7976931348623157e+308

var result = Number.MAX_VALUE + Number.MAX_VALUE
isFinite(result)  // 判断一个数值是否是finite
false

// isNaN()会先试图转换为数值
isNaN(NaN)
true
isNaN(10)
false
isNaN("100") // 100
false
isNaN(false) // 0
false
isNaN("hello")
true
isNaN(undefined)
true


Number()  // 将任意数据类型转换为数值
parseInt() // 将字符串转换为整数，可指定基数
parseFloat() // 将字符串转换为浮点数，不可指定基数
```


- string
```javascript
'\u03a3'
"Σ"
var cc = '\u03a3'
undefined
cc.length
1
var aa=10
aa.toString() //toString()方法转化为字符串，不可转换null和undefined

String(null) // String()函数转换为字符串
"null"
String(undefined)
"undefined"

// 要把某个值转换为字符串，可以使用加号操作符（3.5 节讨论）把它与一个字符串（ "" ）加在一起
```

- ~按位非操作的本质：操作数的负值减 1

```javascript
  var num1 = 25; // 二进制 00000000000000000000000000011001
  var num2 = ~num1; // 二进制 11111111111111111111111111100110
  alert(num2); // -26
```
- switch 语句在比较值时使用的是全等操作符，因此不会发生类型转换


  

