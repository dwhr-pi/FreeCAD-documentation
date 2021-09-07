 {{VeryImportantMessage|(November 2018) This information may be incomplete and outdated. For the latest API, see the [https://www.freecadweb.org/api autogenerated API documentation].}}

Modulul Parte este conexiunea directă dintre FreeCAD și kernelul OpenCasCade. Acesta oferă în principal [ TopoShapes](TopoShape_API.md), care este tipul principal de obiect utilizat de OpenCascade. Modulul Parte conține, de asemenea, o varietate de funcții de comoditate pentru a crea și manipula topoShapes. Exemplu: 
```python
import Part
mycube = Part.makeBox(2,2,2)
Part.show(mycube)
```


<div class="mw-translate-fuzzy">


{{APIFunction | __fromPythonOCC__ | OCC.Object | metoda Helper pentru a converti un pythonOCC într-o formă formă internă | A}}

Part.Shape


{{APIFunction | __sortEdges__ | lista muchiilor | Metoda ajutorul pentru sortarea unei liste neordonată margini (margini), care, ulterior, două muchii adiacente împart un nod comun | o listă de margini}}


{{APIFunction | __toPythonOCC__ | | Part.Shape | Metodă de ajutor pentru conversia unei forme interne într-o formă pythonocc | un OCC.Shape}}


{{APIFunction | cast_to_shape | Part.Shape | Distribuția tipului real de formă | }}


{{APIFunction | export | list | string | Exportați o listă de obiecte într-un singur fișier |}}


{{APIFunction | getSortedClusters | lista margini | Metoda Helper pentru sortarea și gruparea unei varietăți de margini | }}


{{APIFunction | en | insert | string | string | Introduceți fișierul (cale dată ca prim argument) în documentul dat (al doilea argument). }}


{{APIFunction | makeBox | lungime, lățime, înălțime, [pnt, dir] | Face o zonă în punctul cu dimensiuni (lungime, lățime, înălțime). În mod prestabilit, punctul este la Vector (0,0,0) iar direcția la Vector (0,0,1) | Creează o formă}}


{{APIFunction | makeCircle | radius, [pnt, dir, angle1, angle2] | Face un cerc cu o anumită rază. În mod prestabilit, punctul este la Vector (0,0,0), iar direcția este Vector (0,0,1), unghiul1 este 0 ° și unghiul2 este 360 ​​° | Creați o formă}}


{{APIFunction | makeCompound | list | Creați un compus dintr-o listă de forme. | Creați o formă}}


{{APIFunction | makeCone | radius1, radius2, height, [pnt, dir, angle] | Face un con cu raza și înălțimea. Punct implicit este vectorul (0,0,0), iar direcția este vectorul (0,0,1), iar unghiul este de 360 ​​° | Creare formă}}


{{APIFunction | makeCylinder | rază, înălțime, [pnt, direcție, unghi] | face un cilindru cu o anumită dimensiune și o rază. În mod prestabilit, punctul este la Vectorr (0,0,0), iar direcția este Vector (0,0,1) și unghiul este 360 ​​° | Creați o formă}}


{{APIFunction | makeHelix | pitch, height, radius, [angle] | Face o helix cu o înălțime, înălțime și rază date. Implicit, o suprafață cilindrică este utilizată pentru a crea spirala. Dacă există un al patrulea parametru, se utilizează în schimb o suprafață conică | Creează o formă}}


{{APIFunction | makeLine | (x1, y1, z1), (x2, y2, z2) | Crearea unei linii la două puncte | Crearea unei forme}}


{{APIFunction | makeLoft | shapelist <profiles>, [boolean <solid>, boolean <ruled>] Crează o formă de loft utilizând lista de profile. Opțional face un solid (vs suprafață / coajă) sau face rezultatul o suprafață condusă | Crearea unei forme loft | Crearea unei forme}}


{{APIFunction | makePlane | lungime, lățime, [pnt, dir] | Creați un plan. Implicit, punctul este la Vector (0,0,0) și direcția la Vector (0,0,1) | Creați o formă}}


{{APIFunction | makePolygon | list | Crearea unui poligon cu o listă de vectori | Crearea unei forme}}


{{APIFunction | makeRevolution | Curve [Vmin, Vmax unghiul pnt, dir] | Face o formă de revoluție prin rotirea curbei, sau o porțiune a acesteia cu privire la o anumită axă (punct, direcție). În mod implicit, vmin și vmax sunt setate la limitele curbei, unghiul este 360 ​​°, punctul este Vector (0,0,0) și direcția este Vector (0,0,1). formă}}


{{APIFunction | makeRuledSurface | Edge sau Wire, Edge or Wire | Crează o suprafață setată din două margini sau fire. Dacă firele sunt folosite, acestea trebuie să aibă același număr de muchii. | Crearea unei forme}}


{{APIFunction | makeShell | list | Creează un shell pe o listă de fețe. | Creează o formă}}


{{APIFunction  | makeSolid | Part.Shape | Creează un înveliș exterior solid, în interiorul unei forme |. Creează o formă}}


{{APIFunction | makeSphere | radius, [pnt, dir, angle1_First, angle2_Fin, angle3] | Creează o sferă a unei raze date. Implicit, punctul este la Vector (0,0,0), iar direcția este la Vector (0,0,1), unghiul 1 este -90 °, unghiul 2 este de 90 ° și unghiul3 este 360 ​​° | Creați o formă}}


{{APIFunction | makeTorus | raza1, radius2, [pnt, directia, unghiul1, unghiul2, unghiul] | Creeaza un torus cu date de raza de raza. În mod implicit, punctul este la Vector (0,0,0), iar direcția este la vector (0,0,1), unghiul 1 este 0 °, unghiul 2 este 360 ​​° și unghiul este 360 ​​° | Creați o formă }}


{{APIFunction | makeTube | margine, float | Creați un tub. | Creați o formă}}


{{APIFunction | en | open | string | Creați un document nou și încărcați fișierul în document }}


{{APIFunction | en | read | string | Încarcă fișierul și returnează o formă. | O formă}}


{{APIFunction | en | show | shape | Adăugați forma documentului activ sau creați unul dacă nu există niciun document. | }}


</div>


 

[Category:API{{\#translation:}}](Category:API.md) [Category:Poweruser Documentation{{\#translation:}}](Category:Poweruser_Documentation.md)