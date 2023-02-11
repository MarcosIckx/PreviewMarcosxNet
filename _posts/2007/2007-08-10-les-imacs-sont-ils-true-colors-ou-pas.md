---
title: les iMac sont-ils True Color ou pas ?
date: 2007-08-10
category: Matériel
---

Comme vous le savez tous, Apple vient de renouveler toute la gamme iMac, abandonnant le 17″, et ne gardant plus que le 20″ et 24″.

Steve Jobs, lors du keynote, a mis l’accent sur les matériaux utilisés dans ces iMacs: l’Aluminium et le Verre.

Et il expliquait qu’Apple utilisait déjà l’Aluminium dans les versions PRO de ses ordinateurs. Le Mac Pro est en aluminium. Le MacBookPro est en aluminium. Et l’iPhone contient également de l’aluminium.

Il en a également profité pour indiquer que ces iMacs ne seraient disponibles qu’en “Glossy”. Car le glossy donne une meilleure image, plus lumineuse, plus vraie, … et c’est ce que les utilisateurs préfèrent.

Bref, tout cela pour nous faire comprendre que les iMacs sont maintenant plus professionels qu’auparavant.

Mais franchement, est ce qu’un professionnel (ou même un amateur) de la photo, un webmaster, de la mise en page … pourrait vraiment être intéressé par ces iMacs ?

La réponse est non. Tout simplement parce que ces écrans ne sont toujours pas “TRUE COLORS”.

C’est bien d’avoir des écrans “glossy” qui permettent d’avoir une meilleur rendu des couleurs. Mais si les couleurs affichées sont bridées, à quoi ca sert ?

Qu’entends on par le vocabulaire “TRUE COLORS” ? 

Chaque pixels est composés des 3 couleurs primaires Rouge, Vert Bleu (RVB, ou RGB en anglais).

Chacune de ces couleurs primaires peuvent, lorsqu’elles sont stockées sur 8 bits avoir 256 nuances (2^8). Et mises ensembles, elles peuvent afficher 256^3 soit 16.777.216 nuances de couleurs. C’est ce qu’on appelle le TRUE COLORS.

Le problème est que les dalles des iMacs sont des dalles provenant de LG/Philips, connues sous la référence LM201WE3. Or, si vous lisez cet excellent article, http://forums.anandtech.com/messageview.aspx?catid=31&threadid=2049206, vous y apprendrez la chose suivante concernant notre dalle:

> 20.1″: LG Flatron L204WT, 1680×1050 (16:10)
> 
> Panel: TN (LG.Philips LM201WE3); 6-bit+Hi-FRC, 16.7M colors 
> 
> Image Delay (rt+lag, estimated): Low (25 ms) 
> 
> Specifications: LG Flatron L204WT 
> 
> HDCP Compliant: Yes 
> 
> More Info: prad.de 
> 
> Price: ~$250 USD


Tout d’abord, on y apprend que la dalle, est une dalle TN (twisted nematic). Or les dalles TN sont réputées pour avoir un angle de vision plus restreint que les autres types de dalles, mais ont également du mal à avoir une répartition uniforme de la brillance. Ce qui est génant pour un professionnel de la photo.

Bien qu’il soit indiqué que la dalle puisse afficher 16.7M couleurs, on notera que les couleurs primaires ne sont pas codées sous 8 bits mais seulement sous 6bits. 

Or, avec 6 bits par couleurs, on ne peut produire véritablement que 262144 couleurs. (2^6= 64; 64^3 = 262.144 couleurs). Et non 16.7M.

Mais il est indiqué que la dalle est 6-bit+Hi-FRC.

Hi-FRC signifie High Frame Rate Control. C’est une technologique qui joue sur 2 choses:

- le taux de rafraichissement. Imaginer un point à l’écran. Et je lui dit de basculer plusieurs fois du point noir en point blanc. Et cela rapidement. Notre oeil va percevoir un point gris. Si on affiche rapidement 3 points blancs suivi d’un point noir, on percevra un point gris clair. Si on affiche rapidement 1 point blanc et trois points noir, on percevra un point gris foncé.

Imaginer maintenant que je veuille afficher un point de nuance [127] sur une palette de 256 nuances. Mais je n’ai que 64 nuances. J’afficherai un point de nuance 31 une fois. Puis un point de nuance 32, 3 fois. Cela dans un temps très court. Ce qui simulerait un point de nuance [31.75]. Transposé dans la palette de 256 couleurs, ca fait un point de nuance [127]. Le problème est qu’on a jamais vraiment affiché un point de nuance [127]. Ce n’est qu’une apparance, un mirage.

- le dithering (simulation d’une couleur en la composant de 2 (ou plusieurs) autres couleurs) est un procédé bien connu pour ce qui est de l’impression par encre. On simule toute une gamme de couleurs en affichant l’un à coté de l’autre pleins de petits points de couleurs différentes. 

Imaginer que je veux afficher un rectangle d’une couleur uniforme [127] sur une palette de 256 nuances. Mais je n’ai que 64 nuances. J’afficherai un point de nuance 31 + nuance 32 + nuance 32 + nuance 32. Et ca me fera en moyenne une nuance de 31.75. Multiplié par 4, ca fait bien une nuance de 127. Le but est atteint. Visuellement, notre oeil peut être trompé. Mais jamais mon écran n’a vraiment affiché des points de nuances 127, comme l’aurait fait un écran 8bits/couleur.

Cette technologie ne peut jamais afficher réellement les 16millions de couleurs mais vous fait croire qu’elle peut afficher 16millions de couleurs.

La nouvelle gamme d’iMac ne permet pas d’afficher réellement 16Millions de couleurs. C’est un leurre.

Un autre problème que je vois à cette technologie (Hi-)FRC est qu’elle génère bien plus de basculements de vos cristaux liquides. Imaginer que pour afficher un point gris, je dois à chaque fois dire à l’écran, affiche un point blanc. maintenant un noir. maintenant un blanc, maintenant un noir. Le cristal liquide a du changé 4 fois d’état. Si je peux dire affiche un point gris pendant la même période de temps, il ne change qu’une fois d’état.

Or ce changement d’état du cristal liquide est effectué par un transistor. Et plus on fait travailler un transistor, plus on raccourci sa durée de vie. Et plus on raccourci la durée de vie d’un transistor, plus vite on risque de voir apparaitre des points morts à l’écran.

Je ne peux que vous conseiller la lecture de cet article, expliquant clairement ce qu’est HI-FRC et comment ca fonctionne: http://www.unionen.se/pub/swec/Hi-FRC.pdf

un autre lien: http://www.xbitlabs.com/articles/other/display/lcd-guide_11.html

