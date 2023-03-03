---
layout: default
title: "test 1"
permalink: /Tests/Test1/
redirect_from: /_pages/Test/test1/
otherLinks:
  - url: "../../../_archives/2007.md"
    title: 2007
  - url: "../../../_archives/2022.md"
    title: 2022
  - url: "../../categories.md"
    title: categories
  - url: "../../tags.md"
    title: tags
links:
  link-1:
    url: https://blog.marcosx.net
    alt: mon blog
    title: lien vers mon blog
pictures_base_url: /img/
images:
  img-1: 
    url: Accueil.png
    small_url: Accueil.png
    medium_url: AirPrint.png
    large_url: iPadOS16.PNG
    alt: image du profil de marcos ickx
    title: profil de Marcos Ickx
    dark:
      url: https://pbs.twimg.com/profile_images/1615483864784281601/4Tjaa2pw_400x400.jpg
      small_url: https://pbs.twimg.com/profile_images/1615483864784281601/4Tjaa2pw_400x400.jpg
      medium_url: /img/posts/2020/04/03/Support-Accessoires-USB-iPadOS-13.3/iPadOS-Version-13.3.1.jpeg
      large_url: /img/posts/2020/04/03/Support-Accessoires-USB-iPadOS-13.3/App-Fichiers-Cle-USB.jpeg
  img-2: 
    url: iPadOS16.PNG
    alt: image 2 du profil de marcos ickx 
  img-2-dark:
    url: /img/posts/2019/08/01/Support-Accessoires-USB-iOS-12/Reglages-Ethernet.jpeg
    alt: image sombre 2 du profil marcos ickx    
---

Bonjour de @MarcosIckx


![bonjour][hello]

[HEllO]: Profile-twitter-MarcosIckx.png "Bonjourno"

{% comment %}
{% assign posts = "" | split: "," %}
{% for post in site.posts  %}
{% assign sort_date = post.update | default: post.date %}
{% assign post = post | push: sort_date %}
{{ post }}
{{ post.date }} / {{ post.update}} 

sort date : {{ post.sort_date }}

{% assign posts = posts | push: post %}
{% endfor %}

{% assign posts = posts |  sort: "sort_date"%}
{% for post in posts  %}
 
## {{ post.title }} ({{ post.sort_date }})

{{ post.url }}

{{ post.description }}

{% endfor %}

{% endcomment %}

Image 1 - pas de Lien 1 :

{% include picture.html img=page.images.img-1 %}

Image 1 - pas de Lien 1 - reference via array :

{% include picture.html img=page.images["img-1"] %}
Image 1 - Lien 1 :

{% include picture.html link=page.links.link-1 img=page.images.img-1  %}


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

