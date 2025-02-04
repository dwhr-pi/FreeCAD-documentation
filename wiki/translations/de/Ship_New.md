---
- GuiCommand:/de
   Name:Ship New‏‎
   Name/de:Schiff Neu‏‎
   Icon:Ship_Instance.svg
   MenuLocation:Schiffskonstruktion → Ein neues Schiff erstellen
   Workbenches:[Schiff](Ship_Workbench/de.md)|
Shortcut=
   SeeAlso:
---

# Ship New/de


</div>

## Beschreibung

Erstelle ein neues Schiff oder eine neue Schiffsinstanz.

Ship works over **Ship entities**, that must be created on top of provided geometry. Geometry must be a solid, or set of solids.The following criteria must be taken into account:

-   All hull geometry must be provided (including symmetric bodies).
-   Starboard geometry must be included at negatives *y* domain.
-   Origin (0,0,0) point is the **Midship section** (Midpoint between after and forward perpendicular) and **base line** intersection.

![](images/FreeCAD-Ship-SignCriteria.jpg ) 
*Ship sign criteria*

## Anwendung


<div class="mw-translate-fuzzy">

Um eine **Schiffsinstanz** (auch bekannt als: ein neues Schiff) zu erstellen, wähle die Geometrie s60 und führe das **Schiffserstellungswerkzeug** aus {{MenuCommand/de|Schiffskonstruktion → Neues Schiff erstellen}}


</div>


<div class="mw-translate-fuzzy">

Der Dialog zum Erstellen von Schiffsaufgaben und einige Anmerkungen unter [3D Ansicht](3D_view/de.md) werden gezeigt. Die Anmerkungen werden entfernt, wenn du das Schiffs-Erstellungswerkzeug schließt, machen dir also keine Sorgen.


</div>

Die meisten relevanten Schiffsdaten müssen eingeführt werden (das Schiff verwendet ein progressives Dateneinführungssystem, so dass grundlegende Operationen durchgeführt werden können, wenn nur die grundlegenden Schiffsdaten bekannt sind; mit zunehmender Komplexität der Operationen werden mehr Informationen benötigt).

## Ship data 


<div class="mw-translate-fuzzy">

## Schiffsdaten

Hier müssen die wichtigsten Abmessungen aufgeführt werden:

-   Länge: Länge zwischen den Loten, 25,5 m für dieses Schiff.
-   Breite: Gesamte Schiffsbreite, 3,389 m für dieses Schiff.
-   Tiefgang: Entwurfstiefgang, 1,0 m für dieses Schiff.


</div>

![](images/FreeCAD-Ship-S60ShipCreationFront.png )


<div class="mw-translate-fuzzy">

![Frontansichtsanmerkungen](images/FreeCAD-Ship-S60ShipCreationFront.png )


<center>

Längen Anmerkungen.


</center>


</div>

Normalerweise hängt die Länge zwischen den Loten vom Entwurfstiefgang ab. Wenn du also nicht weißt, wie lang dein Schiff ist, kannst du den Tiefgang einstellen und die Länge anpassen, um einen Schnittpunkt zwischen Bug und Tiefgang zu erhalten.

![](images/FreeCAD-Ship-S60ShipCreationSide.png )


<div class="mw-translate-fuzzy">

![Seitenansichtsanmerkungen](images/FreeCAD-Ship-S60ShipCreationFront.png )


<center>

Breitenanmerkungen.


</center>


</div>


<div class="mw-translate-fuzzy">

Dasselbe Verfahren gilt für die Breitenpassung. Hinweis: Dieser angeforderte Wert ist die gesamte Breite, aber die Anmerkung bezieht sich nur auf die Steuerbordhälfte des Schiffes.


</div>


<div class="mw-translate-fuzzy">

Wenn du die **Accept** Schaltfläche drückst, wird eine neue Schiffsinstanz mit dem Namen **Schiff** im Dialogfeld *Kennzeichen & Attribute* erstellt. Wir brauchen die Geometrie nicht mehr, du kannst sie also ausblenden.


</div>

## Tutorien


<div class="mw-translate-fuzzy">

-   [FreeCAD Schiffs s60 Tutorium](FreeCAD-Ship_s60_tutorial/de.md)
-   [FreeCAD Schiffs s60 Tutorium (II)](FreeCAD-Ship_s60_tutorial_(II)/de.md)


</div>


<div class="mw-translate-fuzzy">





</div>


{{Ship_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > Ship New/de
