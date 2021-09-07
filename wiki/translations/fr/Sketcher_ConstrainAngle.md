---
- GuiCommand:/fr
   Name:Sketcher ConstrainAngle
   Name/fr:Sketcher Contrainte angulaire
   MenuLocation:Sketch → Contraintes d'esquisse → Contrainte angulaire
   Workbenches:[Sketcher](Sketcher_Workbench/fr.md)
   Shortcut:**A**
   SeeAlso:[Sketcher Contrainte dimensionnelle](Sketcher_ConstrainDistance/fr.md), [Sketcher Contrainte perpendiculaire](Sketcher_ConstrainPerpendicular/fr.md)
---

## Description

La Contrainte d\'Angle est une [Donnée de contrainte](Sketcher_Workbench/fr#Contraintes_d'esquisse.md) destinée à fixer les angles sur le croquis. Elle est capable de fixer des pentes de lignes individuelles, les angles entre les lignes, les angles des intersections de courbes, et l\'espace d\'angles d\'arcs circulaires

## Utilisation

La contrainte peut être appliquée de quatre manières différentes :

-   aux lignes individuelles
-   entre les lignes
-   aux intersections de courbes
-   aux arcs de cercles

Pour appliquer une contrainte d\'angle, il faut suivre les étapes suivantes :

1.  Sélectionnez une, deux ou trois entités dans l\'esquisse. Le mode sera choisi en fonction de la sélection.
2.  Lancez la contrainte en utilisant plusieurs méthodes:
    -   En appuyant sur le bouton **<img src=images/Sketcher_ConstrainAngle.svg style="width:16px"> [Fixer l'angle...](Sketcher_ConstrainAngle/fr.md)** dans la barre d\'outils.
    -   Utilisation du raccourci clavier **A**. (**A** est pour **A**ngle)
    -   L\'utilisation de **Sketch → Contraintes d'esquisse → <img src=images/Sketcher_ConstrainAngle.svg style="width:16px"> Contraindre angulaire** forme l\'entrée de menu supérieure
3.  Une boîte de dialogue d\'édition de référence apparaît.
4.  Modifiez l\'angle si nécessaire. **Remarque :** L\'angle peut être entré comme une expression qui sera évaluée et le résultat sera stocké.
5.  Cliquez sur **OK**

Comme avec toute contrainte de référence, il est possible de changer la valeur d\'angle plus tard en double-cliquant sur la contrainte dans la liste contrainte ou une vue 3D. La saisie d\'une valeur négative entraînera la direction de l\'angle à basculer.

## Modes de contrainte 

### Angle de pente de la ligne 

**Sélection Acceptée :** ligne

<img alt="" src=images/Sketcher_ConsraintAngle_mode1.png  style="width:600px;">

La contrainte définit l\'angle polaire de la direction de la ligne. C\'est l\'angle entre la ligne et l\'axe X de l\'esquisse.

### Durée Arc (v0.15) 

**Sélection acceptée :** arc de cercle

<img alt="" src=images/Sketcher_ConsraintAngle_mode2.png  style="width:600px;">

Dans ce mode, la contrainte fixe la valeur angulaire de l\'arc de cercle

### Entre des lignes 

**Sélection acceptée :** ligne + ligne

<img alt="" src=images/Sketcher_ConsraintAngle_mode3.png  style="width:600px;">

Dans ce mode, la contrainte fixe l\'angle entre deux lignes. Il n\' est pas obligatoire que les lignes se coupent.

### Entre les courbes à l\'intersection (angle par point) (v0.15) 

\"\'Sélection acceptée :\'\" toute ligne/courbe + toute ligne/courbe + tout point

<img alt="" src=images/Sketcher_ConsraintAngle_mode4.png  style="width:600px;">

Dans ce mode, l\'angle entre deux courbes est contraint au point d\'intersection. Le point d\'intersection peut être sur les extensions de courbes. Le point doit être explicitement spécifié, étant donné que les courbes se croisent généralement dans plus d\'un point.

Pour que la contrainte fonctionne correctement, le point doit être sur les deux courbes. Donc, comme la contrainte est invoquée, le point sera automatiquement ajouté sur les deux courbes ([Aide pour contraindre](Sketcher_helper_constraint/fr.md), si nécessaire), et l\'angle entre les courbes sera contraint en ce point. Ces [Assistants de contraintes](Sketcher_helper_constraint/fr.md) sont des contraintes régulières simples. Ils peuvent être ajoutés manuellement ou supprimés. Il n\'y a pas d\'assistant de contraintes sur l\'image ci-dessus par exemple parce que le point sélectionné est déjà à l\'intersection des courbes.

## Script

L\'Angle Contraint peut être créer depuis une [macros](Macros/fr.md) et depuis la console python en utilisant : 
```python
# line slope angle
Sketch.addConstraint(Sketcher.Constraint('Angle',iline,angle))

# angular span of arc
Sketch.addConstraint(Sketcher.Constraint('Angle',iarc,angle))

# angle between lines
Sketch.addConstraint(Sketcher.Constraint('Angle',iline1,pointpos1,iline2,pointpos2,angle))

# angle-via-point (no helper constraints are added automatically when from python)
Sketch.addConstraint(Sketcher.Constraint('AngleViaPoint',icurve1,icurve2,geoidpoint,pointpos,angle))
``` où :

:\* `Sketch` est un objet d\'esquisse:

:\* `iline, iline1, iline2` sont des nombres entiers spécifiant les lignes par leurs nombres ordinaux dans `Sketch`.

:\* `pointpos1, pointpos2` devrait être 1 pour point de départ et 2 pour le point de fin. Le choix des points permet de définir l\'angle interne (ou externe) et il affecte la façon dont la contrainte est dessinée à l\'écran.

:\* `geoidpoint` et `pointpos` dans `AngleViaPoint` sont les indices précisant le point d\'intersection.

:\* `angle` est la valeur d\'angle en radians. L\'angle est compté entre vecteurs tangents dans le sens antihoraire. Les vecteurs tangents pointent du début à la fin pour les lignes (ou vice versa si le point final est fourni dans l\'angle entre le mode de lignes) et le long du sens anti-horaire pour les cercles, arcs et ellipses.La valeur est également acceptée comme un angle (par exemple `App.Units.Quantity('45 deg')`)

La page [Sketcher : Écrire des scripts](Sketcher_scripting/fr.md) explique les valeurs qui peuvent être utilisées pour `iline`, `iline1`, `iline2`, `pointpos1`, `pointpos2`, `geoidpoint` et `pointpos` et contient d\'autres exemples sur la façon de créer des contraintes à partir de scripts Python.





{{Sketcher Tools navi

}}  