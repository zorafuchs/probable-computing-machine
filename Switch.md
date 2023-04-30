---
aliases: 
- Multiport Bridge
tags:
- public
- knowledge
title: Switch
date created: "2023-02-27T06:48:39"
date modified: "2023-03-27T07:07:15"
---

# Switch
Grundsätzlich ein [[Layer 2]]-Gerät.

Wenn ein moderner Switch auf [[Network Layer]] arbeiten soll, muss dies configuriert werden. [[Network Layer]] wird für [[Remote Access]] zwingend benötigt.

Auf [[Layer 2]] arbeitet ein Switch mit [[MAC-Adresse|MAC-Adressen]], auf [[Network Layer]] braucht er eine [[IP-Adresse]]

## IP-Addressen und Ports Konfigurieren
[[ITN_Module_2 - Basic Switching and End Device Configuration - WOd.pdf#page=45]]

[[IP-Adresse]] wird einem [[Virtual LAN]] zugeordnet, mit folgenden Konfigurationen: Jeder Port gehört default-mässig zum VLAN1, ist ein Sicherheitsrisiko und muss richtig konfiguriert werden.

[[IP-Adresse|IP-Adressen]] werden immer einem [[Virtual LAN]] zugeteilt und nie einem einzelnen [[Port]]

[[Switch Virtual Interface]] wird verwendet

## Protokolle für Ansteuerung
Defaultmässig kann man [[telnet]] und [[ssh]] Protokolle übertragen. Es muss eingestellt werden, dass mit [[ssh]] gearbeitet werden. Nur [[ssh|ssh2]] ist sicher.

[[User Execution Mode]] ist by default aktiviert. Um [[Privileged Execution Mode]] muss der befehl `enable` verwendet werden.

## Konfigurationssprache (shell?)
Etwas anschauen: befehl `show`
[[ITN_Module_2 - Basic Switching and End Device Configuration - WOd.pdf#page=36]]
Etwas anwenden: befehl `terminal`
Etwas konfigurieren: befehl `configure terminal`
Etwas rückgängig machen: befehl `no`

Einträge sind wie ein tonband -> alles wird aufgenommen, bevor man umkonfiguriert, muss mit `no` bestehende konfigurationen rückgängig gemacht werden.

## Save Configurations
[[ITN_Module_2 - Basic Switching and End Device Configuration - WOd.pdf#page=37]]
Wenn man Konfigurationen macht, sind die erstmal nur in der [[Running Configuration]] im [[RAM|RAM]] gespeichert. Will man Konfigurationen beständig gespeichert, müssen die Konfigurationen in die [[Startup Configuration]] gespeichert werden: `copy running-configuration startup-configuration`

## Vorgehensweise
Konfigurationen werden in [[ASCII]]-Files gespeichert werden

Man Konfiguriert nicht alles selber, sondern kopiert die Konfigurationsfiles zusammen.

- Befehle werden durch einen [[Interpreter]] verarbeitet.
- Befehle müssen nicht vollständig ausgeschrieben werden, sondern nur so weit bis sie eindeutig erkennbar sind [[ITN_Module_2 - Basic Switching and End Device Configuration - WOd.pdf#page=22]]

## Passwort Konfigurieren
[[ITN_Module_2 - Basic Switching and End Device Configuration - WOd.pdf#page=32]]

## Frames Verteilen
Ports sind nicht bekannt:
- Verschickt Frame an alle Ports, weil er die Adresse nicht kennt
- Kriegt eine Antwort auch dem Port, bei welchem die Adresse stimmt
- Adresse-Port connection wird gespeichert in [[CAM Table]]
[[MAC Fludding]]

## Arten
- [[Store-and-Forward Switching]]
- [[Cut-Through Switching]]
- [[Fragment-Free Switching]]

## Memory Buffering
Teure Switches: Grosser Zwischensspeicher für [[Frame]]s ([[Memory Buffering]])
