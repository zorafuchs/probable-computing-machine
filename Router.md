---
aliases: 
tags:
- public
- knowledge
title: Router
date created: "2023-03-20T07:56:46"
date modified: "2023-03-27T07:28:55"
---

# Router
- No Shutdown -> Aktives Netzwerk
- [[Routing Table]]

- Per default bei konfiguriertem Interface: alles wird ins Netzwerk weitergeleitet

- [[Access Control List]]

## Static Routes
Manuell eingegebene Routen
- Hohe Sicherheit
- Sehr effizient

## Dynamic Routes
Jeder Router teilt den anderen Routern alles über ihre Netzwerke mit
- Permanenter Austausch
- Verschiedene Protokolle

## Initial Router Settings
Standart-Passwörter: Cisco / Class

## Interfaces
Configurationen werden gesetzt und gespeichert, sind aber zu beginn noch nicht angewendet.

Überall wo eine [[IP-Adresse]] gesetzt wird, müssen die Konfigurationen mit `no shutdown` aktiviert werden.

[[IPv6]]-Prefix-Length auf 64 einstellen.

Es können mehrere Netzwerke konfiguriert werden. Alles wird defaultmässig zwischen den Netzwerken durchgegeben.

Es kann

## Default Gateway
Quat zero - aucted zero??

0.0.0.0 -> [[Default Gateway]]
Es wird immer die präziseste Route für Weiterleitungen verwendet.
