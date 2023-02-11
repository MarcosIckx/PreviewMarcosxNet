---
date: 2008-09-11
category: "Time Machine"
title: "ZBack : Time Machine pour ZFS !"
---

Vous avez très certainement déjà entendu parlé de ZFS (Zetta File System) le système de fichiers développé principalement par Sun, et qui est maintenant supporté par Mac OS X Leopard Server ?

Sachez que James Gosling, père du langage Java, travaille sur un projet : un Time Machine pour ZFS.

Ci dessous une traduction d’un extrait de la [description du projet][projet] pour se faire une idée de ce à quoi ressemblera la fenêtre

> Utilisez ZFS pour remonter le temps
> 
> ZBack est un navigateur de fichiers pour revenir dans le temps, à l’aide des snapshots ZFS
> 
> ZBack est un simple navigateur de fichier qui comprends ZFS et vous permet de naviguer parmi les snapshots en les voyant comme un repère dans le temps. Le navigateur comprends deux points dans le temps = “Maintenant” et “Auparavant”. “Maintenant” est l’état actuel du système de fichiers; “Auparavant” est un snapshot. En allant dans les sens contraire des aiguilles d’une montre, depuis le coin supérieur gauche, les composants de la fenêtre sont :
> 
> Une liste déroulante pour choisir le système de fichiers ZFS (mountpoint) où l’on désire naviguer. S’il n’y en a qu’un seul, il sera présélectionné et la liste désactivée.
> Une liste déroulante avec des entrées pour chaque répertoire contenu dans le répertoire en cour de visualisation.
> 
> Si vous désirez remonter dans la hiérarchie, il suffit de choisir le parent approprié.
> 
> Une liste avec les noms de tous les fichiers situés dans le répertoire courant. Il y a quatre styles d’affichage pour les entrées :
> 
> * Barré : existait auparavant, mais n’existe plus maintenant. Il a été effacé.
> * Vert : Existe maintenant mais pas auparavant. C’est un nouveau fichier.
> * Gras: existe maintenant et auparavant, mais il a été modifié depuis lors.
> * Normal: existe maintenant et auparavant, et c’est le même contenu.
> 
> Au bas de la fenêtre, il y a un curseur pour choisir le ‘Auparavant”. A l’extrême gauche se situe le début du temps (le snapshot le plus ancien). A l’extrème droite se trouve “maintenant”.
> 
> La partie droite de la fenêtre est constituée de 4 onglets :
> 
> Contenu : le contenu du fichier actuellement sélectionné.
> Diff : les différences entre les deux versions du fichier (soit “Auparavant” et “Maintenant” ou “Auparavant” et “Juste Après”)
> Préférences
> Aide

Apple va-t-il tirer profit de ce projet Open Source pour que Time Machine puisse également supporter ZFS ?
