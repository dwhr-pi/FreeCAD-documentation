---
- GuiCommand:/it
   Name:Ship New
   Name/it:Nuova‏‎
   MenuLocation:Ship design → Crea una nuova nave
   Workbenches:[Ship](Ship_Workbench/it.md)
   Shortcut:
   SeeAlso:
---

# Ship New/it


</div>


<div class="mw-translate-fuzzy">

## Introduzione

Da fare


</div>

Create a New Ship or new Ship Instance.

Ship works over **Ship entities**, that must be created on top of provided geometry. Geometry must be a solid, or set of solids.The following criteria must be taken into account:

-   All hull geometry must be provided (including symmetric bodies).
-   Starboard geometry must be included at negatives *y* domain.
-   Origin (0,0,0) point is the **Midship section** (Midpoint between after and forward perpendicular) and **base line** intersection.

![](images/FreeCAD-Ship-SignCriteria.jpg ) 
*Ship sign criteria*

## Usage

In order to create a **Ship instance** (in other words, a New Ship), select the hull solid geometry and invoke **Ship design → Create a new ship**.


<div class="mw-translate-fuzzy">

Appare il dialogo per la Creazione della barca e nella vista 3D viene mostrata la sua sagoma con alcune annotazioni. Non preoccupatevi delle annotazioni perché vengono rimosse quando si chiude lo strumento di creazione della nave.


</div>

Devono essere introdotti i dati principali della nave (FreeCAD-Ship utilizza un sistema di introduzione dei dati progressivo, in questo modo le operazioni di base possono essere eseguite utilizzando i dati di base della nave, e le ulteriori informazioni sono necessarie solo quando le operazioni diventano più complesse).

## Ship data 


<div class="mw-translate-fuzzy">

### Dati della nave 

Le dimensioni principali che devono essere introdotte qui:

-   *Length*: lunghezza tra le perpendicolari, 25,5 m per questo scafo.
-   *Beam*: baglio, larghezza massima della barca, 3,389 m per questo scafo.
-   *Draft*: immersione, 1,0 m per questo scafo.


</div>

![](images/FreeCAD-Ship-S60ShipCreationFront.png )


<div class="mw-translate-fuzzy">

![Front view annotations](images/FreeCAD-Ship-S60ShipCreationFront.png )


<center>

Annotazioni di lunghezza nella vista frontale.


</center>


</div>

La distanza tra le perpendicolari dipende dall\'immersione, quindi se non si conosce la lunghezza tra le perpendicolari è possibile impostare l\'immersione e regolare la lunghezza in modo da ottenere l\'intersezione del dritto o ruota di prua (linea superiore della prua) con la [linea di galleggiamento](http://it.wikipedia.org/wiki/Linea_di_galleggiamento).

![](images/FreeCAD-Ship-S60ShipCreationSide.png )


<div class="mw-translate-fuzzy">

![Side view annotations](images/FreeCAD-Ship-S60ShipCreationSide.png )


<center>

Annotazioni sulla vista laterale.


</center>


</div>


<div class="mw-translate-fuzzy">

Lo stesso procedimento è valido per il baglio. Si noti che viene richiesto il valore del [baglio maestro](http://it.wikipedia.org/wiki/Baglio_%28nautica%29) (larghezza massima) , ma l\'annotazione si riferisce solo alla metà di dritta della barca.


</div>


<div class="mw-translate-fuzzy">

Quando si preme il pulsante **OK**, il programma crea la nuova istanza barca, questa nuova istanza è denominata **Ship** nell\'albero \'\' Etichette e Attributi\'\'. Ora la geometria originale non è più necessaria, quindi è possibile nasconderla.


</div>

## Tutorial


<div class="mw-translate-fuzzy">

-   [/it\|Tutorial Ship s60, prima parte ](FreeCAD-Ship_s60_tutorial.md)
-   [Tutorial Ship s60, seconda parte](FreeCAD-Ship_s60_tutorial_(II)/it.md)


</div>





{{Ship_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > Ship New/it
