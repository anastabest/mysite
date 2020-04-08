---
title: FUNCTIONS JAVA SCRIPT
date: 2020-03-22 01:08:13
---


  **function** - это блок кода, предназначенный для выролнения  конкретной задачи. 
  _Выполняется_ **function** когда что-то ее вызывает. 

  Ключевое слово **function** может _использоваться для определения функции внутри выражения._
  Можно  _определять **функции** используя конструктор_ **Functiоn** и _объявление функции_.**(function declaration)** 
  
```
<script>
function myFunction(p1, p2) {
  return p1 * p2;
}
document.getElementById("demo").innerHTML = myFunction(4, 3);
</script>                                                      // 12

// В этом примере вызывается функция, которая выполняет вычисление 
   и    возвращает результат:
```

# Синтаксис функции JavaScript
**function** ключевое слово, потом следует **имя** , потом следуют **скобки ()** 

```
function name(parameter1, parameter2, parameter3) {
  // код для выполнения
}
```

 _Параметры функции_  указаны в скобках () в определении функции.

_Аргументы функции_ - это значения, полученные функцией при ее вызове.

# Вызов функции
*Код внутри функции* будет **выполняться** , когда «что-то» _вызывает (calls) функцию:_  **(invokes calls)**

* Когда происходит **событие** (когда пользователь _нажимает кнопку_)
* Когда он **вызывается (calls)** _из кода JavaScript_
* **Автоматически** (самостоятельно вызывается)

# Возврат функции  
**RETURN _оператора_**
Когда JavaScript _достигает return оператора, функция_**_прекращает выполнение._**

Если функция была вызвана из оператора, JavaScript «вернется» для выполнения кода после вызова оператора.

Функции часто вычисляют **возвращаемое значение** . Возвращаемое значение «возвращается» обратно «вызывающему»:

```
<script>
var x = myFunction(4, 3);
document.getElementById("demo").innerHTML = x;

function myFunction(a, b) {
  return a * b;
}
</script>        //12
```
можно `повторно использовать код`: определите код один раз и используйте его много раз, `с разными аргументами`, чтобы получить разные результаты.

```
<script>
function toCelsius(f) {
  return (5/9) * (f-32);
}
document.getElementById("demo").innerHTML = toCelsius(77);
</script>                                                 //25
```

**Оператор () вызывает функцию**
toCelsiusссылается на объект функции и toCelsius()ссылается на результат функции.

```
<script>
function toCelsius(f) {
  return (5/9) * (f-32);
}
document.getElementById("demo").innerHTML = toCelsius;
</script>                                      //function toCelsius(f) { return (5/9) * (f-32); }
```
**Функции, используемые в качестве переменных**
Функции можно использовать так же, как вы используете переменные, во всех типах формул, назначений и вычислений.

```
Вместо использования переменной для хранения возвращаемого значения функции:

var x = toCelsius(77);
var text = "The temperature is " + x + " Celsius";
Вы можете использовать функцию напрямую, как значение переменной:

var text = "The temperature is " + toCelsius(77) + " Celsius";
```


```
<script>
document.getElementById("demo").innerHTML =
"The temperature is " + toCelsius(77) + " Celsius";

function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
} 
</script>                    //The temperature is 25 Celsius
```

# `Локальные переменные`
Переменные, объявленные в функции JavaScript, становятся **ЛОКАЛЬНЫМИ** для этой функции.
Доступ к локальным переменным возможен только из функции.

```
// code here can NOT use carName

function myFunction() {
  var carName = "Volvo";
  // code here CAN use carName
}

// code here can NOT use carName
```
```
<script>
myFunction();

function myFunction() {
  var carName = "Volvo";
  document.getElementById("demo1").innerHTML =
  typeof carName + " " + carName;
}

document.getElementById("demo2").innerHTML =
typeof carName;                                    //string Volvo

                                                      //undefined
</script>
```
Локальные переменные создаются при запуске функции и удаляются при ее завершении.








