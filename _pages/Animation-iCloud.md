---
layout: video
title: Vidéo Animation iCloud.com
description: Capture vidéo que l´on peut voir sur iCloud.com
permalink: videos/Animation-iCloud.com/
video:
  id: Animation-iCloud.com
  url: /img/posts/2022/12/17/Protection-Avancee-Des-Donnees/animation-iCloud.com.mp4
  alt: Vidéo Animation iCloud.com
  type: video/mp4
  title: Lien vers vidéo de l´animation que l´on peut voir sur iCloud.com
videos:
  - id: Animation-iCloud.com
    url: /img/posts/2022/12/17/Protection-Avancee-Des-Donnees/animation-iCloud.com.mp4
    alt: Vidéo Animation iCloud.com
    type: "video/mp4"
    title: Lien vers vidéo de l´animation que l´on peut voir sur iCloud.com
debug: false
---

ceci est un test

{{page.debug}}

## valeurs passée par collection

{{page.video}}

{% include video.html videoInfos=page.video debug=page.debug %}

## valeurs passée par position 0

{{page.videos[0]}}

{% include video.html videoNr=0 debug=page.debug %}

## valeurs passée en direct

{% include video.html src=page.video.url description=page.video.alt debug=page.debug %}
