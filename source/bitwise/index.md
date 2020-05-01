---
title: Bitwise
date: 2020-04-30 11:59:12
---
Побитовые операции JavaScript
---

---
Битовые операторы JavaScript
---
**Operator	Name	Description**

& ____ (AND) ___ Sets each bit to 1 if both bits are 1
Устанавливает каждый бит в 1, если оба бита равны 1

---
| __ (OR) ___ Sets each bit to 1 if one of two bits is 1
Устанавливает каждый бит в 1, если один из двух битов равен 1

---
^  ___ (XOR) ___ Sets each bit to 1 if only one of two bits is 1
Устанавливает каждый бит в 1, если только один из двух битов равен 1

---
~ ___  (NOT) ___ Inverts all the bits
Инвертирует все биты

---
<< ___(Zero fill left shift) ___	Shifts left by pushing zeros in from the right and let the leftmost bits fall off
 Сдвиг влево, нажав нули справа, и пусть самые левые биты падают

---
>>___(Signed right shift)__ Shifts right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off
Сдвиг влево, толкая нули справа и оставляя самые левые биты

---

JavaScript побитовое И (&)
---
Побитовое И возвращает 1, только если оба бита равны 1:
```

<script>
document.getElementById("demo").innerHTML = 5 & 1;         //1
</script>            
```

---

JavaScript Побитовое ИЛИ (|)
---
```
<script>
document.getElementById("demo").innerHTML = 5 | 1; //5
</script>

```
---
JavaScript побитовый XOR (^)
---
Побитовый XOR возвращает 1, если биты разные:
```

<script>
document.getElementById("demo").innerHTML = 5 ^ 1; //4
</script>
```


---
JavaScript побитовый НЕ (~)
---
```
script>
document.getElementById("demo").innerHTML = ~ 5;  //-6
</script>
```
---
JavaScript (нулевое заполнение) битовое смещение влево (<<)
---
Это смещение нуля влево. Один или несколько нулевых битов вставляются справа, и самые левые биты падают:
```
<script>
document.getElementById("demo").innerHTML = 5 << 1;   //10
</script>

```
---
JavaScript (сохранение знака) Битовый сдвиг вправо (>>)
---
Это знак сохранения правого сдвига. Копии самого левого бита вставляются слева, а самые правые биты падают:
```
<script>
document.getElementById("demo").innerHTML = -5 >> 1;  //-3
</script>

```
---
JavaScript (нулевая заливка) вправо Shift (>>>)
---
Это смещение нуля вправо. Один или несколько нулевых битов вводятся слева, а самые правые биты падают:
```
<script>
document.getElementById("demo").innerHTML = 5 >>> 1;   //2
</script>
```
---
Преобразование десятичного числа в двоичное
---
```

<script>
document.getElementById("demo").innerHTML = dec2bin(-5);        //11111111111111111111111111111011
function dec2bin(dec){
  return (dec >>> 0).toString(2);
}
</script>
```
---
Преобразование двоичного в десятичное
---
```
<script>
document.getElementById("demo").innerHTML = bin2dec(101);   //5
function bin2dec(bin){
  return parseInt(bin, 2).toString(10);
}
</script>
```
---
