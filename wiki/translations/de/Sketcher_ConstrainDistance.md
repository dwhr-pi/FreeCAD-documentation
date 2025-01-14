---
- GuiCommand:/de
   Name:Sketcher ConstrainDistance
   Name/de:Skizzierer BeschränkeAbstand
   MenuLocation:Skizze → Skizzen Beschränkungen → Abstand Beschränken
   Workbenches:[Skizzierer](Sketcher_Workbench/de.md)
   Shortcut:**Umschalten** + **D**
   SeeAlso:[Horizontalen Abstand beschränken](Sketcher_ConstrainDistanceX/de.md), [Vertikalen Abstand beschränken](Sketcher_ConstrainDistanceY/de.md)
---

# Sketcher ConstrainDistance/de

## Description


<div class="mw-translate-fuzzy">

## Beschreibung

Die **Beschränke Abstand** beschränkt die Länge einer Linie, den senkrechten Abstand zwischen einem Punkt und einer Linie oder den Abstand zwischen zwei Punkten auf einen bestimmten Wert.


</div>

![](images/Sketcher_ConstrainDistance_example.png )

## Anwendung

1.  Wähle zwei Punkte oder eine Linie oder einen Punkt und eine Linie.
2.  Aufrufen des Befehls auf verschiedene Weise:
    -   Drücke die **[<img src=images/Sketcher_ConstrainDistance.svg style="width:16px"> [Abstand beschränken](Sketcher_ConstrainDistance/de.md)** Schaltfläche in der Skizzierer Werkzeugleiste.
    -   Verwende die **Shift** + **D** Tastaturkürzel. (**D**\' steht für **D**istance; engl.: Abstand)
    -   Verwende den **Skizze → Skizziererbeschränkungen  → [<img src=images/Sketcher_ConstrainDistance.svg style="width:16px"> Abstand beschränken** Eintrag aus dem oberen Menü.
3.  Ein Einblenddialogfeld wird geöffnet, um den Wert zu bearbeiten oder zu bestätigen. Drücken **OK**, um den Wert zu bestätigen.

**Hinweis**: Das Beschränkungswerkzeug kann auch ohne vorherige Auswahl gestartet werden. Um den lotrechten Abstand zwischen einem Punkt und einer Linie zu setzen, muss der Punkt zuerst selektiert werden. Als Voreinstellung ist der Befehl im \"Continue Mode\", um neue Beschränkungen zu erstellen; drücke die rechte Maustaste oder **Esc** einmal zum Beenden des Befehls.

### Fingerzeig

Falls anwendbar, erwäge bitte die Verwendung der **[<img src=images/Sketcher_ConstrainDistanceX.svg style="width:16px"> [Horizontaler Abstand](Sketcher_ConstrainDistanceX/de.md)** oder **[<img src=images/Sketcher_ConstrainDistanceY.svg style="width:16px"> [Vertikaler Abstand](Sketcher_ConstrainDistanceY/de.md)** Beschränkungen stattdessen. Diese Beschränkungen sind robuster und schneller zu berechnen als das **BeschränkungAbstand** Werkzeug.

## Skripten

Abstand vom Ursprung:


```pythonSketch.addConstraint(Sketcher.Constraint('DistanceX', Edge, PointOfEdge, App.Units.Quantity('123.0 mm')))```

Abstand zwischen zwei Endpunkten:


```pythonSketch.addConstraint(Sketcher.Constraint('Distance', Edge1, PointOfEdge1, Edge2, PointOfEdge2, App.Units.Quantity('123.0 mm')))```


<div class="mw-translate-fuzzy">

Länge der Linie (die GUI erlaubt die Auswahl der Kante, aber das ist nur eine Abkürzung für die Nutzung der beiden Endpunkte der gleichen Linie):


</div>


```pythonSketch.addConstraint(Sketcher.Constraint('Distance', Line, 1, Line, 2, App.Units.Quantity('123.0 mm')))```

Distanz von Punkt (`Edge, PointOfEdge`) zum nächsten Punk auf Linie (`Line`):


```pythonSketch.addConstraint(Sketcher.Constraint('Distance', Edge, PointOfEdge, Line, App.Units.Quantity('123.0 mm')))```

Die [Skizzierer Skripten](Sketcher_scripting.md)-Seite erklärt die Werte, die für `Edge1`, `Edge2`, `Edge`, `PointOfEdge1`, `PointOfEdge2`, `PointOfEdge` und `Line` verwendet werden können, und enthält weitere Beispiele, wie man Beschränkungen aus Python-Skripten erstellt.





{{Sketcher Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Sketcher](Sketcher_Workbench.md) > Sketcher ConstrainDistance/de
