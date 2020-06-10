# Software Architekturen

**Autor:** Pia Schreiner

**Modul:** Spezielle Gebiete des Software Engineerings



## Definition und Beschreibung

- Definiert die Komponenten eines Software-Systems und beschreibt Verbindungen zwischen den Komponenten
- Im Rahmen der Erstellung einer Software Architektur werden grundlegende Entscheidungen für den weiteren Systementwurf getroffen (z.B die Wahl der Plattform, die Auswahl von Entwicklungssystemen oder die einzusetzende Datenbank)
- Software Architektur ist zugleich Prozess und Gegenstand
- Eine gute Softwarearchitektur berücksichtigt:
  - Die Beschreiung der Elemente aus denen ein Softwaresystem besteht
  - Die Interaktion zwischen diesen Elementen
  - Entwurfsmuster (Patterm) die durch die Softwarekomposition leiten
  - Geltende Bedingungen für die Entwurfsmuster



## Motivation

- Vorteile durch sorgfältig geplante Software-Architektur:
  - Effiziente Softwareentwicklung
  - Perfomance gezielt steigern
  - Zeiteinsparung realisieren
  - Software-Budget optimieren
  - Gezielt Risiken minimieren
  - Kompakte Software in Umfang und Funktion designen
  - Wertvolles Wissen zu Software im Unternehmen erhalten und bewahren

## Notation von Softwarearchitekturen



## Entwurf einer Software



### Grobentwurf



### Feinentwurf



## Bewertung von Software-Architekturen

- Motivation zur Bewertung
- Bewertung liefert keine Zahlen sondern quantitative Aussagen (zB im Gegensatz zu Messung von Quellcode)
- Bewertung auf die Erreichung von Qualitätsmerkmalen (ISO 25010) --> Kurzauflistung siehe Softwarequalität
- Es gibt verschiedene Methoden bei der Bewertung

### Qualitative Bewertung



### Quantitative Bewertung



### Verfahren und Hilfsmittel bei der Bewertung



## Herangehensweise an Architektur und Design

- In der Software Entwicklung gibt es für alle Schritte Muster
  - Muster für die Analyse
  - Muster für den Entwurf
  - Muster für die Implementierung
  - Muster für das Testen
- Für den Softwareentwurf unterscheidet man je nach Granularität zwischen:
  - Entwurfsmuster
  - Architekturmuster

### Entwurfsmuster



### Architekturmuster

Architekturmuster können mittels Kategorien eingeordnet werden:

#### Chaos zu Struktur

- Organisation der Vielzahl der Komponenten und Objekte eines Softwaresystems
- Aufteilung der Funktionalität des Gesamtsystems in kooperierende Subsysteme

- Beispiele:
  - Schichtenarchitektur
  - Domain Driven Design
    - Ports and Adapters (hexagonale Architektur)
    - Onion Architektur
    - Clean Architektur
  - Pipes und Filter
  - Blackboard

#### Muster für verteilte Systeme

- Unterstützt die Verwendung verteilter Ressourcen und Dienste in Netzwerken

- Beispiele:
  -  Client-Server
  - Serviceorientierte Architektur (SOA)
  - Peer-to-Peer

#### Adaptive / Anpassbare Systeme

- Beispiele:
  - Reflexion
  - Dependency Injection

#### Interaktive Systeme (Mensch-Computer-Interaktion)

- Beispiele:
  - Model-View-Controller (MVC)
  - Presentation Abstraction Model (PAC)



## Quellen

