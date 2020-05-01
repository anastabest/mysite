---
title: Сравнения
date: 2020-04-16 14:05:43
---

Сравнение JavaScript и логические операторы
---

---

Сравнение и Логические операторы используются для проверки ` true` или ` false` .

---
Операторы сравнения
---
# 
Операторы сравнения используются в логических выражениях для определения равенства или разницы между переменными или значениями.
# 
Учитывая это x = 5, таблица ниже объясняет операторы сравнения:

---
`==`	equal to   равно

---
`===`	equal value and equal type      === равное значение и равный тип

---
`!=`	not equal

---
`!==`	not equal value or not equal type

---
`>`	greater than   > больше чем

---
`<`	less than

---
`>=`	greater than or equal to

---
`<=`	less than or equal to	

---
# 
# 
# 
# 
---
Как это можно использовать
---
Операторы сравнения могут использоваться в условных выражениях для сравнения значений и выполнения действий в зависимости от результата:
```
if (age < 18) text = "Too young";
```
# 
---
# 
Логические Операторы
---
Логические операторы используются для определения логики между переменными или значениями.
# 
Учитывая это x = 6 и y = 3, таблица ниже объясняет логические операторы:
# 
---
# 
`&&`	and  	(x < 10 && y > 1)   is true
# 
---
# 
`||`	or	   (x == 5 || y == 5)      is false
# 
---
# 
`!`	not	   !(x == y)   is true
# 
---
# 
Условный (троичный) оператор  /(Conditional (Ternary) Operator)
---
JavaScript также содержит условный оператор, который присваивает значение переменной на основе некоторого условия.
# 
---
variablename = (condition) ? value1:value2 
# 
---
```
<p>Input your age and click the button:</p>

<input id="age" value="18" />  больше чем

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
function myFunction() {
  var age, voteable;
  age = document.getElementById("age").value;
  voteable = (age < 18) ? "Too young":"Old enough";
  document.getElementById("demo").innerHTML = voteable + " to vote.";
}
</script>
```
 
---
# 
Сравнение разных типов
---
# 
Сравнение данных разных типов может дать неожиданные результаты.
# 
При сравнении строки с числом JavaScript преобразует строку в число при сравнении. Пустая строка преобразуется в 0. Нечисловая строка преобразуется в `NaN `всегда `false`.
# 
больше примеров : (https://www.w3schools.com/js/js_comparisons.asp)

---
# 
При сравнении двух строк «2» будет больше «12», потому что (в алфавитном порядке) 1 меньше 2.
# 
Чтобы обеспечить правильный результат, переменные должны быть преобразованы в правильный тип перед сравнением:
```
<h2>JavaScript Comparisons</h2>

<p>Input your age and click the button:</p>

<input id="age" value="18" />

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
function myFunction() {
  var age, voteable;
  age = Number(document.getElementById("age").value);
  if (isNaN(age)) {
    voteable = "Input is not a number";
  } else {
    voteable = (age < 18) ? "Too young" : "Old enough";
  }
  document.getElementById("demo").innerHTML = voteable;
}
</script>
```