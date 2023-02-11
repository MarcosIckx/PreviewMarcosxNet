---
date: 2008-03-29
category: Safari
title: WebKit et Opera ont passé le test Acid3. Mais est-ce cela le plus important ?
---

Ce mercredi, Opera a [annoncé][AnnonceOpéra] avoir réussi à passer le test Acid 3.

([Le test Acid 3 a été mis sur pied][Acid3] pour vérifier le rendu des navigateurs web lors de l’utilisation de fonctionnalités qu’on retrouve de plus en plus sur les sites web dynamiques.

Quelques instants plus tard, c’était au tour des développeurs de WebKit (le moteur de rendu utilisé par Safari) [d’annoncer][AnnonceWebKit] qu’ils avaient passé le test Acid3.

Et l’équipe de WebKit furent les premiers à le prouver réellement, en mettant à disposition dès le lendemain, une version publique de WebKit, permettant à tout le monde de voir par eux-même que WebKit atteint bien le score de 100%.

Opera a, quand à lui, rendu hier une version publique de leur navigateur, tout en indiquant ceci

> Still, we do not recommend using this build for regular Web surfing as it lacks some of the security-related features found in our regular desktop version

ce qui n’encourage pas vraiment à utiliser Opera.

Mais est-on vraiment mieux logé avec WebKit ?

Lorsqu’on sait [qu’il n’aura fallu que 2 minutes][Faille] pour que le Mac Book Air mis à disposition lors d’un concours de hacking tombe dans les mains d’un “hacker”, et cela grâce à une faille de Safari (qui utilise Webkit comme moteur), on peut également se poser des questions sur la fiabilité de ce navigateur.

A notez que les propos tenus par le hacker laissent entendre qu’il a bien profité d’une faille présente dans Safari 3.1, la toute dernière version de Safari. Mais il nous est impossible de savoir si cette faille existe encore dans la toute dernière version de WebKit.

La fondation Mozilla a décidé, elle, de rester concentré sur la sortie de FireFox 3.0 (prévue pour juin de cette année).

Shaver, sur son blog, dit ceci à propos du test Acid3 et de FireFox 3.0 :

> We’re still taking fixes for important issues, but virtually none of the issues on the Acid 3 list are important enough for us to take at this stage. We don’t want to be rushing fixes in, or rushing out a release, only to find that we’ve broken important sites or regressed previous standards support, or worse introduced a security problem

Ce qu’on pourrait traduire par

> Nous sommes toujours occupés à fixer certains problèmes importants. Et virtuellement aucun des problèmes soulevés par le test Acid3 sont suffisamment importants pour qu’on s’en occupe à ce stade ci. Nous ne désirons pas nous précipiter en fixant des problèmes ou en sortant une nouvelle version, uniquement pour remarquer par la suite que certains sites importants ne s’affichent plus comme il faut, ou qu’on ne supporte plus comme il faut les standards précédents, ou, pire encore, qu’on aurait introduit un problème de sécurité.

Bref, oui WebKit et Opera ont rendu public des versions de leur navigateurs qui passent le test Acid3. Et oui, ca leur a permis d’avoir leur moment de gloire sur internet.
Mais, à choisir, on aurait aimé, en tant qu’utilisateur d’internet, qu’ils passent leur temps à rendre leur navigateur plus stable et plus sécurisé.

Finalement, dans cette course-là, ce sera peut-être la fondation Mozilla qui aura fait le bon choix. Nous verrons, dans quelques semaines, qui avait raison.

[AnnonceOpéra]: https://web.archive.org/web/20160904072355/http://my.opera.com/desktopteam/blog/2008/03/26/opera-and-the-acid3-test
[Acid3]: https://web.archive.org/web/20160904072355/http://ln.hixie.ch/?start=1200301306&order=-1&count=1
[AnnonceWebKit]: https://web.archive.org/web/20160904072355/http://webkit.org/blog/173/webkit-achieves-acid3-100100-in-public-build/
[Faille]: https://web.archive.org/web/20160904072355/http://www.computerworld.com/action/article.do?command=viewArticleBasic&articleId=9072959
