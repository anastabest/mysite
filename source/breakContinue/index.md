---
title: Break Continue
date: 2020-04-29 07:55:15
---

----
`break` Заявление «выпрыгивает» из цикла.

`continue` Утверждение «перепрыгивает» на одну итерацию в цикле.

---
#
Оператор `break `также может быть использован для выхода из цикла.  
`break `Оператор разрывает петлю и продолжает выполнение кода после цикла (если таковые имеются):

```
<p>A loop with a <b>break</b> statement.</p>

<p id="demo"></p>

<script>
var text = "";
var i;
for (i = 0; i < 10; i++) {
  if (i === 3) { break; }
  text += "The number is " + i + "<br>";
}
document.getElementById("demo").innerHTML = text;
</script>
```
```
//JavaScript Loops
//A loop with a break statement.

//The number is 0
//The number is 1
//The number is 2

```

Продолжить заявление
---

`continue `Заявление ломается одна итерация (в цикле), если происходит определенное условие, и продолжается со следующей итерации цикла.


```
<p>A loop with a <b>continue</b> statement.</p>

<p>A loop which will skip the step where i = 3.</p>

<p id="demo"></p>

<script>
var text = "";
var i;
for (i = 0; i < 10; i++) {
  if (i === 3) { continue; }
  text += "The number is " + i + "<br>";
}
document.getElementById("demo").innerHTML = text;
</script>
```
```
Цикл с оператором continue.

Цикл, который пропустит шаг, где i = 3.
The number is 0
The number is 1
The number is 2
The number is 4
The number is 5
The number is 6
The number is 7
The number is 8
The number is 9
```



---
# JavaScript-метки
Чтобы пометить операторы JavaScript, перед оператором нужно указать имя метки и двоеточие:
label:
statements
---
# 
Чтобы пометить операторы JavaScript, перед оператором нужно указать имя метки и двоеточие:

_label:_
_statements_


**break labelname;**

**continue labelname;**

 

# 
`continue` Утверждение (с или без ссылки этикетки) могут быть использованы только **пропустить одну итерацию цикла** .



Оператор `breakбез` ссылки на метку может быть использован только для **выхода из цикла или переключателя** .


Со ссылкой этикетки, заявление перерыва может быть использовано , чтобы **выскочить из любого блока кода** :

```
<h2>JavaScript break</h2>

<p id="demo"></p>

<script>
var cars = ["BMW", "Volvo", "Saab", "Ford"];
var text = "";

list: {
  text += cars[0] + "<br>"; 
  text += cars[1] + "<br>"; 
  break list;
  text += cars[2] + "<br>"; 
  text += cars[3] + "<br>"; 
}

document.getElementById("demo").innerHTML = text;
</script>
```
```
JavaScript break
BMW
Volvo
```
---
**`*Блок кода - это блок кода между {и}.*`**


---
