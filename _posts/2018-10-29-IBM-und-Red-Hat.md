---
layout: post
title:  "IBM und Red Hat"
date:   2020-12-10 00:00:00 +0100
category: Linux
tags: ibm cloud linux redhat centos fedora
author: Der-Eddy
keyword: roterhut
---

[Am 29. Oktober 2018 gaben IBM](https://newsroom.ibm.com/2018-10-28-IBM-To-Acquire-Red-Hat-Completely-Changing-The-Cloud-Landscape-And-Becoming-Worlds-1-Hybrid-Cloud-Provider) [und Red Hat bekannt](https://www.redhat.com/en/about/press-releases/ibm-acquire-red-hat-completely-changing-cloud-landscape-and-becoming-worlds-1-hybrid-cloud-provider?intcmp=701f2000000RWK2AAO) das IBM sich alle Aktien von Red Hat zum Preis von 190$ (Börsenkurs zur Ankündigung: 116$), also insgesamt 34 Milliarden Dollar, kauft und sich damit Red Hat einverleibt.

Red Hat ist die derzeit größte Linux Firma der Welt und betreut nicht nur Linux-Distributionen wie das namens gebende Red Hat sondern auch CentOS, Fedora und CoreOS. Oben drauf beschäftigt Red Hat eine sehr große Zahl an Linux Entwicklern welche maßgeblich an Projekten wie Wayland, Xorg, Gnome, flatpak, GTK, systemd und vielen weiteren wichtigen Bestandteilen von Linux arbeiten. IBM wird jedoch wahrscheinlich am Cloud Provider Geschäft mehr interessiert sein, da sie auch dort versuchen wieder mehr Fuß zu fassen zwischen Google, Amazon, Microsoft und Alibaba.

Damit ist dieser Einkauf einer der Größten in der IT-Industrie und wirft eine Menge Angst auf. Was wohl nicht von irgendwo kommt, eingekaufte Firmen von IBM sind intern oft bekannt als "Blue Washing", bei dem bestehende Prozesse der eingekauften Firma durch IBM Lösungswege ausgetauscht werden, völlig egal ob sie für diesen Fall besser sind oder nicht, zumindest bleibt der CEO von Red Hat weiterhin als dieser Aktiv. Bleibt die große Angst ab wann IBM die Open-Source Arbeit der unzähligen Linux Entwickler als "unnötig" einstuft und eindampft, wie es leider schon häufiger nach dem Einkauf von IBM geschehen ist. 

Im Moment kann leider niemand genau sagen was wie Linux, wie wir es kennen, sich durch diese Einverleibung verändert wird. Im besten Fall erkennt IBM wie wichtig die Arbeit von Red Hat und all ihren Mitarbeitern ist um ein gutes Linux System aufzubauen. Im schlimmsten Fall wird IBM rigerös den roten Stift ansetzen und jede "unnötige" Arbeit streichen die Red Hat bislang in Kauf genommen hat für das Wohl von Linux.

Ich für meinen Teil werde meine Bestrebungen wegen einem Wechsel von Ubuntu auf Fedora, erst mal auf Eis legen und warten wie die Sache auf lange Sicht ausgehen wird. In der Zeit finde ich vielleicht eine passendere Linux-Distribution. Aber erst mal müssen sich noch Aktionäre und Investoren von Red Hat darüber einigen.

<h2>Update: 10.12.2020</h2>
Am <a href="https://blog.centos.org/2020/12/future-is-centos-stream/">8.12.2020 gibt es eine große Ankündigung von CentOS</a> zu dem Thema. Nach 26 Monaten seit der Ankündigung zur Red Hat Übernahme scheint man nun Konsequenzen zu ziehen und "degradiert" CentOS zu einem Beta-Test von RHEL. Anscheinend hatte ein Erbsenzähler bei IBM bemerkt das einige Firmen lieber kostenlos CentOS nutzen anstelle für Lizenzen für RHEL zu zahlen.

Beginnend 2022 wird CentOS 8 auf eine Art rolling release umgestellt namens "CentOS Stream" und damit zwar immer noch sehr ähnlich zu RHEL aber eben nicht mehr 1:1 gleich. Genau genommen war das aber vorher schon nicht immer der Fall, CentOS hatte sich oft sehr lange Zeit gelassen für Security Updates, der Konkurrent Oracle Linux macht das zu einem seiner Pluspunkte gegenüber CentOS deutlich:

{% include image.html url="centos-delay.png" description="Quelle: https://linux.oracle.com/switch/centos/" %}

Während Oracle Linux sich als Ersatz positionieren (mit <a href="https://blog.dbwatch.com/how-to-avoid-oracles-licensing-traps">fragwürdigen Oracle Lizenzkosten</a>), hat sich schnell Mitbegründer von CentOS Gregory Kurtzer zu Wort gemeldet:

{% include image.html url="Greg.png" description="Quelle: https://blog.centos.org/2020/12/future-is-centos-stream/#comment-183642" %}

Das neue Projekt hat bereits Forum und Namen bekommen: <a href="https://forums.rockylinux.org/">Rocky Linux</a>

Man kann auch positives aus der Ankündigung herausziehen, wie zum Beispiel das Red Hat jetzt vielleicht endlich mal rolling releases massentauglich machen könnte und den Mythos brechen könnte das diese nicht zuverlässig laufen und sofort kaputtgehen. Oder das man endlich mal wieder frischen Wind in die RHEL forks gebracht hatte, nachdem CentOS seit Jahren eher träge mit Entwicklung und Updates sich hinter RHEL herschleppen. Realistisch betrachtet werden aber die meisten sich eher nach Alternativen umschauen und vielleicht bei Rocky Linux oder Oracle Linux hängen bleiben oder sich ganz Red Hat abwenden und eher Richtung SUSE/OpenSUSE umschauen.
