---
date: 2011-07-25
category: macOS
title: Dans Mac OS X Lion apparait un process nommé pbox. Qu’est ce que ce process pbox ?
---
Dans Mac OS X Lion (10.7), dans la liste des processus en cours d’exécution, vous pouvez voir un process nommé pboxd.
Qu’est-ce que ce process ? A quoi sert-il ?

pboxd est le diminutif de PowerBox Daemon. Ce daemon va permettre aux applications tournant dans le bac à sable (sandbox) d’intéragir avec des ressources situées en dehors du bac à sable.

Ainsi, une application, du style traitement de texte par exemple, tournant dans le bac à sable n’a par défaut aucun accès en lecture/écriture à vos fichiers. Lorsque vous demanderez à votre application d’ouvrir un fichier, l’application va interagir avec le PowerBox Daemon, qui va vous afficher la boite de dialogue “ouvrir un fichier”, vous permettant de sélectionner le fichier que vous désirez ouvrir dans le traitement de texte.

Votre application gagnera ainsi les droits de lecture pour ce fichier, et uniquement ce fichier là.

Le PowerBox Daemon va également permettre à votre application d’utiliser les services qui apparaissent dans le menu Service.

