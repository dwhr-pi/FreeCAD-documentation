---
- GuiCommand:/fr
   Name:Assembly3 CreateAssembly
   Name/fr:Assembly3 Créer un assemblage
   Icon:Assembly_New_Assembly.svg
   Workbenches:[Assembly3](Assembly3_Workbench/fr.md)
   Shortcut:**A** **N**
---

# Assembly3 CreateAssembly/fr

## Description

La commande **Assembly3 Créer un assemblage** ajoute un nouvel objet de la branche **Assembly** à l\'arbre de conception.

Chaque objet de la branche est un <img alt="" src=images/Assembly_Assembly_Tree.svg  style="width:24px;"> un conteneur d**\'assemblage** et contient quatre conteneurs de groupe :

:   \- un pour les <img alt="" src=images/Assembly_Assembly_Constraints_Tree.svg  style="width:24px;"> **Contraintes** (qui est caché tant qu\'il est vide)
:   \- Un pour les <img alt="" src=images/Assembly_Assembly_Element_Tree.svg  style="width:24px;"> 
**Eléments**
:   \- Un pour les <img alt="" src=images/Assembly_Assembly_Part_Tree.svg  style="width:24px;"> 
**Pièces**
:   \- Un pour les <img alt="" src=images/Assembly_Assembly_Relation_Tree.svg  style="width:24px;"> **Relations** (qui sont cachées par défaut et qui seront révélées lorsque <img alt="" src=images/Assembly_GotoRelation.svg  style="width:16px;"> [Go to relation](Assembly3_GoToRelation/fr.md) est utilisé.)

 L\'objet **Assemblage** ajouté avec tous les conteneurs visibles ressemble à ceci (0.20.pre et Link Branch) :

<img alt="" src=images/Assembly3_Example-Tree-07.png  style="width:190px;"> <img alt="" src=images/Assembly3_Example-Tree-08.png  style="width:190px;">

## Utilisation

1.  Créez un conteneur d\'assemblage vide en appuyant sur **<img src="images/Assembly_New_Assembly.svg" width=16px> [Create assembly](Assembly3_CreateAssembly/fr.md)
**
    ou utilisez le raccourci clavier : **A** puis **N**

---
[documentation index](../README.md) > Assembly3 CreateAssembly/fr