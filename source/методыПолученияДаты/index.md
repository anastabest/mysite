---
title: Методы Получения Даты
date: 2020-04-15 13:49:01
---
# 
**Эти методы могут использоваться для получения информации от объекта даты:**
```
getFullYear()	Get the year as a four digit number (yyyy)
```
# 
```
getMonth()	Get the month as a number (0-11)
```
# 
```
getDate()	Get the day as a number (1-31)
```
# 
```
getHours()	Get the hour (0-23)
```
# 
```
getMinutes()	Get the minute (0-59)
```
# 
```
getSeconds()	Get the second (0-59)
```
# 
```
getMilliseconds()	Get the millisecond (0-999)
```
# 
```
getTime()	Get the time (milliseconds since January 1, 1970)
```
# 
```
getDay()	Get the weekday as a number (0-6)
```
# 
```
Date.now()	Get the time. ECMAScript 5.
```
# 
# 
Метод getTime () /The getTime() Method
---
`getTime() `Метод возвращает количество миллисекунд , прошедших с 1 января 1970 года:
```
<script>
var d = new Date();
document.getElementById("demo").innerHTML = d.getTime();
</script>

//Функция getTime () возвращает количество миллисекунд с  January 1, 1970.: 1586948352476
```
# 
Метод getFullYear ()
---
`getFullYear()` Метод возвращает год даты как четырехзначный номер:

# 
Метод getMonth ()
--- 
`getMonth()` Метод возвращает месяц даты в виде числа (0-11):
# 
**Вы можете использовать массив имен и ` getMonth()` вернуть месяц как имя:**
```
<script>
var d = new Date();
var months = ["January","February","March","April","May","June","July","August","September","October","November","December"];
document.getElementById("demo").innerHTML = months[d.getMonth()];
</script>
```
# 
Метод getDate ()
---
` getDate()` Метод возвращает день даты в виде числа (1-31):
# 
Метод getHours ()
---
` getHours()` Метод возвращает часы даты как число (0-23):
# 
Метод getMinutes ()
---
` getMinutes()` Метод возвращает протокол даты как число (0-59):
# 
Mетод getSeconds ()
---
 `getSeconds() `Метод возвращает секунды даты как число (0-59):
 # 

Метод getMilliseconds ()
---
`getMilliseconds()` Метод возвращает миллисекунды дату как число (0-999): 
# 
Метод getDay ()
---
 `getDay() `Метод возвращает день недели даты в виде числа (0-6):
 # 
**Вы можете использовать массив имен и getDay()вернуть день недели как имя:**
```
<script>
var d = new Date();
var days = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"];
document.getElementById("demo").innerHTML = days[d.getDay()];
</script>
```
Методы даты UTC
---
Методы даты UTC используются для работы с датами UTC (даты универсального часового пояса):
```
getUTCDate()	
     Same as getDate(), but returns the UTC date
```

```
getUTCDay()
	Same as getDay(), but returns the UTC day
```

```
getUTCFullYear()
	Same as getFullYear(), but returns the UTC year
```

```
getUTCHours()
     Same as getHours(), but returns the UTC hour
```

```
getUTCMilliseconds()
	Same as getMilliseconds(), but returns the UTC milliseconds
```

```
getUTCMinutes()
	Same as getMinutes(), but returns the UTC minutes
```

```
getUTCMonth()
	Same as getMonth(), but returns the UTC month
```

```
getUTCSeconds()
	Same as getSeconds(), but returns the UTC seconds
```


