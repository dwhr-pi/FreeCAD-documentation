# Ubuntu Snap/fr
{{TOCright}}

## Introduction

Un package [Ubuntu Snap](Ubuntu_Snap/fr.md), ou simplement [Snap](Ubuntu_Snap/fr.md) est un format de distribution similaire à [AppImage](AppImage/fr.md) en ce qu\'il est destiné à être un \"package installable universel\" pour déployer le logiciel pour les systèmes Linux. Les snaps ont été introduits par Ubuntu mais ils sont destinés à fonctionner dans toutes les distributions Linux tant que le démon Snap, ou `snapd`, est disponible dans le système cible.

Un package Snap a deux caractéristiques principales:

-   Les programmes sont mis en bac à sable afin de ne pas interférer avec le reste du système d\'exploitation.
-   Les programmes sont mis à jour automatiquement en arrière-plan afin d\'obtenir la dernière version de l\'application.

Pour d\'autres façons d\'installer le logiciel, voir [Installation sous Linux](Installing_on_Linux/fr.md).

## Installation

L\'utilisation de Snaps est expérimentale. Les Snaps actuels sont générés et hébergés par des bénévoles.

Pour tous les systèmes où Snaps doit être installé, le démon Snap doit être installé en premier. Le package est normalement appelé `snapd`.

### Debian/Ubuntu

Pour Debian/Ubuntu et les systèmes similaires qui utilisent le gestionnaire APT, le démon est installé comme suit:


{{Code|lang=bash|code=
sudo apt install snapd
}}

Pour installer la version stable de Snap, utilisez:


{{Code|lang=bash|code=
sudo snap install freecad
}}

Pour installer la version de développement de Snap, utilisez:


{{Code|lang=bash|code=
sudo snap install --edge freecad-ppd
}}

### Manjaro

Pour installer la version stable de Snap, utilisez:


{{Code|lang=bash|code=
snap install freecad
}}

Pour installer la version de développement de Snap, utilisez:


{{Code|lang=bash|code=
snap install --edge freecad-ppd
}}

## Remarques

Pour savoir quelle version de développement est installée, tapez ce qui suit dans l\'interface de ligne de commande :


{{Code|lang=bash|code=
snap info freecad-ppd
}}

## Mode avancé 

Les commandes suivantes sont destinées aux utilisateurs qui sont familiers avec git et ont un dépôt cloné localement du dépôt FreeCAD en amont.


{{Code|lang=bash|code=
git clone https://github.com/FreeCAD/FreeCAD
cd FreeCAD/
}}

Pour trouver le dernier numéro de révision amont (également connu sous le nom de \"HEAD\") :


{{Code|lang=bash|code=
git rev-list --count HEAD
}}

Pour traduire la version de développement en cours en un numéro de révision (assurez-vous que vous êtes dans votre dépôt FreeCAD cloné comme mentionné ci-dessus) :


{{Code|lang=bash|code=
snap info freecad-ppd {{!}}

grep -e \'\^installed:\' {{!}} awk -F \' \' \'{ print \$2 }\' {{!}} cut -d\'\~\' -f2 {{!}} xargs -I{} git rev-list \--count {} }}

La différence entre les chiffres vous indiquera le nombre de révisions en retard du snap par rapport au développement (edge).

## Liens

Plus d\'informations sur les efforts en cours pour gérer Snaps :

-   [0.19 Snap Preview a besoin de \"testeurs\"](https://forum.freecadweb.org/viewtopic.php?f=4&t=46044), ancien Snap de **vejmarie**.
-   [Discussion: Discussion: état du composant logiciel Snap (Snap Packaging)](https://forum.freecadweb.org/viewtopic.php?f=42&t=46853), version plus récente du Snap par **ppd**.

-   [AppImage](AppImage/fr.md) - un autre format autonome de type \'binaire\' pour exécuter FreeCAD
-   [Flatpak](Flatpak/fr.md)



---
![](images/Right_arrow.png) [documentation index](../README.md) > Ubuntu Snap/fr
