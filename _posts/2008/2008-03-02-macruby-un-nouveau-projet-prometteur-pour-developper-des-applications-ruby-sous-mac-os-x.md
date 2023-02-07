---
date: 2008-03-02
category: Programmation
title: "MacRuby : un nouveau projet prometteur pour développer des Applications Ruby sous Mac OS X"
---

Alors que les développeurs Ruby sous Mac OS X ont déjà la possibilité de développer des Applications Ruby qui s’intègrent au mieux avec le Mac OS X grâce à RubyCocoa qui fait office de passerelle entre Ruby et Objective-C, voilà qu’Apple annonce un tout nouveau projet sur MacOSForge.net, nommé MacRuby.

## Mais qu’est ce que RubyCocoa et MacRuby ?

Le projet RubyCocoa est un projet OpenSource, sous licence GPL, [hébergé sur sourceforge.net][RubyCocoa].
Le but de ce projet est d’établir une passerelle entre Ruby et Objective-C, permettant depuis Ruby de contrôler des objets Objective-C et vice-versa. Il est ainsi possible d’écrire des applications Cocoa où Ruby et Objective-C peuvent être mélangés.

Non seulement RubyCocoa est livré avec Mac OS X 10.5, Léopard. D’ailleurs, Apple a profité de la mise à jour de Mac OS X 10.5.2 pour mettre à jour la version de RubyCocoa qui est livré avec, la 0.13.2. Mais RubyCocoa est également disponible pour Mac OS X 10.4, Tiger.

Le projet MacRuby quant à lui, est un tout nouveau projet, conduit par Apple, également OpenSource, sous licence Ruby, et [hébergé sur MacOsForge.net][MacRuby].

A la différence de RubyCocoa, MacRuby est en fait, une version de Ruby (actuellement, c’est la version 1.9 de Ruby qui est implémentée) qui tourne grâce au Runtime d’Objective-C, et qui tire profit du système de Garbage Collector d’Objective-C.

Une autre différence, est que tous les objets Ruby, sous MacRuby, sont également des objets Objective-C, puisqu’ils héritent de NSObject. Les classes primitives Ruby que sont String, Array, Hash, héritent de leur équivalent Objective-C, NSString, NSArray, NSDictionary.

Il est donc très aisé de passer un String ou un Array Ruby vers une classe Objective-C qui demande un NSString ou NSArray comme argument. Et cela se fait sans aucune nécessité de conversion.

On voit déjà quelques uns des avantages, prometteurs, de MacRuby par rapport à RubyCocoa.

Si vous désirez en savoir plus sur MacRuby, nous ne pouvons que vous conseiller d’aller jeter un oeil sur [sa page d’accueil][Accueil].

[RubyCocoa]: https://web.archive.org/web/20210617202216/http://rubycocoa.sourceforge.net/HomePage
[MacRuby]: https://web.archive.org/web/20210617202216/http://ruby.macosforge.org/
[Accueil]: https://web.archive.org/web/20210617202216/http://trac.macosforge.org/projects/ruby/wiki/MacRuby
