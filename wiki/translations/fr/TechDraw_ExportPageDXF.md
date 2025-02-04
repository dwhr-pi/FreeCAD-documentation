---
- GuiCommand:/fr
   Name:TechDraw ExportPageDXF
   Name/fr:TechDraw Exporter au format DXF
   MenuLocation:TechDraw → Exporter une page au format DXF
   Workbenches:[TechDraw](TechDraw_Workbench/fr.md)
   Version:0.18
   SeeAlso:[TechDraw Exporter au format SVG](TechDraw_ExportPageSVG/fr.md), [Draft DXF](Draft_DXF/fr.md)
---

# TechDraw ExportPageDXF/fr

## Description

L\'outil Exporter la page en Dxf enregistre une page de dessin en un fichier au format [DXF](DXF/fr.md)

## Utilisation

1.  Sélectionnez une page dans l\'arborescence si le document contient plusieurs pages.
2.  Cliquer sur le bouton **<img src="images/TechDraw_ExportPageDXF.svg" width=16px> [Exporter une page au format DXF](TechDraw_ExportPageDXF/fr.md)
**
3.  Sélectionnez un emplacement et un nom de fichier.

### Limitations

-   Les dimensions radiales et de diamètre ne s\'exporteront correctement que si elles sont \"à l\'intérieur\" de l\'arc.
-   La mise à l\'échelle n\'est pas prise en charge. Le DXF sera dessiné dans la taille réelle de la page TechDraw.
-   Les unités ne sont pas prises en charge. Le DXF sera dessiné en millimètres (mm). Le texte de cote sera affiché exactement tel qu\'il est affiché dans TechDraw.
-   TechDraw ne peut pas exporter un [TechDraw Vue Draft](TechDraw_DraftView/fr.md) ou une [TechDraw Vue architecturale](TechDraw_ArchView/fr.md) vers DXF. Ces vues sont des éléments [SVG](SVG/fr.md) générés en interne par l\'[atelier Draft](Draft_Workbench/fr.md), il n\'y a donc pas de forme géométrique à exporter. Pour exporter une vue au format DXF, elle doit avoir été créée avec [TechDraw Vue](TechDraw_View/fr.md) ou [TechDraw Projection de groupe](TechDraw_ProjectionGroup/fr.md). Par exemple, sélectionnez un [Arch Plan de section](Arch_SectionPlane/fr.md), puis utilisez [Draft Vue 2D d\'une forme](Draft_Shape2DView/fr.md) pour créer une forme de projection plate, puis utilisez [TechDraw Vue](TechDraw_View/fr.md) sur cet objet. Vous pouvez également sélectionner les objets dans l\'arborescence ou la fenêtre 3D et exporter vers DXF à l\'aide de **Fichier → [Export](Std_Export/fr.md)**.
-   Le cartouche d\'une page est également un modèle [SVG](SVG/fr.md), il ne sera donc pas non plus exporté vers DXF.
-   En général, TechDraw ne peut exporter vers DXF que les éléments pris en charge par la classe `Import::ImpExpDxfWrite` du [Module d\'importation](Draft_DXF/fr.md).

## Remarques

-   Cette fonction exporte les versions R12 (AC1009) et R14 (AC1014) de [DXF](DXF/fr.md).
    -   R12 est une version plus ancienne et plus simple de la norme mais devrait être lisible par la plupart des autres logiciels.
    -   R14 est la version par défaut. Elle inclut entre autres la prise en charge des splines et des ellipses.
-   Ces paramètres affectent la sortie:
    -   
        **Outils → Editer paramètres → BaseApp/Preferences/Mod/Import → DxfVersionOut**
        
        . Il s\'agit d\'une valeur entière. Les entrées valides sont 12 ou 14. La valeur par défaut est 14.

    -   
        **Outils → Editer paramètres → BaseApp/Preferences/Mod/Import → DiscretizeEllipses**
        
        . Il s\'agit d\'une valeur booléenne. Si `True`, les splines et les ellipses sont converties en polylignes; si `False`, les splines et les ellipses sont écrites en tant qu\'objets splines et ellipses. Par défaut `False`. Si le paramètre DxfVersionOut est 12, les splines et les ellipses sont toujours converties en polylignes.

    -   
        **Outils → Editer paramètres → BaseApp/Preferences/Mod/Import → maxsegmentlength**
        
        . Il s\'agit d\'une valeur flottante. Si les splines et les ellipses sont converties en polylignes, ce paramètre détermine la longueur du segment.

## Script


**Voir aussi:**

[TechDrawGui API](TechDrawGui_API/fr.md) et [Débuter avec les scripts](FreeCAD_Scripting_Basics/fr.md).

L\'outil Sauvegarder en DXF peut être utilisé dans des [macros](Macros/fr.md) et à partir de la console [Python](Python/fr.md) à l\'aide des fonctions suivantes:


```python
TechDraw.writeDXFPage(page,filename)
```





{{TechDraw Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [TechDraw](TechDraw_Workbench.md) > TechDraw ExportPageDXF/fr
