---
aliases: Layer 3
tags:
- public
- knowledge
title: Network Layer
date created: "2023-03-20T07:46:15"
date modified: "2023-03-21T10:27:39"
---

# Network Layer

Keine Fehlerkontrolle

Best effort -> Kürztmöglichster Weg zum Ziel wird umgesetzt

Adressierung: Logische Adresse -> [[IP-Adresse]] und [[Subnet Mask]] (gehören immer zusammen)

- Eigene [[IP-Adresse]] im gleichen Netz wie die Ziel [[IP-Adresse]]
	- In [[ARP-Table]] wird nachgeschaut welche [[MAC-Adresse]] zu der Ziel [[IP-Adresse]] gehört
- Eigene [[IP-Adresse]] gehört nicht zum gleichen Netz wie Ziel [[IP-Adresse]]
	- Gibt es ein [[Default Gateway]]-Eintrag für die [[IP-Adresse]]?
[[Network Layer]]

Operations
- Addressing end devices
- Encapsulation
- Routing
- De-encapsulation

Characteristics
- Connectionless (Gerät weiss nicht ob Packete ankommen)
- Best Effort (Schnellster Weg)
- Media Independent (Egal welche Medien, zb kabel verwendet werden)

[[Fragmentation]]

[[IPv4 Packet Header Fields]]
[[IPv6 Packet Header Fields]]
