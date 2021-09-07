---
- GuiCommand:/de
   Name:Draft Angle   Name/de:Draft Angle
   MenuLocation:Entwurf → [Objektfang](Draft_Snap/de.md) → Winkel
   Workbenches:[Draft](Draft_Module/de.md), [Arch](Arch_Module/de.md)
   SeeAlso:[Objektfang](Draft_Snap/de.md), [Objektfang umschalten](Draft_ToggleSnap/de.md)
---


</div>


{{Draft Tools navi/de}}


<div class="mw-translate-fuzzy">

## Beschreibung

Diese Methode rastet an den Punkten von Kreisen und Kreisbögen in Schritten von 30° und 45° an Kreisbögen ein; das umfasst 0°, 60°, 90°, 180°, 210°, 270° und andere ganzzahlige Vielfache.


</div>

This snap option currently only works properly for circular edges on a plane parallel to the XY plane of the global coordinate system, the angles are relative to that plane.

![](images/Draft_Snap_Angle_example.png )


<div class="mw-translate-fuzzy">


*Rastet am zweiten Punkt einer Linie am Kreis ein, am 45°-Winkel des Keisbogens; kleine Kreise zeigen alle möglichen Rastpositionen*


</div>


{{Userdocnavi/de}}

For general information about snapping see [Draft Snap](Draft_Snap.md).


<div class="mw-translate-fuzzy">

### Anwendung

1.  Stelle sicher, dass **<img src="images/Snap_Lock.svg" width=16px> [Draft Umschalten Ein/Aus](Draft_ToggleSnap/de.md)** und **<img src="images/Snap_Angle.svg" width=16px> [Snap Winkel](Draft_Angle/de.md)** eingeschaltet sind.
2.  Wähle ein Draft-Werkzeug zum Zeichnen einer Form.
3.  Bewege den Cursor über ein Kreis- oder Kreisbogenobjekt.
4.  Der Kreis oder Kreisbogen wird gelb hervorgehoben und ein kleiner weißer Kreis wird den Punkt des Kreisbogens anzeigen, an dem der neue Punkt verbunden wird; dieser Punkt wird im Winkel von 30° oder 45° oder einem Vielfachen zur Horizontalen angezeigt.
5.  Klicke, um den neuen Punkt zu verbinden.


</div>

## Preferences

See [Draft Snap](Draft_Snap#Preferences.md).


<div class="mw-translate-fuzzy">


{{docnav/de
|[Senkrecht](Draft_Perpendicular/de.md)
|[Mittelpunkt](Draft_Center/de.md)
|[Draft Snap](Draft_Snap/de.md)
|IconL=Draft Perpendicular.png
|IconC=Workbench_Draft.svg
|IconR=Draft Center.png
}}


</div>


 