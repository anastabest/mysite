---
title:  метод  getElementById().

date: 2020-02-28 11:47:26
---
# _Java Script_ ## Скриптовый язык
Скриптова мова (англ. scripting language) — мова програмування, розроблена для запису «сценаріїв», послідовностей операцій, які користувач може виконувати на комп'ютері.


Динамі́чна мо́ва!
Динамі́чна мо́ва дозволяє визначати типи даних і здійснювати синтаксичний аналіз і компіляцію «на льоту», безпосередньо на етапі виконання.



## Метод JavaScript HTML является getElementById().


- Метод используется для «поиска» HTML-элемента (с id = «demo») и изменения элемента content ( innerHTML) на «Hello JavaScript»

   ## пример

        <p id="demo">JavaScript can change HTML content.</p>

        <button type="button" onclick='document.getElementById("demo").innerHTML = "Hello JavaScript!"'>Click Me!</button>


- при нажатии кнопки меняется текст;


**Атрибуты**
* Все элементы HTML могут иметь **атрибуты**
*  **Атрибуты** предоставляют _дополнительную информацию об элементе_
* **Атрибуты** всегда _указываются_ в начальном теге
* **Атрибуты** обычно входят в _пары имя / значение,_ такие как: **name = "value"**

**Атрибут** `href`   `<a href="https://www.w3schools.com">This is a link</a>`
**Атрибут** `src`    `<img src="img_girl.jpg">`
**Атрибут** `width` и `height`  `<img src="img_girl.jpg" width="500" height="600">` 
**Атрибут** `alt`   `<img src="img_girl.jpg" alt="Girl with a jacket">`
**Атрибут** `style`  `<p style="color:red">This is a red paragraph.</p>`
 `style`  Атрибут используется для указания стиля элемента, как цвет, шрифт, размер и т.д
**Атрибут заголовка** `title`

```
<p title="I'm a tooltip">
Mouse over this paragraph, to display the title attribute as a tooltip.
</p>
```


**Атрибут** `lang`

```  
<!DOCTYPE html>
<html lang="en-US">
<body>

...

</body>
</html>    
```
**Вложенные элементы HTML** 
Элементы HTML могут быть вложенными (элементы могут содержать элементы).

Все документы HTML состоят из вложенных элементов HTML.

Этот пример содержит четыре элемента HTML:

```
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

# JavaScript может изменять значения атрибутов HTML
        <button onclick="document.getElementById('myImage').src='pic_bulbon.gif'">Turn on the light</button>

        <img id="myImage" src="pic_bulboff.gif" style="width:100px">

        <button onclick="document.getElementById('myImage').src='pic_bulboff.gif'">Turn off the light</button>

* В этом примере JavaScript изменяет значение src атрибута (source) <img>тега:
# Изменение стиля элемента HTML - это вариант изменения атрибута HTML
        <p id="demo">JavaScript can change the style of an HTML element.</p>

        <button type="button" onclick="document.getElementById('demo').style.fontSize='35px'">Click Me!</button>

# Может скрывать элементы
        <button type="button" onclick="document.getElementById('demo').style.display='none'">Click Me!</button>



# Может отображать элементы
        <p>JavaScript can show hidden HTML elements.</p>

        <p id="demo" style="display:none">Hello JavaScript!</p>

        <button type="button" onclick="document.getElementById('demo').style.display='block'">Click Me!</button>
