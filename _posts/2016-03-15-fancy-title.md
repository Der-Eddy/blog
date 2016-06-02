---
layout: post
title:  "Fancy Title"
date:   2016-03-15 15:03:00 +0100
category: Blog
tags: info js blog
author: Der-Eddy
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

**Nachtrag:**  
Man kann dies natürlich auch in reinem CSS erreichen, jedoch sind diese Konstrukte wenn man einen flüssigeren Übergang haben möchte zielich groß und wenn ich schon JQuery in die Seite einbinde, warum nicht auch einfacher?
