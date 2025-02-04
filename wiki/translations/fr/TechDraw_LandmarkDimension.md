---
- GuiCommand:/fr
   Name:TechDraw LandmarkDimension
   Name/fr:TechDraw Dimension de repère
   MenuLocation:TechDraw → Dimensions → Insérer une dimension de repère
   Workbenches:[TechDraw](TechDraw_Workbench/fr.md)
   Version:0.19
   SeeAlso:[TechDraw Dimension horizontale](TechDraw_HorizontalDimension/fr.md), [TechDraw Dimension verticale](TechDraw_VerticalDimension/fr.md)
---

# TechDraw LandmarkDimension/fr

## Description

L\'outil Dimension de repère ajoute une cote linéaire à une vue. La cote est basée sur deux points **feature** (Draft.Point ou Part.Vertex) du modèle 3D. Remarquez que les points doivent être des objets **feature** qui apparaissent dans le modèle de la [vue en arborescence](Tree_view/fr.md). Les sommets aléatoires d\'une forme ne fonctionneront pas.

Le but de cet outil est de fournir une solution de contournement à la corruption de dimension provoquée par des problèmes \"[dénomination topologique](topological_naming_problem/fr.md)\". Les points sources doivent utiliser des [Expressions](Expressions/fr.md) ou un autre mécanisme contenant pour établir leur position. Étant donné que les points sont des [Objets Document](App_DocumentObject/fr.md) et non des composants de forme, leur nom ne change pas avec les recalculs et donc ils sont faciles à trouver.

Voir [TechDraw Cote de longueur](TechDraw_LengthDimension/fr#Propri.C3.A9t.C3.A9s.md) pour en savoir plus sur les dimensions et les noms topologiques.

Dimension de repère se comporte généralement comme toute autre dimension.

## Utilisation

1.  Sélectionnez 2 objets Point dans la [vue en arborescence](Tree_view/fr.md) ou la [vue 3D](3D_view/fr.md).
2.  Sélectionnez également la vue à laquelle la dimension doit être ajoutée.
3.  Appuyez sur le bouton **<img src="images/TechDraw_LandmarkDimension.svg" width=16px> [Insérer une dimension de repère](TechDraw_LandmarkDimension/fr.md)
** ou **TechDraw → Dimensions → Insérer une dimension de repère**
4.  Une dimension sera ajoutée à la vue. Le texte de cote peut être déplacé vers la position souhaitée.

## Limitations

L\'outil Dimension de repère est initialement limité aux dimensions \"Distance\". D\'autres types peuvent être ajoutés si la demande le justifie.

## Propriétés

Dimension de repère n\'introduit aucune nouvelle propriété.

## Script


**Voir aussi:**

[TechDraw API](TechDraw_API/fr.md) et [Débuter avec les scripts](FreeCAD_Scripting_Basics/fr.md).

L\'outil Dimension de repère peut être utilisé dans des [macros](Macros/fr.md) et à partir de la console [Python](Python/fr.md) à l\'aide des fonctions suivantes:


```python
dim1 = FreeCAD.ActiveDocument.addObject('TechDraw::LandmarkDimension','Landmark')
dim1.Type = "Distance"
dim1.References2D=[(TDView, 'Vertex1')]
dim1.References3D=[(Point3d1, 'Vertex1')]
dim1.References3D=[(Point3d2, 'Vertex1')]
rc = page.addView(dim1)
```





{{TechDraw Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [TechDraw](TechDraw_Workbench.md) > TechDraw LandmarkDimension/fr
