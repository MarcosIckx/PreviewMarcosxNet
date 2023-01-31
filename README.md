# Bienvenue sur le repository qui sert à générer le site de [blog.marcosx.net]

Il y a bien longtemps, j´avais un site www.marcosx.net, hébergé chez OVH et 
ça tournait sous une vieille version de wordpress, avec un theme dynamique 
et une base de données.
Mais, au final, je ne maitrisais plus rien.

Et j´ai donc décidé de repartir de rien. En créant un nouveau blog qui serait hébergé sur 

Je vais essayer ci-dessous de résumer l´évolution du site.

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
3. Là, dans la partie Custom Domain, je mets [blog.marcosx.net] dans custom domain et je coche la case **Enforce HTTPS**

Ainsi, on aura bien tout corectement configuré coté DNS, http, https, et certificats.

Je peux créer maintenant ma première page.

J´ai donc créé [ma première page index.html] (https://github.com/MarcosIckx/MarcosIckx.github.io/commit/0f90b3a63fc553368aee52eebe786027aa766786?diff=split) statique où tout était inclus dedans

Je patouille un peu avec le CNAME, mais finalement, je comprends qu´il doit contenir blog.marcosx.net.

En attendant, je crée d´autres fichiers.

vous expliquer la structure du site.
Le site est construit de façon statique par 
[GitHub Pages] qui lui-même utilise [jekyll] qui lui-même utilise [liquid].
J´ai pris la décision de n´utiliser aucun theme et de n´utiliser que du CSS et HTML. 
Pas de Javascript.
Par contre, j´ai pris la décision d´utiliser [kramdown], qui permet d´aller un peu plus loin que markdown.

J´ai commencé tout petit, pour bien comprendre les bases.
Avec un css des plus simples, et un post vraiment très très simple.

~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ 


