---
title: Даты  /  JavaScript Date Objects
date: 2020-04-13 18:35:46
---
JavaScript **Date Object** позволяет нам работать с датами:
# 
**JavaScript `new Date()`**
```
<script>
var d = new Date();
document.getElementById("demo").innerHTML = d;
</script>      //Tue Apr 14 2020 12:51:57 GMT+0300 (за східноєвропейським літнім часом)
```
---
# 
**Объекты Date создаются с помощью `new Date()` конструктора.**
# 
**4 способа** создания нового объекта даты:
# 
`new Date()`

---
`new Date(year, month, day, hours, minutes, seconds, milliseconds)`

---
`new Date(milliseconds)`

---
`new Date(date string)`

---
# 
`new Date()` создает новый объект даты с **текущей датой и временем** :

---
# 
`new Date(year, month, ...)`создает новый объект даты с **указанной датой и временем .**
```

<script>
var d = new Date(2018, 11, 24, 10, 33, 30, 0);
document.getElementById("demo").innerHTML = d;
</script>                                        //Mon Dec 24 2018 10:33:30 GMT+0200 (за східноєвропейським стандартним часом)
```
---
# 
`new Date(dateString)` создает новый объект датa **из строки даты :**
```
<script>
var d = new Date("October 13, 2014 11:13:00");
document.getElementById("demo").innerHTML = d;
</script>                                        //Mon Oct 13 2014 11:13:00 GMT+0300 (за східноєвропейським літнім часом)
```
---
# 
`new Date(milliseconds)` создает новый объект даты как **нулевое время плюс миллисекунды :**
```
<script>
var d = new Date(0);
document.getElementById("demo").innerHTML = d;
</script>

```
---
# 
Методы даты
---
Когда объект Date создается, ряд **методов** позволяет вам работать с ним.
# 
# 
Отображение дат
---
# 
JavaScript (по умолчанию) будет выводить даты в формате полнотекстовой строки:
# 
Когда вы отображаете объект даты в HTML, он автоматически преобразуется в строку с помощью `toString()`метода.
```
d = new Date();
document.getElementById("demo").innerHTML = d;
```

Такой же как:
```
d = new Date();
document.getElementById("demo").innerHTML = d.toString();  //Tue Apr 14 2020 14:35:07 GMT+0300 (за східноєвропейським літнім часом)
``` 
# 
`toUTCString()`Метод преобразует дату в строку UTC (стандартный дисплей даты).
```
var d = new Date();
document.getElementById("demo").innerHTML = d.toUTCString();   //Tue, 14 Apr 2020 11:36:13 GMT
```
# 
`toDateString()`Метод преобразует дату в более читаемый формат:
```
var d = new Date();
document.getElementById("demo").innerHTML = d.toDateString();       //Tue Apr 14 2020
``` 