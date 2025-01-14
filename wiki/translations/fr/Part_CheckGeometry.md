---
- GuiCommand:/fr
   Name:Part CheckGeometry‏‎
   Name/fr:Part Vérifier la géométrie
   MenuLocation:Pièce → Vérifier la géométrie
   Workbenches:[Part](Part_Workbench/fr.md)
---

# Part CheckGeometry/fr

## Description

L\'outil **<img src="images/Part_CheckGeometry.svg" width=16px> [Part Vérifier la géométrie](Part_CheckGeometry/fr.md)** exécute une vérification et indique si la géométrie est un solide valide. L\'outil vérifie si la [Représentation par les Bords](https://fr.wikipedia.org/wiki/B-Rep) (BRep ou [B-rep](Glossary/fr#B.md)) du modèle est valide.

## Utilisation

1.  Sélectionnez une pièce (attention à sélectionner la pièce entière et pas seulement une face pour vérifier la validité du solide).
2.  Lancez l\'outil soit en:
    -   En cliquant sur le **<img src="images/Part_CheckGeometry.svg" width=16px> [Analyse la géométrie](Part_CheckGeometry/fr.md)** disponible dans la barre d\'outils de l\'atelier Part.
    -   En utilisant **Pièce → <img src="images/Part_CheckGeometry.svg" width=16px> Vérifier la géométrie** dans le menu supérieur.
3.  Le panneau de tâches **Settings** s\'ouvre, sauf si **Skip settings page** est activé. Voir [Options](#Options.md) pour plus d\'informations. Cliquez sur **Run check**.

Les résultats seront présentés dans le [Panneau des tâches](Task_panel/fr.md). Si la vérification a produit des erreurs : cliquez dans le rapport sur un message d\'erreur spécifique et l\'objet géométrique correspondant (arête, face, etc.) sera mis en surbrillance dans la [vue 3D](3D_view/fr.md).

**Remarque :** FreeCAD ne dispose pas de méthodes de réparation automatique pour les solides, vous devez donc examiner les étapes nécessaires pour modéliser cette géométrie spécifique et essayer de réparer l\'erreur par vous-même.

## Options

### Skip settings page 

Si cette case est cochée, les prochaines utilisations de l\'outil n\'afficheront pas le panneau de tâches **Settings**.

### Run BOP check 

Si cette case est cochée, une vérification supplémentaire des opérations booléennes (BOP) est effectuée. {{Version/fr|0.19}}

### Log errors 

Si cette case est cochée, toutes les erreurs trouvées sont également enregistrées dans la [Vue rapport](Report_view/fr.md). {{Version/fr|0.19}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Part](Part_Workbench.md) > Part CheckGeometry/fr
