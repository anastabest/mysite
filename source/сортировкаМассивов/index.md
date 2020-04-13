---
title: Сортировка Массивов - /JavaScript Sorting Arrays/
date: 2020-04-13 15:23:10
---
`sort()` Метод сортирует массив по алфавиту
```
<p>The sort() method sorts an array alphabetically.</p>

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits;

function myFunction() {
  fruits.sort();
  document.getElementById("demo").innerHTML = fruits;
}
</script>
```
`reverse()` Метод изменяет элементы в массиве.
```
<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
// Create and display an array:
var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits;

function myFunction() {
  // First sort the array
  fruits.sort();
  // Then reverse it:
  fruits.reverse();
  document.getElementById("demo").innerHTML = fruits;
}
</script>
```
Числовая сортировка
---
По умолчанию `sort()` функция сортирует значения в виде строк .
Однако, если числа отсортированы как строки, «25» больше, чем «100», потому что «2» больше, чем «1».

Из-за этого `sort()` метод будет давать неверный результат при сортировке чисел.
```
<p>Click the button to sort the array in ascending order.</p>

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
var points = [40, 100, 1, 5, 25, 10];
document.getElementById("demo").innerHTML = points;  

function myFunction() {
  points.sort(function(a, b){return a - b});
  document.getElementById("demo").innerHTML = points;
}
</script>
```
---
Функция сравнения
---
Цель функции сравнения - определить альтернативный порядок сортировки.
# 
Функция сравнения должна возвращать отрицательное, нулевое или положительное значение в зависимости от аргументов:
```
function(a, b){return a - b}
```
Когда `sort()` функция сравнивает два значения, она отправляет значения в функцию сравнения и сортирует значения в соответствии с возвращенным (отрицательным, нулевым, положительным) значением.
# 
**Пример:**
# 
Функция сравнения сравнивает все значения в массиве по два значения за раз (a, b).
# 
При сравнении 40 и 100 sort()метод вызывает функцию сравнения (40, 100).
# 
Функция вычисляет 40 - 100 (a - b), и поскольку результат отрицательный (-60), функция сортировки будет сортировать 40 как значение ниже 100.
```
<button onclick="myFunction1()">Sort Alphabetically</button>
<button onclick="myFunction2()">Sort Numerically</button>

<p id="demo"></p>

<script>
var points = [40, 100, 1, 5, 25, 10];
document.getElementById("demo").innerHTML = points;  

function myFunction1() {
  points.sort();
  document.getElementById("demo").innerHTML = points;
}
function myFunction2() {
  points.sort(function(a, b){return a - b});
  document.getElementById("demo").innerHTML = points;
}
</script>
```
Сортировка массива в случайном порядке
---
```
<p>Click the button (again and again) to sort the array in random order.</p>

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
var points = [40, 100, 1, 5, 25, 10];
document.getElementById("demo").innerHTML = points;  

function myFunction() {
  points.sort(function(a, b){return 0.5 - Math.random()});
  document.getElementById("demo").innerHTML = points;
}
</script>
```
The Fisher Yates Method
---
```
<p>Click the button (again and again) to sort the array in random order.</p>

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
var points = [40, 100, 1, 5, 25, 10];
document.getElementById("demo").innerHTML = points;  

function myFunction() {
var i, j, k;
  for (i = points.length -1; i > 0; i--) {
    j = Math.floor(Math.random() * i)
    k = points[i]
    points[i] = points[j]
    points[j] = k
  }
  document.getElementById("demo").innerHTML = points;
}
</script>

```
Найти самое высокое (или самое низкое) значение массива
---
после сортировки массива вы можете использовать индекс для получения самых высоких и самых низких значений.

Сортировка по возрастанию:
```
<p>The lowest number is <span id="demo"></span>.</p>

<script>
var points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return a-b});
document.getElementById("demo").innerHTML = points[0];   //The lowest number is 1. 
</script>
```
# 
**//теперь points [0] содержит самое низкое значение**
**// и points [points.length-1] содержит наибольшее значение**
# 
# 
Сортировка по убыванию:
# 
```
<p>The highest number is <span id="demo"></span>.</p>

<script>
var points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return b-a});
document.getElementById("demo").innerHTML = points[0];
</script>
```
# 
**// теперь points [0] содержит наибольшее значение**
**// и points [points.length-1] содержит самое низкое значение**
# 
# 
Использование `Math.max () `для массива
Вы можете использовать, Math.max.applyчтобы найти наибольшее число в массиве:
---
```
<script>
var points = [40, 100, 1, 5, 25, 10];
document.getElementById("demo").innerHTML = myArrayMax(points);

function myArrayMax(arr) {
  return Math.max.apply(null, arr);  //The highest number is 100.
}
</script>
```
# 
# 
# 
`Math.max.apply(null, [1, 2, 3])` эквивалентно `Math.max(1, 2, 3).`
Использование Math.min () для массива
---
# 

Вы можете использовать, Math.min.applyчтобы найти наименьшее число в массиве:
```
<p>The lowest number is <span id="demo"></span>.</p>

<script>
var points = [40, 100, 1, 5, 25, 10];
document.getElementById("demo").innerHTML = myArrayMin(points);

function myArrayMin(arr) {
  return Math.min.apply(null, arr);  //The lowest number is 1.
}
</script>
```
`Math.min.apply(null, [1, 2, 3])` эквивалентно `Math.min(1, 2, 3).`
# 
---
# 
Мои Мин / Макс Методы JavaScript    //My Min / Max JavaScript Methods
---
Самое быстрое решение - это использовать «домашний» метод.
# 
Эта функция просматривает массив, сравнивая каждое значение с наибольшим найденным значением:
**Пример (Найти Макс)**
```
<p>The highest number is <span id="demo"></span>.</p>

<script>
var points = [40, 100, 1, 5, 25, 10];
document.getElementById("demo").innerHTML = myArrayMax(points);

function myArrayMax(arr) {
  var len = arr.length;
  var max = -Infinity;
  while (len--) {
    if (arr[len] > max) {
      max = arr[len];            //The highest number is 100.
    }
  }
  return max;
}
</script>
```
# 
Эта функция просматривает массив, сравнивая каждое значение с самым низким найденным значением:
```
<p>The lowest number is <span id="demo"></span>.</p>

<script>
var points = [40, 100, 1, 5, 25, 10];
document.getElementById("demo").innerHTML = myArrayMin(points);

function myArrayMin(arr) {
  var len = arr.length;
  var min = Infinity;
  while (len--) {
    if (arr[len] < min) {
      min = arr[len];
    }
  }
  return min;    //The lowest number is 1.
}
</script>
```
Сортировка массивов объектов
---
# 
Массивы JavaScript часто содержат объекты:
# 
```
var cars = [
  {type:"Volvo", year:2016},
  {type:"Saab", year:2001},
  {type:"BMW", year:2010}
];
```
# 
Даже если объекты имеют свойства разных типов данных, sort()метод можно использовать для сортировки массива.
# 
Решение состоит в том, чтобы написать функцию сравнения для сравнения значений свойств:
# 
```
<button onclick="myFunction()">Sort</button>

<p id="demo"></p>

<script>
var cars = [
  {type:"Volvo", year:2016},
  {type:"Saab", year:2001},
  {type:"BMW", year:2010}
];

displayCars();

function myFunction() {
  cars.sort(function(a, b){return a.year - b.year});
  displayCars();
}

function displayCars() {
  document.getElementById("demo").innerHTML =
  cars[0].type + " " + cars[0].year + "<br>" +    //Saab 2001
                                                  // BMW 2010
                                                  // Volvo 2016
  cars[1].type + " " + cars[1].year + "<br>" +
  cars[2].type + " " + cars[2].year;
}
</script>
```
# 
Сравнение свойств строки
# 
```

<button onclick="myFunction()">Sort</button>

<p id="demo"></p>

<script>
var cars = [
  {type:"Volvo", year:2016},
  {type:"Saab", year:2001},
  {type:"BMW", year:2010}
];

displayCars();

function myFunction() {
  cars.sort(function(a, b){
    var x = a.type.toLowerCase();
    var y = b.type.toLowerCase();
    if (x < y) {return -1;}
    if (x > y) {return 1;}
    return 0;
  });
  displayCars();
}

function displayCars() {
  document.getElementById("demo").innerHTML =
  cars[0].type + " " + cars[0].year + "<br>" +
  cars[1].type + " " + cars[1].year + "<br>" +
  cars[2].type + " " + cars[2].year;
}
</script>       //BMW 2010
                //Saab 2001
                //Volvo 2016

```