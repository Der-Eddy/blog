---
layout: post
title:  "Hackspace"
date:   2020-03-06 14:00:00 +0100
category: Hackspace
tags: hackspace
author: Der-Eddy
preview: outside.jpg
keyword: bk
---

Hackspaces bzw. Hackerspaces oder FabLabs sind vor einigen Jahren geradezu wie Pilze aus dem Boden geschossen, jede größere Stadt hatte mindestens einen eröffnet. Vor allem auch durch den Chaos Computer Club (CCC) wurden viele lokale Vereine gegründet die ähnliche Räumlichkeiten bereitstellen.

Vor etwas mehr als einen Monat hab ich mich nun endlich auch getraut in einem meiner lokalen Hackspaces vorbeizuschauen und mir das selber mal anzuschauen. Dafür besuchte ich die <a href="https://www.binary-kitchen.de/wiki/doku.php">Binary-Kitchen</a> welche seit 7 Jahren in Regensburg besteht und eigene Räumlichkeiten anbietet für Vereinsmitglieder und außenstehende. Der Name kommt unter anderem davon das dort auch leidenschaftlich gerne gekocht wird, es gibt aber auch andere Interessen abseits von IT-Themen wie einen eigenen Garten oder eigene Bienenstöcke. Der Verein hat auch andere Vereine wie <a href="https://www.regensburg-repariert.de/">Regensburg Repariert</a> oder die Amateurfunker in Regensburg eingegliedert. Interessanterweise gehört die Binary-Kitchen derzeit jedoch nicht offiziell zum CCC als "Erfa-Kreis", trotz großer Nähe zu diesem.

{% include image.html url="outside.jpg" description="Die Front des Hauptgebäudes ist mit LED Spielereien geschmückt" %}

Jeden Montag Abend werden gerne Führungen dort angeboten durch die 3 größeren Räume: Einer "Lounge" mit angegliederter Küche, im Keller ein Labor mit Lötstationen, 3D-Druckern und Amateurfunker Equipment und auf der gegenüberliegenden Straßenseite eine Werkstatt mit CNC Fräse, Lasercutter und anderem Werkzeug. Vor allem der 80W CO<sub>2</sub> Lasercutter um unter anderem Holz oder Plexiglas über SVG Dateien "auszuschneiden" hat es mir angetan, in einem zukünftigen Blog-Eintrag wird es mehr Informationen zu ersten Projekten damit von mir geben. Einige Beispiele was man aus Holz machen kann, <a href="https://florianfesti.github.io/boxes/html/generators.html">findet man hier</a>.

{% include image.html url="inside.jpg" description="Im Hauptraum findet man in jeder Ecke spannende Sachen" %}

Auch spannend für mich ist der Grad der Heimautomatisierung welche man dort aufgebaut hat, auch komplett offline ohne Cloud Anbindung. Im Hauptraum gibt es viele verschiedene Lampen welche man über ein OpenHab Webinterface ein-/ausschalten kann oder teilweise sogar die Farbe umstellen kann. Der Kompressor in der Werkstatt wird nach einer bestimmten Uhrzeit als Lärmschutzgründen abgeschaltet, der Lasercutter geht erst an wen ein passendes Fenster zur Lüftung offen ist oder das Aufzeichnen von Temperaturen oder Feinstaub in der Luft. Außerdem gibt es in beiden Gebäuden Monitore an den Wänden speziell, um das OpenHab Interface anzuzeigen.

Das Haupt-Gebäude hat auch eine interessante Türsteuerung: Vereinsmitglieder können die Tür per App öffnen und von innen gibt es eine Ampel-ähnliche Steuerung. 

{% include image.html url="doorlock.jpg" description="Außer mit der App, kann man die Tür auch per Hardware steuern" %}

- "Grün" bedeutet, dass die Tür offen für alle ist, das wird auch auf der Webseite so öffentlich angezeigt. 
- "Gelb" bedeutet, dass ein Mitglied anwesend ist, jedoch nicht im Hauptraum ist um Nicht-Mitglieder zu empfangen. 
- "Rot" steht schlicht dafür das niemand anwesend ist und die Tür zuschließt, auch diesen Status findet man auf der Webseite.

Anhand des Status der Tür hängen auch andere Heimautomatisierungen ab, so laufen die Lampen im Hauptraum abends auch, nur wenn die Tür offen ist oder die Heizungen schalten sich ab wen niemand anwesend ist.