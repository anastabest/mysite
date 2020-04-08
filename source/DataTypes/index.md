---
title: Data Types   Типы Данных
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

# Массивы JavaScript
Массивы JavaScript написаны в квадратных скобках.
Элементы массива разделяются запятыми.

      <script>
      var cars = ["Saab","Volvo","BMW"];

      document.getElementById("demo").innerHTML = cars[0];
      </script>                                             // Saab

_**Индексы массива начинаются с нуля, что означает, что первым элементом является [0].**_

# JavaScript объекты
Объекты JavaScript пишутся с помощью фигурных скобок {}.

Свойства объекта записываются в виде пар имя: значение, разделенных запятыми.
```
<script>
var person = {
firstName : "John",
lastName  : "Doe",
age     : 50,
eyeColor  : "blue"
};
document.getElementById("demo").innerHTML =
person.firstName + " is " + person.age + " years old.";    // John is 50 years old.
</script>
```   


# Тип оператора

**typeof Оператор**

### возвращает тип переменной или выражением: 

      <script>s
      document.getElementById("demo").innerHTML = 
      typeof "" + "<br>" +                             
      typeof "John" + "<br>" +                string                                          
      typeof "John Doe";                               //Returnsstring   
      </script>                                        //Returns string
                                                       //Returns string
# 
      <script>
      document.getElementById("demo").innerHTML =       
      typeof 0 + "<br>" +                               //number 
      typeof 314 + "<br>" +                             //number
      typeof 3.14 + "<br>" +                            //number
      typeof (3) + "<br>" +                             //number
      typeof (3 + 4);                                   //number
      </script>

# Значение **UNDEFINED**  typeof **undefined**

В JavaScript переменная без значения имеет:

* _значение_ **undefined**. Тип тоже undefined.
       <script>
        var car;
        document.getElementById("demo").innerHTML =
        car + "<br>" + typeof car;                     // undefined
        </script>                                      // undefined
* Любую переменную можно очистить, установив значение в **undefined**. Тип тоже будет undefined.

# Значение **NULL**   typeof **object**
В JavaScript _null это «ничего»_. Что-то, чего не существует.
typeof **null** является **объектом**

### **очистить _объект_,**  установив его в **null**


       <script>
       var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
       person = null;                                       
       document.getElementById("demo").innerHTML = typeof person;
       </script>                                               // object
       
**undefined** и **null** _равны_ по значению, но _различаются_ по типу






###  **очистить _объект_**, установив его в **undefined**
       <script>
       var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
       person = undefined;
       document.getElementById("demo").innerHTML = person;
       </script>                                          // undefined

# 

        typeof undefined           // undefined
        typeof null                // object

        null === undefined         // false
        null == undefined          // true

## **Примитивное _значение данных_** 
 - это одно простое значение данных *без дополнительных свойств и методов.*

**typeof** _oператор возвращает  один из этих примитивных типов:_

 * string
 * number
 * boolean
 * undefined
# 
       <script>
       document.getElementById("demo").innerHTML = 
       typeof "john" + "<br>" +                     // string
       typeof 3.14 + "<br>" +                       // number   
       typeof true + "<br>" +                       // boolean 
       typeof false + "<br>" +                      // boolean
       typeof x;                                    // undefined 
       </script>
#  

# Комплексные данные **Complex Data** (returns)
**typeof** *oператор* может *возвращать* одно из двух сложных типов:

* function
* object
# 

**typeof** *возвращает* оператор «объект» для *объектов, массивов, и нуля.*

**typeof** оператор *не возвращает* «объект» *для функций.*



       <script>
       document.getElementById("demo").innerHTML = 
       typeof {name:'john', age:34} + "<br>" +       // object
       typeof [1,2,3,4] + "<br>" +                   // object
       typeof null + "<br>" +                        // object
       typeof function myFunc(){};                   // function 
       </script>
       