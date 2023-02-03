---
layout: post
title: Apple devrait fournir une JVM 64 bits avec Mac OS X Léopard
date: 2007-05-13
category: WWDC
---

[Léopard]: https://web.archive.org/web/20210617204628/http://www.apple.com/fr/macosx/leopard/ "Archive page d´Apple consacrée à Léopard"
[système d’exploitation 64 bits]: https://web.archive.org/web/20210617204628/http://www.apple.com/fr/macosx/leopard/64bit.html "Archive page d´Apple consacrée au 64 bits de Léopard"
[WWDC07]: https://web.archive.org/web/20210617204628/http://developer.apple.com/wwdc/sessions/ 
[Session 147]: https://web.archive.org/web/20210617204628/http://developer.apple.com/wwdc/sessions/index.html#147
[Session 535]: https://web.archive.org/web/20210617204628/http://developer.apple.com/wwdc/sessions/index.html#535
[Session 138]: https://web.archive.org/web/20210617204628/http://developer.apple.com/wwdc/sessions/index.html#138
[Session 5032]: https://web.archive.org/web/20210617204628/http://developer.apple.com/wwdc/sessions/index.html#5032
[Session 1059]: https://web.archive.org/web/20210617204628/http://developer.apple.com/wwdc/sessions/index.html#1059


Apple va sortir cette année une nouvelle version de son système d’exploitation, [Léopard].
Une des particularités de Léopard, c’est que ce sera un [système d’exploitation 64 bits].

Et lorsqu’on fouille l’agenda du [WWDC07], on y trouve quelques sessions concernant Java:

[Session 147]\: Advanced Java Development on Mac OS X
[Session 535]\: Bring Your Java Application to Mac OS X Leopard
[Session 138]\: Discover Java on Mac OS X Leopard
[Session 5032]\: Java and WebObjects Lab
[Session 1059]\: Java on Mac OS X Lab

Or, lorsque vous demandez de voir les détails du contenu de la session 147, voici ce qu’on peut y lire (c’est nous qui soulignons)

>  Listen as members of Apple’s Java engineering team show you how to add polish to your Java application. Learn how to use resolution-independent artwork, adopt custom Aqua controls from within Swing, and how to open documents from the Finder. You will also discover tricks for integrating toolkits such as SWT and Cocoa within your application, and find out if your application should go 64-bit. This session covers the advanced features you need to maximize the features of Java on Mac OS X Leopard.

et pour la session 138, il est dit ceci

>  New features and performance enhancements make Java a greatly improved technology on Mac OS X Leopard. Discover how Leopard makes the Java development experience better than ever with resolution independence, a crisper Aqua look and feel, a 64-bit virtual machine, and more. Get the latest news on WebObjects and find out how other developers are using Java successfully on Mac OS X.

Ce qui semble indiquer qu’Apple compte fournir avec Mac OS X Léopard une version 64 bits de la JVM. Etant donné que Java 6 n’est toujours pas sorti en version finale sous Mac OS X, on peut supposer, que Mac OS X Léopard sera livré avec une version 64 bits de Java 6.

Notez également, au passage, que la session 147 expliquera également comment intégrer SWT et Cocoa dans vos applications Java. Que du bonheur.

Une autre session qui devrait intéresser pas mal de développeurs Java sous Mac OS X, est la session 315: Tracing Software Behavior with DTrace

>  Get an introduction to DTrace, the popular open source project that Apple has optimized for and integrated into Mac OS X. DTrace is embedded in the core of Leopard, underpinning many analysis instruments in the new Xray application. Learn how to directly interact with DTrace from the command line to observe the runtime behavior of an application, the kernel, or the entire system to gain valuable insight.

Avoir une JVM 64bits ainsi que DTrace sous Mac OS X Léopard rend cette plateforme encore plus intéressante pour les développeurs Java.

Reste à voir maintenant si Apple sortira une version finale de Java 6 32bits pour les OS précédents à Léopard. Vu le passé d’Apple, nous avons bien peur que non. Mais lorsqu’on voit toutes les nouveautés qui seront intégrées dans Mac OS X Léopard, il serait tout de même dommage de s’en priver.
