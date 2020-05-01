---
title: Булевые
date: 2020-04-16 13:27:17
---
**JavaScript Booleans**

---
JavaScript Boolean представляет одно из двух значений:**true** или **false** .

---
Булевы значения
---
Очень часто в программировании вам понадобится тип данных, который может иметь только одно из двух значений, например
# 
- ДА НЕТ
- ВКЛ ВЫКЛ
- ИСТИНА / ЛОЖЬ
# 
Для этого в JavaScript есть **логический** тип данных. Он может принимать только значения **true** или **false** .

---
The Boolean() Function
---
Вы можете использовать `Boolean()` функцию, чтобы узнать, является ли выражение (или переменная) истинным:
```
<p>Display the value of Boolean(10 > 9):</p>

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
function myFunction() {
  document.getElementById("demo").innerHTML = Boolean(10 > 9);
}
</script>
```
```
Display the value of Boolean(10 > 9):

Try it

true
```
# 
```
<p>Display the value of 10 > 9:</p>

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
function myFunction() {
  document.getElementById("demo").innerHTML = 10 > 9;
}
</script>
```
```
Display the value of 10 > 9:

Try it

true
```
---
Сравнения и условия
---
```
==	equal to	if (day == "Monday")
```
```
>	greater than	if (salary > 9000)
```
```
<	less than	if (age < 18)
```
---
# 
Everything With a "Value" is True
---
**Все с «ценностью» - правда**
# 
```

<script>
var b1 = Boolean(100);
var b2 = Boolean(3.14);
var b3 = Boolean(-15);
var b4 = Boolean("Hello");
var b5 = Boolean('false');
var b6 = Boolean(1 + 7 + 3.14);

document.getElementById("demo").innerHTML =
"100 is " + b1 + "<br>" +
"3.14 is " + b2 + "<br>" +
"-15 is " + b3 + "<br>" +
"Any (not empty) string is " + b4 + "<br>" +
"Even the string 'false' is " + b5 + "<br>" +
"Any expression (except zero) is " + b6;
</script>
```
```
100 is true
3.14 is true
-15 is true
Any (not empty) string is true
Even the string 'false' is true
Any expression (except zero) is true
```
---
# 
Everything Without a "Value" is False
---
**Все без «ценности» ложно**
Логическое значение 0 (ноль) равно false :
```
<p>Display the Boolean value of -0:</p>

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
function myFunction() {
  var x = -0;
  document.getElementById("demo").innerHTML = Boolean(x);
}
</script>
```
```
Display the Boolean value of -0:

Try it

false
```
---
# 
Логическое значение -0 (минус ноль) является ложным :
```
<p>Display the Boolean value of -0:</p>

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
function myFunction() {
  var x = -0;
  document.getElementById("demo").innerHTML = Boolean(x);
}
</script>

```
```
Display the Boolean value of -0:

Try it

false
```
# 
Логическое значение "" (пустая строка) равно false :
```
<p>Display the Boolean value of "":</p>

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
function myFunction() {
  var x = "";
  document.getElementById("demo").innerHTML = Boolean(x);
}
</script>
```
```
Display the Boolean value of "":

Try it

false
```
Логическое значение undefined равно false :
```
<p>Display the Boolean value of undefined:</p>

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
function myFunction() {
  var x;
  document.getElementById("demo").innerHTML = Boolean(x);
}
</script>

```
```
Display the Boolean value of undefined:

Try it

false
```
Логическое значение null равно false :
```
<p>Display the Boolean value of null:</p>

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
function myFunction() {
  var x = null;
  document.getElementById("demo").innerHTML = Boolean(x);
}
</script>
```
```
 //false
```
Логическое значение false равно (как вы уже догадались) false :
```
<script>
function myFunction() {
  var x = false;
  document.getElementById("demo").innerHTML = Boolean(x);
}
</script>
```
```
false
```
Логическое значение NaN является ложным :
```
<script>
function myFunction() {
  var x = 10 / "H";
  document.getElementById("demo").innerHTML = Boolean(x);
}
</script>
```

```
//false
```
---
# 

Логические значения могут быть объектами
---
# 
Обычно логические значения JavaScript являются примитивными значениями, созданными из литералов:

`var x = false;`

Но логические значения также могут быть определены как объекты с ключевым словом new:

`var y = new Boolean(false);    ` 

```
p>Never create booleans as objects.</p>
<p>Booleans and objects cannot be safely compared.</p>

<p id="demo"></p>

<script>
var x = false;                // x is a boolean
var y = new Boolean(false);  // y is an object
document.getElementById("demo").innerHTML = typeof x + "<br>" + typeof y;
</script>
```
# 
При использовании `==` оператора, равные булевы равны:
# 
```
<script>
var x = false;                // x is a boolean
var y = new Boolean(false);  // y is an object
document.getElementById("demo").innerHTML = (x==y);
</script>

```
# 
При использовании `===` оператора равные логические значения не равны, поскольку `=== `оператор ожидает равенства как по типу, так и по значению.

# 
``` 
<script> 
var x = false;                 // x is a number
var y = new Boolean(false);  // y is an object
document.getElementById("demo").innerHTML = (x===y);    //false
</script>
```
# 
Объекты нельзя сравнивать:
# 
```
<script>
var x = new Boolean(false);  // x is an object
var y = new Boolean(false);  // y is an object
document.getElementById("demo").innerHTML = (x==y);  //false
</script>
```
**`Обратите внимание на разницу между (x == y) и (x === y).`**
**`Сравнение двух объектов JavaScript всегда возвращает false.`**
