---
layout: post
title:  "Fancy Title"
date:   2016-03-15 15:03:00 +0100
category: Blog
tags: info js blog
author: Der-Eddy
keyword: fancytitle
---
Ich hab nun den Titel ein wenig aufgepept, nun mit ein wenig Terminal Flair und einem blinkenden Cursor.

Der Javascript Code vom Cursor ist mit JQuery übrigens schnell eingetragen:

```html
<script>
    function cursorAnimation() {
                $('#cursor').animate({
                    opacity: 0
                }, 'slow', 'swing').animate({
                    opacity: 1
                }, 'slow', 'swing');
            }
    setInterval ('cursorAnimation()', 600);
</script>
```

**Nachtrag:**  
Man kann dies natürlich auch in reinem CSS erreichen, jedoch sind diese Konstrukte wenn man einen flüssigeren Übergang haben möchte zielich groß und wenn ich schon JQuery in die Seite einbinde, warum nicht auch einfacher?

**Nachtrag 2:**  
Da ich gerade Lust auf CSS Animations habe, habe ich mich noch mal dran gesetzt:

```css
#cursor {
  display: inline;
  -webkit-animation: 1s blink ease infinite;
  -moz-animation: 1s blink ease infinite;
  -ms-animation: 1s blink ease infinite;
  -o-animation: 1s blink ease infinite;
  animation: 1s blink ease infinite;
}

@keyframes "blink" {
  50% {
    opacity: 0.0;
  }
}

@-moz-keyframes blink {
  50% {
    opacity: 0.0;
  }
}

@-webkit-keyframes "blink" {
  50% {
    opacity: 0.0;
  }
}

@-ms-keyframes "blink" {
  50% {
    opacity: 0.0;
  }
}

@-o-keyframes "blink" {
  50% {
    opacity: 0.0;
  }
}
```

Blöd ist nur das [animation](https://developer.mozilla.org/de/docs/Web/CSS/CSS_Animations/CSS_Animationen_nutzen) leider immer noch "nur" ein Arbeitsentwurf ist sodass jeder Browser sein eigenes Süppchen kocht und man ohne Vendor Präfixe nicht umher kommt. Mit [Compass](http://compass-style.org) und [Sass](http://sass-lang.com/) könnte man das aber noch abkürzen.
