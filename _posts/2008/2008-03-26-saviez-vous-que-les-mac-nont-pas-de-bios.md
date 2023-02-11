---
date: 2008-03-26
category: Matériel
title: Saviez-vous que les Mac n’ont pas de BIOS ?
---

Toute personne  sait que la majorité des ordinateurs personnels vendus aujourd’hui possèdent encore et toujours un BIOS. Et que c’est ce même BIOS qui est responsable d’aller lire le MBR qui va lui charger l’OS en mémoire (je simplifie grandement. Ne m’en veuillez pas. Si vous désirez en savoir plus sur le BIOS et MBR, allez voir [le tutoriel de Baptiste Wicht sur developpez.com][dvp]).

Mais saviez-vous que les MacIntel n’ont pas de BIOS ? Et qu’ils ne “bootent” pas grâce au MBR ?

Lors de l’abandon des processeurs PowerPC pour les processeurs Intel, Apple n’a pas choisi d’utiliser le BIOS, mais d’utiliser l’EFI.

EFI est l’abréviation de Extensible Firmware Interface.

L’EFI est quelque chose qu’Intel voudrait faire adopter par les constructeurs. Mais pour que les constructeurs adoptent l’EFI, il faudrait que les OS supportent l’EFI. Et, jusqu’à preuve du contraire, l’OS qui a la plus grande part de marché actuellement, c’est Windows.

Et, d’après le site de Microsoft, seules les versions de Windows Server 2003 et 2008 supporte l’EFI pour la plateforme Intel Itanium. Ce qui exclut donc les processeurs Intel Core 2 Duo, qui sont ceux que l’ont retrouve sur la plupart des PC vendus aujourd’hui. Windows Server 2008 devrait également supporter les processeurs Core 2 Duo d’Intel. Mais on ne peut pas dire que ce sont là les versions de Windows que l’on rencontre sur la majorité des PC vendus aujourd’hui. A ce jour, ni Windows XP, ni Windows Vista, sorti l’année passée, ne supporte l’EFI. (Notez qu’on retrouve un support de EFI 2.0 dans le Service Pack 1 de Windows Vista sorti récemment) Ce qui explique grandement pourquoi les cartes mères vendues aujourd’hui, autres que celles équipées du processeur Itanium, sont toujours équipées d’un Bios et n’ont généralement pas d’EFI.

Sauf en ce qui concerne les Mac. Apple, du fait qu’il vend une solution intégrée, a pu, sans aucun problème, ni aucun remord, adopter l’EFI.

Un autre avantage d’utiliser l’EFI au lieu du Bios, tient dans sa première lettre, E, qui signifie Extensible.

Apple pouvait donc étendre les fonctionnalités de l’EFI pour pouvoir proposer sous MacIntel les même fonctionnalités qu’elle proposait déjà sur les Mac PowerPC, comme, par exemple, le Target Mode (la possibilité de transformer son Mac en disque dur FireWire lorsque connecté à un autre Mac).

En plus d’utiliser l’EFI en lieu et place du Bios, Intel encourage également grandement à ce que l’EFI supporte le GPT. GPT est l’abréviation de GUID Partition Table. GUID étant également l’abréviation de Global Unique IDentifier.

Apple, qui utilisait précédemment l’OpenFirmware et l’APT (son propre système de Table de Partition, Apple Partition Table) n’a eu aucun problème à adopter le GPT au lieu du MBR, vu que l’APT est plus proche, conceptuellement, du GPT que du MBR. Le choix du GPT au lieu du MBR fut donc tout à fait logique.

Mais attention. La spécification du GPT possède quelques coins d’ombre concernant sa possible implémentation. Par exemple, la GPT ne donne pas de règle stricte à propos du partitionnement d’un disque.

Apple a donc établi [sa propre politique quant au partitionnement d’un disque][Partition]. Par exemple, une partition doit être aligné sur un bloc de 4K. Sur des disques compris entre 1 et 2Go (des cléfs usb, par exemple), une zone de 128Mo sépare les 2 partitions. Sur des disques de plus de 2Go (cad tous les disques durs vendus aujourd’hui) il y a toujours une partition réservée à l’EFI qui est créée. La taille de cette partition est fixée à 200Mo.

A notez que le firmware inclut dans les MacIntel contient également une émulation du Bios. C’est grâce à cela, que les MacIntel peuvent proposer Windows XP ou Windows Vista en Dual Boot.

[dvp]: https://web.archive.org/web/20210617200146/http://baptiste-wicht.developpez.com/tutoriel/windows/demarrage/

[Partition]: https://web.archive.org/web/20210617200146/http://developer.apple.com/technotes/tn2006/tn2166.html#SECPARTITIONINGPOLICY
