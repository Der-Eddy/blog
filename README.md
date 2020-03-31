blog.eddy-dev
=====================

Mein auf GitHub gehosteter statischer Blog welcher [Jekyll](https://jekyllrb.com/) nutzt: https://blog.eddy-dev.net

Komponenten:
-------------
- [Jekyll](https://jekyllrb.com/) erstellt eine statische Webseite aus Markdown und einer template engine ([Liquid](https://github.com/Shopify/liquid))
Vorteil ist das es vom Konzept her keine Datenbank oder Backend in z.B. PHP gibt welche angreifbar wären
- [Fomantic-UI](https://fomantic-ui.com/) ist das CSS/UI Framework meiner Wahl um die Webseite schön zu gestalten
- jQuery wird genutzt aus bequemlichkeit und um relativ einfach Bilder "lazy" nachzuladen
- [GitHub Pages](https://pages.github.com/) hostet die komplette Webseite kostenlos mit einer sehr guten Uptime

Build:
-------------
[Jekyll](https://jekyllrb.com/) installieren und dann über den Befehl `jekyll build` den Blog nach `_site` erzeugen.  
Alternativ wird über `jekyll serve` auch der Blog über einen minimalen Webserver ausgegeben und bei Dateiänderung aktualisiert.

Screenshots:
-------------
![page](https://i.imgur.com/zcoza1S.png)

![updates](https://i.imgur.com/Td2M4OC.png)
