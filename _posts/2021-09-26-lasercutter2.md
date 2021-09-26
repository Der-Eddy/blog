---
layout: post
title:  "Lasercutter Teil 2 - Lötrauchabsaugung"
date:   2021-09-26 15:00:00 +0100
category: Hackspace
tags: hackspace laser
author: Der-Eddy
preview: collage.jpg
keyword: bklaserlöt
---
In einem letzten [Blog Eintrag]({% link _posts/2020-03-09-lasercutter.md %}) hatte ich bereits meine Anfänge mit einem Lasercutter erzählt. Dies Mal habe ich etwas Nützlicheres damit gebastelt und was ich eigentlich schon lange anschaffen hätte sollen: Eine Lötrauchabsaugung

{% include image.html url="collage.jpg" description="Kompakt und mobil, endlich eine Lötrauchabsaugung" %}

Obwohl ich bleifreies Lot verwende, so ist auch dieses nicht komplett unbedenklich und auch deren Dämpfe sollte man in einem geschlossenen Raum nicht zu viel einatmen. Mit dem kommenden Winter wird es schwerer mal eben durchzulüften während man lötet und fertige Lösungen zur Absaugung fangen bei mindestens 30 € an und werden schnell teuer. Da ich noch einen alten Computerlüfter herumliegen hatte und noch andere Kleinigkeiten habe ich einfach mir selber was gebastelt.
Die Einkaufsliste ist dabei relativ kurz ausgefallen:

- [Aktivkohlefilter](https://www.conrad.de/de/p/toolcraft-79-7202-aktivkohlefilter-l-x-b-x-h-120-x-120-x-10-mm-2283829.html) (5,50 €)
- [Wippschalter](https://www.conrad.de/de/p/tru-components-wippschalter-r13-112a-b-b-0-i-250-v-ac-6-a-1-x-aus-ein-rastend-1-st-1565955.html) (2,10 €)
- [Batterieclip](https://www.conrad.de/de/p/beltrona-9v-i-clip-s-batterieclip-1x-9-v-block-druckknopfanschluss-l-x-b-x-h-26-x-13-x-8-mm-650514.html) (1 €)
- [Batteriehalter 8 x AA](https://www.conrad.de/de/p/takachi-sn38a-batteriehalter-8x-mignon-aa-kabel-l-x-b-x-h-107-9-x-31-x-28-mm-1882352.html) (7,50 €)
- [8 x AA-Batterien](https://www.conrad.de/de/p/basetech-mignon-aa-batterie-alkali-mangan-2650-mah-1-5-v-24-st-1604976.html) (~1,50 €)
- [Klettband zum Kleben](https://www.conrad.de/de/p/toolcraft-kl50x100sc-klettband-zum-aufkleben-haft-und-flauschteil-extrastark-l-x-b-100-mm-x-50-mm-schwarz-1-paar-419957.html) (1 €)
- Sekundenkleber (~1 €)
- ~130 mm² 3 mm dickes Sperrholz Pappel zum lasern (3~9 €)

Das meiste hatte ich bei meinem letzten Einkauf aus China von AliExpress noch in Fülle da, sodass der endgültige Preis für mich selber noch mal deutlich nach unten ging.

Ich habe mich bei der Stromversorgung für 8 x AA 1,5V Batterien entschieden da diese günstig zu bekommen sind, das Projekt mobil zum Mitnehmen machen und weil einfach noch genug davon herumliegen hatte. Der Batteriehalter ist mithilfe von Klettband innen befestigt um diesen rauszunehmen und mit neuen Batterien aufzufüllen. Mit meinem Multimeter habe ich eine Spannung von 12,41 V gemessen. Einen Nachteil gibt es hier natürlich: Und zwar sinkt die Spannung von AA-Batterien gegen Ende ihrer Laufzeit und der Lüfter wird langsamer drehen. Genaue Laufzeiten habe ich auch noch aufstellen können und muss diese noch selber austesten in den kommenden Wochen.

{% include image.html url="multimeter.jpg" description="Damit läuft der 12 V Computerlüfter mit voller Geschwindigkeit" %}

Der Aktivkohlefilter ist mithilfe von Sekundenkleber angeklebt und hält überraschend stabil. Bis ich die richtigen Abmessungen für die Löcher vom Lüfter hatte, hab ich drei Versuche benötigt. Der Wippschalter hält ohne Kleber im ausgelaserten Loch. Das Grundgerüst zum lasern habe ich mithilfe von [Boxes.py generiert](https://www.festi.info/boxes.py/ClosedBox?FingerJoint_angle=90.0&FingerJoint_style=rectangular&FingerJoint_surroundingspaces=2.0&FingerJoint_edge_width=1.0&FingerJoint_finger=2.0&FingerJoint_play=0.0&FingerJoint_space=2.0&FingerJoint_width=1.0&x=150&y=68&h=150&outside=0&thickness=3.0&format=svg&tabs=0.0&debug=0&labels=0&reference=0&burn=0.1&render=0) und dann mithilfe von Inkscape erweitert um Löcher für Wippschalter, Filter und Lüfter passend herauszuschneiden.

{% include image.html url="SolderFumev4.svg" description="SVG Vektordatei zum lasern mit 3 mm Pappel" %}

In ersten Tests mit einer Kerze habe ich festgestellt das der Lüfter fast *zu gut* läuft und im Video unten fast die Flamme der Kerze komplett eingezogen hat. Man könnte natürlich noch eine Form eines Voltage Regulators einbauen, um etwa stabile 12 V zu liefern oder auf weniger zu gehen damit der Lüfter langsamer läuft.

{% include video.html youtube-id="yUIQnX5Po_A" thumbnail="kerze.jpg" %}

Zuerst hatte ich die Idee als "Serviceklappe" das obere Holzstück mit dem Aufdruck und Wippschalter zu nutzen. Nach ersten Tests habe ich jedoch festgestellt das auch die vordere Platte mit dem Filter möglich ist, wenn man alle anderen Platten etwas schief verklebt. Einmal eingesetzt muss man erst mit einem spitzen Gegenstand die Platte rausfrimmeln und hält gut. Das hat den Vorteil das man eines Tages den Filter relativ einfach tauschen kann.
