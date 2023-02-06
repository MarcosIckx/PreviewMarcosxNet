---
layout: post
author: Marcos Ickx
title: "WWDC 2007: Developper sous Leopard ? Oui, mais sous MacIntel"
description: Apple annonce a le WWDC 2007 des nouveautés pour développer pour macOS Léopard. Mais ils ne sont disponibles que sous Mac Intel
date: 2007-06-16
category: WWDC
---

Plus on avance dans la semaine, plus on se rend compte qu’Apple délaisse clairement de plus en plus la plateforme PPC.

Si vous êtes développeurs Mac ou sous Mac, vous êtes invité à passer aux MacIntel.

Qu’est ce qui nous fait dire cela ?

## Leopard 64Bits


Tout d’abord, il faut savoir que lors du KeyNote de lundi, Steve Jobs avait présenté parmi les 10 nouveautés choisies sur les 300 contenues dans Leopard le fait que Leopard serait un OS 64 bits

Seulement voilà. Il semble tout d’abord que Leopard ne sera pas disponible pour les Mac tournant avec un PPC G3. Leopard ne tournerait que sur un G4, G5 ou MacIntel.

## Rosetta

Alors que Steve Jobs a bien dit que Cocoa serait également en 64 bits, il semblerait que Rosetta, qui permet de faire tourner des applications PPC sur Intel n’est pas 64 bits.

Un développeur Mac sous PPC est donc obligé de soit garder son application PPC en 32 bits pour qu’elle puisse également tourner sur les MacIntel via Rosette. Soit rendre son application 64bits disponible en UB (Universal Binary. Application ayant le code PPC et le code Intel. Plus d’émulation via Rosetta dans ce cas).

## Java 6 uniquement sur MacIntel ?

Pour un développeur Java, ca risque d’être encore plus ennuyant.

Vu que les sessions consacrées à Java était concentrées sur la fin de la semaine principalement, il nous a fallu attendre un peu plus pour savoir de quoi il retourne.

Mais, on peut déjà dire que nos dires se confirment.

Tout d’abord, Apple a profité du WWDC pour mettre à jour son site. Du moins la partie anglaise. Or on retrouve sur cette page consacrée au 64Bits (vu que Léopard sera un OS 64Bits) la mention suivante:

> 64-bit frameworks.
> 
> In addition to the POSIX and math libraries supported in Tiger, Leopard enables developers to build complete 64-bit applications using the Cocoa, Quartz, OpenGL, and X11 GUI frameworks. You can even use 64-bit Java on capable Intel processors. And the 64-bit and 32-bit versions of the libraries are built from exactly the same code base, to ensure a consistent experience for both developers and users.

De plus, quelqu’un qui était présent au WWDC a dit ceci concernant la session « Discover Java for Leopard ».

> Pas vraiment de grosses nouvelles, sauf que si vous êtes intéressés par Java 6, vous êtes mieux de passer à Intel si vous êtes encore sur PPC.

Qu’est ce que cela signifie.

Si en s’en tient à ce que dit Apple,

1. il y aura bien un JVM 64Bits disponible pour léopard.

2. la version 64bits de la JVM sera disponible UNIQUEMENT pour ceux qui ont des Mac Intels. Ce qui est dommage pour les possesseurs de Mac PPC.

Si on recoupe cela avec les déclarations de la personne présente au WWDC,

3. Il est évident que cette version 64Bits de Java sera Java 6.

Mais rien ne dit qu’il y aura une version 32 bits de Java 6 disponible pour les Mac PPC. Assez génant, n’est-ce pas. (remarquez que rien ne dit le contraire non plus. Faudra attendre la verion public de Leopard pour savoir finalement quoi)

## Les jeux uniquement sur MacIntel

Toujours durant le Keynote, Steve Jobs a fait monter sur scène des patrons de société de jeux annoncant que les possesseurs de Mac pourraient jouer. Seulement voilà. Le même jour, TransGaming fait savoir à tous que cela est rendu possible grâce à la technologie Cider qu’elle vend. Le seul hic. C’est que cela n’est possible que sous les MacIntel. Les possesseurs de Mac PPC ne pourront pas profiter de ces jeux. Et vous, en tant que développeur, il vous faut développer vos jeux sous Windows, et utiliser Cider pour les faire tourner sous Mac OS X mais uniquement sur des machines MacIntel.

## Conclusion
Il est clair que les Mac PPC ont vraiment un pied dans la tombe. Et qu’un développeur Mac a intérêt, si cela n’est pas encore fait, à s’acheter un MacIntel rapidement après la sortie de Leopard. Pour les développeurs Java, la question est de savoir si Apple sortira tout de même une version 32 bits de Java SE 6 pour les Mac PPC. C’est à espérer.
