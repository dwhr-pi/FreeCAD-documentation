---
- GuiCommand:/ru
   Name:Part Helix
   Name/ru:Винтовая Спираль
   MenuLocation:Деталь → [Создать примитивы...](Part_Primitives/ru.md) → Спираль
   Workbenches:[Part(Деталь)](Part_Workbench/ru.md),  [OpenSCAD](OpenSCAD_Workbench/ru.md)
   SeeAlso:[Примитивы](Part_Primitives/ru.md)
---

# Part Helix/ru


</div>

## Описание


**[<img src=images/Part_Helix.svg style="width:16px"> [Спираль](Part_Helix/ru.md)**

создаёт геометрический примитив в форме спирали, которая задаётся радиусом, шагом и общей высотой.

Обычно винтовая спираль используется для [создания резьб](Thread_for_Screw_Tutorial/ru.md) в сочетании с закрытым профилем и операцией **<img src="images/Part_Sweep.svg" width=16px> [Развёртка(Sweep)](Part_Sweep/ru.md)** детали. Этот процесс работает практически так же как и в [верстаке PartDesign ](PartDesign_Workbench/ru.md) с помощью инструмента **[<img src=images/PartDesign_AdditivePipe.svg style="width:16px"> [PartDesign Аддитивная(добавочная) труба](PartDesign_AdditivePipe/ru.md)**.

## Применение


<div class="mw-translate-fuzzy">

1.  Переключитесь на <img alt="" src=images/Workbench_Part.svg  style="width:24px;"> [верстак Part](Part_Workbench/ru.md).
2.  Диалог Создания Примитивов доступен несколькими способами:
    -   Нажмите на кнопку **[<img src=images/Part_Primitives.svg style="width:16px"> [Примитивы](Part_Primitives/ru.md)** на панели команд Деталь.
    -   Используйте меню **Деталь → [<img src=images/Part_Primitives.svg style="width:16px"> [Создать примитивы...](Part_Primitives/ru.md) → Спираль(Helix)**


</div>

![](images/PartHelixPrimitivesOptions_en.png )

#### Параметры


<div class="mw-translate-fuzzy">

-    {{Parameter|Шаг(Pitch):}}Шаг соответствует промежутку между двумя последовательными \"витками\" спирали, измеренным вдоль главной оси спирали.

-    {{Parameter|Высота(Height):}}Высота соответствует общей высоте спирали, измеренной вдоль главной оси спирали.

-    {{Parameter|Радиус(Radius):}}Радиус соответствует радиусу круга, построенного спиралью при взгляде на спираль сверху или снизу.

-    {{Parameter|Угол(Angle)}}: По умолчанию спираль построена на воображаемом цилиндре. С помощью этой опции можно построить спираль на воображаемом конусе. Этот угол соответствует углу конуса. Значение должно находиться в диапазоне от 0 до +90 градусов.

-    {{Parameter|Лево или Правозаходная(Right-handed or Left-handed):}}Этот параметр указывает [направление захода](https://en.wikipedia.org/wiki/Screw_thread) спирали.


</div>

#### Размещение

-    {{Parameter|X:}}Основная ось спирали будет перемещена по оси X на значение, которое вы укажите в этом поле.

-    {{Parameter|Y:}}Основная ось спирали будет перемещена по оси Y на значение, которое вы укажите в этом поле.

-    {{Parameter|Z:}}Основная ось спирали будет перемещена по оси Z на значение, которое вы укажите в этом поле.

-    {{Parameter|Направление(Direction):}}По умолчанию главной осью спирали является ось Z. Здесь у вас есть возможность редактировать главную ось спирали. Если вы выберете параметр \"определяется пользователем (user defined) \...\", вам будет предложено указать главную ось спирали, введя координаты ее вектора.

-    {{Parameter|3D Вид(View):}}позволяет выбрать центр в 3D-виде.

## Опции

### Свойства

После создания спирали у вас есть возможность редактировать её параметры.

+++
| ![](images/PartHelixProperty_en.png ) | Параметры в этом меню аналогичны описанным выше.                                               |
|                                                          | **Основание(Base)**                                                          |
|                                                          | \* {{Parameter|Размещение(Placement):}} позволяет перемещать или вращать спираль |
|                                                          |                                                                                                |
|                                                          | -                                                                               |
|                                                          |     {{Parameter|Angle:}}                                                                       |
|                                                          |                                                                                             |
+++



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Part](Part_Workbench.md) > Part Helix/ru
