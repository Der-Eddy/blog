---
layout: post
title: "Raspberry Pi 4 über USB booten"
date: 2020-05-26 17:00:00 +0100
category: RasPi
tags: raspberry pi linux
author: Der-Eddy
keyword: raspi
---

Nachdem ich meine letzten beiden Raspberry Pis Version 1 und 3 durch Eigenverschulden gebricked hatte, kam ich auf die Idee endlich mal Version 4 des beliebten Einplatinencomputers zu kaufen. Die Vorteile gegenüber dem letzten Model lagen klar auf der Hand:

- Mehr Arbeitsspeicher (2 bis 4 GB statt nur 1 GB RAM)
- Ethernet und USB Hub sind jetzt getrennt und teilen sich nicht mehr denselben USB 2.0 Bus
- Gigabit Ethernet ist damit jetzt möglich
- USB Typ-A 3.0 an zumindest zwei Buchsen möglich die direkt per PCIe Lane an dem SoC hängen
- Zwei Micro-HDMI 2.0 Ausgänge (beide bis zu 4K Auflösung) statt nur einem HDMI Ausgang
- Der neue BCM2711 SoC kann nativ H.265 Videos in 4K dekodieren
- Der Micro-SD Karten Leser ist nun schneller bei 50 MB/s statt 25 MB/s

Vor allem die Umstellung von Ethernet und USB Hub auf eigene PCIe Lanes macht den Raspberry Pi 4 nun endlich als Mini-NAS nützlich.
Aber es gibt aber Nachteile:

- Trotz 64 bit ARM SoC nutzt das offizielle Raspbian nur 32 bit
- Erhöhter Stromverbrauch über die USB Typ-C Stromversorgung (15 Watt a 5V/3A) gegenüber den 12 Watt a 5V/2,5A des Vorgängers
- Micro-HDMI statt HDMI Ausgang
- Kein voller Support für andere Linux Distributionen außer Raspbian
- Kein USB Boot ab Werk

{% include image.html url="raspberrys.jpg" description="Meine Sammlung an Raspberry Pi 1, 3 und 4" %}

Den letzten Punkt kann man jedoch seit dem 15. Mai 2020 beheben, knapp 11 Monate nach Release der neuen Version 4 des Einplatinencomputers [tauchte auf GitHub eine Beta-Version der Firmware](https://github.com/raspberrypi/rpi-eeprom/blob/master/firmware/release-notes.md) für den EEPROM auf der das booten über USB erlauben würde. Bis zu diesem Tag musste man immer über eine Micro-SD Karte erst mal den Bootloader starten und danach auf eine System-Partition auf USB verweisen, aber jetzt geht das ganz ohne extra Micro-SD Karte und nativ).

Das Aufspielen des EEPROM Updates ist derzeit noch mit etwas Mühen verbunden:
Man braucht eine Micro-SD Karte mit Raspbian und aktuellen System über `apt update`, `apt upgrade` und `rpi-update`. Nach einem Reboot kann man jetzt im `rpi-epprom` Paket auf den Beta-Zweig wechseln, dafür editiert man die Datei `/etc/default/rpi-epprom-update` von

    FIRMWARE_RELEASE_STATUS="critical"

auf

    FIRMWARE_RELEASE_STATUS="beta"

Und nun spielt man die neueste Beta Firmware über `rpi-eeprom-update` auf, dafür sucht man sich die aktuellste Version der `pieeprom-*.bin` Datei im Verzeichnis `/lib/firmware/raspberrypi/bootloader/beta/`. Zum heutigen Zeitpunkt (26.05.2020) sieht der ganze Befehl so aus:

    sudo rpi-eeprom-update -d -f /lib/firmware/raspberrypi/bootloader/beta/pieeprom-2020-05-15.bin

Nach einem abschließenden Reboot sollte der Raspberry Pi 4 nun endlich von USB booten können und die Micro-SD Karte für andere Zwecke verwendet werden. Das Einzige, was noch fehlt, ist die Bootloader Firmware eines Laufwerks eurer Wahl (z.B. USB-Stick oder SATA SSD/HDD über USB Adapter) anzupassen:
Schreibt zuerst das neueste Raspbian auf euer Laufwerk und kopiert dann alle `*.elf` und `*.dat` Dateien aus dem `/boot` Verzeichnis eures gerade genutzten Raspbian von Micro-SD zum `/boot` Verzeichnis des USB Laufwerks. Bei der Gelegenheit kann eine leere Datei namens `ssh` angelegt werden im `/boot` Verzeichnis so fern man direkt über SSH auf den RasPi zugreifen möchte.

Doch lohnt sich die Mühe? Ich habe die neue Beta EEPROM Firmware gleich mal getestet und eine SanDisk 16GB Micro-SD Karte, einen SanDisk 32GB USB 3.0 Stick und eine SanDisk 120GB SATA SSD über einen ELUTENG USB 3.0 zu SATA Adapter im Benchmark gegeneinander antreten lassen. Zum Einsatz kam die Benchmark Kollektion von [storage.jamesachambers.com ](https://storage.jamesachambers.com) welche DD, HD Parm, IOZone und FIO vereint.

<table class="ui inverted celled table">
  <thead>
    <tr><th>Gerät</th>
    <th>Disk Read</th>
    <th>Cached Read</th>
    <th>Write</th>
    <th>IOPS Read</th>
    <th>IOPS Read</th>
  </tr></thead>
  <tbody>
    <tr>
      <td>
        <h4 class="ui image header">
          <i class="inverted sd card icon"></i>
          <div class="content">
            Micro-SD Karte
            <div class="sub header">16 GB Class 10
          </div>
        </div>
      </h4></td>
      <td>
        41 MB/s
      </td>
      <td>
        40 MB/s
      </td>
      <td>
        11,6 MB/s
      </td>
      <td>
        ~2500 IOPS
      </td>
      <td>
        ~770 IOPS
      </td>
    </tr>
    <tr>
      <td>
        <h4 class="ui image header">
          <i class="inverted usb icon"></i>
          <div class="content">
            USB-Stick
            <div class="sub header">32 GB USB 3.0
          </div>
        </div>
      </h4></td>
      <td>
        95 MB/s
      </td>
      <td>
        48 MB/s
      </td>
      <td>
        76 MB/s
      </td>
      <td>
        ~1700 IOPS
      </td>
      <td>
        ~870 IOPS
      </td>
    </tr>
    <tr>
      <td>
        <h4 class="ui image header">
          <i class="inverted hdd outline icon"></i>
          <div class="content">
            SSD
            <div class="sub header">120 GB SATA 3
          </div>
        </div>
      </h4></td>
      <td>
        300 MB/s
      </td>
      <td>
        200 MB/s
      </td>
      <td>
        140 MB/s
      </td>
      <td>
        ~18400 IOPS
      </td>
      <td>
        ~9500 IOPS
      </td>
    </tr>
  </tbody>
</table>

Mit einer schnelleren Micro-SD Karte hätte ich wahrscheinlich an der maximalen Grenze von 50 MB/s kratzen können, weder SD-Karte noch USB-Stick bekommen jedoch ordentliche IOPS Werte hin. Dafür fühlt sich das System auf einer SATA SSD erstmal richtig flott an, vor allem wenn man über `apt` Pakete installiert dauert, das keine halbe Ewigkeit mehr, sondern geht, genauso schnell wie auf einem richtigen Desktop oder Laptop. Ein weiteres Plus ist das SSDs wear-leveling besitzen während der Großteil aller SD Karten und USB-Sticks das nicht haben, außerdem kann man selbst ohne wear-leveling eine viel längere Laufzeit erwarten gegenüber den billigeren Flash-Chips in SD Karten und USB-Sticks.
Leider hatte ich keinen schnellen USB 3.1 Stick zur Hand, [Benchmarks](https://storage.jamesachambers.com/benchmark/25597) zeigen jedoch auf das man über einen etwas teureren USB-Stick auch sehr schnell ans Ziel kommt.

Trotz Beta-Status lief das EEPROM Firmware Update sehr gut bei mir, die ersten Bug-Fixes trudeln auch bereits ein. Sobald die Firmware als stabil gekennzeichnet wurde, wird es auch einfacher diese aufzuspielen und ein einfaches 'rpi-update' sollte in einem zukünftigen Update genügen.