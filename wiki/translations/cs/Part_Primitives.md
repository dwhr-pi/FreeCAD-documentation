# Part Primitives/cs
---
- GuiCommand:/cs   Name:Part_CreatePrimitives   Name/cs:Díl Vytváření základních geometrických tvarů   MenuLocation:Díl -> Díl Vytváření zákl.geom.tvarů   |Workbenches:[SeeAlso:[[Part_Shapebuilder/cs|Díl Skládání tvarů](Part_Workbench/cs___díl]].md)---


</div>

## Description


<div class="mw-translate-fuzzy">

Nástroj pro vytváření různých parametrických geometrických tvarů,


</div>

<img alt="" src=images/Part_Primitives_example.png  style="width:800px;"> 
*Primitive shapes that can be created with the [Part Workbench](Part_Workbench.md).*

## Usage

To create a primitive, either

\#\* press the **<img src="images/Part_Primitives.svg" width=24px> '''Create primitives'''** button in the toolbar.

\#\* select the **Part → Create primitives...** from the menu bar.

1.  In the appearing dialog select primitive type, set its parameters and location, finally press **Create**

The dialog keeps open so that you can subsequently create further primitives.

To edit a primitives there are 2 ways:

Using the dialog: <small>(v0.19)</small> 

1.  Select the primitive in the tree and double-click on it.
2.  The same dialog will open that was also used to create the primitive. Change there the parameters and you get a live preview of the changed primitive.
3.  To finish the editing press **OK**.

Using the [property editor](Property_editor.md):

1.  Select the primitive in the tree.
2.  Edits its properties in the Properties table.


<div class="mw-translate-fuzzy">

-   V současnosti může tento nástroj parametricky vytvářet
    -   [Rovinu](Part_Plane/cs.md)
    -   [Box](Part_Box/cs.md)
    -   [Válec](Part_Cylinder/cs.md)
    -   [Kužel](Part_Cone/cs.md)
    -   [Kouli](Part_Sphere/cs.md)
    -   [Elipsoid](Part_Ellipsoid/cs.md)
    -   [Torus (vypadá jako nafouknutá duše z kola)](Part_Torus/cs.md)
    -   [Hranol](Part_Prism/cs.md) <small>(v0.14)</small> \*:
    -   [Klín](Part_Wedge/cs.md)
    -   [Šroubovice](Part_Helix/cs.md)
    -   [Spirála](Part_Spiral/cs.md) <small>(v0.14)</small> \*:
    -   [Kružnice](Part_Circle/cs.md)
    -   [Elipsa](Part_Ellipse/cs.md)
    -   [Přímka](Part_Line/cs.md) (Hrana)
    -   [Bod](Part_Point/cs.md) (Vrchol)
    -   [Pravidelný mnohoúhelník](Part_RegularPolygon/cs.md) <small>(v0.14)</small> \*:


</div>

The following primitives can be created:

-   <img alt="" src=images/Part_Plane.svg  style="width:32px;"> [Plane](Part_Plane.md): Creates a plane.
-   <img alt="" src=images/Tree_Part_Box_Parametric.svg  style="width:32px;"> [Box](Part_Box.md): Creates a box. This object can also be created with the <img alt="" src=images/Part_Box.svg  style="width:32px;"> [Box](Part_Box.md) tool.
-   <img alt="" src=images/Tree_Part_Cylinder_Parametric.svg  style="width:32px;"> [Cylinder](Part_Cylinder.md): Creates a cylinder. This object can also be created with the <img alt="" src=images/Part_Cylinder.svg  style="width:32px;"> [Cylinder](Part_Cylinder.md) tool.
-   <img alt="" src=images/Tree_Part_Cone_Parametric.svg  style="width:32px;"> [Cone](Part_Cone.md): Creates a cone. This object can also be created with the <img alt="" src=images/Part_Cone.svg  style="width:32px;"> [Cone](Part_Cone.md) tool.
-   <img alt="" src=images/Tree_Part_Sphere_Parametric.svg  style="width:32px;"> [Sphere](Part_Sphere.md): Creates a sphere. This object can also be created with the <img alt="" src=images/Part_Sphere.svg  style="width:32px;"> [Sphere](Part_Sphere.md) tool.
-   <img alt="" src=images/Part_Ellipsoid.svg  style="width:32px;"> [Ellipsoid](Part_Ellipsoid.md): Creates a ellipsoid.
-   <img alt="" src=images/Tree_Part_Torus_Parametric.svg  style="width:32px;"> [Torus](Part_Torus.md): Creates a torus. This object can also be created with the <img alt="" src=images/Part_Torus.svg  style="width:32px;"> [Torus](Part_Torus.md) tool.
-   <img alt="" src=images/Part_Prism.svg  style="width:32px;"> [Prism](Part_Prism.md): Creates a prism.
-   <img alt="" src=images/Part_Wedge.svg  style="width:32px;"> [Wedge](Part_Wedge.md): Creates a wedge.
-   <img alt="" src=images/Part_Helix.svg  style="width:32px;"> [Helix](Part_Helix.md): Creates a helix.
-   <img alt="" src=images/Part_Spiral.svg  style="width:32px;"> [Spiral](Part_Spiral.md): Creates a spiral.
-   <img alt="" src=images/Part_Circle.svg  style="width:32px;"> [Circle](Part_Circle.md): Creates a circular edge.
-   <img alt="" src=images/Part_Ellipse.svg  style="width:32px;"> [Ellipse](Part_Ellipse.md): Creates an elliptical edge.
-   <img alt="" src=images/Part_Point.svg  style="width:32px;"> [Point](Part_Point.md): Creates a point (vertex).
-   <img alt="" src=images/Part_Line.svg  style="width:32px;"> [Line](Part_Line.md): Creates a line (edge).
-   <img alt="" src=images/Part_RegularPolygon.svg  style="width:32px;"> [Regular Polygon](Part_RegularPolygon.md): Creates a regular polygon.

## Scripting


**See also:**

[Part scripting](Part_scripting.md)

Test the creation of the primitives with a script. <small>(v0.19)</small> 

This can be run from the [Python console](Python_console.md). 
```python
import parttests.part_test_objects as pto
pto.create_test_file("example_file")
```

This script is located in the installation directory of the program, and can be examined to see how the basic primitives are built. 
```python
$INSTALL_DIR/Mod/Part/parttests/part_test_objects.py
```

It can be used as input to the program as well. 
```python
freecad $INSTALL_DIR/Mod/Part/parttests/part_test_objects.py
```



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Part](Part_Workbench.md) > Part Primitives/cs
