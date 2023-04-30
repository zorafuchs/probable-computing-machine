---
aliases: 
tags:
- public
- knowledge
title: Frame
date created: "2023-03-20T06:36:51"
date modified: "2023-03-20T07:01:37"
---

# Frame

Datenpacket mit Zieladresse ([[MAC-Adresse]] plus [[Port]])

## Grösse

64-1518 Bytes
Jumbo frames = grösser als 1500 (Müssen bei den Einstellungen erlaubt werden)

- 8 bytes - [[Preamble]] and [[SFD]]
- 6 bytes - Destination [[MAC-Adresse]]
- 6 bytes - Source [[MAC-Adresse]]
- 2 bytes - Type / Length
- 45 - 1500 bytes - Data
- 4 bytes - [[FCS]]
