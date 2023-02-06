---
title: Java 5 ne sera pas la dernière version de Java sous Mac OS X
date: 2007-10-30
category: Java
---

n fouinant sur le site de l’Apple Developper Connection dédié à Java, on trouve, en libre accès (sans même devoir s’inscrire), le PDF intitulé
Java on Mac OS X v10.5 Release Notes

On y apprend de tas de choses intéressantes.

1. Tout d’abord, il y est dit que Mac OS X v10.5 est livré aussi bien avec J2SE 5.0 (1.5.0_13-b05) et J2SE 1.4 (1.4.2_16-b05). Il n’y a pas de support de J2SE 1.3 sous Mac OS X v10.5.

Apple recommande fortement l’utilisation de J2SE 5.0, notant J2SE 1.4 comme déprécié.

2. Java est disponible dans toutes les langues standards de Mac OS X. Y compris donc les nouvelles langues qui sont apparues dans Leopard.

3. On y apprend que Java 5 fonctionne en 64 bits sous Leopard. Mais si on lance Java depuis le terminal, c’est par défaut la version 32 bits qui est lancée. Il suffit de rajouter les paramètres ‘-d32′ ou ‘-d64′ pour forcer l’usage de la version 3é ou 64 bits de la JVM. Du moins, pour les machines Intel.

Parmi la longue liste des problèmes connus et résolus, celui-ci me semble le plus intéressant pour les développeurs Java puisqu’il devrait leur donner de l’espoir :

> The Aqua Look and Feel in Mac OS X Leopard is a new implementation, and does not provide
> backwards compatibility to any client code that uses classes in the apple.laf.* package. The legacy Aqua Look and Feel classes are present in this release for Mac OS X, but will be disabled and/or removed in future releases of Java on Mac OS X.

puisqu’Apple y parle de supprimer le support des classes apple.laf.* dans les futures versions de Java sur Mac OS X. Ce qui laisse sous-entendre que Java 1.5 n’est pas la dernière version de Java sur Mac OS X.

Lisez la [Release Note de Java sur Mac OS X v10.5][Release Note]

[Release Note]: https://web.archive.org/web/20210617211150/http://developer.apple.com/releasenotes/Java/JavaLeopardRN/JavaLeopardRN.pdf
