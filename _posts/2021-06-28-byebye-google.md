---
layout: post
title:  "Bye Bye Google"
date:   2021-06-28 15:00:00 +0100
category: Umstieg
tags: calyxos android privacy firefox degoogle
author: Der-Eddy
keyword: byebyegoogle
preview: calyxos.png
---
Vor über zwei Jahren bin ich von [meinem alten iPhone auf mein immer noch aktuelles Google Pixel Handy umgestiegen]({% link _posts/2019-02-23-byebye-apple.md %}). Das hat ehrlicherweise einen weiteren Umstieg nach hinten verschoben, den ich schon seit sehr langer Zeit plane: Endlich Tschüss zu Google zu sagen und wieder einen großen Teil meiner Privatsphäre zurückerlangen. Es gibt sogar einen eigenen Wikipedia Artikel nur um Kritikpunkte über Google bzw. deren übergeordneten Konzern Alphabet aufzulisten: [Kritik an der Google LLC](https://de.wikipedia.org/wiki/Kritik_an_der_Google_LLC). Wer immer noch nicht versteht, warum ich weg von Google möchte, kann gerne mal durch [Google Takeout](https://google.com/takeout) bzw. [Google Maps Zeitachse](https://www.google.de/maps/timeline?hl=de) durchgehen und sich selber ein Bild darüber machen, was Google eigentlich über mich weiß. Gründe gegen Google gibt es also genug, aber leider gibt es auch viele Gründe warum ich mit Google fest verkettet war oder teilweise immer noch bin.

{% include image.html url="maps.png" description="Was habe ich am 9. März 2019 gemacht? Während ich das schon lange nicht mehr weiß, könnte mir Google es genau erzählen" %}

Vor 2017 hat Google bei seinem Mail Dienst Gmail auch noch völlig unverblümt alle E-Mails automatisch analysieren lassen, inzwischen [ist Google da ein wenig zurückgerudert](https://blog.google/products/gmail/g-suite-gains-traction-in-the-enterprise-g-suites-gmail-and-consumer-gmail-to-more-closely-align/) nimmt sich aber immer noch weitreichende Rechte zum Lesen einiger Daten aus dem Gmail Postfach heraus um Features wie "Smart Reply" effizienter zu nutzen oder erlaubt Gmail Add-ons weiterhin Zugang.

{% include image.html url="delete.png" description="In seinen Datenschutzeinstellungen bietet Google einige Stellrädchen an, unter anderem auch das automatische Löschen einiger Aktivitäten alle 3/18/36 Monate" %}

Ein Blick, in den [Google Privatsphärecheck](https://myaccount.google.com/privacycheckup/) lohnt, sich da Google inzwischen ein wenig dem Datenschutz entgegenkommt, wenn man es sich so einstellt, von Haus aus darf man aber keine Wunder erwarten.

<h2>Android</h2>

Einer der größten Elefanten im Raum ist hier klar, dass ich Android nutze auf einem Gerät von Google selbst. Glücklicherweise stellt sich der letzte Punkt als die Rettung heraus den neue Custom Android Roms wie [CalyxOS](https://calyxos.org/) oder [GrapheneOS](https://grapheneos.org/) laufen nahezu ausschließlich auf Google Pixel Geräten mit dem einfachen Grund, das man hier den Bootloader wieder sperren kann trotz eigener Keys, damit wird die Custom Rom wieder genauso sicher gegenüber physischen Angriffen wie das vorinstallierte Android. Außerdem liefert Google für seine eigenen Geräte pünktlich monatlich (Sicherheits-)Updates und beide CalyxOS und GrapheneOS können deswegen mit neuestem Android 11 punkten.

{% include image.html url="version.jpg" description="Nutze ich aktiv seit einigen Monaten: CalyxOS" %}

CalyxOS im Speziellen hat es mir angetan, leider ist mir GrapheneOS zu restriktiv und beschneidet brutal die Nutzungsmöglichkeiten des Handys durch den Versuch so Datenschutzfreundlich wie maximal möglich zu werden. Bei der Installation von CalyxOS wird man stattdessen gefragt, ob man MicroG vorinstallieren möchte oder nicht. [MicroG](https://microg.org/) als Alternative zu Google Play Services versucht viele der API Schnittstellen so Datenschutzfreundlich wie möglich bereitzustellen aber kann, das nicht immer bewerkstelligen, weswegen es von GrapheneOS nicht unterstützt wird. Zusätzlich fragt CalyxOS ob man den [Aurora Store](https://auroraoss.com/) installieren möchte, eine open source App um Apps aus dem Google Play Store herunterzuladen ohne Google Play Dienste. Weitere Alternativen wären [/e/OS](https://e.foundation/) oder [LineageOS](https://lineageos.org/). Jedoch unterstützt /e/ noch nicht mein Pixel 3 und LineageOS hängt oft sehr stark hinter Android Feature Updates hinterher, Beispielweise kam LineageOS 18.1 basierend auf Android 11 erst im April 2021 heraus.

<h3>CalyxOS AOSP vs. Pixel Android</h3>

In meinem [alten Blog Eintrag zum Umstieg auf Google Pixel]({% link _posts/2019-02-23-byebye-apple.md %}) hatte ich schon angemerkt das Google hier sich das Recht rausnimmt exklusive Pixel Features zu Android hinzuzufügen welche oft erst Monate/Jahre später in die Open Source Variante von Android "AOSP" einfliesen (wenn überhaupt). Durch den Umstieg auf eine Custom Android Rom wie CalyxOS verliert man hier diese Features, das ist aber nur halb so schlimm, weil die Entwickler einige Features selber hinzugefügt haben bzw. von LineageOS übernahmen haben die man bei Google wohl nie bekommen würde. Besonders erfreut bin ich über die Option einen Screensaver einzustellen während das Handy auflädt oder gedockt ist, ein Feature was komischerweise immer noch [Google Pixel Stand](https://store.google.com/de/product/pixel_stand?hl=de) exklusiv ist (welcher 79 € kostet). Außerdem findet man seit einigen Monaten eine Systemfirewall App vor, um ganz einfach Apps den Netzwerkverkehr zu entziehen. Anders als "Stock" Android gibt es auch eine nützliche Musik App standardmäßig während man bei Android lange Zeit nur die eher spärliche Google Music App bekam welche neuerdings von Youtube Music ersetzt wird.

{% include image.html url="firewall.jpg" description="Bei normalem Android wäre so etwas nur über lokale VPN Lösungen wie Blokada möglich" %}

Das nächste coole Feature ist das man sich automatisch Updates vom [F-Droid Store](https://f-droid.org/) herunterladen und installieren lassen kann, bei normalem Android ist, das nicht möglich da F-Droid keine Systemapp ist und Google behält sich dieses Privileg seinem Google Play Store vor. Ähnlich geht es zukünftig auch mit dem Aurora Store, diesem fehlt die Möglichkeit schlicht seit dem letzten großen Update. Das einzige, was wirklich fehlt, sind In-App Käufe aus dem Google Play Store, man kann sich im Aurora Store mit seinem Google Account anmelden und gekaufte Apps zu installieren aber In-App Käufe können nicht abgerufen werden. Das ist besonders traurig bei der App vom deutschen Wetterdienst, diese entfaltet erst nach einem In-App-Kauf sein volles Potenzial.

<h3>Alternative Apps</h3>

Seit ich den F-Droid Store entdeckt habe versuche ich möglichst viele Apps von dort zu beziehen. F-Droid erlaubt ausschließlich open source Apps und das F-Droid Team kompiliert diese selber, außerdem sind Tracker und Werbung explizit verboten. Einige Alternativen möchte ich hier auflisten, welche ich selber nutze:

- E-Mail: [FairEmail](https://f-droid.org/en/packages/eu.faircode.email)
- Browser: [Fennec](https://f-droid.org/en/packages/org.mozilla.fennec_fdroid) (Firefox Fork)
- Messenger: [Element](https://f-droid.org/en/packages/im.vector.app/) (Matrix), [Telegram FOSS](https://f-droid.org/en/packages/org.telegram.messenger/), Signal (wird von CalyxOS bereit gestellt) / [Molly](https://github.com/mollyim/mollyim-android)
- Bilder: [Simple Gallery](https://f-droid.org/en/packages/com.simplemobiletools.gallery.pro)
- Password Manager: [AuthPass](https://f-droid.org/en/packages/design.codeux.authpass.fdroid/), [KeePassDX](https://f-droid.org/en/packages/com.kunzisoft.keepass.libre/), [Bitwarden](https://f-droid.org/packages/com.x8bit.bitwarden)
- 2FA OTP: [Aegis Authenticator](https://f-droid.org/en/packages/com.beemdevelopment.aegis/), [andOTP](https://f-droid.org/en/packages/org.shadowice.flocke.andotp), [Bitwarden](https://f-droid.org/packages/com.x8bit.bitwarden)
- Tastatur: [FlorisBoard](https://f-droid.org/en/packages/dev.patrickgold.florisboard), [OpenBoard](https://f-droid.org/en/packages/org.dslul.openboard.inputmethod.latin/)
- YouTube: [NewPipe](https://f-droid.org/en/packages/org.schabi.newpipe/)
- Kalender/Kontakte Syncronisierung: [DAVx⁵](https://f-droid.org/en/packages/at.bitfire.davdroid/)
- VPN: [WireGuard](https://f-droid.org/en/packages/com.wireguard.android/), [Mullvad VPN](https://f-droid.org/en/packages/net.mullvad.mullvadvpn/)
- Reddit: [Slide](https://f-droid.org/en/packages/me.ccrama.redditslide/), [Infinity](https://f-droid.org/en/packages/ml.docilealligator.infinityforreddit)
- Launcher: [Discreet Launcher](https://f-droid.org/en/packages/com.vincent_falzon.discreetlauncher), [Posidon Launcher](https://f-droid.org/en/packages/posidon.launcher/)
- Maps: [OsmAnd~](https://f-droid.org/en/packages/net.osmand.plus/)
- Manga Reader: [Tachiyomi](https://f-droid.org/en/packages/eu.kanade.tachiyomi), [Hendroid](https://f-droid.org/en/packages/org.nonononoki.hendroid/)
- QR Code Scanner: [QR & Barcode Scanner](https://f-droid.org/en/packages/com.example.barcodescanner/)
- Video Player: [mpv-android](https://f-droid.org/en/packages/is.xyz.mpv/), [VLC](https://f-droid.org/en/packages/org.videolan.vlc)
- SFTP Server: [primitive ftpd](https://f-droid.org/en/packages/org.primftpd/)
- PC Notification Sync: [KDE Connect](https://f-droid.org/en/packages/org.kde.kdeconnect_tp/)
- Corona Tracing: [Corona Contact Tracing Germany](https://f-droid.org/en/packages/de.corona.tracing/)
- Twitter: [Twidere X](https://f-droid.org/en/packages/com.twidere.twiderex/), [Fritter](https://f-droid.org/en/packages/com.jonjomckay.fritter/)

{% include image.html url="fdroid.png" description="Im F-Droid Store kann ich guten Gewissens jegliche App herunterladen ohne mit Werbung, In-App Käufen oder Trackern bombadiert zu werden" %}

Trotz dieser nicht kleinen Liste, gibt es viele Apps trotzdem nicht im F-Droid Store. Komischerweise sind darunter auch Firefox und Signal, als Firefox Ersatz gibt es aber Fennec und CalyxOS liefert Signal als System App aus für SMS. Für Signal gibt es auch den Fork [Molly](https://github.com/mollyim/mollyim-android) mit eigenem F-Droid repository. Ansonsten sollte der Aurora Store den Rest abdecken, jedoch geht eine App hier komplett unter: Die Pixel Camera App oder oft GCam genannt
Eines der großen Verkaufsargumente für das Google Pixel, ist deren Kamera App welche aus dem kleinen Kamerasensor unglaubliche Bilder zaubern kann. Diese findet sich jedoch weder im AOSP noch im Play Store / Aurora Store zum Laden. Meine momentane Lösung ist sich von APKMirror die "GCam - BSG's Google Camera port" App zu laden. Das ist nicht die schönste Möglichkeit an die App zu kommen aber verzichten möchte ich auf die App auch nicht.

Eine andere App wofür ich noch keinen guten Ersatz gefunden ist meine Musik App, genauer genommen [BlackPlayer EX](https://play.google.com/store/apps/details?id=com.kodarkooperativet.blackplayerex&hl=en&gl=us) den ich immerhin per gekaufter Zusatz-App freischalten konnte, anstelle von In-App Käufen.

<h2>YouTube</h2>

Der zweite große Elefant im Raum ist wohl klar YouTube, mit seiner gigantischen Monopolstellung kommt man kaum drum herum. [PeerTube](https://joinpeertube.org/) versucht das Problem durch ein dezentralisiertes Peer-to-Peer-Netzwerk abzulösen, leider ist dieses jedoch oft sehr langsam und man findet vor allem Content hier, welcher schlicht überall anderswo gelöscht werden würde, weil es gegen die AGB verstoßen würde. Während ich PeerTube von der Seite im Blick behalte habe ich stattdessen einen genaueren Blick auf [Invidious](https://github.com/iv-org/invidious) geworfen und hoste eine eigene Instanz davon auf meinem Server für privaten Gebrauch. 

{% include image.html url="invidious.png" description="Invidious bietet auch an, als Proxy gegenüber YouTube zu agieren, zusätzlich zu anderen netten Features" %}

Invidious ist ein alternatives Frontend für YouTube und kann auch meine Watch History speichern sowie Playlisten. Ähnlich verhält es sich mit [NewPipe](https://f-droid.org/en/packages/org.schabi.newpipe/) als App für Handy und bietet ähnliche Funktionalitäten an ohne direkt Google alles zu erzählen. Invidious und NewPipe unterstützen beide auch [SponsorBlock](https://sponsor.ajay.app/) wodurch viele Youtube Videos gleich viel angenehmer zum Anschauen werden, leider gibt es momentan noch keine Möglichkeiten meine Playlisten und Watch History zwischen beiden zu teilen.

Ich nutze Invidious erst seit kurzem und habe ich schon einige Kleinigkeiten gefunden die nerven oder fehlen, ich werde es weiter testen, weil es bislang die beste Alternative für mich darstellt.

<h2>Gmail</h2>

Gmail war der Grund warum ich überhaupt einen Google Account erstellt hatte, der Umstieg hier ist für mich auch noch lange nicht vorbei und wird das wahrscheinlich nie richtig werden. Als Ersatz für Gmail nutze ich hauptsächlich momentan die [Groupware Lösung von meinem VPS Anbieter Netcup](https://www.netcup.de/groupware/), das kostet zwar wenige Euro im Monat aber dafür kann ich E-Mail-Adressen mit meiner Domain nutzen. Groupware bietet außerdem einen Kalender und ein Kontaktbuch das sich über CalDAV und CardDAV über [DAVx⁵](https://f-droid.org/en/packages/at.bitfire.davdroid/) aufs Handy synchronisieren lassen. Der einzige Wermutstropfen hier ist das Netcup keine Catch-All/Wildcard E-Mail-Adressen anbietet. Eine andere beliebte Alternative wäre [ProtonMail](https://protonmail.com/), evtl. schaue ich mir das auch noch eines Tages genauer an.

{% include image.html url="sogo.png" description="SOGo wird nicht nur von meinem VPS Anbieter, sondern auch von Mailcow genutzt" %}

Vor einigen Jahren hatte ich noch selbst gehostetes [Mailcow](https://mailcow.email/) genutzt aber meine E-Mails wurden ständig bei verschiedenen Anbietern als Spam markiert, obwohl ich alle Einstellungen vorgenommen habe für maximale Sicherheit aber das schien mir ein Kampf gegen Windmühlen.

Trotz allem behalte ich jedoch meinen Google Account für Gmail, weil ich mich über die vielen Jahren bei hundert verschiedenen Diensten mit meiner Gmail Adressen angemeldet habe und es extrem lange dauert nach und nach alle umzustellen.

<h2>Webbrowser</h2>

Glücklicherweise bin ich seit vielen Jahren Nutzer von Firefox und musste ich mich hier nicht von Google Chrome trennen was warum auch immer der absolut beliebteste Webbrowser weltweit geworden ist. Vor allem nach den letzten Bestrebungen von Google [Werbeblocker Add-ons zu beschneiden](https://www.heise.de/newsticker/meldung/Chrome-Erweiterungen-Google-macht-Zugestaendnis-im-Werbeblocker-Streit-4445967.html) oder ihren Vorstoß [Cookies durch ihr eigenes Fingerprinting (FLoC)](https://amifloced.org/) zu ersetzen hoffe ich das Google Chrome endlich mal ein wenig Marktanteile verliert.

Leider funktionieren einige Websites (namentlich auch viele Google eigene Webseiten) gar nicht oder nur sehr schlecht mit Browsern die nicht auf Chromium basieren. Dafür nutze ich [ungoogled-chromium](https://github.com/Eloston/ungoogled-chromium) als Zweit-Browser, weil Chromium selber, obwohl es Open Source ist, trotzdem gerne mit Google Servern sich mitteilt.

Auf dem Handy nutze ich statt Firefox jedoch den Firefox-Fork Fennec, weil Firefox selber nicht bei F-Droid erhältlich ist.

{% include image.html url="proton.png" description="Das neue Proton Interface von Firefox 89 ist gewöhnungsbedürftig aber gefällt mir mit jeden Tag mehr" %}

Leider muss ich jedoch auch sagen, dass Firefox in seiner Standardausstattung nicht dem entspricht, was ich mir vorstelle, von einem perfekten Webbrowser. So rüste ich für Firefox normalerweise [uBlock Origin](https://addons.mozilla.org/de/firefox/addon/ublock-origin/) nach und nehme [einige Privatsphäre-Einstellungen](https://privacytools.io/browsers/#about_config) vor. Dennoch bietet Firefox auch wirklich praktische Funktionen wie [Firefox Multi-Account Containers](https://addons.mozilla.org/de/firefox/addon/multi-account-containers/) bzw. [Google Container](https://addons.mozilla.org/de/firefox/addon/google-container/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search).

<h2>Suchmaschine</h2>

Google begann als Internet Suchmaschine und ist immer noch Marktführer hier bei weitem und ich muss gestehen das Google durch die vielen Daten über einen auch wirklich passende Suchergebnisse liefert. Jede Suchmaschine, die Wert auf Privatsphäre legt, wird deshalb immer hinterherhinken. Trotzdem benutze ich seit vielen Jahren jedoch standardmäßig [DuckDuckGo](https://duckduckgo.com/) als Alternative. DuckDuckGo bekommt einen großen Teil seiner Suchergebnisse von Bing aber unterhält auch eigene Scraper. Besonders praktisch finde ich die sogenannten [Bangs](https://duckduckgo.com/bang) bei dennen z.B. "!aw" einen direkt zum Arch Linux Wiki führen oder "!stackoverflow" direkt zu StackOverflow, wer unzufrieden mit dem Suchergebnis ist, kann auch mit "!g" direkt bei Google suchen. Dennoch ist auch bei DuckDuckGo Zweifel angebracht da die Firma hinter der Suchmaschine "Duck Duck Go Inc" ihren Sitz in Amerika hat und damit dem [CLOUD Act](https://de.wikipedia.org/wiki/CLOUD_Act) und [PATRIOT Act](https://de.wikipedia.org/wiki/USA_PATRIOT_Act) bzw. [Freedom Act](https://de.wikipedia.org/wiki/USA_Freedom_Act) unterliegen.

{% include image.html url="enteentegeh.png" description="Nicht weniger als die totale Privatsphäre verspricht DuckDuckGo" %}

Alternativen zu DuckDuckGo aus europäischen Gefilden sind z.B. [SearX](https://searx.me/) und [Qwant](https://www.qwant.com/?l=de). SearX hat den interessanten Vorteil das man diese Meta-Suchmaschine selber betreiben kann während Qwant vor allem in Frankreich an Bekanntheit gewinnt. Leider konnte ich mich in beide noch nicht wirklich einarbeiten, vor allem SearX bei einigen öffentlichen Instanzen war für mich immer sehr langsam und brachte mich selten schnell zum Ziel als ich, das letzte Mal es genutzt hatte. Bis vor einigen Jahren war Startpage auch noch eine beliebte Methode um Google Suchanfragen hinter einem Proxy zu verschleiern, leider wurde der Dienst im Grunde 2019 von einer Werbefirma namens System1 aufgekauft und kann damit kaum weiterempfohlen werden.

<h2>Google Maps</h2>

Google Maps ist ein sehr mächtiges Werkzeug um Routen zu planen, den Weg von X zu finden, sich zu erkundigen, wann Restaurant Y geöffnet hat oder nachzuschauen, ob auf der Autobahn wieder Stau ist. Alternativen wie [OpenStreetMap](https://www.openstreetmap.org/) oder Apps wie [OsmAnd~](https://f-droid.org/en/packages/net.osmand.plus/) wirken fast schon primitiv im direkten Vergleich. Wenig hilft es auch das OpenStreetMap und Google Maps Straßen teilweise anders benennt. Hin und wieder navigiere ich dann doch noch mal zu Google Maps über den mobilen Browser, immerhin trackt mich Google hier weniger krass als in der richtigen App.

<h2>Google Übersetzer</h2>

Google Übersetzer ist keine Frage ein mächtiges Werkzeug und die Kamera Funktion hat schon einige male mir aus der Patsche geholfen. Ich versuche so oft es geht Alternativen wie [LibreTranslate](https://libretranslate.com/), [SimplyTranslate](https://translate.metalune.xyz/) oder [DeepL](https://www.deepl.com/translator) zu nutzen aber lande trotzdem immer mal wieder zurück bei Google Übersetzer.

<h2>Android Auto</h2>

Mein neuestes Auto hat Support für Android Auto und das habe ich auch eine Zeit lang genutzt. Android Auto ist jedoch extrem stark verzahnt mit Google Maps und sendet permanent Daten, wirklich innovative Funktionen wie eine Anzeige für die besten Ampelzeiten fehlen jedoch trotzdem. Es gibt momentan keine open source Alternative und in AOSP ist Android Auto auch nicht zu finden. Schade aber mein Auto hat von sich auch eine Navigationsfunktion und kann Musik per Bluetooth abspielen, wodurch das Anschließen an ein Ladekabel entfällt und mein Handy in der Hosentasche verbleiben kann.

<h2>Google Authenticator</h2>

Ich bin mir unsicher, ob Google das absichtlich gemacht hat oder es einfach nur Zufall ist das eine Zweit-Faktor-Authentisierung oft mit Google Authenticator wie ein Synonym verwendet wird. Fakt ist jedoch das TOTP/HOTP Token Generatoren nicht an Google gebunden sind und es eine Menge alternativer Apps gibt. Glücklicherweise habe ich mich da früh nach Alternativen um gesucht und hatte gute Erfahrungen mit [Aegis Authenticator](https://f-droid.org/en/packages/com.beemdevelopment.aegis/) und davor [andOTP](https://f-droid.org/en/packages/org.shadowice.flocke.andotp) gemacht. In Zukunft möchte ich auch dem integrierten OTP Token Generator in Bitwarden eine Chance geben.

<h2>Google Fonts</h2>

Wahrscheinlich eher weniger bekannt aber [letztes Jahr im April](https://github.com/Der-Eddy/blog/commit/3c91584060611bc4ee2835dcceba3a288e6eb465) habe ich Beispielweise in diesem Blog die Aufrufe für die Lato Schriftart auf einen lokalen Abruf geändert anstelle von googleapis. Lizenz-technisch war das kein Problem. Eine komplette Alternative wäre z.B. [Font Library](https://fontlibrary.org/en) Falls ich in Zukunft noch mal auf der Suche nach einer passenden Schriftart bin.

<h2>Google DNS</h2>

Obwohl DNS Resolver ein eher technisches Thema sind, wissen heutzutage auch viele weniger technisch versierte Nutzer das 8.8.8.8 der DNS Resolver von Google ist. Google DNS hat den Vorteil das er jederzeit extrem schnell ist und im Sekundentakt die DNS Einträge aktualisiert, während man bei einigen DNS Resolvern von ISPs kann man gerne mehrere Stunden warten für eine Aktualisierung wartet und/oder Weiterleitungen auf Suchmaschinen bekommt bei unbekannten Webseiten. Der nächst größere DNS Service wäre von Cloudflare die sich aber auch in ihren AGB vorenthalten Daten bei der Nutzung zu erheben, um ihre CDN Caching Lösung weiter zu optimieren. [Quad9](https://quad9.net/) bekam erst vor kurzem einen Dämpfer von der deutschen Justiz [als Sony gegen sie geklagt hatte an einem deutschen Gericht](https://www.heise.de/news/Urheberrechtsverletzung-Sony-erwirkt-einstweilige-Verfuegung-gegen-DNS-Resolver-6111633.html). Ein weiterer beliebter Service aus Deutschland wäre noch [LibreDNS](https://libredns.gr/). In der Vergangenheit hatte ich meinen eigenen DNS Resolver aufgesetzt auf Basis von [Adguard Home](https://github.com/AdguardTeam/AdguardHome) oder [Pi-Hole](https://pi-hole.net/).

<h2>Google Analytics</h2>

Wer Webseiten betreibt, möchte oft wissen wie viele Nutzer und wie die Nutzer ihre Seiten nutzen. [Matomo](https://matomo.org/matomo-on-premise/) (ehemals Piwik) hatte mir da in der Vergangenheit oft gute Dienste geleistet. Lange Zeit hatte ich aber kein Tracking mehr genutzt bis ich vor kurzem über [umami](https://umami.is/) gestolpert was anonymes Tracking erlaubt ohne Cookies (und damit DSGVO-konform ohne Banner) mit weniger Ressourcen als Matomo und dabei auch noch gut aussieht. Dieser Blog benutzt seit kurzem übrigens auch umami!

<h2>Google Photos</h2>

Anscheinend für sehr viele Menschen sind der unlimited Storage von Bildern zu Google Photos für Google Pixel Geräte der ausschlaggebende Grund es zu kaufen. Ich habe sogar von einigen gelesen die sich extra ein Google Pixel der ersten Generation gekauft haben mehrere Jahre später, weil es den Bilder-Upload in Original Qualität erlaubt statt "nur" Hoher Qualitätsstufe und das Ausnutzen um Bilder von ihrer Vollformat Kamera auf das Pixel übertragen und dann in die Google Cloud.
Ich habe das selber nie verstanden und dort nahezu nie etwas hochladen lassen.

Ich habe aber kurz nach Alternativen gesucht wie z.B. [PiGallery2](https://bpatrik.github.io/pigallery2/), [Photonix](https://photonix.org/) oder [Piwigo](https://www.piwigo.org/) aber brauche dann für den Moment dann doch keines davon.

<h2>Google Drive/Docs</h2>

Ich brauche zum Glück nur sehr selten und wenig Speicher für Google Drive und ich habe das Glück das mein [lokaler Hackspace]({% link _posts/2020-03-06-hackspace.md %}) für ihre Mitglieder eine [Nextcloud](https://nextcloud.com/) Instanz mit 1 GB Speicher bereitstellt für jedes Mitglied. Dort kann ich zum Beispiel PDF Dateien hochladen und sie einfach mit anderen Leuten teilen, was meine Hauptnutzung von Google Drive war.

<h2>Google Hangouts / Google+ / Ingress</h2>

Vor einigen Jahren als ich noch Ingress gespielt habe, war Google Hangout und Google+ noch sehr beliebt in meiner Gruppe da Ingress bzw. Niantic damals noch offiziell zu Google gehörten. Das hat sich insofern gelöst als das Google Handgouts und Google+ von Google eingestellt wurden und ich inzwischen aufgehört habe Ingress zu spielen und Niantic sowieso nicht mehr zu Google gehört.

<h2>Google Keep</h2>

Für Notizen habe ich mir eine eigene Instanz von [HedgeDoc](https://hedgedoc.org/) (ehemals CodiMD) auf meinem Server installiert und nutze diese gelegentlich.

<h2>Google Music</h2>

Wie weiter oben bereits erwähnt hatte ich Google Music nie genutzt bevor es eingestellt wurde, nachdem ich aber [Navidrome](https://www.navidrome.org/) mal ausgetestet habe fand ich die Idee schon verlockend meine Musik zentral zu speichern und über verschiedene Clients auf dieselbe Bibliothek zugreifen zu können. Momentan nutze ich aber dann doch noch meine offline Musiksammlung, vielleicht wird daraus in Zukunft wieder etwas.

<h2>WearOS / Google Fit</h2>

Googles eigenes Betriebssystem für Smartwatches hatte ich bislang noch gar nicht auf den Schirm, weil ich einfach keine Smartwatch haben wollte. Es gibt jedoch mit [AsteroidOS](https://asteroidos.org/) ein interessantes Projekt welches WearOS datenschutzfreundlich gestalten möchte ähnlich von Android Custom Roms. Leider unterstützt AsteroidOS nur sehr wenige und vor allem alte Smartwatches die kaum zu bekommen sind heutzutage. Ich habe mich momentan jedoch für eine günstige Fitness Tracker Armband entschieden, was ich mit [Gadgetbridge](https://www.gadgetbridge.org/) nutzen kann und so datenschutzfreundlich hinbekomme. Ich hoffe einen eigenen Blog Artikel darüber in Zukunft schreiben zu können.

<h2>Blogger</h2>

Vergisst man gerne aber blogger.com gehört Google. Dieser Blog hier liegt jedoch nicht auf Google Servern, sondern bei [GitHub Pages](https://pages.github.com/) und wird per [Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll) generiert.

<h2>Google Pay</h2>

Meine Bank bietet eine eigene App an, über die ich per NFC bezahlen kann. Ehrlicherweise muss ich jedoch gestehen, dass ich deren Einsatz unter CalyxOS noch nicht ausgetestet habe, weil mir irgendwann das entsperren des Handys per Fingerabdruck beim Bezahlen teilweise echt nervig wurde und ich stattdessen plump per physischer Karte bezahle momentan.

<h2>Google Home / Google Assistant</h2>

Für die Heimautomatisierung erfreut sich Google Home bzw. Google Nest immer größerer Beliebtheit dank Google Assistant und sehr enger Verzahnung mit Android. Anstatt in der Cloud betreibe ich jedoch lieber meine [Heimautomatisierung-Lösung Home Assistant]({% link _posts/2020-08-23-hass.md %}) selber und habe darüber in der Vergangenheit schon einen Blog Artikel geschrieben. Das einzige, was noch fehlt, ist eine wirklich nützliche Spracherkennung jedoch werden in dem Bereich alle möglichen Alternativen sehr schnell aufgekauft wie [vor einigen Monaten erst Snips](https://www.heise.de/newsticker/meldung/Sonos-kauft-franzoesische-Sprachassistenten-Firma-Snips-4593521.html) was vielversprechend aussah.

<h2>Google News</h2>

Hier bin ich altmodisch und pflege meine RSS Sammlung an Nachrichten mithilfe von [FreshRSS](https://www.freshrss.org/) und bin sehr zufrieden damit.

{% include image.html url="freshrss.png" description="Als Startseite in Firefox vielleicht nicht der Hingucker aber sehr informativ" %}

<h2>Fazit</h2>

Der Prozess sich komplett von Google zu trennen wird für mich wohl noch mehrere Jahre dauern und kann unmöglich über Nacht geschehen. Auch ist mir bewusst das viele Alternativen, die ich oben erwähnt, habe nur für meinen eigenen Anwendungszweck gut sein können während manch anderer dann doch eine Alternative bevorzugt oder trotzdem bei Google bleibt. Die Idee hinter dem "degooglen" sollte sein einen Fußabdruck an digitalen Daten, die man an Google aushändigt so klein wie irgend möglich zu halten, hier gilt auch der Grundsatz "Lieber spät als nie".

Wer weitere Alternativen sucht wird eventuell bei [degoogle.jmoore.dev](https://degoogle.jmoore.dev/), [PrivacyTools.io](https://privacytools.io/) oder [Kuketz Blog](https://www.kuketz-blog.de/empfehlungsecke/) wahrscheinlich fündig.
