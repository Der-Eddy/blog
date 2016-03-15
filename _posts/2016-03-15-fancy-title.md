---
layout: post
title:  "Fancy Title"
date:   2016-03-15 15:03:00 +0100
category: info
tags: info, js
author: Der-Eddy
choosen: true
---
Ich hab nun den Titel ein wenig aufgepept, nun mit ein wenig Terminal Flair und einem blinkenden Cursor.

Der Javascript Code vom Cursor ist mit JQuery übrigens schnell eingetragen:

{% highlight html linenos %}
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
{% endhighlight %}
