---
- GuiCommand:/fr
   Name:Draft AddToGroup
   Name/fr:Draft Déplacer vers un groupe
   MenuLocation:Utilitaires → Déplacer vers le groupe...
   Workbenches:[Draft](Draft_Workbench/fr.md), [Arch](Arch_Workbench/fr.md)
   SeeAlso:[Std Créer un groupe](Std_Group/fr.md), [Draft Ajouter au groupe de construction](Draft_AddConstruction/fr.md), [Draft Groupement automatique](Draft_AutoGroup/fr.md), [Draft Sélection groupée](Draft_SelectGroup/fr.md)
---

## Description

La commande <img alt="" src=images/Draft_AddToGroup.svg  style="width:24px;"> **Draft Déplacer vers le groupe** déplace les objets vers un [Std Groupe](Std_Group/fr.md). Elle peut aussi dégrouper des objets.

Dans la version 0.20 de FreeCAD, la commande peut également gérer les objets de type groupe [Arch](Arch_Workbench/fr.md).

## Utilisation

1.  Pour utiliser cette commande, au moins un groupe doit exister.
2.  Sélectionnez un ou plusieurs objets.
3.  Il existe plusieurs façons de lancer la commande :
    -   Appuyez sur le bouton **<img src="images/Draft_AddToGroup.svg" width=16px> [Draft Déplace les objets sélectionnés vers un groupe...](Draft_AddToGroup/fr.md)**.
    -   Sélectionnez le bouton **Utilitaires → <img src="images/Draft_AddToGroup.svg" width=16px> [Draft Déplacer vers le groupe...](Draft_AddToGroup/fr.md)** dans le menu.
    -   Sélectionnez l\'option **Utilitaires → <img src="images/Draft_AddToGroup.svg" width=16px> Déplacer vers le groupe... ** dans le menu contextuel de la [Vue en arborescence](Tree_view/fr.md) ou de la [Vue 3D](3D_view/fr.md).
4.  Un menu s\'affiche près du curseur. Effectuez l\'une des opérations suivantes :
    -   Sélectionnez le groupe dans lequel vous souhaitez déplacer les objets.
    -   Sélectionnez **Dégrouper** pour déplacer les objets hors du ou des groupes dans lesquels ils se trouvent.

## Remarques

-   Les objets peuvent également être déplacés vers un groupe en les glissant et en les déposant sur le groupe dans la [Vue en arborescence](Tree_view/fr.md).
-   Cette commande peut être utilisée pour déplacer des objets vers le [Groupe de construction](Draft_ToggleConstructionMode/fr.md), mais, contrairement à la commande [Draft Déplacer vers un groupe](Draft_AddConstruction/fr.md), elle n\'applique pas la [couleur de la géométrie de la construction](Draft_ToggleConstructionMode/fr#Pr.C3.A9f.C3.A9rences.md).
-   Pour plus d\'informations sur l\'organisation de votre modèle, voir [Structure du document](Document_structure/fr.md) et [Tutoriel Arch](Arch_tutorial/fr#Organiser_votre_mod.C3.A8le.md).





 