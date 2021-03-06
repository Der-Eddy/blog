---
layout: post
title:  "Atom vs. Sublime Text"
date:   2016-03-21 15:00:54 +0100
category: Development
tags: dev editor ide
author: Der-Eddy
keyword: atomvsst
---
Nachdem ich jetzt beide Editors länger getestet habe, möchte ich hiermit meine Erfahrungen nieder schreiben.

<h3>Sublime Text</h3>
Angefangen habe ich vor 2 Jahren nach der Suche nach einen kleinen und leichtgewichtigen Pseudo-"IDE" für meine Python Projekte die nicht nur unter Windows, sondern auch Mac OS X und Linux läuft. [Sublime&nbsp;Text](https://www.sublimetext.com/) war damals das Mittel zur Wahl für diesen Fall, der Editor konnte bereits damals über das inoffizielle Plugin System [Package Control](https://packagecontrol.io/) mit Plugins versorgt werden für jeden Anwendungsfall auch wenn teilweise Plugins ein wenig kosten (z.B. das [SFTP Plugin](https://wbond.net/sublime_packages/sftp) für 30$). Nach einigen Monaten mit Sublime Text bemerkte ich jedoch das einige Funktionen nicht so funktioniert haben wie gewollt oder Plugins Fehlermeldungen ausgaben. Auf der Suche nach alternativen Plugins schaut man jedoch oft in die Röhre, einigen sind auch nicht Open-Source und/oder dokumentiert sodass selbst Hand anlegen auch erschwert wurde und im besten Fall auch bereits mehrere Jahre alt. Die letzten Releases kurz aufgeschlüsselt:  

- 9\. Februar 2016  
- 26\. März 2015 (Hotfix)  
- 24\. März 2015  
- 27\. August 2014  
- 17\. Dezember 2013  
- 27\. Juni 2013
- etc ...  

*[Quelle](https://www.sublimetext.com/3)*

Das Problem entsteht dadurch das an Sublime Text 1 (!) einziger Entwickler arbeitet während das Projekt Closed-Source ist.

<h3>Atom</h3>
Mein erster Eindruck von [Atom](https://atom.io/) war: "Sieht ja nett aus, aber Sublime Text ist besser!", erste Tests bestätigten diese Aussage auch. Nach knapp einem Jahr öffentlicher Beta gab man bekannt: [Atom&nbsp;Version&nbsp;1.0](http://blog.atom.io/2015/06/25/atom-1-0.html) ist raus, der Editor hatte nun alle Funktionen die er haben sollte. Und ich wagte einen weiteren Versuch da ich langsam genervt war von einigen Bugs in Sublime Text und tatsächlich wurde ich dies mal nicht enttäuscht. Atom war nicht nur nun ein vollständiger Editor sondern bot auch genug Möglichkeiten diesen an seinen eigenen Geschmack anzupassen, hunderte Entwickler sprangen auf den Zug auf und entwickelten Open-Source Plugins für Atom und jeden erdenklichen Zweck. Einige Daten von heute (Update: 07. Juni 2016):

**Sublime Text:**  
3.660 Packages (Plugins & Themes)  
*[Quelle](https://packagecontrol.io/stats)*

**Atom:**  
5.646 Packages (4.344 Plugins & 1.302 Themes)  
*[Quelle Plugins](https://atom.io/packages), [Quelle Themes](https://atom.io/themes)*

Damit überholt Atom bereits Sublime Text an Vielfalt in Packages, dies ist wahrscheinlich dem einfachen Aufbau geschuldet der besonders an Web Development angelehnt ist. Jedes namhafte Plugin gibt es auch als Nachbau für Atom, auch z.B. das [SFTP Plugin](https://wbond.net/sublime_packages/sftp) welches 30$ kostet gibt es als [Open-Source Variante](https://atom.io/packages/remote-edit).
Zum heutigen Zeitpunkt (21. März 2016) haben an Atom 285 Entwickler mit gearbeitet ([Quelle](https://github.com/atom/atom/graphs/contributors)), davon auch mehrere Vollzeit Entwickler von GitHub und halten damit den Editor schnell Up-to-date, größere Bugs werden im Beta Channel abgefangen bevor sie die große Masse erreichen. Manko an Atom ist jedoch dadurch das der Editor nicht so stark Low-Level programmiert wurde wie Sublime Text (C++ und Python) sondern in HTML, JavaScript, CSS, und Node.js, spürt man oft das der Editor ein wenig träge ist und auch etwas länger zum starten braucht. Mit jedem Update wird dies jedoch verbessert und Atom bekommt regelmäßiger einen neuen Release im Vergleich zu Sublime Text. Man muss jedoch auch sagen das in der schieren Masse an Plugins, auch viele schnell in ein paar Stunden enstanden sind und nicht gerade effizient im Verbund arbeiten.

<h3>Zusammenfassung</h3>

Zum jetzigen Zeitpunkt rate ich jedem der noch auf der Suche ist, zu Atom, alle Komponenten sind Open-Source sodass man nicht nur bei Bedarf selber den Aufbau sich genauer anschauen kann sondern auch im Fall das z.B. ein Plugin Entwickler keine Lust mehr hat seinen Code übernehmen kann (Was bei Sublime Text Plugins nicht immer gegeben ist). Vor allem da Atom komplett kostenlos ist, während Sublime Text nur kostenlos "getestet" (ohne Zeitbeschränkung) werden kann. Fakt ist jedoch das beide Editors eine gute Grundbasis liefern, man kann sich den restlichen Umfang komplett mit Plugins selber an seine Wünsche gestalten. Zwar hat der Entwickler von Sublime Text Besserung versprochen und bereits sein uraltes Forensystem auf ein modeneres aufgeürstet, jedoch sieht es immer noch sehr mau um seine Aktivität aus.

<h3>Andere Editors die anzumerken sind</h3>

Einen anderen namhaften Editor habe ich hier bewusst außen vor gelassen, die Rede ist von Adobes Projekt [Brackets](http://brackets.io/) welcher zwar auch Open-Source ist jedoch besonders auf Frontend Web Developer abzielt vor allem durch die stark beworbene "Code-Vervollständigung aus einer PSD-Datei" Funktion, solltet ihr Frontend Developer sein ist es nicht verkehrt sich diese Editor vorzuziehen da dieser Funktionen inne hat die man so kaum für die anderen findet bzw. nur abgespeckt.

Ein relativer Neueinsteiger ist auch [Visual&nbsp;Studio&nbsp;Code](https://code.visualstudio.com/), welches genau wie Atom auch [Electron](http://electron.atom.io/) für das GUI benutzt und damit auf ähnliche Probleme trifft (Langsamer Start, teilweise träges GUI). Ich habe damals die erste Version getestet und konnte wirklich nicht viel abgewinnen, der Funktionsumfang war gering und Plugins fast nicht existent.  Das hat sich nach mehreren Monaten geändert und ich sollte noch mal einen neuen eigenständigen Test durchführen. Interessanterweise läuft Visual Studio Code jedoch gefüllt flüssiger als Atom. Auf jeden Fall auch ein Blick Wert.

Der letzte im Bunde ist [Limetext](http://limetext.org/), ein Versuch einen Open-Source Klon von Sublime Text zu erstellen, Limetext hat vor allem den Vorteil das man viele Sublime Text Plugins fast ohne Probleme übernehmen kann. Jedoch bekam der Editor nicht viel Aufmerksamkeit und seit 2 Jahren ist es eher still um den Editor geworden. Es fehlte wohl einfach an einem großen Namen der hinter dem Projekt steht wie im Fall von Atom GitHub, Visual Studio Code Microsoft oder bei Brackets Adobe.
