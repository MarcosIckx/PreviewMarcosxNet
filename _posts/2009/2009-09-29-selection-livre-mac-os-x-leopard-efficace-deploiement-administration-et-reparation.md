---
date: 2009-09-29
category: Livres
title: "Sélection livre : Mac OS X Leopard efficace : Déploiement, administration et réparation"
---
Aujourd’hui, je vais vous parler du livre 
[“Mac OS X Leopard efficace : Déploiement, administration et réparation”][Livre]
, publié dans la collection “Sans taboo” aux éditions Eyrolles.

L’auteur de ce livre, [Guillaume Gete][ggete], n’a pas commencé son livre sur Mac OS X Leopard de façon classique, comme le font la plupart des autres auteurs. En effet, la plupart des livres sur Mac OS X Leopard commence généralement par vous expliquer comme installer et configurer Mac OS X Leopard.

Ici, ce n’est pas le cas.

[Guillaume Gete][ggete] va d’abord rapidement revenir sur le genèse de Mac OS X Leopard. Pour ensuite nous expliquer que même si on retrouve dans un Mac les même composants que l’on retrouve dans un PC, il existe de subtiles différences qui font justement toute la différence entre un Mac et un PC.

Même lorsqu’il aborde l’installation et la configuration de Mac OS X Leopard, il ne le fait pas comme les autres puisqu’il explique d’abord les utilitaires qu’on peut trouver sur le DVD d’installation, ensuite les différentes stratégies (1 ou plusieurs partitions ? Quel schéma de partition ? Quel format de volume ? RAID ou pas ? …) pour enfin aborder l’installation de Mac OS X. Et ensuite la restauration de Mac OS X Leopard.

[L’auteur][ggete] passe également pas mal de temps à expliquer l’organisation des fichiers sous Mac OS X Leopard tel qu’elle est en réalité (ce que l’on voit dans le terminal) et telle qu’elle nous est présentée par le Finder. Y sont abordés les dossiers systèmes les dossiers invisibles, les différents types de comptes, les autorisations. Comment Mac OS X gère les classes de permissions Posix, les listes de contrôles d’accès, comment les permissions sont gérées, …

Est également abordé ce qu’est une application Carbon, une application Cocoa, à quoi sert Rosetta, le futurs de Carbon et Cocoa, …

Vient enfin (chapitre 7) les grandes nouveautés de Mac OS X Leopard où TimeMachine est abordé de façon trop superficielle à mon goût, mais Mail et les différents protocoles que sont SMTP, POP3, IMAP sont abordés, ainsi que Microsoft Exchange.

Le chapitre consacré aux polices de caractères m’a ouvert les yeux sur bien des choses. J’avais toujours considéré les polices de caractères comme de simples fichiers de données. J’ai réalisé qu’une police de caractères se devait plutôt d’être traité comme un logiciel à part entière. Et qui dit logiciel dit licence d’utilisation, achat de licence, …

Le chapitre de la sécurité est un chapitre à ne pas lire à la légère. Ce n’est pas parce qu’on a un Mac qu’on doit prendre à la légère la sécurité de ses données. C’est le seul livre que j’ai lu jusqu’à présent (j’en ai lu bien plus que ceux que je mentionne sur mon blog) qui explique aussi clairement ce qu’est FileVault et comment cela fonctionne, les conséquences de sont utilisations, mais aussi ses limites.

Après avoir parlé de l’impression sous Mac (et donc, de CUPS, le système d’impression de Mac OS X), on a droit à 3 chapitres sur les différents réseaux, protocoles, service d’annuaires, …

Vient ensuite l’administration du Mac depuis la ligne de commande et l’administration de Mac OS X au jour le jour.

Ca, c’était pour décrire un peu ce que vous pouvez trouver dans le livre.

Voici maintenant pourquoi j’ai beaucoup aimé ce livre.

J’ai beaucoup aimé ce livre car il m’a fait découvrir la face caché de l’OS. A chaque fois que cela était possible, Guillaume Gete nous explique comment la fonctionnalité a évolué dans le temps pour devenir ce qu’elle était et en indiquant même où cela allait aller.
Pour prendre un exemple bien concret, lorsqu’il aborde à la page 143 de son livre le mystère du double-clic résolu, il commence tout d’abord pour nous parler des codes type et créateur, ce qui existait avant Mac OS X. Ensuite, il aborde les extensions de fichiers, apparus avec Mac OS X (page 144) pour finalement aborder page 146 les UTI : pour en finir avec les extensions.

Bref, on retrouve dans ce livre qui date déjà de plus d’1 an maintenant ce que Daniel Eran Dilger a écrit récemment sur AppleInsider lorsqu’il a parlé de UTI et des codes types . ([http://www.appleinsider.com/articles/09/09/22/inside_snow_leopards_uti_apple_fixes_the_creator_code.html&page=1][Ai])

En fait, si vous avez lu [le livre de Guillaume Gete][Livre], vous n’auriez pas du tout été surpris en découvrant l’article de Daniel Eran Dilger.

Une autre chose qui m’a également frappé, c’est la facilité avec laquelle [Guillaume Gete][ggete] arrive à expliquer des choses quelque peu complexe. Ainsi lorsqu’il aborde la sécurité sur Mac (chapitre 9), et qu’il y explique FileVault, le trousseau de clef, kerberos, je ne me souviens pas d’avoir entendu lors des différentes formations de sécurité que j’ai suivi ou lu sur des sites ou des livres consacré au Mac et à la sécurité une façon aussi claire d’expliquer Kerberos en théorie. L’analogie qu’il fait entre Kerberos et le fonctionnement d’un ticket d’entrée dans un parc d’attraction fait que finalement on comprend de quoi il retourne. Ca ne fait pas de nous des experts en Kerberos. Mais ca n’empêche que ca m’a permis d’enfin avoir compris son fonctionnement. Je suis souvent dur à la détente. Mais jamais eu cette impression durant la lecture de ce livre.

Bref, si vous désirez mieux connaitre votre Mac OS X, son fonctionnement interne, ses technologies, et mieux l’administrer, je ne peux que vous conseiller ce livre. Ce livre va vraiment bien plus loin que les autres livres consacrés à Mac OS X Leopard que j’ai eu l’occasion de lire.

Attention que [l’auteur][ggete] nous a préparé un nouveau livre : Mac OS X Snow Leopard efficace. D’après ce qu’il a écrit sur [son blog][blog], ce ne sera apparemment pas juste une mise à jour pour Snow Leopard.

> Je suis en train de finaliser avec l’équipe d’Eyrolles mon prochain livre qui portera sur Snow Leopard. Baptisé Mac OS X Snow Leopard Efficace (on ne change pas une équipe qui gagne), ce livre aura un positionnement différent de Leopard Efficace. En effet, il sera plus orienté utilisation avancée pour power user qu’administration du Mac en entreprise. En clair : ce nouveau livre devrait être bien plus accessible à nombre d’entre vous ! J’ai essayé de le blinder en astuces pour augmenter la productivité sur votre Mac, et me suis attaché à essayer d’expliquer certaines technologies assez complexes (en particulier autour du réseau) de la façon la plus simple possible. J’ai également voulu que le livre apporte le maximum d’informations les plus justes possibles : aussi, l’intégralité du livre a été finalisé à partir de la GM de Snow Leopard. Ceci explique donc le délai entre la sortie de Mac OS X 10.6 et celle du livre…
> 
> Autre nouveauté par rapport au précédent bouquin : celui-ci sera intégralement en couleurs, miam !

J’attends donc ce nouveau livre tout en couleur avec impatience, pour le mettre à coté du précédent. Ils devraient vraiment bien se completer.

[Livre]: https://web.archive.org/web/20210617212412/http://www.amazon.fr/gp/product/2212122632?ie=UTF8&tag=marconet-21&linkCode=as2&camp=1642&creative=6746&creativeASIN=2212122632
[ggete]: https://www.gete.net/
[blog]: https://blog.gete.net/2009/09/09/snow-leopard-efficace-bientot-dans-les-bacs/
[Ai]: https://web.archive.org/web/20210617212412/http://www.appleinsider.com/articles/09/09/22/inside_snow_leopards_uti_apple_fixes_the_creator_code.html&page=1

