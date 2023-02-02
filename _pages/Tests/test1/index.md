---
debug: true
layout: default
title: "test 1"
otherLinks:
  - url: "/_archives/2007.md"
    title: 2007
  - url: "/_archives/2022.md"
    title: 2022
links:
  link-1:
    url: https://blog.marcosx.net
    alt: mon blog
    title: lien vers mon blog
images:
  img-1: 
    url: Profile-twitter-MarcosIckx.png
    alt: image du profil de marcos ickx
    title: profil de Marcos Ickx
  img-1-dark:
    url: https://pbs.twimg.com/profile_images/1615483864784281601/4Tjaa2pw_400x400.jpg
    alt: image sombre du profil marcos ickx
    title: profil sombre de Marcos Ickx
  img-2: 
    url: Profile-twitter-MarcosIckx.png
    alt: image 2 du profil de marcos ickx 
  img-2-dark:
    url: https://pbs.twimg.com/profile_images/1615483864784281601/4Tjaa2pw_400x400.jpg
    alt: image sombre 2 du profil marcos ickx    
---

![bonjour][hello]

[HEllO]: Profile-twitter-MarcosIckx.png "Bonjourno"

Image 1 - pas de Lien 1 - pas de  dark :

{% include picture.html img=page.images.img-1  %}

Image 1 - Lien 1 - pas de  dark :

{% include picture.html link=page.links.link-1 img=page.images.img-1  %}

image 1 - pas de lien 1- dark 

{% include picture.html img=page.images.img-1 dark-img=page.images.img-1-dark %}

image 1 - lien 1- dark 

{% include picture.html link=page.links.link-1 img=page.images.img-1 dark-img=page.images.img-1-dark %}

Image 2 - pas de Lien 1 - pas de  dark :

{% include picture.html img=page.images.img-2  %}

Image 2 - Lien 1 - pas de  dark :

{% include picture.html link=page.links.link-1 img=page.images.img-2  %}

Image 2 - pas de lien 1- dark 

{% include picture.html img=page.images.img-2 dark-img=page.images.img-2-dark %}

image 2 - lien 1- dark 

{% include picture.html link=page.links.link-1 img=page.images.img-2 dark-img=page.images.img-2-dark %}

_____
[{{ otherLinks[0].title }}]({{ otherLinks[0].url }})

[{{ otherLinks[1].title }}]({{ otherLinks[1].url }})

Vous aimerez également lire :
  
{% for otherLink in page.otherLinks %}
* [{{ otherLink.title }}]({{ otherLink.url }})
{% endfor %}

