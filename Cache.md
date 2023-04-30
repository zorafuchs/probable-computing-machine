---
aliases: 
- SRAM
tags: 
- public
- knowledge
title: Cache
date created: "2023-04-04T09:40:41"
date modified: "2023-04-04T09:49:23"
---

# Cache
[[07-Vorlesung_Speicher_Peripherie_Rechnerarch.pdf#page=29]]

Ist nahe an der [[CPU]] -> Je weiter weg, desto langsamer der Speicher

Level 1 - Cache oft direkt auf der [[CPU]]
Level 2 - Cache ist etwas weiter weg und kommt deshalb gar nie an die geschwindigkeit des Level 1 Cache heran, deshalb macht es sowieso keinen Sinn hier den schnellsten zu nehmen. Es reicht auch nur bei jedem 2. Takt zu speichern

Adresse = 6 BITS = Tag + Index

Ist 5-10mal teurer als [[DRAM]], dafür schneller
