---
- GuiCommand:/de
   Name:Draft Arc 3Points
   Name/de:Entwurf Bogen 3Punkte
   MenuLocation:Entwurf → Bogen 3 Punkte
   Workbenches:[Entwurf](Draft_Workbench/de.md), [Arch](Arch_Workbench/de.md)
   Shortcut:**A** **T**
   Version:0.19
   SeeAlso:[Entwurf Bogen](Draft_Arc/de.md), [Entwurf Kreis](Draft_Circle/de.md), [Entwurf Ellipse](Draft_Ellipse/de.md)
---

# Draft Arc 3Points/de


</div>

## Beschreibung


<div class="mw-translate-fuzzy">

Das Werkzeug **<img src="images/Draft_Arc_3Points.svg" width=16px> [Arc 3Points](Draft_Arc_3Points/de.md)** erzeugt einen Bogen in der aktuellen [Arbeitsebene](Draft_SelectPlane/de.md), durch Eingabe von drei Punkten, die auf dem Umfang liegen; aus diesen drei Punkten werden Mittelpunkt und Radius bestimmt. Es verwendet das [Entwurf Linienstil](Draft_Linestyle/de.md) , das auf dem [Entwurf Tray](Draft_Tray/de.md) gesetzt ist.


</div>

A Draft Arc is in fact a [Draft Circle](Draft_Circle.md) with a **First Angle** that is not the same as its **Last Angle**.

<img alt="" src=images/Draft_Arc_3Points_example.png  style="width:400px;">


<div class="mw-translate-fuzzy">



*Bogen definiert durch drei Punkte, die auf einem Umfang liegen*


</div>

## Anwendung

See also: [Draft Tray](Draft_Tray.md), [Draft Snap](Draft_Snap.md) and [Draft Constrain](Draft_Constrain.md).


<div class="mw-translate-fuzzy">

1.  Drücke die Taste **<img src="images/Draft_Arc_3Points.svg" width=16px> [Draft Arc 3Points](Draft_Arc_3Points/de.md)** Taste, oder drücke **A** dann **T** Tasten.
2.  Klicke auf einen ersten Punkt in der 3D-Ansicht, oder gib eine Koordinate and press the **<img src="images/Draft_AddPoint.svg" width=16px> Punkt hinzufügen** Taste.
3.  Klicke auf einen zweiten Punkt in der 3D-Ansicht, oder gib eine Koordinate und drücke die **<img src="images/Draft_AddPoint.svg" width=16px> Punkt hinzufügen** Taste.
4.  Klicke auf einen dritten Punkt in der 3D-Ansicht, oder gib eine Koordinate und drücke die **<img src="images/Draft_AddPoint.svg" width=16px> Punkt hinzufügen** Taste.
5.  Der Bogen wird erstellt, nachdem der dritte Punkt angegeben wurde.


</div>

## Optionen

The single character keyboard shortcuts available in the task panel can be changed. See [Draft Preferences](Draft_Preferences.md). The shortcuts mentioned here are the default shortcuts.

-   To manually enter coordinates enter the X, Y and Z component, and press **Enter** after each. Or you can press the **<img src="images/Draft_AddPoint.svg" width=16px> Enter point** button when you have the desired values. It is advisable to move the pointer out of the [3D view](3D_view.md) before entering coordinates.
-   Press **R** or click the **Relative** checkbox to toggle relative mode. If relative mode is on, coordinates are relative to the last point, if available, else they are relative to the coordinate system origin.
-   Press **G** or click the **Global** checkbox to toggle global mode. If global mode is on, coordinates are relative to the global coordinate system, else they are relative to the [working plane](Draft_SelectPlane.md) coordinate system. <small>(v0.20)</small> 
-   Press **T** or click the **Continue** checkbox to toggle continue mode. If continue mode is on, the command will restart after finishing, allowing you to continue creating arcs. <small>(v0.20)</small> 
-   Press **S** to switch [Draft snapping](Draft_Snap.md) on or off.
-   Press **Esc** or the **Close** button to abort the command.

## Notes

-   A Draft Arc can be edited with the [Draft Edit](Draft_Edit.md) command.

## Preferences

See also: [Preferences Editor](Preferences_Editor.md) and [Draft Preferences](Draft_Preferences.md).

-   To change the number of decimals used for the input of coordinates: **Edit → Preferences... → General → Units → Units settings → Number of decimals**.
-   If the **Edit → Preferences... → Draft → General settings → Draft tools options → Use Part Primitives when available** option is checked, the command will create a non-editable [Part Feature](Part_Feature.md) instead of a Draft Circle.

## Eigenschaften


<div class="mw-translate-fuzzy">

Ein Bogenobjekt teilt sich alle Eigenschaften von einem [Entwurf Kreis](Draft_Circle/de.md), aber einige Eigenschaften sind nur für den Kreis sinnvoll. Weitere Informationen unter [ Entwurf Bogen](Draft_Arc/de.md).


</div>

## Skriptsteuerung

See also: [Autogenerated API documentation](https://freecad.github.io/SourceDoc/) and [FreeCAD Scripting Basics](FreeCAD_Scripting_Basics.md).

To create a Draft Arc by 3 points use the `make_arc_3points` method of the Draft module:


```python
arc = make_arc_3points(points, placement=None, face=False, support=None, map_mode="Deactivated", primitive=False)
```

-   Creates an `arc` object from the given `points` list.
-   If a `placement` is given, the center of the circular arc will be moved to this place. See [Placement](Placement.md) for more information.
-   If `face` is `True`, the arc will make a face, that is, it will appear filled.
-   If `support` is given, it is a `LinkSubList`, that is, a list indicating an object and a subelement of that object. This is used so that the object appears referenced to this support.

:   For example: support=[(obj, ("Face1"))].

-   If `map_mode` is given, it is a string defining a type of mapping, for example: map_mode='FlatFace', map_mode='ThreePointsPlane', etc. See [Part EditAttachment](Part_EditAttachment.md) for more information.
-   If `primitive` is `True`, the arc created will be a simple [Part Feature](Part_Feature.md), not a complex Draft object.

Beispiel:


```python
import FreeCAD as App
import Draft

doc = App.newDocument()

points = [App.Vector(0, 0, 0),
          App.Vector(5, 10, 0),
          App.Vector(10, 0, 0)]

arc = Draft.make_arc_3points(points)

doc.recompute()
```


<div class="mw-translate-fuzzy">





</div>



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Draft](Draft_Workbench.md) > Draft Arc 3Points/de
