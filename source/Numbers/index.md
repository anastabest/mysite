---
title: Numbers
date: 2020-04-09 10:55:06
---
NaN - не число
---
NaN является зарезервированным словом JavaScript, указывающим, что число не является допустимым числом.

Попытка сделать арифметику с нечисловой строкой приведет к NaN(не число):
```
<script>
document.getElementById("demo").innerHTML = 100 / "Apple";    //// x will be NaN (Not a Number)
</script>
```

Однако, если строка содержит числовое значение, результатом будет число

* Вы можете использовать глобальную функцию JavaScript, isNaN()чтобы узнать, является ли значение числом:
```
<script>
var x = 100 / "Apple";
document.getElementById("demo").innerHTML = isNaN(x); //true
</script>
```
* Берегись NaN. Если вы используете NaNв математической операции, результат также будет NaN:

---
* Или результатом может быть конкатенация:
```
<script>
var x = NaN;
var y = "5";
document.getElementById("demo").innerHTML = x + y;    //NaN5
</script>
```
* `NaN` это число: `typeof` NaN возвращает number:
```
<script>
var x = NaN;
document.getElementById("demo").innerHTML = typeof x;   //number
</script>
```
# 
# 

# Бесконечность  Infinity
`Infinity`(или `-Infinity`) - это значение, которое JavaScript вернет, если вы вычислите число за пределами максимально возможного числа.
```
<script>
var myNumber = 2; 
var txt = "";
while (myNumber != Infinity) {
   myNumber = myNumber * myNumber;
   txt = txt + myNumber + "<br>";
}
document.getElementById("demo").innerHTML = txt;
</script>
```

//
```
4
16
256
65536
4294967296
18446744073709552000
3.402823669209385e+38
1.157920892373162e+77
1.3407807929942597e+154
Infinity
```
# 
* `Infinity` это число: `typeof Infinity` возвращает number.

# Числа могут быть объектами
