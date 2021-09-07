








{{TOCright}}

## Description

Draft SVG est un module logiciel utilisé par <img alt="" src=images/Std_Open.svg  style="width:24px;"> [Std Ouvrir](Std_Open/fr.md), <img alt="" src=images/Std_Import.svg  style="width:24px;"> [Std Importer](Std_Import.md) et <img alt="" src=images/Std_Export.svg  style="width:24px;"> [Std Exporter](Std_Export.md) pour gérer le format de fichier [SVG](SVG/fr.md).

![](images/Screenshot_inkscape.jpg ) *Inkscape exporte le dessin au format SVG, qui est ensuite ouvert et utilisé dans FreeCAD*

## Importer

Les objets SVG suivants peuvent être importés:

-   objets PATH
-   objets LINE
-   objets RECT
-   objets CIRCLE
-   objets ELLIPSE
-   objets POLYGON
-   objets POLYLINE

### Limitations

FreeCAD n\'importera pas les objets de chemin qui n\'ont qu\'un seul point ([discussion du forum](https://forum.freecadweb.org/viewtopic.php?f=3&t=43856)).

## Exporter

Les objets FreeCAD suivants peuvent être exportés:

-   Lignes et fils (polylignes)
-   Arcs et cercles
-   Surfaces
-   Textes
-   Dimensions

### Limitations 

SVG est un format 2D donc toutes les informations Z seront ignorées (tous les objets seront aplatis).

## Gestion des unités 

Lors de l\'exportation, une unité utilisateur (px) équivaut à un millimètre.

Lors de l\'importation, la largeur, la hauteur et l\'attribut de l\'objet sont respectés. La taille de tous les éléments sont mis à l\'échelle en millimètre, qui est l\'unité interne de FreeCAD. Si le .SVG ne contient pas d\'informations sur sa taille physique, nous supposons qu\'il possède une résolution de 90 DPI. L\'utilisation des unités absolues dans les attributs à l\'intérieur du .SVG doit être évitée. Les unités relatives comme **\" em \"**, **\" ex \"** et **\" % \"** ne sont actuellement pas prisent en charge.

L\'éditeur SVG de [Inkscape](http://inkscape.org/) ne fonctionne actuellement qu\'avec une résolution de **90 DPI**, indépendamment de l\'unité sélectionnée dans Inkscape. Toutes sorties doivent être considérées comme converties à 90 [DPI](http://fr.wikipedia.org/wiki/Point_par_pouce) et arrondi à 6 décimales. Comme FreeCAD (et la norme SVG) est agnostique à la précision de l\'arrondissement fait dans Inkscape, ces valeurs ne seront pas arrondies au moment de l\'entrée, et, les valeurs de millimètres impaires resteront. Si vous avez besoin d\'importer un .SVG il n\'a pas besoin d\'être arrondi, continuez de travailler sur les unités utilisées dans Inkscape (px). La mise à l\'échelle peut être effectuée après l\'importation dans FreeCAD ou, en changeant, la largeur, la hauteur et les attributs de l\'objet.

## Préférences

Pour plus d\'informations, voir: [Préférences d\'Import Export](Import_Export_Preferences/fr.md).

## Script


**Voir aussi:**

[Draft API](Draft_API/fr.md) et [FreeCAD Scripts de base](FreeCAD_Scripting_Basics/fr.md).

Vous pouvez exporter des éléments vers un fichier SVG en utilisant la fonction suivante: 
```python
importSVG.export(exportList, filename)
```

Exemple: 
```python
import Draft, importSVG

Polygon1 = Draft.makePolygon(3, radius=500)
Polygon2 = Draft.makePolygon(5, radius=1500)

objects = [Polygon1, Polygon2]

importSVG.export(objects, "/home/user/Pictures/myfile.svg")
```





 

[Category:File Formats{{\#translation:}}](Category:File_Formats.md)