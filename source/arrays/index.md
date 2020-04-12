---
title: JS Arrays
date: 2020-04-01 13:35:26
---
Массивы JavaScript
---
`Создание массива`
---
Синтаксис:
```
var array_name = [item1, item2, ...];      
```
Массивы JavaScript используются для хранения нескольких значений в одной переменной.
1.
```
<script>
var cars = ["Saab", "Volvo", "BMW"];
document.getElementById("demo").innerHTML = cars;  //Saab,Volvo,BMW
</script>
```
2.
```
var cars = [
  "Saab",
  "Volvo",
  "BMW"
];
```
`Использование ключевого слова JavaScript new`
---
создается массив и присваиваются ему значения:
```
<script>
var cars = new Array("Saab", "Volvo", "BMW");
document.getElementById("demo").innerHTML = cars;
</script>
```
Массив - это специальная переменная, которая может содержать более одного значения за раз.
_Если у вас есть список элементов (например, список имен автомобилей), хранение автомобилей в отдельных переменных может выглядеть следующим образом:_
* var car1 = "Saab";
* var car2 = "Volvo";
* var car3 = "BMW";
`Доступ к элементам массива`
---
Вы получаете доступ к элементу массива, ссылаясь на **номер индекса .**
```
<script>
var cars = ["Saab", "Volvo", "BMW"];
document.getElementById("demo").innerHTML = cars[0];  //Saab
</script>
```
`Изменение элемента массива`
---
```
<script>
var cars = ["Saab", "Volvo", "BMW"];
cars[0] = "Opel";
document.getElementById("demo").innerHTML = cars;  //Opel,VOlVO,BMW
</script>
```
`Доступ к полному массиву`
---
С JavaScript, полный массив может быть доступен путем обращения к имени массива:
```
script>
var cars = ["Saab", "Volvo", "BMW"];
document.getElementById("demo").innerHTML = cars;  //Saab,Volvo,BMw
</script>
```
`Массивы являются объектами`
---
Массивы - это особый тип объектов. typeofОператор в JavaScript возвращает «объект» для массивов.
* Объекты используют имена для доступа к своим «членам». В этом примере person.firstName возвращает John:
```

<script>
var person = {firstName:"John", lastName:"Doe", age:46};
document.getElementById("demo").innerHTML = person["firstName"];  //John
</script>
```
Элементы массива могут быть объектами
---

Переменные JavaScript могут быть объектами. Массивы - это особые виды объектов.

Из-за этого вы можете иметь переменные разных типов в одном массиве.

Вы можете иметь объекты в массиве. Вы можете иметь функции в массиве. Вы можете иметь массивы в массиве:
```
myArray[0] = Date.now;
myArray[1] = myFunction;
myArray[2] = myCars;
```
`Свойства и методы массива`
---
сила массивов JavaScript - это встроенные свойства и методы массива:
```
var x = cars.length;   // The length property returns the number of elements
var y = cars.sort();   // The sort() method sorts arrays
```
Свойство длины
---
`length`Свойство массива возвращает длину массива (количество элементов массива).
```
<script>
var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.length; //4
</script>
```
_Доступ к первому элементу массива_
```
<script>
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var first = fruits[0];
document.getElementById("demo").innerHTML = first;
</script>
```
_Доступ к последнему элементу массива_
```
<script>
var fruits = ["Banana", "Orange", "Apple", "Mango"];
var last = fruits[fruits.length-1];
document.getElementById("demo").innerHTML = last;  //Mango
</script>
```
Looping Array Elements(образование петель)
---
Самый безопасный способ перебрать массив - использовать `for` цикл:
```
<script>
var fruits, text, fLen, i;
fruits = ["Banana", "Orange", "Apple", "Mango"];
fLen = fruits.length;

text = "<ul>";
for (i = 0; i < fLen; i++) {
  text += "<li>" + fruits[i] + "</li>";
}
text += "</ul>";

document.getElementById("demo").innerHTML = text;  
</script>
```
вывод: (не нумерованный список)
```
* Banana
* Orange
* Apple
* Mango
```
Вы также можете использовать Array.forEach()функцию:
```
<script>
var fruits, text;
fruits = ["Banana", "Orange", "Apple", "Mango"];

text = "<ul>";
fruits.forEach(myFunction);
text += "</ul>";
document.getElementById("demo").innerHTML = text;

function myFunction(value) {
  text += "<li>" + value + "</li>";
} 
</script>
```

```
* Banana
* Orange
* Apple
* Mango
```
`Добавление элементов массива`
---
Самый простой способ добавить новый элемент в массив - использовать `push()` метод:
```
<script>
var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits;

function myFunction() {
  fruits.push("Lemon");
  document.getElementById("demo").innerHTML = fruits; //Banana,Orange,Apple,Mango,Lemon
}
</script>
```
# 
_Новый элемент также можно добавить в массив, используя `lengthсвойство`:_
```
<script>
var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits;

function myFunction() {
  fruits[fruits.length] = "Lemon";
  document.getElementById("demo").innerHTML = fruits;  //Banana,Orange,Apple,Mango,Lemon
}
</script>
```
# 

`Ассоциативные массивы`
---
Массивы с **именованными** индексами называются `ассоциативными` массивами **(или хэшами)**. JavaScript не поддерживает массивы с именованными индексами.

**В JavaScript массивы всегда используют пронумерованные индексы**
```
<script>
var person = [];
person[0] = "John";
person[1] = "Doe";
person[2] = 46; 
document.getElementById("demo").innerHTML =
person[0] + " " + person.length;              //John 3
</script>
```
---
// person.length will return 3
// person[0] will return "John"
# 
---
**Разница между массивами и объектами**
---
В JavaScript `массивы` используют _`пронумерованные индексы`_ .  

В JavaScript `объекты` используют _`именованные индексы`_ .
# 
# 
```
Массивы - это особый вид объектов с пронумерованными индексами.
```
**`Когда использовать массивы. Когда использовать объекты.`**
---
* JavaScript не поддерживает ассоциативные массивы.
* Вы должны использовать `объекты`, когда вы хотите, чтобы имена элементов были `строками` (текст) .
* Вы должны использовать `массивы`, когда хотите, чтобы имена элементов были `числами` .
Избегайте нового массива ()
---
Нет необходимости использовать встроенный в JavaScript конструктор newмассива Array ().
# 
**Используйте [ ] вместо этого.**
# 
Эти два разных оператора создают новый пустой массив с именем points:

**var points = new Array( );        // Bad**
**var points = [ ];                  // Good** 
 
 Эти два разных оператора создают новый массив, содержащий 6 чисел:
```
<script>
//var points = new Array(40, 100, 1, 5, 25, 10);  //bad
var points = [40, 100, 1, 5, 25, 10];             //good
document.getElementById("demo").innerHTML = points[0];  //40
</script>
```
**`Как распознать массив`**
---
Проблема в том, что оператор JavaScript `typeof`возвращает " _object"_:
```
<script>
var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = typeof fruits;  //object
</script>
```
# 
# 
* потому что _массив_ JavaScript является _объектом_.
 * **Для решения этой проблемы ECMAScript 5 определяет новый метод Array.isArray():**
```
<script>
var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = Array.isArray(fruits);  //true
</script>
```
# 
# 
* **Для решения этой проблемы вы можете создать свою собственную isArray()функцию:**


```
<script>
var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = isArray(fruits);

function isArray(myArray) {
  return myArray.constructor.toString().indexOf("Array") > -1; //true
}
</script>
```
Вышеприведенная функция всегда возвращает true, если аргумент является массивом.
# 
# 
* **`instanceof`Оператор возвращает истину , если объект создается с помощью данного конструктора:**
```
<script>
var fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits instanceof Array;                                               // true
</script>
```

