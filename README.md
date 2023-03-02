# Bienvenue sur le repository qui sert à générer le site de [blog.marcosx.net]

Il y a bien longtemps, j´avais un site, [www.marcosx.net], hébergé chez OVH et 
ça tournait sous une toute vieille version de wordpress, avec un theme dynamique 
et une base de données.
Mais, au final, je ne maitrisais plus rien.

Et j´ai donc décidé de repartir de zéro, 
en créant un tout nouveau blog dont tous les articles seraient stockés sur [GitHub].

Je vais essayer ci-dessous de résumer 
1. comment j´ai crée le site, 
2. comment je l´ai (dé)structurer
3. comment je l'ai enrichi de certaines choses, ...


## 25 Juin 2019
1. Création d'un compte sur [github] et du repository [marcosickx.github.io]
2. Mise à jour des infos coté OVH pour indiquer que [blog.marcosx.net] 
doit être redirigé vers les serveurs de [GitHub]

Pour cela, 
je me suis rendu dans sur ma page client de OVH, 
ensuite sur mon nom de domaine et sur zone DNS.
Là, je demande de rajouter une entrée DNS, et je choisis CNAME.

Je remplis le *sous domaine* : blog
dans TTL, je choisi *personalisé* et je mets 60 (secondes)
et dans *cible*, je remplis **[marcosickx.github.io].**

Attention à bien mettre un point après `github.io`. C´est d´une importance capitale.

```
blog                                        60 IN CNAME  marcosickx.github.io.
```

Vu qu´il faut attendre 24 heures pour la propagation des changements, on continuera demain.


## 26 Juin 2019 

1. Création du fichier CNAME. C´est lui qui permet à GitHub de savoir vers quel [GitHub page] rediriger [blog.marcosx.net]
2. Depuis [marcosickx.github.io] je me rends sur `settings` et je choisi `page` dans la colonne de gauche.
3. Là, dans la partie `Custom Domain`, je mets [blog.marcosx.net] dans `custom domain` et je coche la case **`Enforce HTTPS`** 
ce qui me permet d´avoir mon site disponible en http**S** avec un certificat valide, renouvelé automatiquement.

Ainsi, on aura bien tout correctement configuré coté DNS, avec redirection du traffic http vers https, et certificats auto-renouvelé.

Je peux donc créer maintenant ma première page.

J´ai donc créé [ma première page index.html](https://github.com/MarcosIckx/MarcosIckx.github.io/commit/0f90b3a63fc553368aee52eebe786027aa766786?diff=split) statique où tout était inclus dedans.

Je patouille un peu avec le CNAME, mais finalement, je comprends qu´il doit contenir [blog.marcosx.net].

En attendant, je vous expliquer un peu la structure actuelle du site.

Le site est construit de façon statique par 
[GitHub Pages] qui lui-même utilise [jekyll] qui lui-même utilise [liquid].

J´ai pris la décision de n´utiliser aucun thème et de n´utiliser que du CSS et HTML. 

Pas de Javascript.

Il y a une exception à cela. J'ai rajouté un peu de Javascript sur la page 404.
C'est vraiment la seule page contenant du Javascript.
Elle permet de pouvoir proposer d'autres URLs qui pourraient être utiles.


Par contre, j´ai pris la décision d´utiliser [kramdown], qui permet d´aller un peu plus loin que markdown.

J´ai commencé de rien, et j'y suis allé petit à petit, 
pour bien comprendre les bases.

Avec une page HTML vraiment très très simple.
ensuite, un CSS très simple également.
page HTML et CSS que j´avais repris d´un tutoriel qui expliquait clairement les premiers pas.

Mais je ne me souviens malheureusement plus de l´adresse de ce tutoriel.

## 31 janvier 2023

### changement table des matières

j´ai changé le include de la table des matières pour utiliser des balises html 5
qui ont l´air de très bien fonctionner même sur tablette et gsm.

### changement vidéos
les videos sont encapsulées dans `figure` et me permet d'utiliser `figcaption`.

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
J´ai copié/collé mon premier plugin que j'ai trouvé ici.

https://stackoverflow.com/questions/14487110/include-jekyll-liquid-template-data-in-a-yaml-variable

en espérant qu´il fonctionne avec la version de [jekyll] utilisé par [GitHub].

je m´en vais écrire un test pour confirmer cela.


## 2 février 2023

### soucis avec plugin 
j´avais oublié que [GitHub page] ne permet pas d´autres plugins que ceux repris sur la whitelist.
donc, ca tombe à l´eau.
on oublie.

### activation de certains plugins whitelisté

j´ai activé 3 plugins
1. le premier me permet de juste taper @identifiant_twitter, et ça devient un lien vers le compte twitter de la personne.
2. le deuxième devrait me permettre de créer des liens relatifs.
et donc, post_url fichier.md deviendrait superflu.
j'ai essayé de l'utiliser mais je n'ai pas réussi à le faire fonctionner. Je vais devoir creuser cela.
3. le troisième, et le dernier, permet de créer des pages de redirection. Ce quii sera très utile dans mon cas, et ce poir 2 raisons: 
  1. j´ai changé le permalink pour qu´il soit plus propre. Du coup, les ancieenes urls donnet une 404. Dommage.
  2. je suis en train de réimporté dans mon blog les anciens posts écrits à l´époque dans wordpress. Mais ceux-ci n´ont pas la même structure de l´URL que ceux de maintenant. Et donc, ça provoque également une 404 au lieu d´afficher le bon lien.

## 3 février 2023
jˆai modifié quelque peu la page dˆerreur 404 pour que 
via du javascript, il propose à l´utilisateur les archives de l´année supposée.

## 5 février 2023

### prototype tri des posts en tenant compte de la date de mise à jour 
j´ai réussi à mettre en place une logique me permettant d´afficher les posts en tenant compte des éventuelles mises à jour. Ainsi, je peux faire remonter si je le desire, des posts qui ont été mis à jour.

Faudra maintenant que je la mette en place là où il faut, mais au moins, il y a un prototype qui fonctionne.

Après, faudra que je regarde quel est l´impact sur les archives.

### prototype post epinglé

j´ai´un prototype de post épinglé qu´on peut trouver dans ce fichier
_pages/Tests/test-mise-en-evidence-articles.md

Après, il faudrait que je paufine le CSS pour que cela ressemble à quelque chose, car ce n´est pas du tout le cas actuellement.

## 11 février 2023

### rajout anciens articles
J´ai passé ces derniere jours à introduire les articles de la précédente version du blog.
Ainsi, ces articles sont à nouveau disponibles pour tout un chacun, et stockés dans [GitHub].

Vous noterez que le tout premier article date de mai 2007, le dernier datant de mai 2012. 
5 ans à écrire, mais quasi personne pour lire ce que j'écrivais à l'époque.

il y a eu une longue absence (de 2013 à 2019) avant que je reprenne le temps de ré-écrire puisque je n´ai repris qu´en 2019.
Puis, la Covid est venue, mettant tout cela entre parenthese.

Je dois encore peaufiner le CSS et d´autres choses, voir TODO LIST ci-dessous, mais en gros, je suis content du résultat.

### modification css et présentation des posts
Sur la page d'accueil les posts sont maintenant précédés de la date.
Actuellement c'est la date de création, mais je pense mettre plutôt la date de mise à jour.
J'ai rajouté deux couleurs de mise en évidence qui sont le rouge et le brun.
Et les ai mis comme bord de couleurs pour les listes des blogs.
Ça donne bien, je dois dire.

À utiliser pour les citations aussi. Ça devrait bien donner.

### Table des matières présente que si nécessaire
Rien de plus énervant que de voir une table des matières et lorsqu'on l'étend, elle est vide.
J'ai donc déplacé la logique pour n'afficher la table des matières que lorsque celle ci n'est pas vide.
Ce qui est bien plus agréable pour l'utilisateur.

### sitemap.xml
le fichier était mal construit car j´avais oublié de mettre
    ---
    layout: null
    ---
 en en-tête.
 
 Du coup, il le rendait par défaut avec le layout default et donc le résultat était un fichier html et non un fichier .xml.
 
 Bref, c´était pas cela.
 
 Maintenant, cela a été fixé, et j´espère que ça aidera les moteurs de recherche à indexer les pages comme il faut.
 
 Ça donnera peut-être un peu plus de visibilité au site.
 
### indexer le site
J'essaye de faire en sorte que le site soit dans les indexs des moteurs de recherche.

## 14 février 2023
Le fichier atom.xml causait plein de soucis
J'ai donc fait quelques recherches et suis finalement tombé sur un site expliquant clairement comment créer ce fichier correctement.
https://jekyllcodex.org/without-plugin/rss-feed/#
Je ne peux que vous le recommander.

J'ai testé ce que ça donnait avec reeder, et ça donne super bien.

## 15 février 2023
j´ai un peu revu la structure du repertoire  _includes pour y voir un peu plus clair
ainsi, il y a maintenant 
1. un sous-répertoire `main` contenant les blocs principaux d´une page.
1.1. les html headers
1.2. la barre de navigation
1.3. le pied de page (footer)
2. un sous-répertoire `taxonomy`, contenant ce qui est en relations avec les tags et les catégories
2.1 entriesPerTaxonomy.html permet de construire la liste des posts par catégories de la même façon que la liste des posts par tags.

j´ai également profité de ces changements pour 
1. rajouter des rel="author" pour les liens vers les pages d´auteur
2. rajouter des rel="prev" et rel="next" pour ce qui est des liens précédent et suivant

en attendand, le site commence à être indexé, ce qui est très bien.
  
17 février 2023
Ajout d'une entrée dns pour authentifier auprès de Bing que je suis bien le propriétaire du site.
ça devrait du coup aider à mieux référencer le site sur ce moteur de recherche aussi.
Du moins, je l'espère.
 
## TO DO LIST

Pas mal de choses dans ma todo list

### modifier  include picture.html 

Revoir la structure pour que l´url de l´image en darkmode soit liée à l´image normale.
Ainsi, on a un lien direct entre les deux.

Ensuite, on pourra l´étendre pour indiquer differents types d´images 
(small, medium, large, portrait & paysage) par exemple.
et il génererait la balise `picture` comme il faut.

### création de rapports

création de page de rapport 
- d´images référencées mais pas trouvées
- de liens référencés mais non trouvés
- de vidéo référencées mais pas trouvées.

### amélioration contraste couleurs CSS
le choix des couleurs et des contrastes ne me plaisent clairement pas pour le moment.
Il va falloir revoir tout cela,

### amélioration page des tags

### amélioration list des posts

Un post prend trop de place en hauteur dans cette liste.

### pouvoir épingler des posts 

ca me permettrait de mettre en évidence le post sur les fonctionnalités de ios16 que j´aime beaucoup.

**update 5/2/2023**

un prototype a été réalisé. 
Faut encore mettre à jour le CSS et ensuite l´intégrer où il se doit.

### pouvoir trier les post par date de dernière modification.

vraiment nécessaire pour, à défaut d´épingler le post, 
le remonter à la date de dernière modification de l´article

**update 5/2/2023**

j´ai une page qui montre que cela fonctionne /Tests/test2.md.

Je ne suis pas sûr que ce soit la meilleure façon de faire, 
mais ça marche.

Faudra maintenant l´implémenter correctement.

### ajouter une image en miniature à coté du post, dans la liste

Ça rends la liste des posts plus agréable, plus digeste.

À voir si ça peut se mettre en place aisément.


### ajouter bannière en haut de la page

### rajouter des favicons
Cela me parait indispensable.

### modification du voir aussi
Avoir pour chaque page un `voir aussi` plus riche et dynamique
c'est à dire qu´en fonction 
- des tags, 
- des catégories et 
- des dates, il mentionnerait des articles ayant des choses en communs.

[www.marcosx.net]: https://www.marcosx.net
[blog.marcosx.net]: https://blog.marcosx.net
[marcosx.github.io]: https://marcosx.github.io
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
