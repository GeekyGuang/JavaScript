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

- 函数会在执行完 return 语句之后停止并立即退出。因此，位于 return 语句之后的任何代码
都永远不会执行。return 语句也可以不带有任何返回值, 返回undefined。

- 内部环境可以通过作用域链访问所有的外部环境，但外部环境不能访问内部环境中的任何变量和函数。

- 使用 var 声明的变量会自动被添加到最接近的环境中。在函数内部，最接近的环境就是函数的局部
环境；在 with 语句中，最接近的环境是函数环境。如果初始化变量时没有使用 var 声明，该变量会自
动被添加到全局环境。

- 如果局部环境中存在着同名标识符，就不会使用位于父环境中的标识符

- object
```javascript
// 对象是引用类型(不能称作类)的实例
// 创建object实例的方法有两种

// 1 构造函数法
var person = new Object()  // 注意O要大写
person.name = "Nicholas"
person.age = 27


// 2 字面量表示法
var person = {
  name: "Nicholas",
  "age": 20,   // 属性名可以使用字符串
  5: "NewYork"  // 5会字段转换为字符串
}

// 或者
var person = {}
person.name = "Nicholas"
person.age = 27

// 访问对象属性
person.name   // 点表示法
person["name"]  // 方括号表示法，方括号内要用字符串或变量
```

- Array
```javascript
// 创建数组类型的方法有两种
// 1. 构造函数
var colors = new Array()
var colors = Array() // new可以省略
var colors = new Array(10) // 指定数组length
var colors = new Array('red', 'blue', 'green') //指定项

// 2. 字面量表示法
var colors = ['red', 'blue', 'green']

// 访问数字, 通过数字索引
colors[0] = 'yellow'

// 修改length删掉后面的项
colors.length = 2

// 在最后面插入一项
colors[colors.length] = 'pink'
colors[colors.length] = 'purple' // 可以不断忘后面加

```


  

