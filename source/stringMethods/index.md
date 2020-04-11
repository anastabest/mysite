---
title: STRING METHODS 
date: 2020-04-08 17:40:05
---
# Строковые методы JavaScript
---
**Строковые методы помогают вам работать со строками**

---
# Поиск строки в строке
Два метода, 
`indexOf()` и
 `search()`, равны?

* Они принимают одинаковые аргументы (параметры) и возвращают одно и то же значение?

Два метода НЕ равны. Это различия:

* search()Метод не может принимать второй аргумент позиции начала.
---
* indexOf()Метод не может принимать мощные значения поиска (регулярные выражения).
---
# Извлечение string частей
3 метода для извлечения части строки:
* `slice(start, end)`
* `substring(start, end)`
* `substr(start, length)`
---
# The slice() Method
```
<script>
var str = "Apple, Banana, Kiwi";
var res = str.slice(7,13);
document.getElementById("demo").innerHTML = res;  //Banana
</script>
```
slice() извлекает часть строки и возвращает извлеченную часть в новой строке.

Метод принимает 2 параметра: начальную позицию и конечную позицию (конечная позиция не включена).

---
```
Помните: JavaScript считает позиции с нуля. Первая позиция 0.
```
---
Если вы опустите второй параметр, метод будет вырезать остальную часть строки:
```
<script>
var str = "Apple, Banana, Kiwi";
var res = str.slice(7);
document.getElementById("demo").innerHTML = res; //Banana, Kiwi
</script>
```
# 
считая с конца:
```
<script>
var str = "Apple, Banana, Kiwi";
var res = str.slice(-12) 
document.getElementById("demo").innerHTML = res;  ////Banana, Kiwi
</script>
```
----
Метод подстроки ()
---
`substring()` похоже на `slice()`.

Разница в том, что `substring()` нельзя принимать отрицательные показатели.

---
Метод `substr ()`
---
`substr()` похоже на `slice().`
Разница в том, что второй параметр указывает **длину** извлеченной части.
```
<script>
var str = "Apple, Banana, Kiwi";
var res = str.substr(7,6);
document.getElementById("demo").innerHTML = res; //Banana
</script>
```
Метод substr () извлекает часть строки и возвращает извлеченные части в новой строке.
# 
Если вы пропустите второй параметр, substr()будет вырезана остальная часть строки.
```
<script>
var str = "Apple, Banana, Kiwi";
var res = str.substr(7);
document.getElementById("demo").innerHTML = res;  //Banana,Kiwi
</script>
```
# 
Если первый параметр отрицателен, позиция отсчитывается от конца строки.
```
<script>
var str = "Apple, Banana, Kiwi";
var res = str.substr(-4);
document.getElementById("demo").innerHTML = res;  //Kiwi
</script>
```

# Замена содержимого строки
`replace()` Метод заменяет указанное значение с другим значением в строке

```
<!DOCTYPE html>
<html>
<body>
<h2>JavaScript String Methods</h2>
<p>Replace "Microsoft" with "W3Schools" in the paragraph below:</p>
<button onclick="myFunction()">Try it</button>
<p id="demo">Please visit Microsoft!</p>
<script>
function myFunction() {
  var str = document.getElementById("demo").innerHTML; 
  var txt = str.replace("Microsoft","W3Schools");
  document.getElementById("demo").innerHTML = txt;
}
</script>
</body>
</html>                
```  
По умолчанию `replace()` метод заменяет **только первое** совпадение.

# Метод concat ()
`concat()` объединяет две или более строки:

<script>
var text1 = "Hello";
var text2 = "World!";
var text3 = text1.concat(" ",text2);
document.getElementById("demo").innerHTML = text3;  //Hello World!
</script>

`concat()` Метод может быть использован вместо оператора плюс. Эти две строки делают то же самое:

var text = "Hello" + " " + "World!";
var text = "Hello".concat(" ", "World!");

---

# String.trim ()
`trim()` метод удаляет пробельные символы с обеих сторон строки:
# 
# 
Извлечение строковых символов
---
* `charAt(position) `
* `charCodeAt(position)`
* `Property access [ ]`
---
# 
# 
Метод charAt ()
---
`charAt()` Метод возвращает символ по указанному индексу (позиции) в строке:


      <script>
      var str = "HELLO WORLD";
      document.getElementById("demo").innerHTML = str.charAt(0); //return H;
      </script>
---

`Преобразование строки в массив`
---
`split()` метода  может  преобразовать строку в массив

      <button onclick="myFunction()">Try it</button>

      <p id="demo"></p>

       <script>
       function myFunction() {
       var str = "a,b,c,d,e,f";
       var arr = str.split(",");
       document.getElementById("demo").innerHTML = arr[0];       //a
     }
     </script>

      


