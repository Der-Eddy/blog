---
layout: post
title:  "Bye Bye Microsoft, Hallo Linux"
date:   2019-02-24 15:00:00 +0100
category: Umstieg
tags: windows arch
author: Der-Eddy
keyword: byebyemicrosoft
preview: archlinux-logo-light.svg
---
Wie in meinem anderen Beitrag, zum Umstieg auf Android, bereits angedeutet wollte ich gerne zu Linux wechseln und konnte es niemals machen da ich immer an iTunes an Windows oder macOS gebunden war.
Angefangen mit freeBSD Servern, übergehend zu Debian und Ubuntu Servern für Minecraft Servern habe ich bereits seit fast 10 Jahren in irgendeiner Form mit Unix zu tun gehabt. Arbeitstechnisch wurde ich, dann zu einem der wenigen in einer ehemaligen Firma, die sich überhaupt mit Linux auskannte und musste mich fortan um das Meiste bezüglich Debian und Ubuntu Servern kümmern. Nach Wechsel der Firma verlief die Leidenschaft zu Linux ein wenig im Sande über die Jahre wieder ein wenig. Trotzdem pflegte ich fast durchgehend einen persönlichen Ubuntu Server für Webserver und andere Spiele Reihen und musste meinen Microsoft Windows Workflow ein wenig anpassen dafür. Irgendwann hab ich gemerkt wie sehr ich Microsoft Windows umstellen musste damit ich überhaupt arbeiten konnte. Außerdem war ich unzufrieden mit der Update-Politik von Windows 10 und habe auch nie verstanden was die Leute so an Windows 7 feiern, Windows Aero war alles andere als Perfekt.

Zwischenzeitlich hatte ich auch mal zum Versuch Arch Linux auf einem Macbook installiert und es gefiel mir schon, jedoch fand ich es zu der Zeit noch nach zu viel Arbeit. Nachdem Arch Linux immer beliebter wurde und ich nach Ersatz für Windows gesucht hatte, wollte ich es noch mal versuchen mit Arch Linux. In einer virtuellen Maschine hatte ich also verschiedene Konfigurationen ausprobiert und die Installation noch mal durchgegangen bis ich anschließend komplett zum Fan wurde.

Die passende Linux Distribution
---

{% include image.html url="archlinux-logo-light.svg" description="" %}

Der Trick von Arch Linux ist nämlich, das Arch Linux ohne grafischen Installer ausgeliefert wird und im Gegensatz zu fast allen anderen Linux Distributionen wie zum Beispiel Debian, Ubuntu oder Fedora keine fixen Releases hat, sondern als sogennantes "Rolling Release" fungiert und Updates von Upstream nur mit wenigen Tagen Abstand in die Main Repositories kommen. Das sorgt dazu das eine Arch Linux Installation immer sehr aktuell bleibt und man keine Monate oder Jahre warten muss auf neuere Versionen außerhalb von Sicherheitspatches. Viele Linux Nutzer sagen deswegen das Arch Linux nicht "stabil" ist und Programm Pakete mindestens mehrere Monate verfügbar sein müssen bevor sie erst als stabil und sicher gelten. Ich hatte jedoch in der Vergangenheit eher das Gegenteil erfahren, wenn ich versuchte einige neuere Pakete in z. B. Ubuntu einzupflegen und dadurch sogar die Upgrade-Installation oft schieflief. Letztlich ist das eigene System nur so stabil wie man es auch stabil macht, der Unterbau kann dabei helfen, aber es ist kein Alleinstellungsmerkmal für ein stabiles System.

Ein weiteres Problem von Linux Distributionen löst Arch Linux sehr gekonnt durch das AUR (Arch User Repository). Linux Distributionen kommen mit einem Paket Manager, welcher auf ein großes Archiv von Paketen Zugriff hat, welche man zusätzlich installieren kann anstatt wie bei Windows ausführbare *.exe Dateien aus dem Internet, aus teilweise dubiosen Quellen, laden muss. Das Problem taucht auf wen ein bestimmtes Programm, das man braucht nicht in den Paketquellen vorhanden ist, dann muss man ähnlich zu Windows entweder *.deb (Debian/Ubuntu) oder *.rpm (Fedora) Archive laden oder auf Snaps/Flatpack/AppImages setzen. Jedoch unterstützen nur Snap Pakete unter Ubuntu Updates und alle anderen müsste man fast immer manuell updaten.
Sogenannte AUR Helper wie z.B. yay oder trizen binden sich nun nahtlos in den offiziellen Paket Manager ein und erlauben den Zugriff auf das AUR welches aus Binary Pakete (wie die offiziellen Paketquellen) besteht sowie Build/Compile Instructions um Pakete aus Git Repositories zu bauen. Das einzige Problem ist, dass das AUR durch die Community verwaltet wird und theoretisch Missbrauch erlaubt, weswegen jedem immer empfohlen wird vorher die Build Instructions anzuschauen bevor man blind etwas installiert.

Ein weiterer Pluspunkt für Arch Linux ist ihr Wiki, das [Arch Wiki](https://wiki.archlinux.org/index.php/Main_page) ist wahrscheinlich im Moment das größte Linux Wiki und geht um einiges mehr ins Detail als z. B. das Ubuntu Wiki, welches teilweise nur eine hübschere Man Page ist. Weil man die Installation auch anhand einer Anleitung im Wiki abschließen muss (sofern man sie nicht schon auswendig kann), lernt man dabei auch ein wenig über die Komponenten im Hintergrund und wie sie ineinander laufen. Natürlich ist es immer noch stark vereinfacht, es ist bei weitem kein LFS (Linux from Sratch) bei dem man noch weiter in jede Komponente gehen muss und sich aktiv mit Kleinigkeiten kümmern muss. In dem Sinne trifft Arch Linux für mich den perfekten Punkt zwischen der Einfachheit eines grafischen Installers oder schlicht überhaupt keinen wie bei LFS.
Dadurch konnte ich auch mein System ein wenig genauer anpassen, anstatt meine Installation auf dem altbekannten ext4 Dateisystem aufzubauen, entschied ich mich für btrfs und eine Verschlüsselung mit LUKS und kann dadurch auf Features wie De-duplication oder Subvolume Snapshots zugreifen, welche bei ext4 nicht auf einer solchen low-level Ebene vorhanden sind.

In Kombination mit den neueren Paketen und "normalen" Standardkonfigurationen, anders als z. B. bei Manjaro, hab ich mich letztlich für Arch Linux entschieden. Fehlt nur noch eine passende Desktopoberfläche (DE / Desktop Environment) weil ich mich noch nicht mit einem barebones Terminal bzw. nur einem Window Manager anfreunden kann.

Die passende Desktopoberfläche
---

Unter Arch Linux kann man so ziemlich jede absurde Kombination installieren, ich habe mich aber erst mal mit den großen Drei auseinandergesetzt, XFCE, Gnome und KDE. XFCE findet seine Nische als leichtgewichtige Oberfläche, welche jedoch auf GTK aufbaut. Gnome war für mich eine absolute Katastrophe, nicht nur das es viel zu viele Ressourcen für zu wenig Nutzen verbraucht, sondern die Entwickler aktiv Features mit neueren Versionen entfernen. In meiner Anfangszeit hatte ich noch Spaß an Gnome 2 gehabt, mit Gnome 3 haben die Entwickler jedoch in meinen Augen nichts Ordentliches hervorgebracht.
Blieb noch KDE Plasma übrig, welches Qt statt GTK nutzt und mit einem großen Umfang an Zusatzsoftware passend für KDE entwickelt.

{% include image.html url="screenshot.png" description="Screenshot über meine beiden Monitore" %}

KDE hat mich wirklich überrascht mit seinem großen Umfang an Optionen und der Möglichkeit über kvantum das Design noch genauer anpassen zu können. Zusätzlich bin ich um einiges mehr zufrieden mit dem File Manager Dolphin als mit der GTK Katastrophe Nautilus. Ein weiteres cooles Feature von KDE ist auch KDE Connect, welches für eine ähnliche Erfahrung wie macOS <> iOS jedoch für Linux <> Android sorgt und Benachrichtigungen oder Dateien austauscht oder die Wiedergabe am Linux Computer automatisch stoppt bei einem Anruf.

{% include image.html url="kdeconnect.png" description="Screenshot vom KDE Connect Einstelletungsdialog" %}

Anschließend entschied ich mich letztlich für KDE Plasma anstatt dem überaus beliebten Gnome 3 oder Alternativen.

Spiele
---

Ein weiteres Problem beim Umstieg waren für mich Spiele, der Großteil meiner Steam Bibliothek ist schließlich Windows exklusiv. Hier preschte Valve letztes Jahr mit Proton für ihre Vertriebsplattform Steam hervor. Proton ist eine Kombination aus Wine, Winetricks, DXVK und anderen Kleinigkeiten um Windows exklusive Spiele unter Linux spielbar zu machen. Eine Auflistung von Nutzer-Berichten zu Proton findet man unter [Protondb](https://www.protondb.com/). Dadurch kommt meine Linux Bibliothek plötzlich auf knapp 70% meiner Windows Bibliothek auf Steam und in Kombination mit meiner Playstation 4, kann ich trotzdem fast jedes Spiel, das ich auch spielen möchte, auch ohne Windows spielen. 
Zugegeben, ich bin kein großer Fan von großen Multiplayer Spielen wie Apex Legends (welche oft Anti-Cheat Maßnahmen nutzen, welche inkompatibel zu Proton sind) oder AAA Spiele (welche oft Denuvo Kopierschutz nutzen, auch größtenteils inkompatibel zu Proton) wie das neueste Assassin's Creed. Wodurch die meisten Spiele, welche Probleme machen, schlicht wegfallen.

{% include image.html url="protondb.png" description="Screenshot von protondb.com" %}

Nach etwa 4 Monaten mit Arch Linux und KDE Plasma bin ich mehr als zufrieden mit dem Wechsel und trauere Windows nicht mehr hinterher. Für einige Kleinigkeiten muss ich immer noch Windows hochfahren, das hält sich aber wirklich in Grenzen von ein mal pro alle paar Wochen.