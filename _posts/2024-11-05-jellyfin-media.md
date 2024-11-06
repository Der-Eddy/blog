---
layout: post
title:  "Jellyfin und wie man es mit Videos befüllt"
date:   2024-11-05 02:00:00 +0100
category: Selfhosting
tags: linux serien filme
author: Der-Eddy
preview: Jellyfin.png
keyword: jellyfin-media
---

Seit einigen Jahren benutze ich [Jellyfin](https://jellyfin.org/), um Serien und Filme auf meinem Fernseher einfacher ansehen zu können, theoretisch könnte ich damit auch meine Bilder-/Audio-/Buch-Sammlung sortieren, aber diese Funktion benutze ich nicht. Jellyfin ist als Fork von Emby entstanden, als Emby von Open Source zu Closed Source wurde und schon vorher damit begonnen hatte, beliebte Features hinter Bezahlschranken zu stellen. Das ist schon ein wenig ironisch. Denn Emby entstand einst als Alternative zu Plex, das seinerseits durch Bezahlschranken negativ auffiel (die Plex Mobile App ist z.B. Premium only). Für mich war die Entscheidung also ziemlich klar, auch wenn vielleicht das Feature X oder Y bei Jellyfin fehlt. Der Einfachheit halber läuft Jellyfin bei mir in einem Docker Container auf meinem Heimserver. Die gute [Dokumentation](https://jellyfin.org/docs/general/quick-start/) erklärt aber auch andere Installationsmethoden und ist wirklich nicht so schwer wie man denkt.

Aber das eigentliche Thema dieses Blogeintrags ist ein anderes, wie fülle ich meinen Medienserver mit Videos?

{% include image.html url="Jellyfin.png" description="Jellyfin mit einigen Videos von Youtube und der ARDmediathek" %}

## MediathekenView
Wer in Deutschland lebt, muss pro Haushalt eine monatliche Gebühr für die öffentlich-rechtlichen Rundfunkanstalten zahlen. Warum also nicht auch deren Online-Mediatheken nutzen? Besonders einfach geht das mit MediathekenView bzw. [MediathekenViewWeb](https://mediathekviewweb.de/), mit dem man die (Video-)Mediatheken ganz einfach durchsuchen und direkt streamen oder downloaden kann. Der Download ist vor allem deshalb wichtig, weil nach dem aktuellen Rundfunkstaatsvertrag die Inhalte der Mediatheken nur zeitlich begrenzt zur Verfügung stehen dürfen. Teilweise ist dies nur für eine Woche, oft aber auch für ein Jahr.  
Zum Beispiel sind in dieser Woche Ghostbusters und Ghostbusters 2 bis zum 10.11.2024 in der 3sat Mediathek verfügbar.

{% include image.html url="GhostbustersI.png" description="Wie es in der 3sat Mediathek ausschaut" %}

{% include image.html url="GhostbustersII.png" description="Wie es in der MediathekenViewWeb ausschaut" %}

Aber auch Serien gibt es, z.B. Killing Eve oder [Feuer & Flamme](https://www1.wdr.de/fernsehen/feuer-und-flamme).

Leider sind die meisten Streams / Downloads nur in deutscher Sprache und ohne eingebaute Metadaten verfügbar. Zum Glück kann Jellyfin (oder ein anderer Media-Server) die Meta-Daten automatisch aus Online-Datenbanken wie IMdb, TheMoviedB oder TheTVDB beziehen und ergänzen. Ich empfehle auch die heruntergeladenen Videos direkt umzubenennen, damit der Mediaserver der Wahl die Metadaten leichter finden kann. Serien sollten am besten das Format "{Serienname} S01E01" haben, damit man sofort weiß, dass es sich um Folge 1 der ersten Staffel handelt.
Wer auf dem Laufenden bleiben will, was gerade in den Mediatheken verfügbar ist, kann z.B. bei [https://feddit.org/c/mediatheque](https://feddit.org/c/mediatheque) vorbeischauen. Hier sammelt die Feddiverse Community interessante Titel.

## Pinchflat um Youtube anzuzapfen
Es gibt Youtube-Videos, die ich lieber auf dem Fernseher als auf dem PC als Second-Screen-Content anschaue, aber leider ist die Youtube-App auf meinem Fernseher voller Werbung und eine Datenschleuder. Abhilfe schafft hier [Pinchflat](https://github.com/kieraneglin/pinchflat). Einmal eingerichtet und mit den gewünschten Youtube-Kanälen und Playlists gefüttert, kümmert sich Pinchflat um den Download der Videos in einen definierten Ordner (in dem Jellyfin dann Ausschau hält)

{% include image.html url="Pinchflat.png" description="Pinchflat kann genauso einfach in einem Docker Container schnell eingerichtet werden" %}

Als Bonus kann man direkt [Sponsorblock](https://sponsor.ajay.app/) auf die Videos anwenden und Werbung vom Content Creator direkt rausschneiden lassen.

{% include image.html url="Pinchflat-settings.png" description="Per Media Profile kann man eine Menge einstellen wie die Videos geladen werden sollen" %}

Damit Jellyfin die Videos nun nach Kanal-Namen mit Thumbnails anzeigt, empfele ich eine neue Library anzulegen mit dem Content Type "Music Videos".

## Privatkopie einer DVD/Blu-Ray
Mit wesentlich mehr Aufwand muss man rechnen, wenn man seine physische DVD/Blu-Ray Sammlung digitalisieren und eine Privatkopie sichern möchte. Das Problem ist hier vor allem das man einen PC mit Blu-Ray Laufwerk benötigt, die nicht gerade billig sind. Zusätzlich hat man das Problem das auf den Discs die Serien/Filme in wenig komprimierten Transport Streams (*.ts) vorliegen, die nicht immer in der richtigen Reihenfolge sind. An dieser Stelle möchte man wahrscheinlich den Stream nochmal in einen effizienteren Codec wie z.B. AV1 oder H256/HVEC vorkomprimieren, was z.B. Plex automatisch kann, Jellyfin aber nicht.  
Ich möchte auch noch mal darauf hinweisen, dass es nicht erlaubt ist, Privatkopien von ausgeliehenen DVDs/Blu-Rays, z.B. aus Bibliotheken, anzufertigen.

## Bonus
Wer informiert werden möchte, sobald neue Episoden bei Jellyfin eintreffen oder neue Youtube-Videos erscheinen, kann Jellyfin und Pinchflat mit [ntfy.sh](https://ntfy.sh/) kombinieren. Die Nutzung von ntfy.sh ist kostenlos, man kann aber auch den ntfy-Server selbst hosten. Einmal in Pinchflat eingerichtet, sieht das dann z.B. so aus:

{% include image.html url="ntfy.png" description="ntfy funktioniert ähnlich zu MQTT mit dem Topic Subscribe System" %}

Um auf dem Laufenden zu bleiben, muss man nicht mehr zur Datenschleuder Youtube/Google gehen und die "Glocke abonnieren".
