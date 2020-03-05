---
layout: post
title:  "GitHub und Microsoft"
date:   2018-06-09 16:00:00 +0100
category: Dev
tags: git open-source ms
author: Der-Eddy
keyword: githubms
---

[Am 4. Juni 2018 gaben GitHub und Microsoft bekannt das Microsoft GitHub aufgekauft haben](https://blog.github.com/2018-06-04-github-microsoft/) für 7,5 Mio. $. Während man sich bei GitHub freut, [wandern mehrere tausende Nutzer auf andere Git Plattformen wie GitLab](https://motherboard.vice.com/en_us/article/ywen8x/13000-projects-ditched-github-for-gitlab-monday-morning) oder hosten sogar ihre Git Web-Oberfläche selber mit [Gitea](http://gitea.io/), [Gogs](https://gogs.io/) oder eben GitLab selber.

Vielen GitHub Nutzern stößt die Ankündigung sauer auf, vor allem auch auf Reddit:

{% include image.html url="reddit.png" %}

Die Realität sieht jedoch anders aus, vor einigen Jahren hat Microsoft angefangen sich mehr mit Open-Source auseinander zu setzen und ihre GitHub Repositories gehören zu den beliebtesten:

{% include image.html url="microsoft-repository.png" %}

Vor allem auch Visual Studio Code gilt [inzwischen als beliebterer Editor](https://insights.stackoverflow.com/survey/2018/#development-environments-and-tools) als Atom.io (welcher von GitHub gepusht wurde) und Visual Studio (ohne "Code") gehört auch immer noch zu den ganz Großen.

{% include image.html url="stackoverflow.png" description="Screenshot von Stackoverflow Developer Survey 2018" %}

Trotzdem bleibt ein fader Beigeschmack, Microsoft nutzt beispielweise bis heute ein proprietäres Format für ihre Office Dokumente.

Aber immerhin hat die Debate über GitHub nun etwas gutes:
Man schaut sich jetzt endlich nach Alternativen um, hosten eventuell seine Git Repositories auf mehreren Servern statt das Monopol nur GitHub zu überlassen.
Zu diesem Zweck habe ich interessante Vor- und Nachteile der beliebtesten Git Web-Oberflächen zusammengetragen:

<h2>GitHub</h2>

\+ Am beliebtesten

\+ Der Status Quo

\+ Kanban Projekt Board

\+ Static Webhosting via GitHub Pages

\+ Snippets

\+ Signierte Commits via GPG key

\+ Merge Approval System


\- Nicht Open-Source

\- Keine privaten Repos ohne zu bezahlen

\- Ändern regelmäßig ihr Interface

\- Kein einfacher Import aus anderen Git Oberflächen

\- Keine Möglichkeit der Authentifizierung bei Import über Git oder SVN Server


<h2>GitLab</h2>

\+ Gratis private Repositories  

\+ Open-Source in der Community Edition  

\+ Selbst hosten ohne Probleme möglich  

\+ Gratis Paid membership für Schulen und big Open-Source Maintener  

\+ CI (Continuous integration) Tests  

\+ Kanban Projekt Board  

\+ Static Webhosting via GitLab Pages  

\+ Einfacher Import aus anderen Git Oberflächen wie GitHub, BitBucket, Google Code und self hosted Gitea oder GitLab  

\+ Snippets  

\+ Signierte Commits via GPG key  

\+ Code Quality Checks  

\+ Merge Approval System  


\- Teilweise etwas träge

\- Releases maximal 2 MB pro Datei

\- Benötigt viele Ressourcen in der Self hosted Variante

<h2>Bitbucket</h2>

\+ Gratis private Repositories

\+ CI Tests

\+ JIRA Support

\+ Kanban Board via Trello Integration

\+ Snippets

\+ Einfacher import aus GitHub, SourceForge und CodePlex

\+ Starke Integration von weiteren Atlassian Diensten


\- Kein Support von signierten Commits via GPG key

\- Starke Abhängikeit von weiteren Atlassian Diensten

\- Self hosted nur via Bezahlung

\- Nicht Open-Source

<h2>Gogs / Gitea</h2>

\+ Gratis private Repositories

\+ Verbrauchen kaum Ressourcen

\+ Einfache Möglichkeit für (self-updating) Mirror

\+ Signierte Commits via GPG key


\- Keine native CI Tests

Gogs und Gitea nehmen sich wirklich nicht viel, außer das Gogs eher an das Interface von GitHub angelehnt ist. Gitea hat sich von Gogs abgespalten da Gogs nur einen Haupt-Maintener hat welcher restriktiv vorgegangen ist, die beiden Projekten übernehmen häufiger neue Features.

Alle fünf bieten diese Basis Features:

\+ Mächtige API

\+ Issue Tracker

\+ Wiki

\+ Pull Requests

\+ Releases

\+ 2FA

\+ Docker Support (für die self hosted Varianten)

\+ Webhooks

\+ Teams bzw. Organisationen

\+ Git LFS
