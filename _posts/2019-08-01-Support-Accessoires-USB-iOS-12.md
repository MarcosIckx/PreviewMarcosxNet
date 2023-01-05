---
layout: post
title: Support des accessoires USB sous iOS 12
date: 2019-08-01
tags: [Accessoires, USB, iOS12]
category: iOS12
---

# Support des accessoires USB sous iOS 12

En prévision de la sortie d’iPadOS, je me suis acheté l’adaptateur lightning-USB 3

[![Photo de l’adaptateur Lightning-USB 3 d’Apple]][Amazon-Adaptateur-Lightning-USB3]

avant que ce ne soit la ruée et qu’ils soient en rupture de stock.

Je l’ai reçu aujourd’hui. Voici mes premières impressions.

# Premier Branchement

Premier branchement de l’adaptateur au lightning à l’iPad (2018) sous iOS 12.4.
Il m’affiche un message disant que l’écran doit être déverrouillé pour que je puisse utiliser l’adaptateur.
Je déverrouille donc l’écran de mon iPad.
Et hop, je vois surgir cette popup. 

![Alerte Mise à Jour d'accesoire disponible]


Je choisi de mettre à jour plus tard.

En attendant, je vais dans les Réglages > Général > Informations.

Une nouvelle ligne apparaît pour l’adaptateur. 

![Nouvelle entrée dans Réglages > Général > Informations pour l'adaptateur Lightning - USB 3]

Et dans les infos détaillées, on apprend que la version du programme interne est la version 1.0.1.

![Version du programme interne de l'adaptateur Lightning - USB 3]

Mais rien à cet endroit ne m’indique qu’une nouvelle version du programme interne de l’adaptateur est disponible et rien ne me permet maintenant d’appliquer la mise à jour.

Personnellement, connaissant le sens du détails d’Apple, j’étais un peu déçu.

Je débranche l’adaptateur, verrouille l’iPad, rebranche l’adaptateur et déverrouille l’iPad.

J’ai du coup à nouveau le message m’invitant à faire la mise à jour de l’adaptateur, ce que j’accepte cette fois-ci.

La mise à jour de l’adaptateur commence, mais pendant cette mise à jour (qui dure un peu de temps), je remarque que l’iPad n’est plus alimenté via ce même adaptateur.

Ça va le faire. J’ai 70% de batterie.

Mais je me pose quand même la question.

Est-ce qu’Apple vérifié le niveau de la batterie avant d’accepter la mise à jour, question que la mise à jour ne s’arrête pas en plein milieu faute de courant ?

Connaissant Apple, je suppose que oui. 

Mais je ne peux l’affirmer.

Bref, voilà, la mise à jour est faite.

La version du programme interne de l’adaptateur est donc passé de la version 1.0.1 à 1.0.5.

![Version du programme interne de l'adaptateur Lightning - USB 3 après mise à jour]

# En route pour quelques tests.

## Clavier

J’avais acheté en 2017 un petit clavier/trackpad pour dépanner quelqu’un (la moitié de l’écran de sa tablette Android ne répondait plus au toucher)

[![Clavier/Trackpad avec Dongle USB]][Amazon-Clavier-Trackpad-Dongle]

C’est avec un dongle USB et transmission entre clavier et le dongle.

Je branche donc le dongle à l’adaptateur lightning-USB.

J’allume le clavier, et hop … 

Il a été reconnu directement en AZERTY.
(C’était pas le cas sous Android.  Je me souviens avoir sué)

Les touches pour gérer le volume, la musique, les flèches.

Tout ça fonctionne. 

Sauf le trackpad 🙁

Ce qui est tout à fait normal puisque je suis actuellement sous iOS 12.4.

## Hub Alimenté
Essayons maintenant d’y connecter un hub USB alimenté.

Qui servira non seulement à alimenter l’iPad mais aussi à brancher le dongle USB du clavier.


J’ai opté pour ce hub USB 3.0 7 ports avec alimentation 24W.

[Hub USB 3.0 7 Ports avec alimentation 24 Watts][Amazon-Hub-USB-3.0-7Ports]

Je branche donc ce hub à la prise murale.

Je branche le câble lightning de l’iPad à ce hub USB au lieu de l’adaptateur secteur livré avec l’iPad. 

La recharge de l’iPad se fait.

C’est bien 👍

Je branche maintenant le hub USB à la prise USB de l’adaptateur Lightning - USB 3, lui-même branché à l’iPad.

J’ai donc 2 fils partant du hub USB vers l’adaptateur Lightning-USB raccordé à l’iPad : 

* 1 pour alimenter l’iPad via le port lightning de l’adaptateur, 
* l’autre pour l’USB

Sur l’un des 6 ports USB encore libre de l’hub USB, j’y branche le dongle du mini clavier/trackpad.

J’allume le clavier. 
Et … 
ça marche aussi bien que si le dongle avait été branché directement à l’adaptateur lightning-USB de l’iPad.

Mais j’ai encore 5 ports USB de libres.

## Casque Micro USB
Et si on branchait un casque-micro USB ?

J’ai un casque plantronics similaire à celui mentionné dans le lien sous la main 
[Casque Micro Plantronics][Amazon-Casque-Micro-USB]

À peine branché, l’icône de l’App Musique apparaît dans le dock avec le symbole des écouteurs 🎧. Un très bon signe.
Et ça marche.


![Le symbole 🎧 apparait dans l'icône de l'App Musique à la droite du Dock]

Essayons maintenant le micro. Je lance donc l’app Dictaphone, j’appuie sur le bouton record. Et ça enregistre ma voix depuis le micro-casque. Superbe nouvelle.

## Clef USB

Essayons une clef USB

Je branche une clef USB au hub USB, et l’app photo d’iOS 12 se lance.

Bon. C’est juste l’importation des photos / vidéos qui est proposée.

Rien d’autre n’est accessible.

Mais ça changera avec iPadOS (et de même sous iOS 13).

J’ai donc maintenant un clavier avec un dongle USB, in micro-casque USB et une clef USB raccordés à l’iPad via l’adaptateur.

Et tous les 3 sont reconnus.

## L'iPhone

Et si je branche mon iPhone ?

Et bien non seulement l’iPhone se charge, mais je peux importer les photos de l’iPhone vers l’iPad si je le désire.

Du coup, j’ai découvert que la photo de  fond d’écran de mon iPhone n’était pas présente dans la photothèque de mon iPad.

Mais j’ai découvert également ceci:

![Dans les Réglages, entre Wi-Fi et Bluetooth apparait une entrée Ethernet dont l'interface est nommée USB iPhone]

![Les infos détaillées de la connection Ethernet]

Oui. Mon iPad a maintenant une connection câblée ethernet via l’iPhone connecté en USB. 

Ça peut toujours être utile, cela.

Malheureusement, rien n’y fait. 

J’arrive pas à surfer sur Internet de cette façon.

Si quelqu’un a une idée du pourquoi. 

Qu’il me fasse signe.

@Sylvain Gamel m'a demandé si j'avais activé le partage de connexion sur l'iPhone.

Je reviens de faire le test, et non, malgré activation du partage de connexion, je n’arrive pas à établir de connexion réseau filaire entre iPad et iPhone.

C’est comme s’il établissait juste la connexion filaire entre iPad et iPhone pour permettre l’import des photos et vidéos et c’est tout. 

Mais pas pour permettre le partage de sa connexion internet. 

Mais bon, on a le partage de connexion en Wi-Fi entre eux qui est dispo.

J'aurais pensé que le partage fonctionnait dans ce genre de contexte. 

Surtout que cela est possible lorsque l’iPhone est raccordé en USB à un Mac.

Mais c'est un poil exotique comme configuration en même temps…

## Lecteur de carte d'identité
J’ai essayé un lecteur de carte d’identité, fort utilisé en Belgique pour accéder aux sites du gouvernement. 

Malheureusement, ça ne marche pas 🙁 mais c’est plus un soucis logiciel que matériel. 

Maintenant, aucune idée si iPadOS va contenir les briques pour cela. Wait & See.

## Écran USB
j'ai également un écran LG Flatron L206WU qui a la particularité de supporter le DisplayLink via un câble USB.

Il fallait donc que je teste cela aussi.

J'ai donc raccordé l’iPad avec l’adaptateur à l’écran DisplayLink.

L’écran sortant de veille, j’avais bon espoir, mais il est resté de marbre (enfin, écran noir).

Je force l’écran à prendre comme source l’USB. 
Mais j’ai toujours un écran noir.

Côté iPad, j’ai eu droit à un message (désolé, j’ai oublié de faire une capture d’écran) me disant qu’il ne peut lire de fichiers.
Il a l’air de reconnaître l’écran comme étant une clef USB 🤔

Est-ce que iPadOS supportera les écrans DisplayLink ?

Je referai le test une fois iPadOS disponible pour vérifier cela encore une fois.

Sur macOS, il faut installer un driver pour que les écrans DisplayLink soient reconnus.

Et [Apple avait tout cassé avec macOS 10.13.4][macOS-10.13.4-Disables-DisplayLink].

Et ceux qui avait acheté duet display étaient vus.

DisplayLink a du sortir des drivers 5.1 pour Mojave.

Mais bon, ça ne coûtait rien d’essayer ce qui se passerait avec l’iPad.

# Résumé

Pour résumer, j’ai donc l’iPad connecté via les prises lightning et USB de l’adaptateur au hub USB alimenté. 

À cet hub USB, J’ai 
* un mini clavier/trackpad sans fil connecté via un dongle ( seul le clavier fonctionne _iOS 12)
* un micro-casques USB
* une clef USB
* un iPhone


Par contre, point de vue câblage, on est d’accord que c’est juste l’horreur. 

![Le Hub USB connecté à l'adaptateur Lightning - USB d'un coté pour l'alimenter. D'un autre coté pour faire office de Hub USB. Et le clavier/trackpad, l'iPhone et le casque micro branchés au Hub USB]

![Le HUb USB connecté à l'adaptateur Lightning - USB d'un coté pour l'alimenter. D'un autre coté poir faire office de Hub USB. Et le clavier/Trackpad, l'iPhone, le casque micro, et finalement la clef USB. Tout cela branché au Hub USB]

Et avoir toujours cet adaptateur qui pendouille à l’iPad, c’est pas vraiment le top. 

Combien de temps tiendra-t-il ?
Mystère.


[macOS-10.13.4-Disables-DisplayLink]: https://plugable.com/2018/03/30/macos-10-13-4-disables-displaylink-duet-display-devices/ "Lien vers article concernant le support d´écran DisplayLink"

[Amazon-Casque-Micro-USB]: https://www.amazon.fr/dp/B0775S8X5C/ "Lien vers Amazon.fr pour Casque Micro USB"

[Amazon-Hub-USB-3.0-7Ports]: https://www.amazon.fr/gp/product/B07JGRTPJS/ "Lien vers Amazon.fr pour Hub USB 7 ports"

[Amazon-Clavier-Trackpad-Dongle]: https://www.amazon.fr/gp/product/B071L2CL4Y/ "Lien vers Amazon.fr pour mini clavier trackpad avec dongle USB"

[Amazon-Adaptateur-Lightning-USB3]: https://www.amazon.fr/gp/product/B01DGDNL2G/ "Lien vers Amazon.fr pour l´Adaptateur Lightning USB3 d´Apple"


[Photo de l’adaptateur Lightning-USB 3 d’Apple]: /img/posts/2019/08/01/Support-Accessoires-USB-iOS-12/Adaptateur-lightning-usb3.jpg "Photot Adaptateur Lightning - USB3 d´Apple"

[Alerte Mise à Jour d'accesoire disponible]: /img/posts/2019/08/01/Support-Accessoires-USB-iOS-12/Alerte-miseajour-accessoire.jpg "Alerte pour indiquer qu'une Mise à jour du firmware est disponible pour l'accessoire"


[Nouvelle entrée dans Réglages > Général > Informations pour l'adaptateur Lightning - USB 3]: /img/posts/2019/08/01/Support-Accessoires-USB-iOS-12/Reglages-General-Information.jpg "La nouvelle entrée dans Informations pour l'adaptateur Lighning-USB3"

[Version du programme interne de l'adaptateur Lightning - USB 3]: /img/posts/2019/08/01/Support-Accessoires-USB-iOS-12/Version-Programme-Interne-Adaptateur-1.0.1.jpg "Version du programme interne de l'adaptateur Lightning - USB 3 lors de son premoer branchement"

[Version du programme interne de l'adaptateur Lightning - USB 3 après mise à jour]: /img/posts/2019/08/01/Support-Accessoires-USB-iOS-12/Version-Programme-Interne-Adaptateur-1.0.5.jpeg "Version du programme interne de l'adaptateur Lightning - USB 3 après la mise a jour"

[Clavier/Trackpad avec Dongle USB]: /img/posts/2019/08/01/Support-Accessoires-USB-iOS-12/Clavier-trackpad-dongle-usb.jpeg "Photo du mini clavier trackpad avec dongle USB"

[Le symbole 🎧 apparait dans l'icône de l'App Musique à la droite du Dock]: /img/posts/2019/08/01/Support-Accessoires-USB-iOS-12/Icone-Apple-music-casque.jpeg "L'App Musique dans le Dock avec le symbole 🎧"


[Dans les Réglages, entre Wi-Fi et Bluetooth apparait une entrée Ethernet dont l'interface est nommée USB iPhone]: /img/posts/2019/08/01/Support-Accessoires-USB-iOS-12/Reglages-Ethernet.jpeg "Entrée Ethernet dans les réglages"

[Les infos détaillées de la connection Ethernet]: /img/posts/2019/08/01/Support-Accessoires-USB-iOS-12/Reglages-Ethernet-details.jpeg "Les infos détaillées de la connection Ethernet"


[Le Hub USB connecté à l'adaptateur Lightning - USB d'un coté pour l'alimenter. D'un autre coté pour faire office de Hub USB. Et le clavier/trackpad, l'iPhone et le casque micro branchés au Hub USB]: /img/posts/2019/08/01/Support-Accessoires-USB-iOS-12/cablage-iPhone.jpeg "Le câblage. Photo prise avec l'iPhone SE"

[Le HUb USB connecté à l'adaptateur Lightning - USB d'un coté pour l'alimenter. D'un autre coté poir faire office de Hub USB. Et le clavier/Trackpad, l'iPhone, le casque micro, et finalement la clef USB. Tout cela branché au Hub USB]: /img/posts/2019/08/01/Support-Accessoires-USB-iOS-12/cablage-iPad.jpeg "Le câblage. Photo prise avec l'iPad 2018"
