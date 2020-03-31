---
title: Data Types
date: 2020-03-31 12:32:03
---
## Переменные JavaScript : числа, строки, объекты и многое другое:

      var length = 16;                               // Number
      var lastName = "Johnson";                      // String
      var x = {firstName:"John", lastName:"Doe"};    // Object

## Объекты могут быть очищены путем установки значения в NULL.

      <script>
      var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
      person = null;
      document.getElementById("demo").innerHTML = typeof person;
      </script>                                                   // object

### Концепция:
--- При добавлении числа и строки JavaScript будет обрабатывать число как строку
_________________

      <script>
      var x = 16 + "Volvo";
      document.getElementById("demo").innerHTML = x;
      </script>                                      
                                                      // 16Volvo
---                                                     
      <script>
      var x = "Volvo" + 16;
      document.getElementById("demo").innerHTML = x;
      </script>                                       // Volvo16                            
------JavaScript оценивает выражения слева направо. Разные последовательности могут давать разные результаты:

       <script>
       var x = 16 + 4 + "Volvo";
       document.getElementById("demo").innerHTML = x;
       </script>  
                                           // 20Volvo
----------------------
       <script>
       var x = "Volvo" + 16 + 4;
       document.getElementById("demo").innerHTML = x;
       </script>                                         // Volvo164

# Типы JavaScript являются динамическими
------------------------------------------------------
_одна и та же переменная может **использоваться для хранения разных типов данных:**_

       <script>
       var x;         // Now x is undefined
       x = 5;         // Now x is a Number
       x = "John";      // Now x is a String

       document.getElementById("demo").innerHTML = x;
       </script>

# Строки JavaScript

Строка (или текстовая строка) - это серия символов

       <script>
       var carName1 = "Volvo XC60";           // Using double quotes
       var carName2 = 'Volvo XC60';           // Using single quotes

       document.getElementById("demo").innerHTML =
       carName1 + "<br>" + 
       carName2; 
       </script>                                  // Volvo XC60
                                                  // Volvo XC60 
* 
 JavaScript имеет только один тип чисел.
* 
 Числа могут быть записаны с десятичными знаками или без них

# JavaScript Booleans
Логические значения могут иметь только два значения: 
true или false.                                              
``` 
<script>
var x = 5; 
var y = 5;                                      // Returns true                                           
var z = 6;                                       // Returns false
document.getElementById("demo").innerHTML =
(x == y) + "<br>" + (x == z);
</script> 
```