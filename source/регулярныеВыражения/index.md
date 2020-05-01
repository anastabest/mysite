---
title: Регулярные Выражения
date: 2020-04-30 14:35:27
---

Регулярные выражения JavaScript
---

---
Регулярное выражение - это последовательность символов, образующая шаблон поиска.

Шаблон поиска можно использовать для операций поиска текста и замены текста.

---
Что такое регулярное выражение?
---
Регулярное выражение - это последовательность символов, образующая шаблон поиска .

Когда вы ищете данные в тексте, вы можете использовать этот шаблон поиска для описания того, что вы ищете.

Регулярное выражение может быть одним символом или более сложным шаблоном.

Регулярные выражения могут использоваться для выполнения всех типов операций текстового поиска и замены текста .

Синтаксис
---
```
/pattern/modifiers;
```
# 
ПРИМЕР:
```
var patt = /w3schools/i;
```
*Пример объяснил*

**/ w3schools / i**   - это регулярное выражение.

**w3schools**  - это шаблон (для поиска).

**i**  является модификатором (модифицирует поиск, чтобы быть нечувствительным к регистру).

---
Использование строковых методов
---
В JavaScript регулярные выражения часто используются с двумя **строковыми методами :** `search()и replace().`

`search()` Метод использует выражение для поиска соответствия, и возвращает позицию матча.

`replace()` Метод возвращает модифицированную строку , в которой заменяется шаблон.

---
# 
# 

Использование поиска по `search ()` со строкой /Using String search() With a String
---
В `search()` методе ищет строку для указанного значения и возвращает позицию матча:
```
<script>
var str = "Visit W3Schools!"; 
var n = str.search("W3Schools");
document.getElementById("demo").innerHTML = n;  // 6
</script>
```
---

Использование поиска `search ()` с регулярным выражением   /Using String search() With a Regular Expression
---
спользуйте регулярное выражение, чтобы выполнить поиск "w3schools" без учета регистра в строке:
```
var str = "Visit W3Schools";
var n = str.search(/w3schools/i);   // 6
```
---





---
Использование String `replace ()` Строкой
---
`replace() `Метод заменяет указанное значение с другим значением в строке:
```
<script>
function myFunction() {
  var str = document.getElementById("demo").innerHTML; 
  var txt = str.replace("Microsoft","W3Schools");
  document.getElementById("demo").innerHTML = txt;
}
</script>
```
результат:
```

Replace "Microsoft" with "W3Schools" in the paragraph below:

Try it
Please visit W3Schools!
```
---
Используйте String `replace ()` с регулярным выражением
---
Используйте регулярное выражение без учета регистра, чтобы заменить Microsoft на W3Schools в строке:

```
<button onclick="myFunction()">Try it</button>

<p id="demo">Please visit Microsoft and Microsoft!</p>

<script>
function myFunction() {
  var str = document.getElementById("demo").innerHTML; 
  var txt = str.replace(/microsoft/i,"W3Schools");
  document.getElementById("demo").innerHTML = txt;
}
</script>
```
//(https://www.w3schools.com/js/tryit.asp?filename=tryjs_regexp_string_replace)

---
# 
# 
# 

---
```
Аргументы регулярного выражения (вместо строковых аргументов) могут быть использованы в методах выше.

Регулярные выражения могут сделать ваш поиск намного более мощным (например, без учета регистра).
```

---
Модификаторы регулярных выражений
---
**Модификаторы** можно использовать для выполнения глобальных поисков без учета регистра:

**i**	Выполнить сопоставление без учета регистра  (Perform case-insensitive matching)
```
<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
function myFunction() {
  var str = "Visit W3Schools";
  var patt1 = /w3schools/i;
  var result = str.match(patt1); 
  document.getElementById("demo").innerHTML = result;      // W3Schools
}
</script>
```
**g**	 Выполнить глобальное совпадение (найти все совпадения, а не останавливаться после первого совпадения)         
         (Perform a global match (find all matches rather than stopping after the first match) )
```
<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
function myFunction() {
  var str = "Is this all there is?";
  var patt1 = /is/g;
  var result = str.match(patt1);
  document.getElementById("demo").innerHTML = result;  // is,is
}
</script>
```         
**m**	Выполнить многострочное сопоставление  (Perform multiline matching)
```
<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
function myFunction() {
  var str = "\nIs th\nis it?";
  var patt1 = /^is/m;
  var result = str.match(patt1);
  document.getElementById("demo").innerHTML = result;   // is
}
</script>
```
---
Шаблоны регулярных выражений
---
_Скобки_ используются для поиска диапазона символов:
[abc]	  Найдите любой символ в скобках (Find any of the characters between the brackets)	
[0-9]	 Найдите любую из цифр в скобках  (Find any of the digits between the brackets)	
(x|y)	 Найдите любую из цифр в скобках  (Find any of the alternatives separated with |)

---
_Метасимволы_ - это символы с особым значением:
---
**\d**	найти цифру (Find a digit)	

---
**\s**	 найти пробел (Find a whitespace character)

---
**\b**	 Найдите совпадение в начале слова, подобного этому: \ bWORD, или в конце слова, подобного этому: WORD \ b(Find a match at the beginning of a word like this:    \bWORD, or at the end of a word like this: WORD\b)

---
**\uxxxx**  Найти символ Unicode, указанный шестнадцатеричным числом xxxx	(Find the Unicode character specified by the hexadecimal number xxxx)

---
Квантификаторы определяют количества:
---
**n+** Соответствует любой строке, которая содержит хотя бы один n	(Matches any string that contains at least one n)

---
**n***	Соответствует любой строке, которая содержит ноль или более вхождений n (Matches any string that contains zero or more occurrences of n)

---
**n?**  Соответствует любой строке, которая содержит ноль или одно вхождение n	(Matches any string that contains zero or one occurrences of n)

---

Использование объекта RegExp
---
В JavaScript объект RegExp является объектом регулярного выражения с предопределенными свойствами и методами.

---
Использование `test ()`
---
` test()` Способ представляет собой способ выражения RegExp.

Он ищет строку для шаблона и возвращает true или false, в зависимости от результата.

В следующем примере выполняется поиск строки для символа «e»:
```
<p>Search for an "e" in the next paragraph:</p>

<p id="p01">The best things in life are free!</p>

<p id="demo"></p>

<script>
text = document.getElementById("p01").innerHTML; 
document.getElementById("demo").innerHTML = /e/.test(text);  // true
</script>
```

---
Использование `exec ()`
---
`exec()` Способ представляет собой способ выражения RegExp.

Он ищет строку для указанного шаблона и возвращает найденный текст как объект.

Если совпадений не найдено, возвращается пустой _(нулевой)_ объект.

В следующем примере выполняется поиск строки для символа «e»:
```
<script>
var obj = /e/.exec("The best things in life are free!");
document.getElementById("demo").innerHTML =
"Found " + obj[0] + " in position " + obj.index + " in the text: " + obj.input;
</script>

// Found e in position 2 in the text: The best things in life are free!
```
