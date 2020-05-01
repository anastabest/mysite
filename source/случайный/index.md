---
title: Случайный
date: 2020-04-16 13:10:43
---
**Java Script Random**

---
# 
Math.random ()
---
`Math.random()` возвращает случайное число от 0 (включительно) до 1 (исключая):
```
<p>Math.random() returns a random number between 0 (included) and 1 (excluded):</p>

<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = Math.random();     // returns a random number
</script> 

```

**`Math.random()` всегда возвращает число ниже 1.**

---
# 
JavaScript случайные целые числа
---
`Math.random() ` используется с `Math.floor() ` может быть использована для получения случайных чисел.
```
<p>Math.floor(Math.random() * 10) returns a random integer between 0 and 9 (both 
included):</p>

<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML =
Math.floor(Math.random() * 10);
</script>                                     // returns a random integer from 0 to 9
```
# 
```
Math.floor(Math.random() * 11);      // returns a random integer from 0 to 10
```
# 
```
Math.floor(Math.random() * 101);     // returns a random integer from 0 to 100
```
# 
```
Math.floor(Math.random() * 10) + 1;  // returns a random integer from 1 to 10
```
# 
```
Math.floor(Math.random() * 100) + 1; // returns a random integer from 1 to 100
```
# 
---
# 
Правильная случайная функция
---
Как видно из приведенных выше примеров, было бы неплохо создать правильную случайную функцию, которая будет использоваться для всех случайных целочисленных целей.
# 
Эта функция JavaScript всегда возвращает случайное число между min (включенным) и max (исключенным):
```
<p>Every time you click the button, getRndInteger(min, max) returns a random number between 0 
and 9 (both included):</p>

<button onclick="document.getElementById('demo').innerHTML = getRndInteger(0,10)">Click Me</button>

<p id="demo"></p>

<script>
function getRndInteger(min, max) {
  return Math.floor(Math.random() * (max - min)) + min;
}
</script>
```
```
Every time you click the button, getRndInteger(min, max) returns a random number between 0 and 9 (both included):

Click Me

return random
```
# 
Эта функция JavaScript всегда возвращает случайное число между min и max (оба включены):
```
<p>Every time you click the button, getRndInteger(min, max) returns a random number between 1 and 10 (both included):</p>

<button onclick="document.getElementById('demo').innerHTML = getRndInteger(1,10)">Click Me</button>

<p id="demo"></p>

<script>
function getRndInteger(min, max) {
  return Math.floor(Math.random() * (max - min + 1) ) + min;
}
</script>                                            
```
```
JavaScript Math.random()
Every time you click the button, getRndInteger(min, max) returns a random number between 1 and 10 (both included):

Click Me

return random
```
