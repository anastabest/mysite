---
title: Формат Даты  /
date: 2020-04-14 14:41:20
---
**JavaScript ввод даты**

есть **3 типа форматов** ввода даты в JavaScript:
# 
  ```
Дата ISO	       «2015-03-25» (Международный стандарт)    ISO Date	
---                ---                                      ---
Короткая дата	   "03/25/2015"                             Short Date 
---                ---                                      ---
Длинная дата	   «25 марта 2015» или «25 марта 2015»      Long Date
---                ---                                      ---
```
---
# 
# 
Ввод даты - даты разбора  _/Date Input - Parsing Dates_
---
 `Date.parse()` метод для ее преобразования в миллисекунды.
```
<p>Date.parse() returns the number of milliseconds between the date and January 1, 1970:</p>

<p id="demo"></p>

<script>
var msec = Date.parse("March 21, 2012");
document.getElementById("demo").innerHTML = msec;
</script>
```
# 
использовать количество миллисекунд, чтобы преобразовать его в объект даты :
```
<script>
var msec = Date.parse("March 21, 2012");
var d = new Date(msec);
document.getElementById("demo").innerHTML = d;
</script>

//Wed Mar 21 2012 00:00:00 GMT+0200 (за східноєвропейським стандартним часом)
```



