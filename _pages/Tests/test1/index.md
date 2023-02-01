---
debug: true
layout: default
title: "test 1"
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
    url: Profile-twitter-MarcosIckx.png
    alt: image sombre du profil marcos ickx
    title: profil sombre de Marcos Ickx
  img-2: 
    url: Profile-twitter-MarcosIckx.png
    alt: image 2 du profil de marcos ickx 
  img-2-dark:
    url: Profile-twitter-MarcosIckx.png
    alt: image sombre 2 du profil marcos ickx    
---

![bonjour][hello]

[HEllO]: Profile-twitter-MarcosIckx.png "Bonjourno"

Image 1 - pas de Lien 1 - pas de  dark :

{% include picture.html img=pages.images.img-1  %}

Image 1 - Lien 1 - pas de  dark :

{% include picture.html link=page.links.link-1 img=pages.images.img-1  %}

image 1 - pas de lien 1- dark 

{% include picture.html img=pages.images.img-1 dark-img=pages.images.img-1-dark %}

image 1 - lien 1- dark 

{% include picture.html link=page.links.link-1 img=pages.images.img-1 dark-img=pages.images.img-1-dark %}

Image 2 - pas de Lien 1 - pas de  dark :

{% include picture.html img=pages.images.img-2  %}

Image 2 - Lien 1 - pas de  dark :

{% include picture.html link=page.links.link-1 img=pages.images.img-2  %}

Image 2 - pas de lien 1- dark 

{% include picture.html img=pages.images.img-2 dark-img=pages.images.img-2-dark %}

image 2 - lien 1- dark 

{% include picture.html link=page.links.link-1 img=pages.images.img-2 dark-img=pages.images.img-2-dark %}


