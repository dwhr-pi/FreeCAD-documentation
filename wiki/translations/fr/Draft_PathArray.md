---
- GuiCommand:/fr
   Name:Draft PathArray
   Name/fr:Draft Réseau selon une courbe
   MenuLocation:Modification → Array tools → Réseau selon une courbe
   Workbenches:[Draft](Draft_Workbench/fr.md), [Arch](Arch_Workbench/fr.md)
   Version:0.14
   SeeAlso:[Draft Réseau orthogonal](Draft_OrthoArray/fr.md), [Draft Réseau polaire](Draft_PolarArray/fr.md), [Draft Réseau circulaire](Draft_CircularArray/fr.md), [Draft Réseau lié selon une courbe](Draft_PathLinkArray/fr.md), [Draft Réseau de points](Draft_PointArray/fr.md), [Draft Réseau lié selon des points](Draft_PointLinkArray/fr.md)
---

## Description

La commande <img alt="" src=images/Draft_PathArray.svg  style="width:24px;"> **Draft Réseau selon une courbe** crée un réseau régulier à partir d\'un objet sélectionné en plaçant des copies le long d\'un chemin. Utilisez la commande [Draft Réseau lié selon une courbe](Draft_PathLinkArray/fr.md) pour créer un réseau [Link](App_Link/fr.md) plus efficace à la place. À l\'exception du type de réseau créé, réseau de liens ou réseau régulier, la commande [Draft Réseau lié selon une courbe](Draft_PathLinkArray/fr.md) est identique à cette commande.

Ces deux commandes peuvent être utilisées sur des objets 2D créés avec l\'[atelier Draft](Draft_Workbench/fr.md) ou l\'[atelier Sketcher](Sketcher_Workbench/fr.md), mais aussi sur de nombreux objets 3D tels que ceux créés avec l\'[atelier Part](Part_Workbench/fr.md), l\'[atelier PartDesign](PartDesign_Workbench/fr.md) ou l\'[atelier Arch](Arch_Workbench/fr.md).

<img alt="" src=images/Draft_PathArray_Example.png  style="width:400px;"> 
*Un réseau Draft selon une courbe*

## Utilisation

1.  Sélectionnez l\'objet que vous souhaitez mettre en réseau.
2.  Ajoutez l\'objet courbe à la sélection. Il est également possible de sélectionner des arêtes à la place. Les arêtes doivent appartenir au même objet. Elles doivent être connectées et doivent être sélectionnées dans le bon ordre.
3.  Il existe plusieurs façons de lancer la commande :
    -   Appuyez sur le **<img src="images/Draft_PathArray.svg" width=16px> [Réseau selon une courbe](Draft_PathArray/fr.md)**.
    -   Sélectionnez l\'option **Modification → Array tools → <img src="images/Draft_PathArray.svg" width=16px> Réseau selon une courbe** dans le menu.
4.  Le réseau est créé.
5.  Vous pouvez éventuellement modifier les [propriétés](#Propri.C3.A9t.C3.A9s.md) du réseau dans l\'[Éditeur de propriétés](Property_editor/fr.md).

## Alignement

L\'alignement des éléments d\'un Draft Réseau selon une courbe dépend des propriétés du réseau et de l\'orientation de l\'objet source. La position de l\'objet source est ignorée : pour les besoins du réseau, les valeurs {{Value|x}}, {{Value|y}} et {{Value|z}} sont fixées à {{Value|0}}. Si la propriété {{PropertyData/fr|Align}} du réseau est définie à `False`, l\'orientation des éléments du réseau est identique à celle de l\'objet source. Si elle a pour valeur `True`, l\'axe X du système de coordonnées local de chaque élément placé est tangent à la trajectoire. Les axes Y et Z des systèmes de coordonnées locaux dépendent de la propriété {{PropertyData/fr|Align Mode}} du réseau. Les autres propriétés du réseau impliquées dans l\'alignement comprennent {{PropertyData/fr|Tangent Vector}}, {{PropertyData/fr|Force Vertical}} et {{PropertyData/fr|Vertical Vector}}.

<img alt="" src=images/Draft_PathArray_example2.png  style="width:600px;"> *3 réseaux basés sur la même courbe non planaire. De gauche à droite : Align est false, Align à true pour Align Mode Original et Align à true pour Align Mode Frenet.*.

### Mode d\'alignement 

Trois modes sont disponibles :

#### Original

Ce mode se rapproche le plus du mode unique {{PropertyData/fr|Align Mode}} disponible dans la version 0.18. Il s\'appuie sur un vecteur normal fixe. Si le chemin est planaire, ce vecteur est perpendiculaire au plan du chemin, sinon un vecteur par défaut, l\'axe Z positif, est utilisé. À partir de ce vecteur normal et du vecteur tangent local (l\'axe X local), un [produit vectoriel](https://fr.wikipedia.org/wiki/Produit_vectoriel) est calculé. Ce nouveau vecteur est utilisé comme axe Z local. L\'orientation de l\'axe Y local est déterminée à partir des axes X et Z locaux.

#### Frenet

Ce mode utilise le vecteur normal local dérivé de la trajectoire à chaque placement d\'élément. Si ce vecteur ne peut pas être déterminé (par exemple dans le cas d\'un segment droit), un vecteur par défaut, toujours l\'axe Z positif, est utilisé à la place. Avec ce vecteur et le vecteur tangent local, le système de coordonnées local est déterminé en utilisant la même procédure que dans le paragraphe précédent.

#### Tangent

Ce mode est similaire à {{PropertyData/fr|Align Mode}}. {{Value|Original}} mais offre la possibilité de pré-rotation de l\'objet source en spécifiant un {{PropertyData/fr|Tangent Vector}}.

### Force Vertical et Vertical Vector 

Ces propriétés ne sont disponibles que si {{PropertyData/fr|Align Mode}} est {{Value|Original}} ou {{Value|Tangent}}. Si {{PropertyData/fr|Force Vertical}} est défini sur `True`, le système de coordonnées local est calculé d\'une manière différente. **Vertical Vector** est utilisé comme vecteur normal fixe. Un produit vectoriel est à nouveau calculé à partir de ce vecteur normal et du vecteur tangent local (l\'axe X local). Mais ce vecteur est maintenant utilisé comme l\'axe Y local. L\'orientation de l\'axe Z local est déterminée à partir des axes X et Y locaux.

L\'utilisation de ces propriétés peut être nécessaire si l\'un des bords du chemin est (presque) parallèle à la normale par défaut du chemin.

## Propriétés

Voir aussi: [Éditeur de propriétés](Property_editor/fr.md)

Un objet Draft Réseau selon une courbe est dérivé d\'un objet [Part Feature](Part_Feature/fr.md) et hérite de toutes ses propriétés (à l\'exception de certaines propriétés Vue qui ne sont pas héritées par les réseaux Link). Les propriétés suivantes sont supplémentaires, sauf indication contraire :

### Données


{{TitleProperty|Link}}

Les propriétés de ce groupe ne sont disponibles que pour les réseaux de liens. Voir [Std Créer un lien](Std_LinkMake/fr#Propri.C3.A9t.C3.A9s.md) pour plus d\'informations.

-    {{PropertyData/fr|Scale|Float}}
    

-    {{PropertyData/fr|Scale Vector|Vector|Hidden}}
    

-    {{PropertyData/fr|Scale List|VectorList}}
    

-    {{PropertyData/fr|Visibility List|BoolList|Hidden}}
    

-    {{PropertyData/fr|Placement List|PlacementList|Hidden}}
    

-    {{PropertyData/fr|Element List|LinkList|Hidden}}
    

-    {{PropertyData/fr|_ Link Touched|Bool|Hidden}}
    

-    {{PropertyData/fr|_ Child Cache|LinkList|Hidden}}
    

-    {{PropertyData/fr|Colored Elements|LinkSubHidden|Hidden}}
    

-    {{PropertyData/fr|Link Transform|Bool}}
    


{{TitleProperty|Alignment}}

-    {{PropertyData/fr|Align|Bool}}: spécifie si les éléments du réseau sont alignés ou non le long du chemin. Si elle vaut `False`, toutes les autres propriétés de ce groupe, à l\'exception de {{PropertyData/fr|Extra Translation}} ne s\'appliquent pas et sont masquées.

-    {{PropertyData/fr|Align Mode|Enumeration}}: spécifie le mode d\'alignement, qui peut être {{Value|Original}}, {{Value|Frenet}} ou {{Value|Tangent}}.

-    {{PropertyData/fr|Extra Translation|VectorDistance}}: spécifie un déplacement supplémentaire pour chaque élément le long du chemin.

-    {{PropertyData/fr|Force Vertical|Bool}}: spécifie s\'il faut remplacer la direction normale par défaut par la valeur de {{PropertyData/fr|Vecteur Vertical}}. Utilisé uniquement si {{PropertyData/fr|Align Mode}} est {{Value|Original}} ou {{Value|Tangent}}. <small>(v0.19)</small> 

-    {{PropertyData/fr|Tangent Vector|Vector}}: spécifie le vecteur d\'alignement. Utilisé uniquement si {{PropertyData/fr|Align Mode}} est {{Value|Tangent}}. {{Version/fr|0.19}}

-    {{PropertyData/fr|Vertical Vector|Vector}}: spécifie le remplacement de la direction normale par défaut. Utilisé uniquement si {{PropertyData/fr|Vertical Vector}} est `True`. {{Version/fr|0.19}}


{{TitleProperty|Objects}}

-    {{PropertyData/fr|Base|LinkGlobal}}: spécifie l\'objet à dupliquer dans le réseau.

-    {{PropertyData/fr|Count|Integer}}: spécifie le nombre d\'éléments dans le réseau.

-    {{PropertyData/fr|Expand Array|Bool}}: indique s\'il faut développer le réseau dans la [Vue en arborescence](Tree_view/fr.md) pour permettre la sélection de ses éléments individuels. Disponible uniquement pour les réseaux de type lien (Link).

-    {{PropertyData/fr|Path Object|LinkGlobal}}: spécifie l\'objet à utiliser pour le chemin. Il doit contenir {{Value|Edges}} dans sa [Part TopoShape](Part_TopoShape.md).

-    {{PropertyData/fr|Path Subelements|LinkSubListGlobal}}: spécifie une liste d\'arêtes de {{PropertyData/fr|Path Object}}. Si elle est renseignée, seules ces arêtes sont utilisées pour le chemin.

### Vue


{{TitleProperty|Link}}

Les propriétés de ce groupe, à l\'exception de la propriété héritée, ne sont disponibles que pour les réseaux liens (Link). Voir [Std Créer un lien](Std_LinkMake/fr#Propri.C3.A9t.C3.A9s.md) pour plus d\'informations.

-    {{PropertyView/fr|Draw Style|Enumeration}}
    

-    {{PropertyView/fr|Line Width|FloatConstraint}}
    

-    {{PropertyView/fr|Override Material|Bool}}
    

-    **Point Size|FloatConstraint**
    

-    {{PropertyView/fr|Selectable|Bool}}: il s\'agit d\'une propriété héritée qui apparaît dans le groupe Sélection pour d\'autres réseaux.

-    {{PropertyView/fr|Shape Material|Material}}
    


{{TitleProperty|Base}}

Les propriétés de ce groupe, à l\'exception de la propriété héritée, ne sont disponibles que pour les réseaux liens (Link). Voir [Std Créer un lien](Std_LinkMake/fr#Propri.C3.A9t.C3.A9s.md) pour plus d\'informations.

-    {{PropertyView/fr|Child View Provider|PersistentObject|Hidden}}
    

-    {{PropertyView/fr|Material List|MaterialList|Hidden}}
    

-    {{PropertyView/fr|Override Color List|ColorList|Hidden}}
    

-    {{PropertyView/fr|Override Material List|BoolList|Hidden}}
    

-    {{PropertyView/fr|Proxy|PythonObject|Hidden}}: il s\'agit d\'une propriété héritée.


{{TitleProperty|Display Options}}

Les propriétés de ce groupe sont des propriétés héritées. Voir [Part Feature](Part_Feature/fr#Propri.C3.A9t.C3.A9s.md) pour plus d\'informations.

-    {{PropertyView/fr|Bounding Box|Bool}}: cette propriété n\'est pas héritée par les réseaux de liens (Link).

-    {{PropertyView/fr|Display Mode|Enumeration}}: pour les réseaux de liens, il peut s\'agir de {{value|Link}} ou {{value|ChildView}}. Pour les autres réseaux, il peut s\'agir de : {{value|Flat Lines}}, {{value|Shaded}}, {{value|Wireframe}} ou {{value|Points}}

-    {{PropertyView/fr|Show In Tree|Bool}}
    

-    {{PropertyView/fr|Visibility|Bool}}
    


{{TitleProperty|Draft}}

-    {{PropertyView/fr|Pattern|Enumeration}}: non utilisé.

-    {{PropertyView/fr|Pattern Size|Float}}: non utilisé.


{{TitleProperty|Object style}}

Les propriétés de ce groupe ne sont pas héritées par les réseaux de liens.

## Script

Voir aussi: [Autogenerated API documentation](https://freecad.github.io/SourceDoc/) et [Débuter avec les scripts FreeCAD](FreeCAD_Scripting_Basics/fr.md).

Pour créer un réseau selon une courbe, utilisez la méthode `make_path_array` ({{Version/fr|0.19}}) de l\'atelier Draft. Cette méthode remplace la méthode dépréciée `makePathArray`.


```python
path_array = make_path_array(base_object, path_object,
                             count=4, extra=App.Vector(0, 0, 0), subelements=None,
                             align=False, align_mode="Original", tan_vector=App.Vector(1, 0, 0),
                             force_vertical=False, vertical_vector=App.Vector(0, 0, 1),
                             use_link=True)
```

-    `base_object`est l\'objet à mettre en réseau. Il peut également s\'agir du `Label` (chaîne de caractères) d\'un objet du document courant.

-    `path_object`est l\'objet courbe. Il peut également s\'agir du `Label` (chaîne de caractères) d\'un objet du document courant.

-    `count`est le nombre d\'éléments dans le réseau.

-    `extra`est un vecteur qui déplace chaque élément.

-    `subelements`est une liste d\'arêtes de `path_object`, par exemple `["Bord1", "Bord2"]`. Si elle est renseignée, seules ces arêtes sont utilisées pour le chemin.

-   Si `align` est `True` les éléments sont alignés le long de la courbe en fonction de la valeur de `align_mode`, qui peut être `"Original"`, `"Frenet"` ou `"Tangent"`.

-    `tan_vector`est un vecteur unitaire qui définit la direction tangente locale des éléments le long de la courbe. Il est utilisé lorsque `align_mode` est `"Tangent"`.

-   Si `force_vertical` est `True` `vertical_vector` est utilisé pour la direction Z locale des éléments le long de la courbe. Il est utilisé lorsque `align_mode` est `"Original"` ou `"Tangent"`.

-   Si `use_link` est `True`, les éléments créés sont des [App Links](App_Link/fr.md) au lieu de copies ordinaires.

-    `path_array`est restitué avec l\'objet réseau créé.

Exemple :


```python
import FreeCAD as App
import Draft

doc = App.newDocument()

p1 = App.Vector(500, -1000, 0)
p2 = App.Vector(1500, 1000, 0)
p3 = App.Vector(3000, 500, 0)
p4 = App.Vector(4500, 100, 0)
spline = Draft.make_bspline([p1, p2, p3, p4])
obj = Draft.make_polygon(3, 500)

path_array = Draft.make_path_array(obj, spline, 6)
doc.recompute()

wire = Draft.make_wire([p1, -p2, -p3, -p4])
path_array2 = Draft.make_path_array(obj, wire, count=3, extra=App.Vector(0, -500, 0), subelements=["Edge2", "Edge3"], align=True, force_vertical=True)
doc.recompute()
```





 