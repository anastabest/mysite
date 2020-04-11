---
title: STRINGS
date: 2020-04-08 15:47:33
---
# Строки JavaScript
---
* Строки JavaScript используются для хранения и манипулирования текстом. 
--- 
* Строка JavaScript содержит ноль или более символов, заключенных в кавычки.
---
```
var carName1 = "Volvo XC60";  // Double quotes
var carName2 = 'Volvo XC60';  // Single quotes
```
# Длина строки
* Чтобы найти длину строки, используйте встроенное lengthсвойство:
```
<script>
var txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
document.getElementById("demo").innerHTML = txt.length;
</script>
```

* Последовательность \"  вставляет двойную кавычку в строку:
```
<script>                                                                //Экранирующая последовательность \ "вставляет двойную кавычку в строку.
var x = "We are the so-called \"Vikings\" from the north.";             //Мы так называемые "викинги" с севера.
document.getElementById("demo").innerHTML = x; 
</script>
```
* Последовательность \'  вставляет одиночную кавычку в строку:
```
<script>
var x = 'It\'s alright.';
document.getElementById("demo").innerHTML = x;    //It's alright.
</script>
```
* Последовательность \\  вставляет в строку обратную косую черту:
```
<script>
var x = "The character \\ is called backslash.";
document.getElementById("demo").innerHTML = x;  //The character \ is called backslash.
</script>
```

             

* Шесть других escape-последовательностей допустимы в JavaScript
---
\b   	Backspace
возврат на одну позицию
---
\f	    Form Feed
Подача формы
---
\n	    New Line
Новая линия
---
\r	Carriage Return
Возврат каретки
---
\t	Horizontal Tabulator
Горизонтальный табулятор
---
\v	Vertical Tabulator
Вертикальный табулятор
---
# 
# 
# Прерывание длинных строк кода
* Если оператор JavaScript не помещается в одну строку, лучше всего его разбить после оператора:
```
<script>
document.getElementById("demo").innerHTML =
"Hello Dolly!";
</script>
```
* Вы также можете разбить строку кода внутри текстовой строки с помощью одной обратной косой черты:
```
<script>
document.getElementById("demo").innerHTML = "Hello \
Dolly!";
</script>
```

# 
# 
# Строки могут быть объектами
---
* Обычно строки JavaScript являются примитивными значениями, созданными из литералов:

var firstName = "John";
---
* Но строки также могут быть определены как объекты с ключевым словом new:

var firstName = new String("John");
---
```
<script>
var x = "John";        // x is a string
var y = new String("John");  // y is an object

document.getElementById("demo").innerHTML =
typeof x + "<br>" + typeof y;              
</script>                                  
```

---
* При использовании ==оператора равные строки равны:
```
<script>
var x = "John";        // x is a string
var y = new String("John");  // y is an object
document.getElementById("demo").innerHTML = (x==y);
</script>
```

* При использовании ===оператора одинаковые строки не равны, поскольку ===оператор ожидает равенства как по типу, так и по значению.
```
<script>
var x = "John";        // x is a string
var y = new String("John");  // y is an object
document.getElementById("demo").innerHTML = (x===y);  //false
</script>
```

`Обратите внимание на разницу между (x==y)и (x===y).`
`Сравнение двух объектов JavaScript всегда вернет false`






