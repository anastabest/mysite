---
title:  методов  getElementById().

date: 2020-02-28 11:47:26
---
## Методов JavaScript HTML является getElementById().


- Метод используется для «поиска» HTML-элемента (с id = «demo») и изменения элемента content ( innerHTML) на «Hello JavaScript»

  * ## пример

        <p id="demo">JavaScript can change HTML content.</p>

        <button type="button" onclick='document.getElementById("demo").innerHTML = "Hello JavaScript!"'>Click Me!</button>


- при нажатии кнопки меняется текст;

# JavaScript может изменять значения атрибутов HTML
        <button onclick="document.getElementById('myImage').src='pic_bulbon.gif'">Turn on the light</button>

        <img id="myImage" src="pic_bulboff.gif" style="width:100px">

        <button onclick="document.getElementById('myImage').src='pic_bulboff.gif'">Turn off the light</button>

-- В этом примере JavaScript изменяет значение src атрибута (source) <img>тега:
# Изменение стиля элемента HTML - это вариант изменения атрибута HTML
        <p id="demo">JavaScript can change the style of an HTML element.</p>

        <button type="button" onclick="document.getElementById('demo').style.fontSize='35px'">Click Me!</button>

# Может скрывать элементы
        <button type="button" onclick="document.getElementById('demo').style.display='none'">Click Me!</button>

        

# Может отображать элементы
        <p>JavaScript can show hidden HTML elements.</p>

        <p id="demo" style="display:none">Hello JavaScript!</p>

        <button type="button" onclick="document.getElementById('demo').style.display='block'">Click Me!</button>
