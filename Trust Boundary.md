---
aliases: 
- Vertrauensgrenze
tags: 
- public
- knowledge
title: Trust Boundary
date created: "2023-03-21T07:41:50"
date modified: "2023-05-06T06:32:41"
---

# Trust Boundary
Vertrauensgrenzen bestehen zwischen Entitäten mit gleichen Vertrauenslevel. Diese Entitäten können Prozesse, Geräte, Benutzer oder Systeme sein.

-> Benutzereingaben sind automatisch eine Trust-Boundary im Threat Model.

## Faustregel
Als Faustregel gilt, dass dort, wo Kontrollmechanismen vorhanden sind – wie etwa eine [[Firewall]], eine Zugriffskontrollliste, eine Sperre oder ein Login – ein guter Ort sein kann, um eine Vertrauensgrenze zu ziehen.

Wenn Code oder Daten an das Gerät einer externen Entität gesendet werden oder deren Code oder Daten an ein modelliertes Gerät oder System gesendet werden, kann es hilfreich sein, eine Vertrauensgrenze zwischen ihnen zu ziehen.
