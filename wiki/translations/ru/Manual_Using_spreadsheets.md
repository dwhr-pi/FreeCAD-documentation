# Manual:Using spreadsheets/ru
<div class="mw-translate-fuzzy">





</div>


{{Manual:TOC/ru}}


<div class="mw-translate-fuzzy">

В FreeCAD есть ещё один интересный для изучения верстак:[Spreadsheet](Spreadsheet_Workbench/ru.md). Этот верстак позволяет создать [Электронную таблицу](https://ru.wikipedia.org/wiki/Электронная_таблица) вроде тех что делаются в [Excel](https://ru.wikipedia.org/wiki/Microsoft_Excel) или [LibreOffice](https://ru.wikipedia.org/wiki/OpenOffice_Calc) прямо в FreeCAD. Эти электронные таблицы затем могут быть наполнены данными, взятыми из вашей модели, и производить некоторые вычисления между значениями. Электронные таблицы могут быть экспортированы в файлы CSV, которые могут импортироваться в любые приложения электронных таблиц.


</div>

В FreeCAD электронные таблицы имеют дополнительную пользу: их ячейки могут получать имя, и после этого на них может ссылаться любое поле, поддерживаемое [механизмом выражений](Expressions.md). Это превращает электронные таблицы в мощные контрольные структуры, где значения в определённых ячейках могут управлять размерами модели. Только одно надо учесть, что FreeCAD запрещает круговые зависимости между объектами, таблица не может устанавливать параметр и в то же время получать значение от того же объекта. Это значит, что таблица и объект взаимно зависимы.

В следующем примере мы создадим пару объектов, получим некоторые их параметры в таблицу, затем используем таблицу для прямого управления параметрами других объектов.

### Чтение свойств 


<div class="mw-translate-fuzzy">

-   Начнём с переключения в [верстак Part](Part_Workbench/ru.md), и создадим несколько объектов: <img alt="" src=images/Part_Box.svg  style="width:16px;"> [куб](Part_Box/ru.md), <img alt="" src=images/Part_Cylinder.svg  style="width:16px;"> [цилиндр](Part_Cylinder/ru.md) и <img alt="" src=images/Part_Sphere.svg  style="width:16px;"> [сферу](Part_Sphere/ru.md).
-   Редактируем их параметр **Placement** (или используем инструмент <img alt="" src=images/Draft_Move.svg  style="width:16px;"> [Move](Draft_Move/ru.md)) чтобы поместить его немного в сторону, чтобы лучше видеть эффекты того, что мы будем делать:


</div>

![](images/Exercise_spreadsheet_01.jpg )

-   Теперь извлечём информацию из этих объектов. Переключимся в [верстак Spreadsheet](Spreadsheet_Workbench/ru.md)
-   Нажмём кнопку <img alt="" src=images/Spreadsheet_Create.png  style="width:16px;"> 
**New Spreadsheet**
-   Дважды кликнем новый объект Spreadsheet в древе проектов, откроется редактор таблиц:

![](images/Exercise_spreadsheet_02.jpg )

Редактор таблиц FreeCAD, хотя и не так закончен и мощен как вышеперечисленные более полные приложения электронных таблиц, всё же имеет большинство общеупотребительных базовых инструментов и функций, вроде возможности изменения оформления ячеек (размер, цвет, выключка), объединение и разбивка ячеек, использование формул вроде **=2+2** или ссылки на другие ячейки с **=B1**.

В FreeCAD поверх этих общих возможностей, есть новая интересная: возможность ссылаться не только на другие ячейки, но и другие объекты в документе, и взять значения из их параметров. Например, примем несколько параметров из трёх ранее созданных объектов. Параметры будут те, что мы видим в окне редактора параметров во вкладке **Data**, при выделении объекта.

-   Начнём с вводом текста в ячейки A1, A2 и A3, чтобы мы запомнили что есть что на будущее, например, **Cube Length**, **Cylinder Radius** и **Sphere Radius**. Для ввода текста просто напишите в поле \"Содержание\" над таблицей, или сделайте двойной клик по ячейке.
-   Теперь получим фактическое значение длины куба. В ячейке B1 напишем **=Куб.Length**. Вы увидите, что таблица имеет механизм автозаполнения, тот же самый, что и в редакторе выражений, использованный в предыдущей главе.
-   Повторим то же для ячеек B2 (**=Цилиндр.Radius**) and B3 (**=Сфера.Radius**).

![](images/Exercise_spreadsheet_03.jpg )

-   Хотя это ожидаемо, значения могут обрабатываться как любые числа, попробуйте, например, ввести в ячейку C1: **=B1\*2**.
-   Теперь мы можем изменить одно из этих значений в редакторе параметров, и изменения немедленно отразятся в таблице. Например, изменим длину куба на **20mm**:

![](images/Exercise_spreadsheet_04.jpg )

Страница [верстака Spreadsheet](Spreadsheet_Workbench/ru.md) покажет подробности о всех возможных операциях и функциях, которые доступны в таблице.

### Запись свойств 

Другое интересное использование верстака Spreadsheet в FreeCAD противоположно тому, что мы делали: вместо чтения значений параметров трёхмерных объектов мы можем назначать им значения. Помните, тем не менее, одно из базовых правил FreeCAD: запрет круговых зависимостей. Поэтому мы не можем использовать ту же таблицу для чтения **и** записи значений в трёхмерный объект. Это может сделать объект зависимым от таблицы, которая будет зависеть от объекта. Вместо этого нам надо сделать другую таблицу.

-   Теперь закроем вкладку таблицы (в трёхмерном окне). Это не обязательно, можно и оставить несколько таблиц открытыми.
-   Нажмём снова кнопку <img alt="" src=images/Spreadsheet_Create.png  style="width:16px;"> 
**New Spreadsheet**
-   Изменим имя новой таблицы на что-то более содержательное, вроде **Ввод** (это делается правым кликом на новой таблице и выбором **Переименовать**).
-   Откроем редактор таблиц двойным кликом по таблице **Ввод**.
-   В ячейке A1 поместим описание, например: \"Размеры Куба\"
-   В ячейке B1 напишем **=5mm** (использование знака \"=\" гарантирует, что значение будет понято как величина, а не текст).
-   Теперь, чтобы использовать это значение за пределами таблицы, надо дать имя ячейке B1 псевдоним. Сделаем правый клик на ячейке, нажмём **Свойства** и выделим вкладку **Псевдоним**. Дадим имя, например, **cubedims**:

![](images/Exercise_spreadsheet_05.jpg )

-   Нажмём **OK** и закроем вкладку таблицы
-   Выделим куб
-   В редакторе параметров кликнем маленькую иконку <img alt="" src=images/Bound-expression-unset.png  style="width:16px;"> **expression** справа от поля **Length**. Это откроет [редактор выражений](Expressions/ru.md), где мы сможем написать **Spreadsheet001.cubedims**. Повторим это для Height и Width:

![](images/Exercise_spreadsheet_06.jpg )

Вы можете удивиться, почему нам понадобилось использовать в выражении \"Spreadsheet001\" вместо \"Ввод\". Это потому, что каждый объект в документе FreeCAD имеет **внутреннее имя**, уникальное для документа, и **метку**, видимую в древе проекта. Если Вы снимите соответствующую опцию в настройках, FreeCAD позволит давать одноименные метки для разных объектов. Поэтому все операции, которые должны однозначно идентифицировать объекты, используют внутренние имена вместо меток, которые могут обозначать разные объекты. Проще всего узнать внутренние имена объектов оставлять открытой панель **просмотр выделения** (меню Вид-\>Панели), она всегда показывает внутреннее имя выбранного объекта:

![](images/Exercise_spreadsheet_07.jpg )

Используя в таблицах псевдонимы ячеек мы можем использовать таблицы для хранения \"основных значений\" в документах FreeCAD. Это может использоваться, например, для моделей различных размеров, сохраняя эти размеры в таблице. Становится лёгким создавать другие модели с различными размерами, просто открыв файл и изменив набор размеров в таблице.

В итоге заметьте, что ограничения внутри эскизов так же могут получать значения из табличных ячеек:

![](images/Exercise_spreadsheet_08.jpg )

Так же можно создать псевдонимы для размерных ограничений (горизонтальных, вертикальных или по расстояниям) в эскизах (которые так же можно использовать за пределами эскизов)

![](images/Exercise_spreadsheet_09.jpg )

**Загрузки**

-   Файл, полученный в этом примере: <https://github.com/yorikvanhavre/FreeCAD-manual/blob/master/files/spreadsheet.FCStd>

**Читать далее**

-   [Верстак Spreadsheet](Spreadsheet_Workbench/ru.md)
-   [Использование выражений в параметрах](Expressions/ru.md)


<div class="mw-translate-fuzzy">





</div>



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Tutorials](Category_Tutorials.md) > Manual:Using spreadsheets/ru
