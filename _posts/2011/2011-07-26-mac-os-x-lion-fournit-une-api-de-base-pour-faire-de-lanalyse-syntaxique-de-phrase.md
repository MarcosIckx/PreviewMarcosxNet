---
date: 2011-07-26
category: Voix
title: Mac OS X Lion fournit une API de base pour faire de l’analyse syntaxique de phrase
---
Hier, en lisant la partie consacrée à Mac OS X Lion du document 
[What’s new in Mac OS X][QdN], j’y ai découvert ceci :

> Linguistic Tagging

Mac OS X v10.7 introduces a linguistic tagging class, 
[NSLinguisticTagger][LT], that lets you break down a sentence into its grammatical components, allowing the determination of nouns, verbs, adverbs, and so on. This tagging works fully for English. The API provides a method to find out what capabilities are currently available in other languages as well.

For more information, see [Foundation Framework Reference][Ref].

En gros, vous passez une phrase, et il va vous dire si ce mot est un nom, un verbe, un adverbe, …

Bref, la base pour pouvoir faire de l’analyse grammaticale. A part que le français n’est que partiellement supporté. Seul l’anglais est actuellement complètement supporté.

[QdN]: https://web.archive.org/web/20210518042224/http://developer.apple.com/library/mac/releasenotes/MacOSX/WhatsNewInOSX/WhatsNewInOSX.pdf
[LT]: https://web.archive.org/web/20210518042224/http://developer.apple.com/library/mac/#documentation/Cocoa/Reference/NSLinguisticTagger_Class/Reference/Reference.html#//apple_ref/occ/cl/NSLinguisticTagger
[Ref]: https://web.archive.org/web/20210518042224/http://developer.apple.com/library/mac/#documentation/Cocoa/Reference/Foundation/ObjC_classic/_index.html#//apple_ref/doc/uid/20001091
