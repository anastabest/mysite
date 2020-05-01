---
title: Математический Объект 
date: 2020-04-16 12:24:51
---
 **Java Script Math Object**

 ---
 - Объект JavaScript` Math` позволяет выполнять математические задачи над числами.
# 
Math.round ()
---
`Math.round(x)` возвращает значение x, округленное до ближайшего целого числа:
```
<p>Math.round(x) returns the value of x rounded to its nearest integer:</p>

<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = Math.round(4.4); //4
</script>
```
# 
```
Math.round(4.7);    // returns 5
Math.round(4.4);    // returns 4
```
---
# 
Math.pow ()
---
`Math.pow(x, y)` возвращает значение x в степень y:
```

<script>
document.getElementById("demo").innerHTML = Math.pow(8,2);  //64
</script>
```
---
# 
Math.sqrt ()
---
`Math.sqrt(x)` возвращает квадратный корень из x:
```
<script>
document.getElementById("demo").innerHTML = Math.sqrt(64); //8
</script>
```
---
# 
Math.abs ()
---
`Math.abs(x)` возвращает абсолютное (положительное) значение x:
```
<script>
document.getElementById("demo").innerHTML = Math.abs(-4.4); //4.4
</script>
```
---
# 
Math.ceil ()
---
`Math.ceil(x)` возвращает значение x, округленное до ближайшего целого числа:
```
<script>
document.getElementById("demo").innerHTML = Math.ceil(4.4);  //5
</script>
```
---
# 
Math.floor ()
---
`Math.floor(x)`возвращает значение х округляется вниз до ближайшего целого числа:
```

<script>
document.getElementById("demo").innerHTML = Math.floor(4.7); //4
</script>
```
---
# 
Math.sin ()
---
`Math.sin(x)` возвращает синус (значение между -1 и 1) угла x (в радианах).
# 
Если вы хотите использовать градусы вместо радиан, вам нужно конвертировать градусы в радианы:
# 
Угол в радианах = Угол в градусах х PI / 180.
# 
```
<script>
document.getElementById("demo").innerHTML = 
"The sine value of 90 degrees is " + Math.sin(90 * Math.PI / 180);
</script>
```
```
//Math.sin(x) returns the sin of x (given in radians):

//Angle in radians = (angle in degrees) * PI / 180.

//The sine value of 90 degrees is 1
```
---
# 
Math.cos ()
---
`Math.cos(x)` возвращает косинус (значение между -1 и 1) угла x (в радианах).
# 
Если вы хотите использовать градусы вместо радиан, вам нужно конвертировать градусы в радианы:
# 
Угол в радианах = Угол в градусах х PI / 180.
# 
```
<script>
document.getElementById("demo").innerHTML = 
"The cosine value of 0 degrees is " + Math.cos(0 * Math.PI / 180);
</script>
```
```
//Math.cos(x) returns the cosine of x (given in radians):
 
//Angle in radians = (angle in degrees) * PI / 180.

//The cosine value of 0 degrees is 1

```
---
# 
Math.min () и Math.max ()
---
` Math.min()` и ` Math.max()` может использоваться, чтобы найти самое низкое или самое высокое значение в списке аргументов:
```
<p>Math.min() returns the lowest value in a list of arguments:</p>

<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML =
Math.min(0, 150, 30, 20, -8, -200);      //-200
</script>
```
# 
```
<p>Math.max() returns the highest value in a list of arguments.</p>

<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML =
Math.max(0, 150, 30, 20, -8, -200);    //150
</script>
```
---
# 
Math.random ()
---
` Math.random()`  возвращает случайное число от 0 (включительно) до 1 (исключая):
```


<p>Math.random() returns a random number between 0 and 1:</p>

<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = Math.random();   // returns a random number

</script>
```
---
# 
Математические свойства (константы)
---
JavaScript предоставляет 8 математических констант, к которым можно обращаться с помощью объекта Math:
```
<script>
document.getElementById("demo").innerHTML = 
"<p><b>Math.E:</b> " + Math.E + "</p>" +
"<p><b>Math.PI:</b> " + Math.PI + "</p>" +
"<p><b>Math.SQRT2:</b> " + Math.SQRT2 + "</p>" +
"<p><b>Math.SQRT1_2:</b> " + Math.SQRT1_2 + "</p>" +
"<p><b>Math.LN2:</b> " + Math.LN2 + "</p>" +
"<p><b>Math.LN10:</b> " + Math.LN10 + "</p>" +
"<p><b>Math.LOG2E:</b> " + Math.LOG2E + "</p>" +
"<p><b>Math.Log10E:</b> " + Math.LOG10E + "</p>";
</script>
```
```
JavaScript Math Constants

 //Math.E: 2.718281828459045

 //Math.PI: 3.141592653589793

 //Math.SQRT2: 1.4142135623730951

 //Math.SQRT1_2: 0.7071067811865476

 //Math.LN2: 0.6931471805599453

 //Math.LN10: 2.302585092994046

 //Math.LOG2E: 1.4426950408889634

 //Math.Log10E: 0.4342944819032518
```
---
# 
Математический конструктор
---
- В отличие от других глобальных объектов, объект Math не имеет конструктора. Методы и свойства являются статическими.

- Все методы и свойства (константы) могут использоваться без предварительного создания объекта Math.

Методы математических объектов
---
(https://www.w3schools.com/js/js_math.asp)

---
полный математический справочник
---
(https://www.w3schools.com/jsref/jsref_obj_math.asp)
