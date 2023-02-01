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
et une alternative pour le mode somnre pourra être proposée.


### premier plugin
J´ai copier/coller mon premier plugin que j'ai trouvé ici.

https://stackoverflow.com/questions/14487110/include-jekyll-liquid-template-data-in-a-yaml-variable

en espérant qu´il fonctionne avec jekyll´utilisé par GitHub.

je m´en vais écrire un test pour confirmer cela.

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
