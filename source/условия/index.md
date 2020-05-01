---
title: Условия
date: 2020-04-16 23:15:53
---

# 
JavaScript, если еще и еще, если     / JavaScript if else and else if
---

---
# 

Условные операторы используются для выполнения различных действий в зависимости от условий.
# 
---
Условные заявления
---
# 
Очень часто, когда вы пишете код, вы хотите выполнять разные действия для разных решений.
# 
Вы можете использовать условные операторы в своем коде, чтобы сделать это.
# 
В JavaScript у нас есть следующие условные выражения:
# 
- Используется ifдля указания блока кода, который должен быть выполнен, если указанное условие истинно
- Используйте elseдля указания блока кода, который будет выполнен, если то же условие ложно
- Используйте, else ifчтобы указать новое условие для проверки, если первое условие ложно
- Используйте switchдля указания множества альтернативных блоков кода, которые должны быть выполнены

---
Заявление `if`
---
Используйте ifоператор, чтобы указать блок кода JavaScript, который будет выполнен, если условие истинно.
# 
---
```
if (condition) {
  //  block of code to be executed if the condition is true
}
```
---
# 
Остальное заявление
---
Используйте `else` оператор, чтобы указать блок кода, который будет выполнен, если условие ложно.
```
if (condition) {
  //  block of code to be executed if the condition is true
} else {
  //  block of code to be executed if the condition is false
}
```
# 
---
# 
Если время меньше 18, создайте приветствие «Добрый день», иначе «Добрый вечер»:
```
if (hour < 18) {
  greeting = "Good day";
} else {
  greeting = "Good evening";
}
```
```
Результат приветствия будет:
Good evening
```

---
# 
Остальное, если заявление
---
Используйте `else if` оператор, чтобы указать новое условие, если первое условие ложно.
```
if (condition1) {
  //  block of code to be executed if condition1 is true
} else if (condition2) {
  //  block of code to be executed if the condition1 is false and condition2 is true
} else {
  //  block of code to be executed if the condition1 is false and condition2 is false
}
```
# 
_Если время меньше 10:00, создайте приветствие «Доброе утро», если нет, но время меньше 20:00, создайте приветствие «Добрый день», иначе «Добрый вечер»:_
# 
```
if (time < 10) {
  greeting = "Good morning";
} else if (time < 20) {
  greeting = "Good day";
} else {
  greeting = "Good evening";
}
```
```
Результат приветствия будет:

Good evening
```
