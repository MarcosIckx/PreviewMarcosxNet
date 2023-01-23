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
  type: video/mp4
  title: Lien vers vidéo de l´animation que l´on peut voir sur iCloud.com
debug: true
---

ceci est un test

{{page.debug}}



valeurs passée par collection
{{page.video}}

{% include video.html videoInfo=page.video debug=true %}

valeurs passée par position
{{page.videos[0]}}

{% include video.html pos=0 debug=true %}

valeurs passée en direct
{% include video.html src=page.video.url description=page.video.alt debug=true %}
