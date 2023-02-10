---
date: 2011-07-26
category: UI
title: "Marre des animations de fenêtres sous Mac OS X Lion ? Désactivez-la"
---

Vous en avez marre des animations de fenêtres sous Mac OS X Lion ?
Il vous est possible de la désactiver.

Mais ne cherchez pas dans les préférences. Il va vous falloir ouvrir le terminal et écrire le code suivant :

    defaults write NSGlobalDomain NSAutomaticWindowAnimationsEnabled -bool NO

Pour les réactiver, suffit de remplacer `NO` par `YES` dans la commande.

    defaults write NSGlobalDomain NSAutomaticWindowAnimationsEnabled -bool YES
