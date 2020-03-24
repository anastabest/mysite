---
title: Js Statements
date: 2020-03-23 06:12:43
---
#  **Statements** (операторы)
        <script>
        var x, y, z;    // Statement 1
        x = 5;          // Statement 2
        y = 6;          // Statement 3
        z = x + y;      // Statement 4
        document.getElementById("demo").innerHTML =
        "The value of z is " + z + ".";  
        </script>

Программа на  JavaScript - список **операторов**- инструкций.

# Заявления 
Операторы JavaScript состоят из:
* Значения
* операторы
* выражения
* ключевые слова 
* комментарии

Это утверждение говорит браузеру написать «Hello Dolly». внутри элемента HTML с id = "demo"

       <p id="demo"></p>

        <script>
        document.getElementById("demo").innerHTML= "Hello Dolly."; // JS получает доступ к элементу HTML, через метод **inerr.HTML****
        </script>


# Блоки кода   в function(){...}
Операторы кода группируются в **блоки кода  {...}** внутри фигурных скобок.
Блоки кода групируют операторы , которые выполняются вместе.
*сгруппированные по блокам, в функциях JavaScript:
        function myFunction() {
          document.getElementById("demo1").innerHTML = "Hello Dolly!";  //используем два пробела для кода; 
          document.getElementById("demo2").innerHTML = "How are you?";
          }




