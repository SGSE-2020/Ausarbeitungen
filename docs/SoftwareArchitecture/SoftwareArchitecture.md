# Software Architekturen

**Autor:** Pia Schreiner

**Modul:** Spezielle Gebiete des Software Engineerings



## Definition und Beschreibung

Eine Software Architektur ist eine Beschreibung aller Komponenten eines Systems sowie aller Verbindungen, welche zwischen den Komponenten bestehen. Dabei geht es nicht um einen detaillierte Entwurf, sondern mehr um Zusammenhänge zwischen den Anforderungen und dem System.

Im Zuge der Definition einer Software Architektur werden grundlegende Entscheidungen für den weiteren Systementwurf getroffen, wie beispielsweise die Wahl der Plattform, die Auswahl von Entwicklungssystemen oder auch der einzusetzenden Datenbank.

In einer guten Softwarearchitektur sollten folgende Aspekte berücksichtigt werden:

- Beschreibung aller Elemente aus denen das System besteht
- Interaktion zwischen den Elementen
- Entwurfsmuster, welche durch die Softwarekomposition leiten
- Geltende Bedingungen für die Entwurfsmuster

- Software Architektur ist zugleich Prozess und Gegenstand



## Motivation und Ziele

Alle Softwaresysteme besitzen eine Architektur, auch wenn niemand diese explizit modelliert hat. Da die Modellierung eines Softwaresystems einen hohen Aufwand erfordert, stellt sich die Frage, zu welchem Zweck eine Architektur modelliert werden sollte und ob dies einen Mehrwert darstellt. 

- Durch die steigende Zahl vernetzter Produkte steigt Komplexität und Umfang von Projekten

- Auch immer mehr organisatorische Einflussfaktoren müssen berücksichtigt werden

- Dadurch wird die Architektur immer relevanter
- Bereits mittelgroße Softwaresysteme haben oftmals matrixartige Systemstrukturen mit vielen Modulen und Subsystemen und strecken sich über viele Schichten mit fachlichen und technischen Querschnitte
- Softwarearchitektur kann diese Komplexität beherrschbar machen und eine Entwicklungs- und Prozessverbesserung erreichen
- Vorteile durch sorgfältig geplante Software Architektur sind:
  - Effiziente Softwareentwicklung ist möglich
  - Performance kann gezielt gesteigert werden
  - Zeit Einsparung kann realisiert werden
  - Software-Budget kann optimieren werden
  - Gezielte Minimierung von Risiken
  - Kompakte Software in Umfang und Funktion designen
  - Wertvolles Wissen zu Software im Unternehmen erhalten und bewahren



## Notation von Softwarearchitekturen



## Entwurf einer Software



### Grobentwurf



### Feinentwurf



## Bewertung von Software-Architekturen

- Motivation zur Bewertung
- Bewertung liefert keine Zahlen sondern quantitative Aussagen (z.B. im Gegensatz zu Messung von Quellcode)
- Bewertung auf die Erreichung von Qualitätsmerkmalen (ISO 25010) --> Kurzauflistung ISO 25010 [siehe Softwarequalität]
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

- [Erzeugungsmuster](https://de.wikipedia.org/wiki/Erzeugungsmuster) (englisch *creational patterns*)

  Dienen der Erzeugung von Objekten. Sie entkoppeln die Konstruktion eines Objekts von seiner Repräsentation. Die Objekterzeugung wird gekapselt und ausgelagert, um den Kontext der Objekterzeugung unabhängig von der konkreten Implementierung zu halten, gemäß der Regel: „Programmiere auf die Schnittstelle, nicht auf die Implementierung!“

  - Factory
  - Singleton

  [Strukturmuster](https://de.wikipedia.org/wiki/Strukturmuster) (englisch *structural patterns*)

  Erleichtern den Entwurf von Software durch vorgefertigte Schablonen für Beziehungen zwischen Klassen.

  - Decorator
  - Composite

  [Verhaltensmuster](https://de.wikipedia.org/wiki/Verhaltensmuster_(Software)) (englisch *behavioral patterns*)

  Modellieren komplexes Verhalten der Software und erhöhen damit die Flexibilität der Software hinsichtlich ihres Verhaltens.

  - State
  - Observer

  

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
  - Schwarzes Brett

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

