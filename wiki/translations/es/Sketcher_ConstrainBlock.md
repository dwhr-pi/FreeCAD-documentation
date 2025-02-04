---
- GuiCommand:/es
   Name:Sketcher ConstrainBlock
   Name/es:Croquizador RestringirBloque
   MenuLocation:Croquis → Restricciones de croquis → Restringir Bloque
   Workbenches:[Croquizador](Sketcher_Workbench/es.md)
   SeeAlso:[Restringir Lock](Sketcher_ConstrainLock/es.md)
   Version:0.17
---

# Sketcher ConstrainBlock/es


</div>

## Descripción

**Constrain Block** blocks a geometric element in place with a single constraint.

It is mainly intended to be used with **[<img src=images/Sketcher_CreateBSpline.svg style="width:16px"> [B-Splines](Sketcher_CreateBSpline.md)**, which can be difficult to fully constrain otherwise.


<div class="mw-translate-fuzzy">

## Utilización


</div>

1.  Select an element to constrain.
2.  Press the **[<img src=images/Sketcher_ConstrainBlock.svg style="width:16px"> [Constrain Block](Sketcher_ConstrainBlock.md)** button.

Or press the button first, and then select the elements.

## Scripting


```pythonSketch.addConstraint(Sketcher.Constraint('Block', Edge))```

The [Sketcher scripting](Sketcher_scripting.md) page explains the values which can be used for `Edge` and contains further examples on how to create constraints from Python scripts.





{{Sketcher Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Sketcher](Sketcher_Workbench.md) > Sketcher ConstrainBlock/es
