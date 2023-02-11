# Bienvenue sur le repository qui sert à générer le site de [blog.marcosx.net]

Il y a bien longtemps, j´avais un site www.marcosx.net, hébergé chez OVH et 
ça tournait sous une vieille version de wordpress, avec un theme dynamique 
et une base de données.
Mais, au final, je ne maitrisais plus rien.

Et j´ai donc décidé de repartir de rien. En créant un nouveau blog qui serait hébergé sur 

Je vais essayer ci-dessous de résumer 
1. comment j´ai crée le site, 
2. comment je l´ai (dé)structurer
3. comment je l'ai enrichi de certianes choses, ...


## 25 Juin 2019
Creation d'un compte sur [github] et du repository [marcosickx.github.io]
Mise à jour des infos coté OVH pour indiquer que blog.marcosx.net 
doit être redirigé vers les serveurs de GitHub

Pour cela, 
je me suis rendu dans sur ma page client de OVH, 
ensuite sur mon nom de domaine et sur zone DNS.
Là, je demande de rajouter une entrée DNS, et je choisi CNAME.

Je remplis le *sous domaine* : blog
dans TTL, je choisi *personalisé* et je mets 60 (secondes)
et dans *cible*, je remplis **marcosickx.github.io.**

Attention à bien mettre un point apres github.io. C´est d´une importance capitale.

```
blog                                        60 IN CNAME  marcosickx.github.io.
```

vu qu´il faut attendre 24 heures pour la propagation des changements, on continuera demain.


## 26 Juin 2019 

1. Création du fichier CNAME. C´est lui qui permet à GitHub de savoir vers quel GitHub page rediriger blog.marcosx.net
2. Depuis [marcosickx.github.io] je me rends sur settings et je choisi page dans la colonne de gauche.
3. Là, dans la partie Custom Domain, je mets [blog.marcosx.net] dans custom domain et je coche la case **Enforce HTTPS** ce qui me permet d´avoir mon site disponible en httpS avec un certificat valide, renouvelé automatiquement.

Ainsi, on aura bien tout correctement configuré coté DNS, redirection http vers https, et certificats.

Je peux créer maintenant ma première page.

J´ai donc créé [ma première page index.html] (https://github.com/MarcosIckx/MarcosIckx.github.io/commit/0f90b3a63fc553368aee52eebe786027aa766786?diff=split) statique où tout était inclus dedans

Je patouille un peu avec le CNAME, mais finalement, je comprends qu´il doit contenir blog.marcosx.net.

En attendant, je vous expliquer un peu la structure actuelle du site.

Le site est construit de façon statique par 
[GitHub Pages] qui lui-même utilise [jekyll] qui lui-même utilise [liquid].

J´ai pris la décision de n´utiliser aucun theme et de n´utiliser que du CSS et HTML. 

Pas de Javascript.

Par contre, j´ai pris la décision d´utiliser [kramdown], qui permet d´aller un peu plus loin que markdown.

J´ai commencé tout petit, pour bien comprendre les bases.
Avec une page html vraiment très très simple.
ensuite, un css très simple également.
page html et css que j´avais repris d´un tutoriel qui expliquait clairement les premiers pas.

Mais je ne me souviens plus de l´adresse de ce tutoriel.

## 31 janvier 2023

### changement table des matières

j´ai changé le include de la table des matières pour utiliser des balises html 5
qui ont l´air de très bien fonctionner même sur tablette et gsm.

### changement vidéos
les videos sont encapsulée dans figure et me permet d'utiliser figcaption.

## 01 février  2023

### include picture.html

j´ai implémenté un include picture.html qui va me faciliter les choses
car toutes les images utilisée dans un post seront mise dans le front matter.
du post, ainsi que les liens.

Ca me facilitera les choses et me permet d´utiliser les balises html 5
les images seront dans un figure, avec un figure caption, en dessous,
l´image pourra être un lien si on le désire.
et une alternative pour le mode sombre pourra être proposée.


### premier plugin
J´ai copier/coller mon premier plugin que j'ai trouvé ici.

https://stackoverflow.com/questions/14487110/include-jekyll-liquid-template-data-in-a-yaml-variable

en espérant qu´il fonctionne avec jekyll´utilisé par GitHub.

je m´en vais écrire un test pour confirmer cela.


## 2 février 2023

### soucis avec plugin 
j´avais oublié que GitHub page ne permet pas d´autres plugins que ceux repris sur la whitelist.
donc, ca tombe à l´eau.
on oublie.

### activation de certains plugins whitelisté

j´ai activé 3 plugins
1. le premier me permet de juste taper @identifiant_twitter, et ça devient un lien vers le compte twitter de la personne.
2. le deuxième devrait me permettre de créer des liens relatifs.
et donc, post_url fichier.md deviendrait superflu.
j'ai essayé de l'utiliser mais ca ne semble pas fonctionner.
3. le troisième, et le dernier, permet de créer des pages de redirection. Ce quii sera très utile dans mon cas, et ce poir 2 raisons: 
  1. j´ai changé le permalink pour qu´il soit plus propre. Du coup, les ancieenes urls donnet une 404. Dommage.
  2. je suis en train de réimporté dans mon blog les anciens posts écrits à l´époque dans wordpress. Mais ceux-ci n´ont pas la même structure de l´URL que ceux de maintenant. Et donc, ça provoque également une 404 au lieu d´afficher le bon lien.

## 3 février 2023
jˆai modifié quelque peu la page dˆerreur 404 pour que 
via du javascript, il propose à l´utilisateur les archives de l´année supposée.

## 5 février 2023

### prototype tri post en tenant commte date mise à jour 
j´ai réussi à mettre en place une logique me permettant d´afficher les posts en tenant compte des éventuelles mises à jour. Ainsi, je peux faire remonter si jenle desire des posts qui ont été mis à jour.

Faudra que je la mette en place là où il faut, mais au moins, il y a une logique.

Après, faudra que je regarde l´impact sur les archives.

### prototype post epinglé

j´ai´un prototype de post épinglé qu´on leut trouver dans ce fichier
_pages/Tests/test-mise-en-evidence-articles.md

Après, faudra que je paufine le CSS pour que cela ressemble à quelque chose, car ce n´est pas le cas actuellement.

## 11 février 2023
J´ai passé ces derniere jours à introduire les articles de la précédente version du blog.
Ainsi, ces articles sont à nouveau disponibles pour tout un chacun.

Vous noterez que le tout premier article date de mai 2007, le dernier datant de mai 2012. 5 ans à écrire, mais quasi personne pour lire.
il y a eu une longue absence avant que je reprenne le temps de ré-écrire puisque je n´ai repris qu´en 2019.
PUis, la Covid est venue, mettant tout cela entre parenthese.

Je dois encore peaufiner le CSS et d´autres choses, voir TODO LIST ci-dessous.


## TO DO LIST

Pas mal de choses dans ma todo list

### modifier  include picture.html 

Revoir la structure pour que l´url de l´image en darkmode soit liée à l´image normale.
Ainsi, on a un lien entre les deux.

Ensuite, on pourra l´étendre pour indiquer differents types d´images 
(small, medium, large, portrait & paysage) par exemple.
et il génererait la balise picture comme il faut.

### création de rapports

création de page de rapport 
- d´images référencées mais pas trouvées
- de liens référencés mais non trouvés
- de vidéo référencées mais pas trouvées.

### amélioration contraste couleurs CSS

### amélioration page des tags

### amélioration list des posts

### pouvoir épingler des posts 

ca me permettrait de mettre en évidence le post sur les fonctionnalités de ios16 que j´aime beaucoup.

**update 5/2/2023**

un prototype a été réalisé. 
Faut encore mettre à jour le CSS et ensuite l´intégrer où il se doit.

### pouvoir trier les post par date de dernière modification.

vraiment nécessaire pour, à défaut d´épingler le post, 
le remonter à la date de dernière modification de l´article

**update 5/2/2023**

j´ai un page qui montre que cela fonctionne /Tests/test2.md
mais je ne suis pas sûr que ce soit la meilleure façon de faire.

Mais ça marche.

Faudra maintenant l´implémenter correctement.

### ajouter une image en miniature à coté du post, dans la liste

### ajouter bannière en haut de la page

### rajouter des favicons

### modification du voir aussi
avoir pour chaque page un voir aussi plus riche et dynamique
c'est à dire qu´en fonctions des 
- tags, 
- catégories et 
- dates, il mentionnerait des articles ayant des choses en communs.


[blog.marcosx.net]: https://blog.marcosx.net
[github]: https://github.com
[marcosickx.github.io]: https://github.com/MarcosIckx/MarcosIckx.github.io/
[GitHub Pages]: https://docs.github.com/fr/pages
[jekyll]: https://jekyllrb.com
[liquid]: https://jekyllrb.com/docs/liquid/
[kramdown]: https://kramdown.gettalong.org/documentation.html
~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ 

## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/MarcosIckx/MarcosIckx.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/MarcosIckx/MarcosIckx.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
