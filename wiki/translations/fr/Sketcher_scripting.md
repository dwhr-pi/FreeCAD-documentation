# Sketcher scripting/fr
{{TOCright}}

## Créer une contrainte en Python 

Une contrainte géométrique, <img alt="" src=images/Sketcher_ConstrainCoincident.svg  style="width:24px;"> <img alt="" src=images/Sketcher_ConstrainPointOnObject.svg  style="width:24px;"> <img alt="" src=images/Sketcher_ConstrainVertical.svg  style="width:24px;"> <img alt="" src=images/Sketcher_ConstrainHorizontal.svg  style="width:24px;"> <img alt="" src=images/Sketcher_ConstrainParallel.svg  style="width:24px;"> <img alt="" src=images/Sketcher_ConstrainPerpendicular.svg  style="width:24px;"> <img alt="" src=images/Sketcher_ConstrainTangent.svg  style="width:24px;"> <img alt="" src=images/Sketcher_ConstrainEqual.svg  style="width:24px;"> <img alt="" src=images/Sketcher_ConstrainSymmetric.svg  style="width:24px;"> <img alt="" src=images/Sketcher_ConstrainBlock.svg  style="width:24px;">, et les contraintes spéciales <img alt="" src=images/Sketcher_ConstrainInternalAlignment.svg  style="width:24px;"> [d\'alignement interne](Sketcher_ConstrainInternalAlignment/fr.md) peuvent être créées à partir de macros et de la console Python en utilisant la commande suivante :


```pythonSketch.addConstraint(Sketcher.Constraint(ConstraintType, EdgeOrPartOfEdge…)) 
```

Une contrainte dimensionnelle, <img alt="" src=images/Sketcher_ConstrainLock.svg  style="width:24px;"> <img alt="" src=images/Sketcher_ConstrainDistanceX.svg  style="width:24px;"> <img alt="" src=images/Sketcher_ConstrainDistanceY.svg  style="width:24px;"> <img alt="" src=images/Sketcher_ConstrainDistance.svg  style="width:24px;"> <img alt="" src=images/Sketcher_ConstrainRadius.svg  style="width:24px;"> <img alt="" src=images/Sketcher_ConstrainDiameter.svg  style="width:24px;"> <img alt="" src=images/Sketcher_ConstrainAngle.svg  style="width:24px;">, et la contrainte spéciale <img alt="" src=images/Sketcher_ConstrainSnellsLaw.svg  style="width:24px;"> [Loi de Snell](Sketcher_ConstrainSnellsLaw/fr.md) peuvent être créés à partir de macros et de la console Python en utilisant la commande suivante :


```pythonSketch.addConstraint(Sketcher.Constraint(DimensionalConstraintType, EdgeOrPartOfEdge…, App.Units.Quantity('float_value unit'))) 
```


:   e.g.


```pythonSketch.addConstraint(Sketcher.Constraint(DimensionalConstraintType, EdgeOrPartOfEdge…, App.Units.Quantity('123.0 mm'))) 
```

Le premier argument `ConstraintType` est décrit ci-dessous dans les [Types de contraintes](#Types_de_contraintes.md).

Une contrainte peut prendre jusqu\'à six arguments qui sont des arêtes ou indiquent quelle sous-partie d\'une arête est utilisée par la contrainte. Consultez la documentation des contraintes individuelles pour plus de détails sur les combinaisons d\'arêtes et de sous-parties d\'arêtes pouvant être passées en arguments. Le principal problème avec cette fonction est d\'identifier correctement le numéro de ligne et le numéro de sommet des lignes que vous souhaitez traiter. Les sections ci-dessous décrivent comment [identifier le numéro d\'une ligne](#Identifier_le_num.C3.A9ro_d.27une_ligne.md)) et comment [Identifier le numéro des sous-parties d\'une ligne](#Identifier_le_num.C3.A9ro_des_sous-parties_d.27une_ligne.md)).

## Types de contraintes 

Pour les contraintes géométriques, le premier argument est l\'un des suivants. Voir la page de fonctionnalités correspondante pour les combinaisons d\'arguments possibles autorisées pour chaque contrainte.

++++
| Code                       | Icon                                                                                       | Feature                                                       |
+============================+============================================================================================+===============================================================+
|             | <img alt="" src=images/Sketcher_ConstrainCoincident.svg  style="width:24px;">       | [Coincident](Sketcher_ConstrainCoincident.md)         |
| `'Coincident'`    |                                                                                            |                                                               |
|                         |                                                                                            |                                                               |
++++
|             | <img alt="" src=images/Sketcher_ConstrainPointOnObject.svg  style="width:24px;"> | [Point On Object](Sketcher_ConstrainPointOnObject.md) |
| `'PointOnObject'` |                                                                                            |                                                               |
|                         |                                                                                            |                                                               |
++++
|             | <img alt="" src=images/Sketcher_ConstrainVertical.svg  style="width:24px;">           | [Vertical](Sketcher_ConstrainVertical.md)             |
| `'Vertical'`      |                                                                                            |                                                               |
|                         |                                                                                            |                                                               |
++++
|             | <img alt="" src=images/Sketcher_ConstrainHorizontal.svg  style="width:24px;">       | [Horizontal](Sketcher_ConstrainHorizontal.md)         |
| `'Horizontal'`    |                                                                                            |                                                               |
|                         |                                                                                            |                                                               |
++++
|             | <img alt="" src=images/Sketcher_ConstrainParallel.svg  style="width:24px;">           | [Parallel](Sketcher_ConstrainParallel.md)             |
| `'Parallel'`      |                                                                                            |                                                               |
|                         |                                                                                            |                                                               |
++++
|             | <img alt="" src=images/Sketcher_ConstrainPerpendicular.svg  style="width:24px;"> | [Perpendicular](Sketcher_ConstrainPerpendicular.md)   |
| `'Perpendicular'` |                                                                                            |                                                               |
|                         |                                                                                            |                                                               |
++++
|             | <img alt="" src=images/Sketcher_ConstrainTangent.svg  style="width:24px;">             | [Tangent](Sketcher_ConstrainTangent.md)               |
| `'Tangent'`       |                                                                                            |                                                               |
|                         |                                                                                            |                                                               |
++++
|             | <img alt="" src=images/Sketcher_ConstrainEqual.svg  style="width:24px;">                 | [Equal](Sketcher_ConstrainEqual.md)                   |
| `'Equal'`         |                                                                                            |                                                               |
|                         |                                                                                            |                                                               |
++++
|             | <img alt="" src=images/Sketcher_ConstrainSymmetric.svg  style="width:24px;">         | [Symmetric](Sketcher_ConstrainSymmetric.md)           |
| `'Symmetric'`     |                                                                                            |                                                               |
|                         |                                                                                            |                                                               |
++++
|             | <img alt="" src=images/Sketcher_ConstrainBlock.svg  style="width:24px;">                 | [Block](Sketcher_ConstrainBlock.md)                   |
| `'Block'`         |                                                                                            |                                                               |
|                         |                                                                                            |                                                               |
++++

Les <img alt="" src=images/Sketcher_ConstrainInternalAlignment.svg  style="width:24px;"> [contraintes d\'alignement internes](Sketcher_ConstrainInternalAlignment/fr.md) se comportent comme des contraintes géométriques pour les besoins du script. Là encore, consultez la page de caractéristiques correspondante pour connaître les combinaisons possibles d\'arguments autorisées pour chaque contrainte.

++++
| Code                                                | Icon                                                                                               | Feature                                                             |
+=====================================================+====================================================================================================+=====================================================================+
|                                      | <img alt="" src=images/Sketcher_ConstrainInternalAlignment.svg  style="width:24px;"> | [InternalAlignment](Sketcher_ConstrainInternalAlignment.md) |
| `'InternalAlignment:EllipseMajorDiameter'` |                                                                                                    |                                                                     |
|                                                  |                                                                                                    |                                                                     |
++++
|                                      | <img alt="" src=images/Sketcher_ConstrainInternalAlignment.svg  style="width:24px;"> | [InternalAlignment](Sketcher_ConstrainInternalAlignment.md) |
| `'InternalAlignment:EllipseMinorDiameter'` |                                                                                                    |                                                                     |
|                                                  |                                                                                                    |                                                                     |
++++
|                                      | <img alt="" src=images/Sketcher_ConstrainInternalAlignment.svg  style="width:24px;"> | [InternalAlignment](Sketcher_ConstrainInternalAlignment.md) |
| `'InternalAlignment:EllipseFocus1'`        |                                                                                                    |                                                                     |
|                                                  |                                                                                                    |                                                                     |
++++
|                                      | <img alt="" src=images/Sketcher_ConstrainInternalAlignment.svg  style="width:24px;"> | [InternalAlignment](Sketcher_ConstrainInternalAlignment.md) |
| `'InternalAlignment:EllipseFocus2'`        |                                                                                                    |                                                                     |
|                                                  |                                                                                                    |                                                                     |
++++

Pour les contraintes dimensionnelles, le premier argument est l\'un des suivants. Voir la page de fonctionnalités correspondante pour les combinaisons d\'arguments possibles autorisées pour chaque contrainte.

++++
| Code                       | Icon                                                                               | Feature                                                       |
+============================+====================================================================================+===============================================================+
|             | <img alt="" src=images/Sketcher_ConstrainDistanceX.svg  style="width:24px;"> | [Horizontal distance](Sketcher_ConstrainDistanceX.md) |
| `'DistanceX'`     |                                                                                    |                                                               |
|                         |                                                                                    |                                                               |
++++
|             | <img alt="" src=images/Sketcher_ConstrainDistanceY.svg  style="width:24px;"> | [Vertical distance](Sketcher_ConstrainDistanceY.md)   |
| `'DistanceY'`     |                                                                                    |                                                               |
|                         |                                                                                    |                                                               |
++++
|             | <img alt="" src=images/Sketcher_ConstrainDistance.svg  style="width:24px;">   | [Distance](Sketcher_ConstrainDistance.md)             |
| `'Distance'`      |                                                                                    |                                                               |
|                         |                                                                                    |                                                               |
++++
|             | <img alt="" src=images/Sketcher_ConstrainRadius.svg  style="width:24px;">       | [Radius](Sketcher_ConstrainRadius.md)                 |
| `'Radius'`        |                                                                                    |                                                               |
|                         |                                                                                    |                                                               |
++++
|             | <img alt="" src=images/Sketcher_ConstrainDiameter.svg  style="width:24px;">   | [Diameter](Sketcher_ConstrainDiameter.md)             |
| `'Diameter'`      |                                                                                    |                                                               |
|                         |                                                                                    |                                                               |
++++
|             | <img alt="" src=images/Sketcher_ConstrainAngle.svg  style="width:24px;">         | [Angle](Sketcher_ConstrainAngle.md)                   |
| `'Angle'`         |                                                                                    |                                                               |
|                         |                                                                                    |                                                               |
++++
|             | <img alt="" src=images/Sketcher_ConstrainAngle.svg  style="width:24px;">         | [Angle](Sketcher_ConstrainAngle.md)                   |
| `'AngleViaPoint'` |                                                                                    |                                                               |
|                         |                                                                                    |                                                               |
++++

Les contraintes de la <img alt="" src=images/Sketcher_ConstrainSnellsLaw.svg  style="width:24px;"> [Loi de Snell](Sketcher_ConstrainSnellsLaw/fr.md) se comportent comme des contraintes dimensionnelles pour les besoins du script. Encore une fois, consultez la page de fonctionnalités correspondante pour les combinaisons d\'arguments possibles autorisées pour chaque contrainte.

++++
| Code                   | Icon                                                                               | Feature                                                |
+========================+====================================================================================+========================================================+
|         | <img alt="" src=images/Sketcher_ConstrainSnellsLaw.svg  style="width:24px;"> | [Snell\'s law](Sketcher_ConstrainSnellsLaw.md) |
| `'SnellsLaw'` |                                                                                    |                                                        |
|                     |                                                                                    |                                                        |
++++

La contrainte <img alt="" src=images/Sketcher_ConstrainLock.svg  style="width:24px;"> [fixe](Sketcher_ConstrainLock/fr.md) est une commande de l\'interface graphique qui crée une contrainte <img alt="" src=images/Sketcher_ConstrainDistanceX.svg  style="width:24px;"> [distance horizontale](Sketcher_ConstrainDistanceX/fr.md) et une <img alt="" src=images/Sketcher_ConstrainDistanceY.svg  style="width:24px;"> [distance verticale](Sketcher_ConstrainDistanceY/fr.md), ce n\'est pas une contrainte en soi.

## Identifier le numéro d\'une ligne 

J\'ai dessiné trois lignes comme indiqué dans la figure suivante.

<img alt="" src=images/PartDesignConstraintPointOnPointScriptingFigure1.jpg  style="width:600px;">

En déplaçant le curseur de la souris au-dessus de la ligne, vous pouvez voir le numéro de la ligne en bas à gauche des fenêtres FreeCAD, voir la figure suivante.

<img alt="" src=images/PartDesignConstraintPointOnPointScriptingFigure2.jpg  style="width:600px;">

Malheureusement la numérotation affichée sur les fenêtres de FreeCAD commence à partir de 1 alors que la numérotation de la ligne utilisée pour le script commence à partir de 0 : cela signifie que vous devez soustraire un à chaque fois que vous voulez faire référence à une ligne.

Les nombres positifs indiquent les arêtes d\'esquisse (lignes droites, cercles, coniques, B-splines, etc.). Les valeurs suivantes peuvent être utilisées pour désigner des éléments qui ne sont pas des arêtes d\'esquisse :

-    `-1`désigne l\'axe horizontal des x

-    `-2`désigne l\'axe vertical y

-    `-n`désigne le numéro de l\'élément de géométrie externe `n-3` (par exemple, l\'élément de géométrie externe avec l\'indice 0 dans la liste aplatie `App.ActiveDocument.Sketch.ExternalGeometry` serait désigné par -3, l\'élément suivant dans la liste aplatie serait -4 et ainsi de suite).

## Identifier le numéro des sous-parties d\'une ligne 

Pour déterminer quelle partie d\'une ligne est affectée par une contrainte, les valeurs suivantes peuvent être utilisées :

-    `0`pour indiquer que la contrainte affecte tout le bord.

-    `1`pour indiquer que la contrainte affecte le point de départ du bord (un cercle entier n\'a pas de point de départ).

-    `2`pour indiquer que la contrainte affecte le point final du bord.

-    `3`pour indiquer que la contrainte affecte le point central de l\'arête. Pour des <img alt="" src=images/Sketcher_CompCreateCircle.png  style="width:24px;"> [cercles](Sketcher_CompCreateCircle/fr.md) et des <img alt="" src=images/Sketcher_CompCreateConic.png  style="width:24px;"> [coniques](Sketcher_CompCreateConic/fr.md) (ellipses), c\'est le centre du cercle ou le centre (intersection des grands et petits axes) de l\'ellipse. Pour des lignes <img alt="" src=images/Sketcher_CreateLine.svg  style="width:24px;"> [droites](Sketcher_CreateLine/fr.md), `3` ne peut pas être utilisé pour indiquer le point central.

-    `n`pour indiquer que la contrainte affecte le n-ième pôle d\'une <img alt="" src=images/Sketcher_CompCreateBSpline.png  style="width:24px;"> [B-spline](Sketcher_CompCreateBSpline/fr.md).

Les sommets indiqués par 1 et 2 sont numérotés selon leur ordre de création. Pour connaître l\'ordre de leur création (si vous avez beaucoup de lignes, vous ne vous souvenez plus quel sommet vous avez créé en premier), il vous suffit de déplacer le curseur de votre souris au-dessus des deux sommets d\'une ligne, voir figure suivante.

<img alt="" src=images/PartDesignConstraintPointOnPointScriptingFigure3.jpg  style="width:600px;">

Si vous lisez par exemple 4 et 5, cela signifie que le sommet avec le numéro le plus bas (4 dans cet exemple) sera référencé en utilisant le numéro 1 (en premier dans la commande de script et le sommet avec le numéro le plus élevé (5 dans cet exemple) sera référencé par en utilisant le numéro 2 dans la commande de script.

## Exemple

Prenons l\'exemple précédent des trois lignes. La figure suivante indique la numérotation de chaque ligne et de leurs sommets selon la convention de script.

<img alt="" src=images/PartDesignConstraintPointOnPointScriptingFigure3Bis.jpg  style="width:600px;"> 
*<b>text en bleu:</b> numéro de ligne, <b>text en noir:</b> numéro de sommets*

La commande `Sketch.addConstraint(Sketcher.Constraint('Coincident',1,2,2,1))` donne le résultat suivant :

<img alt="" src=images/PartDesignConstraintPointOnPointScriptingFigure4.jpg  style="width:600px;">

La commande `Sketch.addConstraint(Sketcher.Constraint('Coincident',0,2,2,2))` donne le résultat suivant :

<img alt="" src=images/PartDesignConstraintPointOnPointScriptingFigure5.jpg  style="width:600px;">


{{Sketcher Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Sketcher](Sketcher_Workbench.md) > Sketcher scripting/fr
