---
layout: post
title:  "Transparente Bilder mit JPG Kompression"
date:   2016-03-23 20:20:54 +0100
category: Development
tags: dev html web
author: Der-Eddy
keyword: transJPG
preview: iPhone.jpg
choosen: true
---
Heute bin ich über ein interessantes Thema gestolpert als ich auf [Reddit unterwegs war](https://www.reddit.com/r/web_design/comments/4bdgj1/somebody_at_apple_forgot_to_use_a_png/). Die Idee ist so simpel wie genial, JPG Bilder durch SVG Masken transparent machen ohne auf schlechte PNG Kompression ausweichen zu müssen. PNG Bilder haben zwar eine gute Qualität, jedoch zählt im Web eher ein schnellerer Auftritt als minimal schönere Bilder. Von der Idee bis zum eigenen Test hats nicht lange gedauert, zum Test benutze ich ein [Mockup eines iPhone Screenshots welchen ich vorletztes Jahr](https://imgur.com/a/dtvKk) angefertigt habe.

Damit das funktioniert muss man jedoch zum JPG noch eine Maske für SVG anlegen. [Eine einfache schwarz-weiß Interpretation reicht dafür aus, in meinem Fall ist sie nur 20 KB groß](https://i.imgur.com/xm3HnrO.jpg).

{% include image.html url="maskecutout.jpg" %}

Anschließend kommt alles in ein SVG HTML Konstrukt.

```html
<svg viewBox="0 0 1000 800" width="100%" height="100%">
  <defs>
    <mask id="iPhoneMask">
      <image width="813" height="1644" xlink:href="https://i.imgur.com/xm3HnrO.jpg"></image>
    </mask>
  </defs>
  <image mask="url(#iPhoneMask)" id="iPhone" width="813" height="1644" xlink:href="https://i.imgur.com/pL5AyGJ.jpg"></image>
</svg>
```

<svg viewBox="-90 0 1000 800" width="100%" height="100%">
  <defs>
    <mask id="iPhoneMask">
      <image width="813" height="1644" xlink:href="{{ site_root }}/img/{{ page.keyword }}/maske.jpg"></image>
    </mask>
  </defs>
  <image mask="url(#iPhoneMask)" id="iPhone" width="813" height="1644" xlink:href="{{ site_root }}/img/{{ page.keyword }}/iPhone.jpg"></image>
</svg><br>

Und siehe da, ein transparenter Hintergrund. Alle Bilder habe ich noch mal in einem [beschrifteten Imgur Album](https://imgur.com/a/2Ae6K) zusammengefast. Anschließend kommt man zum Schluss das JPG Bild (120 KB) + Maske (20 KB), also insgesamt **140 KB** eine Erpsarnis von knapp **75%** gegenüber dem **544 KB** großen PNG Bild bringt. In meinem Fall würde sich es wahrscheinlich weniger lohnen jedoch wenn es um eine größere Anzahl an Bildern oder mit einer höheren Auflösung geht kann man nicht nur eine Menge Traffic einsparen sondern auch wichtige Millisekunden Ladezeit.  
Anzumerken sei auch dass das ganze eher mäßig im Internet Explorer funktioniert, unter IE 8 sogar gar nicht.
