---
title: EVENTS
date: 2020-04-08 13:56:46
---

# События JavaScript
_______________________________________________________________
 Когда JavaScript используется на страницах HTML, JavaScript может `«реагировать»` на эти события.
__________________________________________________________________
# 
# 
# HTML события
HTML-событие может быть тем, что делает браузер, или тем, что делает пользователь.
_Несколько примеров событий HTML:_
* HTML-страница закончила загрузку
* Поле ввода HTML было изменено
* Была нажата кнопка HTML
# 
# 
В приведенном выше примере код JavaScript изменяет содержимое элемента с помощью id = "demo".
```
<button onclick="document.getElementById('demo').innerHTML=Date()">The time is?</button>
```
В следующем примере код изменяет содержимое своего собственного элемента (используя this.innerHTML):
```
<button onclick="this.innerHTML=Date()">The time is?</button>
```

### **`Чаще встречаются атрибуты событий, вызывающие функции:`**
```
<button onclick="displayDate()">The time is?</button>

<script>
function displayDate() {
  document.getElementById("demo").innerHTML = Date();
}
</script>         //Wed Apr 08 2020 14:48:30 GMT+0300 (за східноєвропейським літнім часом)
```
# 
# 
# 


Common HTML Events / Общие события HTML
---
**Events**

`<onchange>`         по изменению... HTML-элемент был изменен
`<onclick>`          по щелчку...	Пользователь щелкает элемент HTML
`<onmouseover>`      при наведении курсора на...  Пользователь наводит указатель мыши на элемент HTML
`<onmouseout>`     Пользователь наводит указатель мыши на элемент HTML
`<onKeyDown>`      Пользователь наводит указатель мыши на элемент HTML
`<onload>`         в процессе	Браузер завершил загрузку страницы
# 
# 

**Что может сделать JavaScript?**
Обработчики событий могут использоваться для обработки и проверки пользовательского ввода, действий пользователя и действий браузера:

* Что нужно делать каждый раз, когда загружается страница
* Что нужно сделать, когда страница закрыта
* Действие, которое должно быть выполнено, когда пользователь нажимает кнопку
* Контент, который должен быть проверен, когда пользователь вводит данные
* И более ...
---
Можно использовать много разных методов, чтобы JavaScript мог работать с событиями:

* Атрибуты событий HTML могут выполнять код JavaScript напрямую
* Атрибуты событий HTML могут вызывать функции JavaScript
* Вы можете назначить свои собственные функции обработчика событий элементам HTML
* Вы можете предотвратить отправку или обработку событий
* И более ...