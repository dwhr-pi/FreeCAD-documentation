---
- GuiCommand:/ru
   Name/ru:Добавить осевую линию между 2 линиями
   Name:TechDraw_2LineCenterLine
   MenuLocation:TechDraw → Добавить Линии → Добавить осевую линию между 2 линиями
   Workbenches:[TechDraw](TechDraw_Workbench/ru.md)
   Version:0.19
   SeeAlso:[Добавить осевую линию к Граням](TechDraw_FaceCenterLine/ru.md), [Добавить осевую линию между 2 точками](TechDraw_2PointCenterLine/ru.md)
---

# TechDraw 2LineCenterLine/ru

## Описание

The 2LineCenterLine tool adds a centerline between two Edges.

<img alt="" src=images/CL2LinesSample.png  style="width:350px;">



*Aligned centerline between 2 Edges*

## Применение

1.  Select 2 Edges in a View. The Edges should be more or less parallel.
2.  Press the **<img src="images/TechDraw_2LineCenterLine.svg" width=16px> Add Centerline between 2 Lines** button
3.  A dialog will open where you can specify attributes of the new centerline.
4.  A centerline will be added between the 2 selected Edges.**If the generated line looks odd or didn\'t generate at all, you may need to use the option** [**Flip Ends**](#Flip_Ends.md).

To delete a Centerline, select it and use the toolbar button **<img src="images/TechDraw_CosmeticEraser.svg" width=16px> [Remove Cosmetic Object](TechDraw_CosmeticEraser.md)**.

## Editing Centerlines 

Any of the centerline command buttons ( **<img src="images/TechDraw_FaceCenterLine.svg" width=16px> [Add Centerline to Face(s)](TechDraw_FaceCenterLine.md)**, **<img src="images/TechDraw_2LineCenterLine.svg" width=16px> Add Centerline between 2 Lines**, **<img src="images/TechDraw_2PointCenterLine.svg" width=16px> [Add Centerline between 2 Points](TechDraw_2PointCenterLine.md)**) can be used to edit any centerline.

1.  Select a centerline.
2.  Press any centerline command button.
3.  A dialog will open where you can change attributes of the centerline.
4.  Press **OK** to see your changes.

## Свойства

Centerlines have no properties of their own, as they are no document objects. They have attributes that can be edited via the dialog.

-   **Orientation**:
    -   **Vertical**: Forces a centerline vertical
    -   **Horizontal**: Forces a centerline horizontal
    -   **Aligned**: Follows the general direction of the Edge for 2 Edge centerline
-   **Shift Horizontal**: Moves the centerline left or right of its normal position
-   **Shift Vertical**: Moves the centerline up or down from its normal position
-   **Rotate**: Rotates the centerline around its center (degrees. + counterclockwise, - clockwise)
-   **Extend By**: Makes the centerline longer by this amount
-   **Color**: Color of centerline
-   **Weight**: Thickness of the centerline
-   **Style**: <img alt="" src=images/Continuous-line.svg  style="width:20px;"> Continuous, <img alt="" src=images/Dash-line.svg  style="width:20px;"> Dash, <img alt="" src=images/Dot-line.svg  style="width:20px;"> Dot, <img alt="" src=images/DashDot-line.svg  style="width:20px;"> DashDot, <img alt="" src=images/DashDotDot-line.svg  style="width:20px;"> DashDotDot
-   **Flip Ends**: Flips endpoints for creation as described below. (attribute removed for FreeCAD 0.20)

## Flip Ends 

<img alt="Sketch how the centerline is constructed" src=images/TD-CenterLineFlip.png  style="width:350px;"> The centerline between 2 lines is drawn between the midpoints (m0 and m1) of the lines that connects the endpoints of the selected lines (p0 and p1), see the sketch. Depending on the point order there are 2 possibilities to draw the connecting lines. The attribute **Flip Ends** flips the way the connecting lines are drawn. In FreeCAD 0.20 the point order is automatically determined so that the **Flip Ends** attribute is no longer necessary.

## Программирование


**См. так же:**

[TechDraw API](TechDraw_API/ru.md) и [Основы составления скриптов FreeCAD](FreeCAD_Scripting_Basics/ru.md).

Centerlines are not accessible from [macros](Macros.md) or the [Python](Python.md) console at this time.





{{TechDraw Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [TechDraw](TechDraw_Workbench.md) > TechDraw 2LineCenterLine/ru
