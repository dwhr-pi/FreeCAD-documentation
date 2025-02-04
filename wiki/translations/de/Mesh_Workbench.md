# <img alt="Polygonnetz Arbeitsbereichssymbol" src=images/Workbench_Mesh.svg  style="width:64px;"> Mesh Workbench/de


{{TOCright}}

## Einführung

Der <img alt="" src=images/Workbench_Mesh.svg  style="width:24px;">[Arbeitsbereich Polygonnetz](Mesh_Workbench/de.md) behandelt [Dreiecksnetze](http://en.wikipedia.org/wiki/Triangle_mesh). Netze sind eine besondere Art von 3D Objekten, die aus dreieckigen Flächen bestehen, die durch ihre Knoten und Kanten miteinander verbunden sind.

Viele 3D Anwendungen, wie [Sketchup](http://de.wikipedia.org/wiki/SketchUp_%28Software%29), [blender](http://de.wikipedia.org/wiki/Blender_%28Software%29), [1](http://de.wikipedia.org/wiki/Maya_%28Software%29%7CMaya) und [3d studio max](http://de.wikipedia.org/wiki/3D-Studio_MAX), verwenden Polygonnetze als wichtigsten Typ von 3D Objekten. Da Polygonnetze sehr einfache Objekte sind, die nur aus Knoten (Punkten), Kanten und (dreieckigen) Flächen bestehen, sind sie sehr einfach zu erstellen, zu modifizieren, zu unterteilen und zu dehnen und können leicht von einer Anwendung zur anderen ohne Verlust übertragen werden. Außerdem können 3D Anwendungen in der Regel sehr große Mengen davon ohne Probleme verwalten, da sie sehr einfache Daten enthalten. Aus diesen Gründen sind Netze oft das 3D Objekt der Wahl, insbesondere bei Anwendungen im Umgang mit Filmen, Animationen und Bilderstellung.

Im Bereich der Ingenieurswissenschaften jedoch stellen Polygonnetze eine große Begrenzung dar: Sie können gekrümmte Flächen nicht genau definieren. Deshalb setzt FreeCAD stattdessen auf [Brep](wikipedia_Boundary_representation.md). Der Arbeitsbereich Polygonnetz bietet einige Befehle zur direkten Änderung von Polygonnetzen, wird aber am häufigsten verwendet, um 3D Netzdaten zu importieren und in einen Festkörper umzuwandeln, zur Verwendung mit dem <img alt="" src=images/Workbench_Part.svg  style="width:24px;">[Arbeitsbereich Part](Part_Workbench/de.md) oder <img alt="" src=images/Workbench_PartDesign.svg  style="width:24px;"> [PartDesign Arbeitsbereich](PartDesign_Workbench/de.md).

<img alt="" src=images/Mesh_example.jpg  style="width:500px;">

## Werkzeuge

Auf alle Werkzeuge des Polygonnetz Arbeitsbereichs kann über das Menü **Polygonnetze** zugegriffen werden. Fast alle Werkzeuge sind auch in einer der Werkzeugleisten **Polygonnetz Werkzeuge** verfügbar.

-   <img alt="" src=images/Mesh_Import.svg  style="width:32px;"> [Netz importieren\...](Mesh_Import/de.md): Importiert ein Netzobjekt aus einer Datei.

-   <img alt="" src=images/Mesh_Export.svg  style="width:32px;"> [Netz exportieren\...](Mesh_Export/de.md): Exportiert ein Netzobjekt in eine Datei.

-   <img alt="" src=images/Mesh_FromPartShape.svg  style="width:32px;"> [Netz aus Form erstellen\...](Mesh_FromPartShape/de.md): Erstellt Netzobjekte aus Formobjekten.

-   <img alt="" src=images/Mesh_RemeshGmsh.svg  style="width:32px;">[Verfeinerung\...](Mesh_RemeshGmsh/de.md): Wiedervernetzt ein Netzobjekt. <small>(v0.19)</small> 

-   Analysieren
    -   <img alt="" src=images/Mesh_Evaluation.svg  style="width:32px;">[Netz auswerten und reparieren\...](Mesh_Evaluation/de.md): Bewertet und repariert ein Netzobjekt.
    -   <img alt="" src=images/Mesh_EvaluateFacet.svg  style="width:32px;"> [Flächeninfo](Mesh_EvaluateFacet/de.md): Zeigt Informationen über Flächen von Netzobjekten an.
    -   <img alt="" src=images/Mesh_CurvatureInfo.svg  style="width:32px;">[Krümmungsinfo](Mesh_CurvatureInfo/de.md): Zeigt Informationen über Flächen von Netzobjekten an: Zeigt die absolute Krümmung von [Krümmungsobjekte](Mesh_VertexCurvature/de.md) an ausgewählten Punkten an.
    -   <img alt="" src=images/Mesh_EvaluateSolid.svg  style="width:32px;">[Festkörpernetz prüfen](Mesh_EvaluateSolid/de.md): Prüft, ob ein Netzobjekt fest ist.
    -   <img alt="" src=images/Mesh_BoundingBox.svg  style="width:32px;">[Begrenzungsinfo\...](Mesh_BoundingBox/de.md): Zeigt die Begrenzungsrahmen Koordinaten eines Netzobjekts an.

-   <img alt="" src=images/Mesh_VertexCurvature.svg  style="width:32px;"> [Krümmungsdiagramm](Mesh_VertexCurvature/de.md): Erstellt Netzkrümmungsobjekte für Netzobjekte.

-   <img alt="" src=images/Mesh_HarmonizeNormals.svg  style="width:32px;"> [Normale harmonisieren](Mesh_HarmonizeNormals/de.md): Harmonisiert die Normalen von Netzobjekten.

-   <img alt="" src=images/Mesh_FlipNormals.svg  style="width:32px;"> [Wendet Normalen](Mesh_FlipNormals/de.md): Wendet die Normalen von Netzobjekten.

-   <img alt="" src=images/Mesh_FillupHoles.svg  style="width:32px;"> [Löcher füllen\...](Mesh_FillupHoles/de.md): Füllt Löcher in Netzobjekten.

-   <img alt="" src=images/Mesh_FillInteractiveHole.svg  style="width:32px;"> [Loch schließen](Mesh_FillInteractiveHole/de.md): Füllt ausgewählte Löcher in Netzobjekten.

-   <img alt="" src=images/Mesh_AddFacet.svg  style="width:32px;">[Dreieck hinzufügen](Mesh_AddFacet/de.md): Fügt Flächen entlang einer Begrenzung eines offenen Netzobjekts hinzu.

-   <img alt="" src=images/Mesh_RemoveComponents.svg  style="width:32px;"> [Komponenten entfernen\...](Mesh_RemoveComponents/de.md): Entfernt Flächen von Netzobjekten.

-   <img alt="" src=images/Mesh_RemoveCompByHand.svg  style="width:32px;">[Komponenten von Hand entfernen\...](Mesh_RemoveCompByHand/de.md): Entfernt Komponenten von Netzobjekten.

-   <img alt="" src=images/Mesh_Segmentation.svg  style="width:32px;"> [Netzsegmente erstellen\...](Mesh_Segmentation/de.md): Erstellt separate Netzsegmente für bestimmte Oberflächentypen eines Netzobjekts.

-   <img alt="" src=images/Mesh_SegmentationBestFit.svg  style="width:32px;">[Netzsegmente aus bestpassenden Flächen erzeugen\...](Mesh_SegmentationBestFit/de.md): Erstellt separate Netzsegmente für bestimmte Oberflächentypen eines Netzobjekts und kann deren Parameter identifizieren.

-   <img alt="" src=images/Mesh_Smoothing.svg  style="width:32px;">[Glätten\...](Mesh_Smoothing/de.md): Glättet Netzobjekte.

-   <img alt="" src=images/Mesh_Decimating.svg  style="width:32px;">[Dezimierung\...](Mesh_Decimating/de.md): Reduziert die Anzahl der Flächen in Netzobjekten. <small>(v0.19)</small> 

-   <img alt="" src=images/Mesh_Scale.svg  style="width:32px;"> [Skalieren\...](Mesh_Scale/de.md): Skaliert Netzobjekte.

-   <img alt="" src=images/Mesh_BuildRegularSolid.svg  style="width:32px;"> [Regelmäßiger Festkörper\...](Mesh_BuildRegularSolid/de.md) Erzeugt ein regelmäßiges parametrisches Volumenkörper Netzobjekt.

-   Boolsche Operation
-   <img alt="" src=images/Mesh_Union.svg  style="width:32px;">[Vereinigung](Mesh_Union/de.md): Erzeugt ein Netzobjekt, das die Vereinigung von zwei Netzobjekten ist.
-   <img alt="" src=images/Mesh_Intersection.svg  style="width:32px;">[Schnittmenge](Mesh_Intersection/de.md): Erstellt ein Netzobjekt, das die Schnittmenge zweier Netzobjekte ist.
-   <img alt="" src=images/Mesh_Difference.svg  style="width:32px;">[Differenz](Mesh_Difference/de.md): Erstellt ein Netzobjekt, das die Differenz von zwei Netzobjekten ist.

-   Schneiden
    -   <img alt="" src=images/Mesh_PolyCut.svg  style="width:32px;"> [Netz schneiden](Mesh_PolyCut/de.md): Schneidet ganze Flächen aus Netzobjekten aus.
    -   <img alt="" src=images/Mesh_PolyTrim.svg  style="width:32px;">[Netz stutzen](Mesh_PolyTrim/de.md): Stutzt Flächen und Teile von Flächen aus Netzobjekten.
    -   <img alt="" src=images/Mesh_TrimByPlane.svg  style="width:32px;">[Netz mit einer Ebene stutzen](Mesh_TrimByPlane/de.md): Stutzt Flächen und Teile von Flächen auf einer Seite einer Ebene aus einem Netzobjekt.
    -   <img alt="" src=images/Mesh_SectionByPlane.svg  style="width:32px;">[Schnitt aus Netz und Ebene erzeugen](Mesh_SectionByPlane/de.md): Erzeugt einen Querschnitt über ein Netzobjekt.
    -   <img alt="" src=images/Mesh_CrossSections.svg  style="width:32px;">[Querschnitte\...](Mesh_CrossSections/de.md): Erstellt mehrere Querschnitte über Netzobjekte. <small>(v0.19)</small> 

-   <img alt="" src=images/Mesh_Merge.svg  style="width:32px;">[Zusammenführen](Mesh_Merge/de.md): Erstellt ein Netzobjekt, indem die Netze von zwei oder mehr Netzobjekten kombiniert werden.

-   <img alt="" src=images/Mesh_SplitComponents.svg  style="width:32px;"> [Nach Komponenten aufgeteilt](Mesh_SplitComponents/de.md): Zerlegt ein Mesh Objekt in seine Komponenten. <small>(v0.19)</small> 

-   <img alt="" src=images/MeshPart_CreateFlatMesh.svg  style="width:32px;">[Netze auspacken](MeshPart_CreateFlatMesh/de.md): Erstellt eine flache Darstellung eines Netzobjekts. <small>(v0.19)</small> 

-   <img alt="" src=images/MeshPart_CreateFlatFace.svg  style="width:32px;">[Fläche auspacken](MeshPart_CreateFlatFace/de.md): Erstellt eine flache Darstellung einer Fläche eines Formobjekts. <small>(v0.19)</small> 

## Einstellungen

Es gibt einige [Exporteinstellungen verwandt mit Netzformaten](Import_Export_Preferences#Mesh_Formats/de.md), aber diese werden von Befehlen, die zu diesem Arbeitsbereich gehören, nicht verwendet. Sie werden von dem Befehl [Std Export](Std_Export/de.md) verwendet.

Netz Arbeitsbereichseinstellungen können in den folgenden Kategorien des [Preferences Editor](Preferences_Editor/de.md) gefunden werden:

-   <img alt="" src=images/Preferences-display.svg  style="width:32px;"> [Anzeige](Preferences_Editor#Display_settings/de.md): Auf dem [Netz Ansicht](Preferences_Editor#Mesh_view/de.md) Reiter können verschiedene Einstellungen vorgenommen werden.
-   <img alt="" src=images/Preferences-openscad.svg  style="width:32px;"> [OpenSCAD](OpenSCAD_Preferences/de.md): Die [Netz Vereinigen](Mesh_Union/de.md), [Netz Schnittmenge](Mesh_Intersection/de.md) und [Mesh Differenz](Mesh_Difference/de.md) Befehle erfordern [OpenSCAD](http://www.openscad.org/) und verwenden die **OpenSCAD funktionsfähig** Einstellung, um die ausführbare Datei zu finden.

## Hinweise

-   Weitere Netzwerkzeuge sind in der Datei <img alt="" src=images/Workbench_OpenSCAD.svg  style="width:24px;"> [OpenSCAD Arbeitsbereich](OpenSCAD_Workbench/de.md) verfügbar.
-   Siehe [Netz Skripten](Mesh_Scripting.md) zum Bearbeiten und Erstellen von Netzen mit [Python](Python/de.md).
-   Siehe auch: [FreeCAD und Netzimport](FreeCAD_and_Mesh_Import/de.md).
-   Siehe [Asymptote](Asymptote/de.md) zum Exportieren von Netzen in das Asymptote Format.





{{Mesh Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Workbenches](Category_Workbenches.md) > [Mesh](Category_Mesh.md) > Mesh Workbench/de
