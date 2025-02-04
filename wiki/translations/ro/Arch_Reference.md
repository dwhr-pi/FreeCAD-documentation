---
- GuiCommand:/ro
   Name:Arch Reference
   Name/ro:Arch Reference
   MenuLocation:Arch → Reference
   Workbenches:[Arch](Arch_Workbench/ro.md)
   Shortcut:
   SeeAlso:[[Arch BuildingPart]]
---

# Arch Reference/ro


</div>

## Descriere

<img alt="" src=images/Arch_reference_screenshot.png  style="width:800px;">


<div class="mw-translate-fuzzy">

Instrumentul de referință vă permite să plasați un obiect în documentul curent care copiază forma și culorile acestuia dintr-un obiect [ Part](Part_Workbench.md) (inclusiv [Arch BuildingPart](Arch_BuildingPart.md)) stocate într-un alt fișier FreeCAD. Dacă se modifică fișierul FreeCAD, obiectul de referință este marcat să fie reîncărcat.


</div>


<div class="mw-translate-fuzzy">

## Cum se folosește 


</div>


<div class="mw-translate-fuzzy">

1.  Press the **<img src="images/Arch_Reference.png" width=16px> '''Arch Reference'''** button
2.  Press the \"Choose file\...\" button and select an existing FreeCAD file
3.  Select one of the included Part-based objects from the drop-down list
4.  Press **OK**


</div>

## Opţiuni


<div class="mw-translate-fuzzy">

-   Obiectul de referință poate fi mutat și rotit, poziția curentă va fi reținută după reîncărcarea obiectului
-   Dacă obiectul original se deplasează în fișierul care conține fișierul, această mișcare se va reflecta în obiectul de referință
-   Faceți clic cu butonul din dreapta pe un obiect Referință în vizualizarea arborescentă, aveți opțiunile de a reîncărca obiectul original sau de a deschide fișierul care conține
-   Pentru a trimite mai multe obiecte simultan, plasați-le într-un [Arch BuildingPart](Arch_BuildingPart.md)
-   Când dezactivați proprietățile de referință din **Update Colors**, nu mai reîncărcați culorile originale, astfel încât să le puteți schimba în siguranță


</div>

## Proprietăți

-    **File**: Fișierul de bază pe care se bazează această componentă

-    **Part**:Partea care trebuie utilizată din fișierul de bază

-    **Update Colors**: Dacă este adevărat, culorile fișierului conectat/link vor fi menținete actualizate

## Scrip-Programare 


<div class="mw-translate-fuzzy">

Instrumentul Reference poate fi utilizat în [macro-uri](Macros/ro.md) și din consola Python utilizând următoarea funcție:


</div>


```python
makeReference ([file_path,object_name])
```

creează un obiect tip Reference din obiectul dat în fișierul specificat.

Exempluː 
```python
import Arch
Arch.makeReference("/path/to/some/file.FSCtd","myPart")
```



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Arch](Arch_Workbench.md) > Arch Reference/ro
