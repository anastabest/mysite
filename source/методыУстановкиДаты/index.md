---
title: Методы Установки Даты в JavaScript
date: 2020-04-15 14:23:41
---
Методы `Set Date` позволяют устанавливать значения даты (годы, месяцы, дни, часы, минуты, секунды, миллисекунды) для объекта Date.
Методы установки даты
---

Методы `Set Date` используются для установки части даты:
```
setDate()	Set the day as a number (1-31)
```

```
setFullYear()	Set the year (optionally month and day)
```

```
setHours()	Set the hour (0-23)
```

```
setMilliseconds()	Set the milliseconds (0-999)
```

```
setMinutes()	Set the minutes (0-59)
```

```
setMonth()	Set the month (0-11)
```

```
setSeconds()	Set the seconds (0-59)
```

```
setTime()	Set the time (milliseconds since January 1, 1970)
```
# 
Метод setFullYear ()
---
`setFullYear()` Метод устанавливает год объекта даты. В этом примере до 2020 года:
```
<script>
var d = new Date();
d.setFullYear(2021);
document.getElementById("demo").innerHTML = d;   //Fri Apr 16 2021 12:04:46 GMT+0300 (за східноєвропейським літнім часом)
</script>
```
`setFullYear()` Метод может при **необходимости** установить месяц и день:
```
script>
var d = new Date();
d.setFullYear(2020, 11, 3);
document.getElementById("demo").innerHTML = d; //Thu Dec 03 2020 12:06:01 GMT+0200 (за східноєвропейським стандартним часом)
</script>
```

Метод setMonth ()
---
`setMonth() ` Метод устанавливает месяц даты объекта (0-11):
```
<script>
var d = new Date();
d.setMonth(11);
document.getElementById("demo").innerHTML = d;   //Wed Dec 16 2020 12:07:22 GMT+0200 (за східноєвропейським стандартним часом)
</script>
```
Метод setDate ()
---
`setDate()`  Метод устанавливает день даты объекта (1-31):
```
<script>
var d = new Date();
d.setDate(15);
document.getElementById("demo").innerHTML = d;//Wed Apr 15 2020 12:14:42 GMT+0300 (за східноєвропейським літнім часом)
</script>
```
# 
# 
Этот `setDate()` метод также можно использовать для _добавления дней к дате_:
```
<script>
var d = new Date();
d.setDate(d.getDate() + 50); 
document.getElementById("demo").innerHTML = d;   //Fri Jun 05 2020 12:13:09 GMT+0300 (за східноєвропейським літнім часом)
</script>
```
---

Метод setHours ()
---
`setHours() ` Метод устанавливает часы даты объекта (0-23):
```
<script>
var d = new Date();
d.setHours(22);
document.getElementById("demo").innerHTML = d; //Thu Apr 16 2020 22:15:37 GMT+0300 (за східноєвропейським літнім часом)
</script>
```
# 
Метод setMinutes ()
---
` setMinutes()` Метод устанавливает протокол дату объекта (0-59):
```
<script>
var d = new Date();
d.setMinutes(30);
document.getElementById("demo").innerHTML = d;  //Thu Apr 16 2020 12:30:50 GMT+0300 (за східноєвропейським літнім часом)
</script>
```
---
Метод setSeconds ()
---
` setSeconds()` Метод задает секунды даты объекта (0-59):
```
<script>
var d = new Date();
d.setSeconds(30);
document.getElementById("demo").innerHTML = d;  //Thu Apr 16 2020 12:17:30 GMT+0300 (за східноєвропейським літнім часом)
</script>
```
---
# 
# 
**Сравнить даты**
---
Даты можно легко сравнить.
# 

В следующем примере сравнивается сегодняшняя дата с 14 января 2100 года:
```
<script>
var today, someday, text;
today = new Date();
someday = new Date();
someday.setFullYear(2100, 0, 14);

if (someday > today) {
  text = "Today is before January 14, 2100.";
} else {
  text = "Today is after January 14, 2100.";
}
document.getElementById("demo").innerHTML = text;  //Today is before January 14, 2100.
</script>
```
---
