---
date: 2008-03-06
category: iPhone
title: Apple a présenté la prochaine mise à jour logicielle de l’iPhone, et son kit de développement
---

Les développeurs vont pouvoir s’en donner à cœur joie. Le SDK pour iPhone est là.

Mais ce n’est pas tout.

Apple m’a vraiment surpris ce soir.

Résumé de la Keynote qu’Apple a tenu ce soir.

## Quelques chiffres
L’iPhone est déjà second sur le marcher des SmartPhones, avec 28% de parts de marcher.

RIM possède 41% de part de marcher.

L’iPhone, c’est 71% du trafic de surf sur internet à l’aide d’un mobile (aux USA).

Mais fini les chiffres. Passons aux choses sérieuses :

## l’iPhone en Entreprise
l’iPhone va s’introruire dans le monde des entreprises, marchant même quelque peu sur les platebandes des Blackberry. En effet, Apple s’est décidé à acheter une licence ActiveSync, permettant à l’iPhone de se synchroniser avec Microsoft Exchange. Ce qui était une condition quasi obligatoire pour pouvoir rentrer dans un entreprise. Tout comme pour les Blackberry, les emails arriveront d’eux-même dans votre iPhone. Plus besoin d’attendre qu’ils se synchronisent avec votre serveur de messagerie. Dès qu’un message vous est envoyé, il sera transmis à votre iPhone. Bref, le push email, ce qui a fait le succès des Blackberry. Egalement la synchronisation des contacts, calendriers, adresses.

Pour s’introduire dans l’entreprise, il fallait aussi proposer du VPN, authentification, certification, WIFI WPA2, politique de sécurité, outils de configuration pour entreprise.

Tout cela sera disponible dans la prochaine mise à jour logicielle de l’iPhone.

Il sera également possible, une fois que l’iPhone aura reçu sa mise à jour logicielle, de bloquer à distance l’iPhone, au cas où celui-ci aurait été volé ou perdu. Cela aussi était important pour les entreprises.



## Un SDK pour l’iPhone
Lorsqu’Apple avait annoncé lors du WWDC 2007, qu’il serait possible d’écrire des Web Applications pour l’iPhone, les développeurs furent fortement déçus, et l’ont fait clairement savoir à Apple. Le développement d’un SDK pour iPhone avait même été démarré.

Aujourd’hui, Apple a finalement présenté son SDK pour iPhone. En fait, ce SDK n’est pas vraiment nouveau. Il existait déjà, puisque c’était celui-là même qui était utilisé par les équipes de développeurs pour l’iPhone. Seulement voilà. C’est une chose que d’avoir des outils de développement interne. C’en est une autre que d’en faire un SDK officiel, qui pourra être utilisé par tout un chacun. Et c’en est encore une autre que de le documenter. C’est ce qu’Apple s’est attelé à faire lorsqu’elle a compris que c’était vraiment cela que les développeurs voulaient.

## Architecture logicielle de l’iPhone

Ce n’est pas un scoop que de dire que les bases logicielles de l’iPhone sont les même que celles que l’on retrouve dans un Mac.

l’OS au coeur de l’iPhone est découpé en 4 couches :

Core OS

Core Service

Media Layer

Cocoa Touch

Les 3 premières couches sont issues de Mac OS X.

La 4ième est elle entièrement nouvelle. En effet, la couche Cocoa telle qu’on la retrouve sous Mac OS X est trop orientée Clavier et Souris. Il a fallu la remplacer par une approche orientée “Touch”. Et donc, ils ont appelé cela “Cocoa Touch”.

## Core OS

Dans le Core OS, on retrouve, bien évidemment le noyau, ou kernel. Mais aussi les librairies systèmes, comme la gestion du protocole TCP/IP, provenant de BSD, la gestion des sockets, de la sécurité, des certificats, des systèmes de fichiers, la technologie Bonjour, mais également la gestion de l’énergie, ou de l’alimentation. Le module en charge de la gestion de l’énergie supervise en fait tous les chips inclus dans l’iPhone, ainsi que les senseurs, et même votre application.

## Core Service

La couche Core Service comprend de nombreux services, Api, qui faciliteront le développement de vos applications. En voici quelques unes :

SQLite : vous permettant de gérer des bases de données pour vos applications

URL Utilities : pour l’accès au Web

Préférences : pour gérer les préférences dans vos applications

Collections, Carnet d’Adresses, Réseaux, Accès Fichiers, Services Réseaux, gestionnaire de Threads, …

Et un autre qui a été mis quelque peu plus en évidence :

Core Location. Il vous permettra de créer facilement des applications qui se baseraient sur l’endroit où vous vous trouvez avec votre iPhone.

## Media Layer

Dans cete couche, on retrouve :

Core Audio,

OpenAL (Utilisé pour les effets surround 2D et 3D),

Audio Mixing,

Audio Recording,

Video Playback,

Support PDF, JPG, PNG, TIFF

Quartz (2D)

Core Animation,

OpenGL ES (spécification d’OpenGL pour les systèmes embarqués)

(Cette liste n’est pas exhaustive)

## Cocoa Touch

Cette couche est, comparée aux 3 autres, très spécifiques à l’iPhone, bien qu’on y retrouve des éléments déjà présents, pour certains, dans les MacBook, MacBook Air et MacBookPro :

Evénements Multi-Touch

Contrôles Multi-Touch

Accéléromètres

Alertes

Vues Hiérarchiques

Internationalisation et Localisation

Web View (rendu pages Web)

People Picker (pour gérer les contacts)

Image Picker (pour gérer les images

Appareil Photo

## Environnement de Développement

Il vous faudra posséder un Mac pour pouvoir développer pour l’iPhone.

C’est XCode qui sera votre environnement de développement pour l’iPhone. Vous aurez accès depuis XCode à la document du SDK, à un débogueur, et même un simulateur pour ceux qui ne possèdent pas d’iPhone.

Il sera possible de faire du “Remote Debugging” si l’iPhone est branché à votre Mac.

L’interface Builder a également été revu pour tenir compte des spécificités de l’iPhone.

Déjà rien que tout cela est fabuleux. Mais le keynote ne s’est pas arrêté là. Car ce qui vient est encore plus soufflant.

## l’iPhone devient une console de Jeux
Pour montrer ce qu’on pouvait faire avec ce SDK, les développeurs d’Apple ont écrit un petit simulateur de Vol spatial. Et c’est en orientant l’iPhone que l’on fait pivoter le vaisseau, descendre, monter, …

Il paraitrait qu’ils n’ont eu besoin que de 2 semaines pour écrire ce petit jeu. Qui fait une belle démonstration de ce que possède l’iPhone dans son ventre.

Mais la grosse surprise, c’est lorsqu’ils ont appelé des représentants de Electronic Arts et de Sega pour montrer ce qu’ils ont pu faire dans un temps très limité avec le SDK, et donner leur réaction.

Electronic Arts est venu présenté une version spécifique pour l’iPhone de “Spoor”, leur nouveau jeu sur l’évolution de la vie. Cela utilise également les accéléromètres pour les déplacements, et il n’aura fallu que 2 semaines à Electronic Arts pour faire l’adaptation du jeu à l’iPhone.

Sega est venu présenté SuperMonkey Ball, jeu qui se joue également en inclinant l’iPhone dans tous les sens. Commentaire de Sega :

“Ceci n’est pas un jeu pour téléphone cellulaire. C’est une console de jeu complète. Et nous avions sous estimé les capacités de l’appareil.”

## Démonstration d’autres applications
AOL était également invité, pour présenter AIM pour iPhone. Développé en 5 jours.

Une démonstration d’une application pour les forces de vente d’une entreprise.

Une autre démonstration d’application pour les docteurs.

Bref, ca promet. La mémoire de l’iPhone risque d’être très vite saturée. Et sa batterie très vite à plat.

## App Store
Mais comment allez-vous bien pouvoir installer toutes ces applications sur votre iPhone ?

via iTunes, pardi. Qui va être enrichi d’une nouvelle section : App Store.

Où il y sera vendu des applications pour l’iPhone.

Vous pourrez ainsi, depuis votre iPhone, en vous rendant sur iTunes, télécharger les applications que vous désirez.

L’App Store sera l’unique moyen pour distribuer vos Applications.

Les développeurs seront libres de fixer le prix de leurs applications. 70% du prix de vente sera reversé au(x) développeur(s) de l’application. Il n’y aura pas de frais à payer pour mettre son application sur l’App Store, ni de frais marketing, ni de frais concernant les cartes de crédits. L’argent sera reversé aux développeurs mensuellement.

Et si vous décidez de ne pas vendre votre application, mais de la donner gratuitement. Et bien Apple prendra 30% du prix fixé (0€) ce qui fera donc 0€. Vous ne serez pas payé par Apple, mais vous ne devrez payer aucun frais à Apple.

Tout le monde sera à la même enseigne. Que vous soyez un petit développeur indépendant, ou une grosse firme de logicielle.

Mais attention. Apple aura un droit de regard sur les applications. Ainsi, pas question de pouvoir proposer via App Store du porno, des malwares, et autres applications qui ne plairaient pas à Apple (VOIP sur le réseau mobile, par exemple _Mais VOIP sur WIFI sera accepté). Pas de logiciels pour désimlocker l’iPhone sur l’App Store.

## Et c’est disponible quand et comment tout cela ?
Une nouvelle mise à jour de l’iPhone, 2.0, est prévue pour fin juin (après la WWDC 2008).

Le SDK est déjà disponible maintenant en téléchargement, mais en Béta.

Les développeurs pourront également avoir la mise à jour de l’iPhone 2 avant les utilisateurs, pour mettre à jour leur iPhone et commencer le développement d’applications.

La mise à jour pour l’iPhone sera gratuite. Mais apparemment payante pour les possesseurs d’iPod Touch.

Le SDK sera téléchargeable gratuitement, mais pour pouvoir publier vos programmes, il vous faudra obtenir un certificat pour signer vos applications. Il vous en coutera 99$. Mais vous devrez payer ce montant qu’une seule fois, apparemment. Ce n’est pas un abonnement annuel, ou une autre astuce de ce genre. EDIT : Eh ben si. C’est 99$ par An, ainsi que 299$ par an pour les entreprises. Et apparemment, même ceux qui ne vendraient pas leurs logiciels devraient payer cette somme annuellement. Aïe.

Cette somme servira à couvrir les frais pour créer un certificat électronique contenant toutes informations vous concernant, vous, développeur.

Il sera même possible de développer des applications uniquement pour votre entreprise. Il vous en coutera alors 299$. Mais attention. Vos applications seront hébergées sur les serveurs d’Apple. En dehors des murs de votre entreprise. Mais accessible que depuis une page privée.

A noter que les inscriptions à ces 2 programmes ne sont pour le moment valable que pour les américains. Il sera étendu prochainement au reste du monde. Il nous faudra donc encore patienter pour cela. En attendant, on peut déjà télécharger le SDK et développer sa première application pour iPhone.

Le montant à payer pour les possesseurs d’iPod Touch n’a pas été communiqué.

## Notre Avis
Personnellement, il y avait longtemps que je n’avais pas été aussi enthousiaste après une annonce d’Apple. Ce qui a été annoncé aujourd’hui n’est vraiment pas rien. Et ne fera, très certainement, que renforcer les ventes de l’iPhone et de l’iPod Touch.

En tout cas, Apple a réussi à piquer ma curiosité. Et peut-être que j’envisagerai, moi qui ne possède même pas de GSM, ni d’iPod (même pas d’autres baladeur), l’achat d’un iPhone ou iPod Touch, juste pour le plaisir de pouvoir y développer toute sorte d’applications.

La vidéo de la keynote : [http://www.apple.com/quicktime/qtv/keynote/][keynote]

l’iPhone en entreprise : [http://www.apple.com/fr/iphone/enterprise/][entreprise]

Le site pour développeurs Apple revisité : [http://developer.apple.com/][developer]

Télécharger le SDK : [http://developer.apple.com/iphone/program/][sdk]

Tous les détails fournit par Apple: [http://developer.apple.com/iphone/program/details.html][details]

[keynote]: https://web.archive.org/web/20210617032428/http://www.apple.com/quicktime/qtv/keynote/

[entreprise]: https://web.archive.org/web/20210617032428/http://www.apple.com/fr/iphone/enterprise/

[developer]: https://web.archive.org/web/20210617032428/http://developer.apple.com/

[details]: https://web.archive.org/web/20210617032428/http://developer.apple.com/iphone/program/details.html
