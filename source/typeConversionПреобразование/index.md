---
title: Type Conversion Преобразование
date: 2020-04-29 08:34:16
---

---
Number () конвертирует в Number, String () конвертирует в String, Boolean () конвертирует в Boolean.

---

# 
Типы данных JavaScript
---

**В JavaScript есть 5 различных типов данных, которые могут содержать значения:**
`string`
 `number`
 `boolean`
 `object`
 `function`
 # 
**Есть 6 типов объектов:**
 `Object`
 `Date`
`Array`
 `String`
 `Number`
 `Boolean`

**И 2 типа данных, которые не могут содержать значения:**
 `null`
 `undefined`

Тип оператора
---
использовать  `typeof `оператор, чтобы найти тип данных переменной JavaScript.
```
<script>
document.getElementById("demo").innerHTML =       
  typeof "john" + "<br>" +
  typeof 3.14 + "<br>" +
  typeof NaN + "<br>" +
  typeof false + "<br>" +
  typeof [1,2,3,4] + "<br>" +
  typeof {name:'john', age:34} + "<br>" +
  typeof new Date() + "<br>" +
  typeof function () {} + "<br>" +
  typeof myCar + "<br>" +
  typeof null;
</script>
```
# 
```
The JavaScript typeof Operator
The typeof operator returns the type of a variable, object, function or expression.

string
number
number
boolean
object
object
object
function
undefined
object
```
---

Пожалуйста, обратите внимание:
---

Тип данных NaN это число
Тип данных массива - объект
Тип данных даты - объект
Тип данных null является объектом
Тип данных неопределенной переменной не **определен**
Тип данных переменной, которой не присвоено значение, также не **определен**
```
Вы не можете использовать, typeofчтобы определить, является ли объект JavaScript массивом (или датой).
```
---
Тип данных typeof
---
` typeof` Оператор не является переменной. Это оператор. Операторы (+ - * /) не имеют данных любого типа.

Но ` typeof` оператор всегда возвращает строку (содержащую тип операнда).

---

Свойство конструктора
---
`constructor` Свойство возвращает функцию конструктора для всех переменных JavaScript.

```
<script>
document.getElementById("demo").innerHTML = 
  "john".constructor + "<br>" +
  (3.14).constructor + "<br>" +
  false.constructor + "<br>" +
  [1,2,3,4].constructor + "<br>" +
  {name:'john', age:34}.constructor + "<br>" +
  new Date().constructor + "<br>" +
  function () {}.constructor;
</script>
```

```
The constructor property returns the constructor function for a variable or an object.

function String() { [native code] }
function Number() { [native code] }
function Boolean() { [native code] }
function Array() { [native code] }
function Object() { [native code] }
function Date() { [native code] }
function Function() { [native code] }
```

**проверить свойство конструктора, чтобы узнать, является ли объект Array**
```
<p>This "home made" isArray() function returns true when used on an array:</p>

<p id="demo"></p>

<script>
var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = isArray(fruits);

function isArray(myArray) {
  return myArray.constructor.toString().indexOf("Array") > -1;              //true
}
</script>
```

**можете проверить, является ли объект функцией Array**
```

<script>
var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = isArray(fruits);

function isArray(myArray) {
  return myArray.constructor === Array;
}
</script>
```

```
JavaScript Array Object
This "home made" isArray() function returns true when used on an array:

true
```

**проверить свойство конструктора, чтобы узнать, является ли объект Date**
```
<script>
var myDate = new Date();
document.getElementById("demo").innerHTML = isDate(myDate);

function isDate(myDate) {
  return myDate.constructor.toString().indexOf("Date") > -1;   //true
} 
</script>
```


можете проверить, является ли объект функцией Date 
---
```
<script>
var myDate = new Date();
document.getElementById("demo").innerHTML = isDate(myDate);

function isDate(myDate) {
  return myDate.constructor === Date;     //true
}
</script>
```

---

Преобразование типов JavaScript
---
Переменные JavaScript могут быть преобразованы в новую переменную и другой тип данных:

* С помощью функции JavaScript
* Автоматически по самому JavaScript
---

Преобразование чисел в строки
---
Глобальный метод String()может преобразовывать числа в строки.

Он может быть использован для любого типа чисел, литералов, переменных или выражений:
```
<script>
var x = 123;
document.getElementById("demo").innerHTML =
  String(x) + "<br>" +           //123
  String(123) + "<br>" +         //123
  String(100 + 23);              //123
</script>
```
**Метод Number `toString()`cделает то же самое.**
```
<script>
var x = 123;
document.getElementById("demo").innerHTML =
  x.toString() + "<br>" +                  //123
   (123).toString() + "<br>" +              //123
   (100 + 23).toString();                  //123
</script> 
```

---
`toExponential() `                    Возвращает строку с округленным числом и написанную с использованием экспоненциальной записи.

---
`toFixed() `                          Возвращает строку с округленным числом и записанным с указанным количеством десятичных знаков.

---
`toPrecision() `                      Возвращает строку с записанным числом указанной длины

---


Преобразование логических значений в строки
---
Глобальный метод `String()` может преобразовывать логические значения в строки.
```
String(false)      // returns "false"
String(true)       // returns "true"
```
Булевый метод `toString()`cделает то же самое.
---
false.toString()   // returns "false"
true.toString()    // returns "true"

---

Преобразование дат в строки
---
Глобальный метод `String()` может конвертировать даты в строки.
```
String(Date())  // returns "Thu Jul 17 2014 15:38:19 GMT+0200 (W. Europe Daylight Time)"
```
Метод Date `toString()`делает то же самое.
```
Date().toString()  // returns "Thu Jul 17 2014 15:38:19 GMT+0200 (W. Europe Daylight Time)"
```
---
getDate()	Get the day as a number (1-31)
getDay()	Get the weekday a number (0-6)
getFullYear()	Get the four digit year (yyyy)
getHours()	Get the hour (0-23)
getMilliseconds()	Get the milliseconds (0-999)
getMinutes()	Get the minutes (0-59)
getMonth()	Get the month (0-11)
getSeconds()	Get the seconds (0-59)
getTime()	Get the time (milliseconds since January 1, 1970)

---

Преобразование строк в числа
---

Глобальный метод` Number()` может преобразовывать строки в числа.

Строки, содержащие числа (например, «3.14»), преобразуются в числа (например, 3.14).

Пустые строки конвертируются в 0.

Все остальное конвертируется в NaN(не число).

Number("3.14")    // returns 3.14
Number(" ")       // returns 0
Number("")        // returns 0
Number("99 88")   // returns NaN

---

`parseFloat()`	Parses a string and returns a floating point number  (Разбирает строку и возвращает число с плавающей запятой)
# 
`parseInt()`      Parses a string and returns an integer      (Разбирает строку и возвращает целое число)

---
Унарный + Оператор     (The Unary + Operator)
--- 
**Унарный оператор** + может быть использован для преобразования переменного в число:
```<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
function myFunction() {
  var y = "5";                                                                  //string
  var x = + y;                                                                  //number
  document.getElementById("demo").innerHTML = typeof y + "<br>" + typeof x;
}
</script>
```
---
Если переменная не может быть преобразована, она все равно станет числом, но со значением NaN (не числом):
var y = "John";   // y is a string
var x = + y;      // x is a number (NaN)

---

Преобразование логических чисел в числа
---
Глобальный метод` Number()` также может преобразовывать логические значения в числа.
```

Number(false)     // returns 0
Number(true)      // returns 1
```
---
Преобразование дат в числа
---
Глобальный метод `Number()` может быть использован для преобразования дат в числа.
```
d = new Date();
Number(d)          // returns 1404568027739
```
# 
Метод даты `getTime()` делает то же самое.
```
d = new Date();
d.getTime()        // returns 1404568027739
```
# 
---
# 
Автоматическое преобразование типов
---
Когда JavaScript пытается работать с «неправильным» типом данных, он пытается преобразовать значение в «правильный» тип.
```

<script>
var x = [];
document.getElementById("demo").innerHTML =
(5 + null) + "<br>"  +
("5" + null) + "<br>" +
("5" + 2) + "<br>" +
("5" - 2) + "<br>" +
("5" * "2") + "<br>" +
("5" / "2") + "<br>"
</script>
```
Результат не всегда то, что вы ожидаете:

5 + null    // returns 5         because null is converted to 0
"5" + null  // returns "5null"   because null is converted to "null"
"5" + 2     // returns "52"      because 2 is converted to "2"
"5" - 2     // returns 3         because "5" is converted to 5
"5" * "2"   // returns 10        because "5" and "2" are converted to 5 and 2

---

Автоматическое преобразование строк
---
JavaScript автоматически вызывает `toString()` функцию переменной, когда вы пытаетесь «вывести» объект или переменную:

---
**document.getElementById("demo").innerHTML = myVar;**

// if myVar = {name:"Fjohn"}  // toString converts to "[object Object]"
// if myVar = [1,2,3,4]       // toString converts to "1,2,3,4"
// if myVar = new Date()      // toString converts to "Fri Jul 18 2014 09:08:55 GMT+0200"

---
Числа и логические значения также преобразуются, но это не очень заметно:

// if myVar = 123             // toString converts to "123"
// if myVar = true            // toString converts to "true"
// if myVar = false           // toString converts to "false"

---
Таблица преобразования типов JavaScript
---
( https://www.w3schools.com/js/js_type_conversion.asp )

---