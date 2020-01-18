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
```


