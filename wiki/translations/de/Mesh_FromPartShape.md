---
- GuiCommand:/de
   Name:Mesh MeshFromShape‏‎
   Name/de:Netz AusTeilForm
   MenuLocation:Polygonnetze → Erzeuge Polygonnetz aus Form...
   Workbenches:[Polygonnetz](Mesh_Workbench/de.md)
---

## Beschreibung


<div class="mw-translate-fuzzy">

Dieser Befehl erzeugt ein Netz aus einem Formobjekt.


</div>


<div class="mw-translate-fuzzy">

Die Umkehroperation ist **<img src=images/Part_ShapeFromMesh.svg style="width:16px"> [Part FormAusNetz](Part_ShapeFromMesh/de.md)** aus dem <img alt="" src=images/Workbench_Part.svg  style="width:24px;"> [Part Arbeitsbereich](Part_Workbench/de.md).


</div>

## Anwendung

1.  Wähle wahlweise ein oder mehrere Objekte aus.
2.  Es gibt mehrere Möglichkeiten, den Befehl aufzurufen:
    -   Drücke die **<img src="images/Mesh_FromPartShape.svg" width=16px> [Netz AusTeilForm](Mesh_FromPartShape/de.md)** Schaltfläche.
    -   Wähle die **Netze → <img src="images/Mesh_FromPartShape.svg" width=16px> Netz aus Form erzeugen...** Option aus dem Menü.
3.  Das **Tessellierung**s Aufgabenpaneel öffnet sich.
4.  Während das Aufgabenpaneel geöffnet ist, kannst du eine neue Auswahl erstellen oder eine bestehende Auswahl ändern.
5.  Wähle den Reiter für den Vernetzer, den du verwenden möchtest.
6.  Gib die erforderlichen Einstellungen an. Siehe [Vernetzer](#Mesher.md).
7.  Drücke die **OK** Schaltfläche, um das Aufgabenpaneel zu schließen und den Befehl zu beenden.

## Vernetzer

Dies sind die verfügbaren Vernetzer und ihre Einstellungen:

### Standard Vernetzer 


<div class="mw-translate-fuzzy">

Du kannst diese Einstellungen ändern:


</div>

### Mefisto Vernetzer 


<div class="mw-translate-fuzzy">

Die einzige Einstellung ist:

-    {{MenuCommand/de|Maximale Kantenlänge}}: Wenn diese Zahl kleiner ist, wird das Netz feiner. Der kleinste Wert ist 0.


</div>

### Netgen Vernetzer 


<div class="mw-translate-fuzzy">

Beispiel:


</div>

### Gmsh Vernetzer 


<small>(v0.19)</small> 

Für Linux Anwender: das externe [Gmsh](https://gmsh.info/) Modul ist erforderlich.

-    **Meshing**: select a meshing option:

    -   
        **Automatic**
        

    -   
        **Adaptive**
        

    -   
        **Delaunay**
        

    -   
        **Frontal**
        

    -   
        **BAMG**
        

    -   
        **Frontal Quad**
        

    -   
        **Parallelograms**
        

-    **Max. element size**: a smaller value results in a finer mesh. Specify {{Value|0}} to have this size automatically determined.

-    **Min. element size**: a smaller value results in a finer mesh. The value should be smaller than the **Max. element size**. Specify {{Value|0}} to have this size automatically determined.

-    **Angle**: seems to be unsupported at this time.

-    **Path**: press the **...** button and browse to the {{FileName|gmsh.exe}} path.

-   If the meshing process takes too long you can press the **Kill** button to abort it.

-   Press the **Clear** button to remove the information in the text area.

## Hinweise

-   This command is not restricted to objects created with the [Part workbench](Part_Workbench.md). It can create a mesh from any object that has a shape including objects created with the [PartDesign workbench](PartDesign_Workbench.md).
-   The [Std Export](Std_Export.md) command can export shape objects directly to a mesh format.
-   See also: [Export to STL or OBJ](Export_to_STL_or_OBJ.md) tutorial.

## Einstellungen

### Standard Vernetzer 

-   The **Surface deviation** setting is stored: **Tools → Edit parameters... → BaseApp → Preferences → Mod → Mesh → Meshing → Standard → LinearDeflection**.
-   The **Angular deviation** setting is stored: **Tools → Edit parameters... → BaseApp → Preferences → Mod → Mesh → Meshing → Standard → AngularDeflection**.
-   The **Relative surface deviation** setting is stored: **Tools → Edit parameters... → BaseApp → Preferences → Mod → Mesh → Meshing → Standard → RelativeLinearDeflection**.

### Gmsh Vernetzer 

-   Der **Pfad** ist abgelegt: **Werkzeuge → Parameter bearbeiten... → BaseApp → Einstellungen → Mod → Mesh → Meshing → gmshExe**.

## Eigenschaften

Siehe: [Polygonnetz Formelement](Mesh_Feature/de.md).

## Skripten


**Siehe auch:**

[FreeCAD Grundlagen Skripten](FreeCAD_Scripting_Basics/de.md).

Um ein Netzobjekt aus einem Formobjekt zu erstellen, verwende die `NetzAusForm` Methode des MeshPart Moduls. Diese Methode hat mehrere Signaturen. Die Signatur bestimmt den zu verwendenden Vernetzer. Das folgende Beispiel verwendet die Mefisto Vernetzer Signatur.


```python
import FreeCAD, Part, Mesh, MeshPart

cyl = FreeCAD.ActiveDocument.addObject("Part::Cylinder","Cylinder")
FreeCAD.ActiveDocument.recompute()

msh = FreeCAD.ActiveDocument.addObject("Mesh::Feature", "Mesh")
msh.Mesh = MeshPart.meshFromShape(Shape=cyl.Shape, MaxLength=1)
msh.ViewObject.DisplayMode = "Flat Lines"
```


<div class="mw-translate-fuzzy">





</div>


{{Mesh Tools navi

}}  