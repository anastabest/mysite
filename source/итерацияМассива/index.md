---
title: Итерация Массива   / Array Iteration
date: 2020-04-13 17:19:50
---
Методы итерации JavaScript
---

---
# 
Методы итерации массива работают с каждым элементом массива.
# 
---
`forEach()` Метод вызывает функцию _(функцию обратного вызова)_ один раз для каждого элемента массива.
# 
```
<p>Calls a function once for each array element.</p>

<p id="demo"></p>

<script>
var txt = "";
var numbers = [45, 4, 9, 16, 25];
numbers.forEach(myFunction);
document.getElementById("demo").innerHTML = txt;

function myFunction(value, index, array) {
  txt = txt + value + "<br>"; 
}
</script>
// 45
// 4
// 9
// 16
// 25
```
# 
Обратите внимание, что функция принимает 3 аргумента:
# 
* Стоимость товара
* Предметный указатель
* Сам массив
# 
Пример можно переписать так:
# 
```
<p>Calls a function once for each array element.</p>

<p id="demo"></p>

<script>
var txt = "";
var numbers = [45, 4, 9, 16, 25];
numbers.forEach(myFunction);
document.getElementById("demo").innerHTML = txt;

function myFunction(value) {
  txt = txt + value + "<br>"; 
}
</script>
// 45
// 4
// 9
// 16
// 25
```
---
# 
Array.map ()
---
`map()` Метод создает новый массив, выполняя функцию для каждого элемента массива.
# 
`map()` Метод не выполняет функцию для элементов массива без значений.
# 
`map()` Метод не изменяет исходный массив.
# 
Этот пример умножает каждое значение массива на 2:
```
<p>Creates a new array by performing a function on each array element.</p>

<p id="demo"></p>

<script>
var numbers1 = [45, 4, 9, 16, 25];
var numbers2 = numbers1.map(myFunction);

document.getElementById("demo").innerHTML = numbers2;

function myFunction(value, index, array) {
  return value * 2;
}
</script>   //90,8,18,32,50
```
# 
функция принимает 3 аргумента:
# 
* Стоимость товара
* Предметный указатель
* Сам массив
# 
Когда функция обратного вызова использует только параметр value, параметры index и array могут быть опущены:
# 
```
<p>Creates a new array by performing a function on each array element.</p>

<p id="demo"></p>

<script>
var numbers1 = [45, 4, 9, 16, 25];
var numbers2 = numbers1.map(myFunction);

document.getElementById("demo").innerHTML = numbers2;

function myFunction(value) {
  return value * 2;
} 
</script>     //90,8,18,32,50
```
---
# 
Array.filter ()
---

`filter()` Метод создает новый массив с элементами массива, проходит тест.

В этом примере создается новый массив из элементов со значением больше 18:
```
<p>Creates a new array with all array elements that passes a test.</p>

<p id="demo"></p>

<script>
var numbers = [45, 4, 9, 16, 25];
var over18 = numbers.filter(myFunction);

document.getElementById("demo").innerHTML = over18;

function myFunction(value, index, array) {
  return value > 18;
}
</script>   //45,25
```
# 
```
<p>Creates a new array with all array elements that passes a test.</p>

<p id="demo"></p>

<script>
var numbers = [45, 4, 9, 16, 25];
var over18 = numbers.filter(myFunction);

document.getElementById("demo").innerHTML = over18;

function myFunction(value) {
  return value > 18;         //45,25
}
</script>
```
---
# Array.reduce ()
`reduce()` Метод запускает функцию для каждого элемента массива , чтобы произвести (уменьшить его до) одно значение.

`reduce()` Метод работает слева направо в массиве. Смотрите также `reduceRight().`
# 

**`reduce() `Метод не уменьшает исходный массив.**
# 
Этот пример находит сумму всех чисел в массиве:
# 
```
<p>This example finds the sum of all numbers in an array:</p>

<p id="demo"></p>

<script>
var numbers = [45, 4, 9, 16, 25];
var sum = numbers.reduce(myFunction);

document.getElementById("demo").innerHTML = "The sum is " + sum;

function myFunction(total, value, index, array) {
  return total + value;
}
</script>                                 //The sum is 99
```
# 
функция принимает 4 аргумента
# 
* Итого (начальное значение / ранее возвращенное значение)
* Стоимость товара
* Предметный указатель
* Сам массив
# 
В приведенном выше примере не используются параметры индекса и массива.
# 
```
<p>This example finds the sum of all numbers in an array:</p>

<p id="demo"></p>

<script>
var numbers = [45, 4, 9, 16, 25];
var sum = numbers.reduce(myFunction);

document.getElementById("demo").innerHTML = "The sum is " + sum;

function myFunction(total, value) {
  return total + value;
}
</script>
```
# 
`reduce() `Метод может принимать начальное значение:
# 
```
<p>This example finds the sum of all numbers in an array:</p>

<p id="demo"></p>

<script>
var numbers = [45, 4, 9, 16, 25];
var sum = numbers.reduce(myFunction, 100);

document.getElementById("demo").innerHTML = "The sum is " + sum;

function myFunction(total, value) {
  return total + value;                   //The sum is 199
}
</script>
```
---
# 
Array.reduceRight ()
---
# 
`reduceRight()` Метод запускает функцию для каждого элемента массива , чтобы произвести (уменьшить его до) одно значение.
# 
В `reduceRight()` работах от справа налево в массиве. Смотрите также `reduce().`
# 
`reduceRight()` Метод не уменьшает исходный массив.
# 
пример находит сумму всех чисел в массиве:
# 
```
<p>This example finds the sum of all numbers in an array:</p>

<p id="demo"></p>

<script>
var numbers = [45, 4, 9, 16, 25];
var sum = numbers.reduceRight(myFunction);

document.getElementById("demo").innerHTML = "The sum is " + sum;

function myFunction(total, value, index, array) {
  return total + value;
}
</script>           //The sum is 99
```
# 
 функция принимает 4 аргумента:

Итого (начальное значение / ранее возвращенное значение)
# 
* Стоимость товара
* Предметный указатель
* Сам массив
# 
# 
```
<p>This example finds the sum of all numbers in an array:</p>

<p id="demo"></p>

<script>
var numbers = [45, 4, 9, 16, 25];
var sum = numbers.reduceRight(myFunction);

document.getElementById("demo").innerHTML = "The sum is " + sum;

function myFunction(total, value) {
  return total + value;
}
</script>       //The sum is 99
```
---
Array.every ()
---
`every()` Проверка метода , если все значения массива пройти тест.
# 
В этом примере проверьте, все ли значения массива больше 18:
```
<p>The every() method checks if all array values pass a test.</p>

<p id="demo"></p>

<script>
var numbers = [45, 4, 9, 16, 25];
var allOver18 = numbers.every(myFunction);

document.getElementById("demo").innerHTML = "All over 18 is " + allOver18;

function myFunction(value, index, array) {
  return value > 18;
}
</script>   //All over 18 is false
```
# 
# 
Array.some ()
---
`some()`Проверка метода , если некоторые значения массива пройти тест.

 пример проверки, если некоторые значения массива больше 18:
```
<p>The some() method checks if some array values pass a test.</p>

<p id="demo"></p>

<script>
var numbers = [45, 4, 9, 16, 25];
var someOver18 = numbers.some(myFunction);

document.getElementById("demo").innerHTML = "Some over 18 is " + someOver18;

function myFunction(value, index, array) {
  return value > 18;
}
</script>      //Some over 18 is true
```
---
# 
# 
Array.indexOf ()
---
`indexOf() `Метод ищет массив для значения элемента и возвращает его позицию.
_Поиск в массиве для элемента «Apple»:_
```

<p id="demo"></p>

<script>
var fruits = ["Apple", "Orange", "Apple", "Mango"];
var a = fruits.indexOf("Apple");
document.getElementById("demo").innerHTML = "Apple is found in position " + a;
</script>           //Apple is found in position 0

<p>The indexOf() does not work in Internet Explorer 8 and earlier versions.</p>
```
**`Синтаксис`**
```
array.indexOf(item, start)
```
---
# 
_item_
пункт      Обязательный. Элемент для поиска.

---
start
начать      Необязательными. С чего начать поиск. Отрицательные  значения начнутся с заданной позиции, начиная с конца, и начнут поиск до конца.
# 
`Array.indexOf()` возвращает -1, если элемент не найден.
# 
Если элемент присутствует более одного раза, он возвращает позицию первого вхождения.

---
Array.lastIndexOf ()
---
`Array.lastIndexOf()` такой же, как `Array.indexOf(),` но возвращает позицию последнего вхождения указанного элемента.
# 
Поиск в массиве для элемента «Apple»:
```
<script>
var fruits = ["Apple", "Orange", "Apple", "Mango"];
var a = fruits.lastIndexOf("Apple");
document.getElementById("demo").innerHTML = "Apple is found in position " + (a + 1);      //Apple is found in position 3
</script>
```
---
# 
Array.find ()
---
`find()` Метод возвращает значение первого элемента массива , который проходит тестовую функцию.
# 
 пример находит (возвращает значение) первый элемент, который больше 18:
```
<script>
var numbers = [4, 9, 16, 25, 29];
var first = numbers.find(myFunction);

document.getElementById("demo").innerHTML = "First number over 18 is " + first;

function myFunction(value, index, array) {
  return value > 18;
}
</script>       //First number over 18 is 25
```
---
Array.findIndex ()
---
`findIndex()` Метод возвращает индекс первого элемента массива , который проходит тестовую функцию.
# 
Этот пример находит индекс первого элемента, который больше 18:
```
<script>
var numbers = [4, 9, 16, 25, 29];
var first = numbers.findIndex(myFunction);

document.getElementById("demo").innerHTML = "First number over 18 has index " + first;

function myFunction(value, index, array) {
  return value > 18;
}
</script>    //First number over 18 has index 3
```