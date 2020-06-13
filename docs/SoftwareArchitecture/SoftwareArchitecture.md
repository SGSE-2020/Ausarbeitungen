# Software Architekturen

**Autor:** Pia Schreiner

**Modul:** Spezielle Gebiete des Software Engineerings



## Was ist eine Software Architektur?

Eine Software Architektur ist eine Beschreibung aller Komponenten eines Systems sowie aller Verbindungen, welche zwischen den Komponenten bestehen. Dabei geht es nicht um einen detaillierte Entwurf, sondern mehr um Zusammenhänge zwischen den Anforderungen und dem System.

Im Zuge der Definition einer Software Architektur werden grundlegende Entscheidungen für den weiteren Systementwurf getroffen, wie beispielsweise die Wahl der Plattform, die Auswahl von Entwicklungssystemen oder auch der einzusetzenden Datenbank.

In einer guten Softwarearchitektur sollten folgende Aspekte berücksichtigt werden:

- Beschreibung aller Elemente aus denen das System besteht
- Interaktion zwischen den Elementen
- Entwurfsmuster, welche durch die Softwarekomposition leiten
- Geltende Bedingungen für die Entwurfsmuster
- Software Architektur ist zugleich Prozess und Gegenstand



### Architektursichten

- Es gibt verschiedene Sichten auf eine Softwarearchitektur

- Warum Sichten?
  - Betrachtung aus verschiedenen Blickwinkeln dient der Komplexitätsbewältigung bei Anforderungen, Struktur und Umsetzung
  - verschiedene Beteiligte mit unterschiedlichen Rollen und Expertise
  - Transparenz
  - Entkopplung von verschiedenen System-Aspekten

- Es gibt verschiedene Modelle die verschiedene Sichten auf eine Architektur darstellen. In dieser Ausarbeitung gehe ich auf das `4+1 Sichtenmodell` von Philippe Kruchten ein.

  

### 4+1 Sichten Modell

Beschreibung der Sichten:

- Logische Sicht
  - beschäftigt sich mit der Funktionalität des Systems für den Endnutzer. Dabei werden verschiedene UML Diagramme zur Darstellung genutzt.
    - Klassendiagramm
    - Kommunikationsdiagramm
    - Sequenzdiagramm
- Entwicklungssicht
  - Beschreibt das System vom Standpunkt eines Entwicklers und beschäftigt sich mit dem Softwaremanagement.
    - Komponentendiagramm
    - Paketdiagramm
- Prozesssicht
  - Beschäftigt sich mit den dynamischen Aspekten des Systems. Hier werden die Prozesse des Systems verdeutlicht und beschreibt die Kommunikation der Prozesse hinsichtlich des Laufzeitverhaltens.
    - Aktivitätsdiagramm
    - Sequenzdiagramm
- Physische Sicht
  - Beschreibt das System vom Standpunkt des Systemarchitekten
- Szenarios
  - Die fünfte Sicht zeigt wichtige Anwendungsfälle und Anwendungsszenarien auf. Diese können abläuft zwischen Komponenten und Prozessen beschreiben und helfen Architekturelemente zu identifizieren und zu veranschaulichen.
    - Use Case Diagramm



![4+1 Sichtenmodell](img/4+1Model.png)





## Motivation und Ziele

Alle Softwaresysteme besitzen eine Architektur, auch wenn niemand diese explizit modelliert hat. Da die Modellierung eines Softwaresystems einen hohen Aufwand erfordert, stellt sich die Frage, zu welchem Zweck eine Architektur modelliert werden sollte und ob dies einen Mehrwert darstellt. 

- Durch die steigende Zahl vernetzter Produkte steigt Komplexität und Umfang von Projekten

- Auch immer mehr organisatorische Einflussfaktoren müssen berücksichtigt werden

- Dadurch wird die Architektur immer relevanter
- Bereits mittelgroße Softwaresysteme haben oftmals matrixartige Systemstrukturen mit vielen Modulen und Subsystemen und strecken sich über viele Schichten mit fachlichen und technischen Querschnitte
- Softwarearchitektur kann diese Komplexität beherrschbar machen und eine Entwicklungs- und Prozessverbesserung erreichen und dient als Kommunikationsgrundlage
- Vorteile durch sorgfältig geplante Software Architektur sind:
  - Effiziente Softwareentwicklung ist möglich
  - Performance kann gezielt gesteigert werden
  - Zeit Einsparung kann realisiert werden
  - Software-Budget kann optimieren werden
  - Gezielte Minimierung von Risiken
  - Kompakte Software in Umfang und Funktion designen
  - Wertvolles Wissen zu Software im Unternehmen erhalten und bewahren



## Notation



## Entwurf einer Software



### Grobentwurf



### Feinentwurf



## Bewertung von Software-Architekturen

- Motivation zur Bewertung
  - Identifikation von potenziellen Risiken
  - die Beurteilung der Realisierung von Qualitätsanforderungen durch die Architektur 
    - Identifikation der Schwachstellen und deren Überarbeitungsaufwand
  - die Identifikation von Möglichkeiten zur Wiederverwendung von Softwarekomponenten und anderen Artefakten
- Bewertung auf die Erreichung von Qualitätsmerkmalen (ISO 25010) --> Kurzauflistung ISO 25010 [siehe Softwarequalität]
  - Immer basierend auf den Anforderungen daher nicht immer alle der Qualitätsmerkmale relevant

![Qualitätsmerkmale](img/Qualitätsmerkmale.png)

Bild Quelle: https://www.informatik-aktuell.de/entwicklung/methoden/was-ist-eigentlich-architekturbewertung.html



### Qualitative Bewertung

- Die Qualitative Bewertung setzt auf Fokussierung, die Durchsprache von Lösungsansätzen und die Erfahrung und Argumente der Workshop Beteiligten. Restrisiko bleibt.

- Bewertung liefert keine Zahlen sondern quantitative Aussagen (z.B. im Gegensatz zu Messung von Quellcode)

- Qualitative Bewertungsmethoden überprüfen, ob die Lösungsansätze und Entscheidungen in der Architektur zu den Zielen des Vorhabens passen. 

- Für die qualitative Bewertung gibt es verschiedene Methoden und Ansätze

  - Szenario basierte Verfahren
    - Szenario basierte Architekturbewertungsverfahren verstehen sich häufig als ein Vorgehensmodell, welches zu einer Architekturbewertung führt. Die Szenario basierten Verfahren liefern mehr als nur eine Rechenmethodik oder Messanweisungen, sie beschreiben mehr oder weniger detailliert Schritte, über die man zu einer Architekturbewertung gelangt. Die wichtigsten Schritte in einer Szenario basierten Architekturbewertung finden sich in vielen der unterschiedlichen Verfahren wieder.
    - Ein sogenanntes Qualitätsszenario ist dabei eine beispielhafte Verwendung des zu betrachtenden Systems. Und zwar so, dass ein Qualitätsmerkmal die Hauptrolle spielt
    - Es gibt verschiedene Szenario basierte Methoden, die bekannteste ist ATAM
      - ATAM
      - CBAM (konzentriert sich auf Kosten Nutzen Bewertungen)
  - Ausfüllen von vorgefertigten Fragebögen und Checklisten

  

| Vorteile                                                 | Nachteile                                                    |
| -------------------------------------------------------- | ------------------------------------------------------------ |
| Bereits früh anwendbar                                   | Durchsprache ist kein Messen (ein "Restrisiko" bleibt)       |
| Passt auf alle Qualitätsmerkmale                         | Workshops nicht trivial in der Durchführung (Planung, Moderation ... ) |
| Bindet Stakeholder optimal ein und fördert den Austausch |                                                              |



### Quantitative Bewertung

- Die quantitative Bewertung setzt auf vermeintlich belastbarere Fakten
  - misst den Quelltext der Software und die Struktur der Elemente und deren Beziehungen untereinander

- Wird toolgestützt durchgeführt

  - Beispiele für Tools von Code Analyse

- Ansätze für die quantitative Bewertung:

  - Statische Code-Analyse

    - Metrikauswertungen können Problemgebiete in der Software identifizieren und vor allem im Bereich der Wartbarkeit unterstützen bestehende Softwareteile zu bewerten oder Aufwände zu fokussieren.

  - Dynamische Code-Analyse 

    - Dynamische Analyse kann in den Bereichen der Performanz, Skalierung oder Zuverlässigkeit gute Aufschlüsse über die Tauglichkeit einer Softwarelösung geben und kann bei bestehenden Systemteilen mit realistischen Einsatzszenarien prüfen ob Architekturideen tatsächlich greifen.

  - Strukturanalyse

    - Der Code wird in seiner Gliederung und Abhängigkeiten visualisiert und kann anschließend auf Best-Practices und Problemherde untersucht werden. Auch die Abweichung von Architekturideen wird sichtbar und kann zur Überarbeitung von Architektur- oder Codeseite führen.

    

| Vorteile                                          | Nachteile                                                  |
| ------------------------------------------------- | ---------------------------------------------------------- |
| Wenig Bauchgefühl, Zahlen sind gute Argumente     | Vergleichsweise spät einsetzbar                            |
| Messungen leicht automatisierbar und wiederholbar | Messungen können nicht alle Qualitätsmerkmale gut erfassen |
|                                                   | Gefahr der Missdeutung und Fehlleitung                     |



## Herangehensweise an Architektur und Design

- In der Software Entwicklung gibt es für alle Schritte Muster
  - Muster für die Analyse
  
  - Muster für den Entwurf
  
  - Muster für die Implementierung
  
  - Muster für das Testen
  
    
- Für den Softwareentwurf unterscheidet man je nach Granularität zwischen:
  - Entwurfsmuster
    - feingranular - eher die Lösung eines lokalen Problems
  - Architekturmuster
    - große Sicht auf die ganze Anwendung

### Entwurfsmuster

- Sind innerhalb der Softwarearchitektur- und Entwicklung allgemeine, wieder verwendbare Lösungsmuster für wiederkehrende Entwurfsprobleme
  - Sie bieten eine Vorlage zur Problemlösung für bestimmte Kontexte
  - Haben sich bereits bewährt
- Legen eine Struktur von Subsystemen fest

- Entwurfsmuster gliedern sich in Grundtypen
  - Erzeugungsmuster
  - Strukturmuster
  - Verhaltensmuster

- Entwurfsmuster verbessern Kommunikation im Team
  - bieten Diskussionsgrundlage um über die Softwarearchitektur zu sprechen



#### Erzeugungsmuster

- befasst sich mit der Erzeugung von Objekten
- entkoppeln Objektkonstruktion von der Objektrepräsentation

**Beispiele:**

- *Factory*

- *Singleton*

  

#### Strukturmuster

- Beschreibt die Komposition von Klassen Objekten

**Beispiele:**

- *Decorator*
- *Composite*



#### Verhaltensmuster

- Beschreibt wie Klassen oder Objekte miteinander kommunizieren und wie die Verantwortlichkeiten verteilt sind

**Beispiele:**

* *State*

* *Observer*



### Architekturmuster

- Beschreiben Systemstrukturen, welche die Gesamtarchitektur eines Systems festlegen
- Spezifizieren, wie Subsysteme zusammenarbeiten

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

