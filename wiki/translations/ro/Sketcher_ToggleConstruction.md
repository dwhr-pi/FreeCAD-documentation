---
- GuiCommand:/ro
   Name:Sketcher ToggleConstruction
   Name/ro:Activează/dezactivează construcția geometrică
   Icon:Sketcher_AlterConstruction.svg
   Workbenches:[Sketcher](Sketcher_Workbench.md)
   MenuLocation:Sketch → Geometria schitei → Activează/dezactivează construcția geometrică
---

# Sketcher ToggleConstruction/ro


</div>

## Descriere

Acest instrument vă permite să comutați formele geometrice selectate din / în modul de construcție. Poate fi folosit pe orice tip de formă geometrică: linie, arc sau cerc.

Modul de construcției este un instrument important al sketcher-ului. Când se utilizează o schiță pentru operarea în 3D, Modul de construcție este ignorat.


<div class="mw-translate-fuzzy">

În modul editare schiță, geometria construcției este afișată ca fiind albastră și nu va deveni verde atunci când o schiță este complet constrânsă. Odată ce ieșiți din modul schiță, pe ecran se ascunde geometria de construcție.


</div>


<div class="mw-translate-fuzzy">

Liniile de construire pot fi utilizate ca axă de rotație de către funcționalitatea [PartDesign Revolution](PartDesign_Revolution.md) .


</div>

<img alt="" src=images/Sketcher_ConstructionMode_fr_01.png  style="width:480px;">


<div class="mw-translate-fuzzy">

## Utilizare


</div>


<div class="mw-translate-fuzzy">

-   Selectați una sau mi multe obiecte geometrice în vizualizarea 3D, apoi click pe instrument sau accesați-l din meniu.


</div>

## Exemplu

Utilizați Construction mode pe câteva elemente dals schiței,

<img alt="" src=images/Sketcher_ConstructionMode_fr_01.png  style="width:450px;">


<div class="mw-translate-fuzzy">

și odată ce ați părăsit modul de editare a schiței, geometria transformată în construcție a devenit invizibilă pe ecran (dar este încă prezentă în modul de editare Sketcher).


</div>

<img alt="" src=images/Sketcher_ConstructionMode_fr_02.png  style="width:450px;">

## Notes

-    **[<img src=images/Sketcher_CreatePoint.svg style="width:16px"> [Create Point](Sketcher_CreatePoint.md)**will always create points in construction mode regardless of the toolbar toggle state, select the desired points in the [3D view](3D_view.md) after creation and click **[<img src=images/Sketcher_ToggleConstruction.svg style="width:16px"> [Toggle construction](Sketcher_ToggleConstruction.md)** to change them to normal geometry. <small>(v0.19)</small> 


<div class="mw-translate-fuzzy">


</div>


{{Sketcher Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Sketcher](Sketcher_Workbench.md) > Sketcher ToggleConstruction/ro
