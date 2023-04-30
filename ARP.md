---
aliases: 
- Address Resolution Protocol
tags: 
- public
- knowledge
title: ARP
date created: "2023-03-27T06:35:18"
date modified: "2023-03-27T06:49:40"
---

# ARP
[[MAC-Adresse|MAC-Adressen]]-[[IP-Adresse|IP-Adressen]] Verbindungen werden in einer [[ARP-Table]] gespeichert.

ARP-Request wird geschickt
- Ich möchte einer [[IP-Adresse]] etwas schicken
- Ist das Netzwerk gleich, senden wir an die [[MAC-Adresse]], die wir in der [[ARP-Table]] finden.
- Ist das Netzwerk nicht gleich, wird die [[MAC-Adresse]] des [[Default Gateway]] in der [[ARP-Table]] gefunden und das Packet dorthin geschickt.

```pwsh
arp -a
```

- Tiefste [[IP-Adresse]] ist die Adresse des [[Default Gateway]]
- Höchste [[IP-Adresse]] oder `225.225.225.225` ist die [[Broadcast]]-Adresse
- 224...... ist eine [[Multicast]]-Adresse

Exessive [[ARP]]-[[Broadcast]]


ARP-[[Spoofing]]
