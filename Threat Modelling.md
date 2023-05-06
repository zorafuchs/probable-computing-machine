---
aliases: 
tags:
- public
- knowledge
title: Threat Modelling
date created: "2023-03-21T07:33:15"
date modified: "2023-05-06T07:13:55"
---

# Threat Modelling
- Ein Prozess zur Vorhersage von Cyber-[[Risk|Risiken]]
- Konstruktive Form der Qualitätssicherung

Wird beispielsweise im [[System Development Life Cycle]] angewendet

1. Woran arbeiten wir? ([[Risk Identification]])
2. Was kann schief gehen? ([[Risk Analysis]])
3. Was machen wir damit? ([[Risk Treatment]])
4. Haben wir gute Arbeit geleistet? ([[Monitoring]])

## Vorgehen
1. Datenfluss-diagramm / Zerlegen der Anwendung
2. Bedrohung identifizieren
3. Bedrohung bewerten

## Zerlegen der Anwendung
- Objekte identifizieren
- Datenfluss zwischen Objekte identifizieren
- Bestimme die schützenswerten [[Asset]]s
- Bestimme Schwachstellen und Verwundbarkeiten des Systems ([[CWE]] und [[CVE]] falls vorhanden)

Komponenten:
- Einheit
- Prozess
- DB
- Datenfluss
- [[Trust Boundary]]

## Methoden
[[STRIDE]] - [[Risk|Risiko]] entdecken / finden
[[DREAD]] - [[Risk|Risiko]] bewerten
[[Cyber Kill Chain]] - Beschreibung von Cyberangriffen
[[MITRE ATT@CK Framework]] - Wissensdatenbank von gegnerischen Taktiken und Techniken
[[MITRE D3FEND]] -
