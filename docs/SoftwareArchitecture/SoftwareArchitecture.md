# Software Architekturen

**Autor:** Pia Schreiner

**Modul:** Spezielle Gebiete des Software Engineerings



## Was ist eine Software Architektur?

Eine Software Architektur ist eine Beschreibung aller Komponenten eines Systems sowie aller Verbindungen, welche zwischen den Komponenten bestehen. Dabei geht es nicht um einen detaillierte Entwurf, sondern mehr um Zusammenhänge zwischen den Anforderungen und dem System.

Im Zuge der Definition einer Software Architektur werden grundlegende Entscheidungen für den weiteren Systementwurf getroffen, wie beispielsweise die Wahl der Plattform, die Auswahl von Entwicklungssystemen oder auch der einzusetzenden Datenbank. Software Architektur stellt also den Plan eines Systems dar und keinesfalls das System selbst. 

Um gute Software zu entwickeln ist es für Software Architekten wichtig sich mit der Beschreibung des Softwaresystems zu beschäftigen. In einer guten Softwarearchitektur sollten folgende Aspekte berücksichtigt werden:

- Beschreibung aller Elemente aus denen das System besteht
- Interaktion zwischen den Elementen
- Entwurfsmuster, welche durch die Softwarekomposition leiten
- Geltende Bedingungen für die Entwurfsmuster
- Software Architektur ist zugleich Prozess und Gegenstand



### Architektursichten

Um eine Software Architektur in Gänze begreifen zu können, kann man aus verschiedenen Sichten auf eine Softwarearchitektur schauen. Dies ist sinnvoll, da verschiedene Beteiligte an einem Softwareprojekt unterschiedliche Rollen wahrnehmen und auch in verschiedenen Gebieten Expertise besitzen. Die verschiedenen Sichten sorgen dafür, dass man die Softwarearchitektur aus verschiedenen Blickwinkeln betrachtet. Dies sorgt für mehr Transparenz und kann der Komplexitätsbewältigung im Rahmen von Anforderungen, Struktur und Umsetzung sorgen. Außerdem findet so eine Entkopplung verschiedener System-Aspekte statt und diese können dadurch einzeln genauer betrachtet werden.

Für die Betrachtung einer Software Architektur aus verschiedenen Sichten, gibt es bereits einige Modelle. Die bekanntesten sind dabei das `4+1 Sichtenmodell` von Philippe Kruchten sowie die `vier Arten von Sichten` von Starke.



### 4+1 Sichten Modell nach Kruchten

Das 4+1 Sichten Modell von Philippe Kruchten stellt die Blickwinkel auf das System aus verschiedenen Rollen innerhalb der vier Hauptsichten dar. Zusätzlich können Use Cases und Szenarios betrachtet werden, um die Architektur besser darzustellen. Diese Zusatzbetrachtung stellt das +1 dar. Bei den insgesamt vier Schichten handelt es sich um eine logische Sicht, eine Enwicklungssicht, eine Prozesssicht sowie eine Physische Sicht.

#### Logische Sicht

Die logische Schicht beschäftigt sich mit der Funktionalität des Systems für den Endnutzer. Diese Funktionalität wird mit Hilfe von verschiedenen UML-Diagrammen dargestellt. Die logische Sicht betrachtet die Phase der Anforderungsanalyse und verwendet unter anderem die folgenden Artefakte:

- Klassendiagramm
- Verbundstrukturdiagramm

#### Entwicklungssicht

Die Entwicklungssicht beschreibt das System vom Standpunkt eines Entwicklers. Dabei beschäftigt sich diese mit dem Softwaremanagement und hat einen Fokus auf die Modularisierung in Subsysteme. Folgende Artefakte werden zur Darstellung verwendet:

- Komponentendiagramm
- Paketdiagramm

#### Prozesssicht

Die Prozesssicht beschreibt das System vom Standpunkt des Systemintegrators. Dabei beschäftigt sich diese mit den dynamischen Aspekten des Systems. Der Fokus liegt dabei auf der Beschreibung aller Prozesse sowie die Kommunikation derer hinsichtlich des Laufzeitverhaltens. Hierfür kommen alle Artefakte zum Einsatz, welche in der Lage sind Aktivitäten und Prozesse zu beschreiben, wie z.B.:

- Aktivitätsdiagramm
- Sequenzdiagramm
- Kommunikationsdiagramm

#### Physische Sicht

Beschreibt das System vom Standpunkt eines Systemarchitekten. Dabei geht es um die Abbildung der Software auf die Hardware sowie die Verteilungsaspekte. Dabei werden Artefakte wie eine Netzwerktopologie eingesetzt.

#### Szenario Sicht

Die Szenario Sicht stellt eine Beschreibung wichtiger Anwendungsfälle und Anwendungsszenarien dar. Diese bieten eine Darstellung von Abläufen zwischen Komponenten und Prozessen. Dies bietet die Möglichkeit Architekturelemente zu identifizieren und zu veranschaulichen. Genutzte Artefakte für die Darstellung sind:

- Use Case Diagramm
- User Stories



![4+1 Sichtenmodell Kruchten](img/4+1Model.png)			*Quelle: [4]*



### Vier Arten von Sichten von Starke

Das Sichten Modell von Starke beschreibt die Blickwinkel auf die Architektur mehr auf das System bezogen und im Gegensatz zu Kruchten weniger auf den Standpunkt verschiedener Rollen bezogen. 

#### Kontextabgrenzung

Bei der Sicht auf die Kontextabgrenzungen wird die Einbettung des Systems in seine Umgebung betrachtet. Dabei wird das System als Blackbox in seinem Kontext aus einer Vogelperspektive dargestellt. Die Kontextabgrenzung bietet eine sehr abstrahierte Sicht auf die Architektur. Im Detail  beschreibt die Kontextabgrenzung die Namen und Funktion aller Nachbarsysteme, die Art der mit den Nachbarsystemen ausgetauschten Daten sowie Metainformationen der Schnittstellen oder übertragenen Daten. Weiterhin können Datenformate sowie Übertragungsmedien beleuchtet werden, vorausgesetzt sie sind zu diesem Zeitpunkt schon relevant.

#### Bausteinsicht

In der Bausteinsicht wird der interne Aufbau das Systems in Form einer statischen Struktur dargestellt. Dabei werden die Strukturen des Systems, der Subsysteme, Komponenten beleuchtet. Außerdem wird das Zusammenwirken der einzelnen Bausteine (Schnittstellen) dargestellt. Die Bausteinsicht wird ausgehend von der Kontextabgrenzung top-down entwickelt. Die Bausteinsicht enthält Blackbox sowie White box Bausteine. Blackbox Bausteine stellen dabei nur Schnittstellen und Funktionen dar, während White box Bausteine als Verfeinerung die innere Struktur zeigen. Dabei werden die folgenden Artefakte verwendet:

- Komponentendiagramm
- Paketdiagramm

#### Laufzeitsicht

Eine Laufzeitsicht beschreibt im Gegensatz zur Bausteinsicht die dynamische Struktur und die Bausteine des Systems, welche zur Laufzeit existieren. Darüber hinaus stellt sie dar, wie die Bausteine zusammenwirken. Die Aktivitäten werden mit folgenden Artefakten dargestellt:

- Sequenzdiagramm
- Kommunikationsdiagramm

#### Verteilungssicht (Infrastruktur)

Die Verteilungs- oder Infrastruktursicht beschreibt die technische Ablaufumgebung. Dabei werden die Hardwarekomponenten beschrieben, auf denen das System läuft. Im Detail werden hier Rechner, Prozessoren und Speicher beleuchtet auf denen die Softwarebestandteile des Systems ausgeführt oder Daten gespeichert werden. Außerdem werden Kanäle beschrieben, über die zwischen den Knoten Daten übertragen werden. Die Darstellung der Sicht findet mit Hilfe der folgende Artefakte statt:

- Deploymentdiagramm
- Netzwerktopologie

![Sichten Starje](img/ArchitekturSichtenStarke.jpg)

​			*Quelle: [5]*



## Motivation und Ziele

Alle Softwaresysteme besitzen eine Architektur, auch wenn niemand diese explizit modelliert hat. Da die Modellierung eines Softwaresystems einen hohen Aufwand erfordert, stellt sich die Frage, zu welchem Zweck eine Architektur modelliert werden sollte und ob dies einen Mehrwert darstellt. Durch die steigende Zahl vernetzter Produkte steigt die Komplexität und der Umfang von Softwareprojekten. Außerdem müssen auch immer mehr organisatorische Einflussfaktoren berücksichtigt werden. Auf Grund dessen wird der Entwurf einer guten und effizienten Software Architektur immer relevanter.

Bereits mittelgroße Softwaresysteme verfügen oftmals bereits über matrixartige Systemstrukturen, welche viele Module und Subsysteme enthalten. Diese strecken sich oft über viele Schichten und beinhalten fachliche sowie technische Querschnitte. Eine gute Software Architektur kann diese Komplexität beherrschbar machen und eine Entwicklungs- und Prozessverbesserung erreichen. Außerdem dient die Software Architektur als Kommunikations- und Diskussionsgrundlage für verschiedene Beteiligte.

Vorteile durch eine sorgfältige geplante Software-Architektur sind:

- Effiziente Softwareentwicklung ist möglich
- Performance kann gezielt gesteigert werden
- Zeit Einsparung kann realisiert werden
- Software-Budget kann optimieren werden
- Gezielte Minimierung von Risiken
- Kompakte Software in Umfang und Funktion designen
- Wertvolles Wissen zu Software im Unternehmen erhalten und bewahren



## Bewertung von Software-Architekturen

Um zu die entwickelte Software Architektur zu validieren und zu überprüfen ob diese als Lösungskonzept für das vorhandene Problem dienen kann, ist es sinnvoll eine Bewertung durchzuführen. Diese kann helfen, potenzielle Risiken zu erkennen und die Realisierung von Qualitätsanforderungen durch die Architektur zu beurteilen. Weiterhin kann eine Bewertung dazu beitragen die Schwachstellen sowie deren Überarbeitungsaufwand zu analysieren. Im Zuge der Bewertung werden oftmals auch Möglichkeiten zur Wiederverwendung von Softwarekomponenten und anderen Artefakten erarbeitet.

Die Bewertung einer Software Architektur erfolgt grundsätzlich anhand der Erreichung bestimmter Qualitätsmerkmale. Die `ISO 25010` definiert für diesen Zweck eine Reihe von Qualitätskriterien für Software und IT-Systeme. Die in dem untenstehenden Bild sichtbaren 8 Kernkriterien werden von der Norm definiert. Alle Kernkriterien besitzen Unterkriterien, welche zu erreichen sind um das Kernziel umfassend zu erfüllen.

![Qualitätsmerkmale](img/Qualitätsmerkmale.png)

​       *Quelle: [6]*



### Qualitätsbaum

Der Qualitätsbaum ist der Ausgangspunkt für die Bewertung einer Software Architektur. Er stellt eine Beschreiung der zu erreichenden Qualitätsziele dar. Dabei wird eine hierarchische Struktur aufgestellt, welche die Qualitätsmerkmale aus der `ISO 25010` für die eigenen Bedürfnisse anpasst und nur die für spezifische Software relevanten Qualitätsmerkmale enthält. Im Qualitätsbaum können je nach Softwareanforderungen einzelne Kernkriterien oder nur einige Unterkriterien weggelassen werden. Auf Basis des Qualitätsbaums können anschließend verschiedene Bewertungsmethoden durchgeführt werden. Das untenstehende Bild verdeutlicht ein Beispiel eines Qualitätsbaums, in welchem einige Kernkriterien nicht relevant sind.

![Qualitätsbaum Beispiel](img/BeispielQualitätsbaum.jpg)

​     *Quelle: [10]*



### Qualitative Bewertung

- Die Qualitative Bewertung setzt auf Fokussierung, die Durchsprache von Lösungsansätzen und die Erfahrung und Argumente der Workshop Beteiligten. Restrisiko bleibt.

- Bewertung liefert keine Zahlen sondern quantitative Aussagen (z.B. im Gegensatz zu Messung von Quellcode)

- Qualitative Bewertungsmethoden überprüfen, ob die Lösungsansätze und Entscheidungen in der Architektur zu den Zielen des Vorhabens passen. 

- Für die qualitative Bewertung gibt es verschiedene Methoden und Ansätze

  - Szenario basierte Verfahren
    - Szenario basierte Architekturbewertungsverfahren verstehen sich häufig als ein Vorgehensmodell, welches zu einer Architekturbewertung führt. Die Szenario basierten Verfahren liefern mehr als nur eine Rechenmethodik oder Messanweisungen, sie beschreiben mehr oder weniger detailliert Schritte, über die man zu einer Architekturbewertung gelangt. Die wichtigsten Schritte in einer Szenario basierten Architekturbewertung finden sich in vielen der unterschiedlichen Verfahren wieder.
    - Ein sogenanntes Qualitätsszenario ist dabei eine beispielhafte Verwendung des zu betrachtenden Systems. Und zwar so, dass ein Qualitätsmerkmal die Hauptrolle spielt
    - Es gibt verschiedene Szenario basierte Methoden, die bekannteste ist ATAM
      - ATAM (Identifikation von Risiken und Nichtrisiken hinsichtlich der geforderten Qualitätssmerkmale)
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



## Entwurf einer Software

- Wie komme ich zu einer Softwarearchitektur?

- Phasen der Softwareentwicklung
  - Anforderungsanalyse -> Anforderungen an SW, Rahmenbedingungen
  - Grobdesign -> Klärung der Funktionalität und Systemarchitektur, erste Modelle
  - Feindesign -> Detaillierte Ausarbeitung der Komponenten, Schnittstellen, Datenstrukturen
  - Implementierung
  - Test und Integration
- Je nach Vorgehensweise wird zwischen Phasen hin und her gesprungen oder nacheinander abgehandelt (klassisch vs. agil)

![Phasen Softwareentwicklung](img/PhasenSoftwareentwicklung.png)

Quelle: https://www.axxessio.com/de/blog-de/axx42-erstellung-it-architektur



- Software Architektur entsteht in  der Entwurfphase, welche Grob und Feindesign beinhaltet.

- Der Entwurf einer Software findet nach Abschluss der Analyse statt. Die Analyse beinhaltet die Phase der Anforderungsermittlung sowie die Formulierung der Anforderungs- und Systemspezifikation (Pflichten- und Lastenheft).

- Bei der Entwicklung eines Softwareentwurfs geht man meist iterativ vor und der Entwurf nimmt mit jeder Iterationsphase an Granularität zu. Man unterscheidet daher den Grobentwurf vom Feinentwurf.

- Ziel des Softwareentwurfs ist es die Vorgaben der Anforderungsdefinition möglichst umfassend zu berücksichtigen

  

### Grobentwurf / Architekturentwurf

- Festlegen von Randbedingungen

  - Vorgabe der Hardware
  - Vorgabe Betriebssystem
  - Vorgabe Middleware
  - Vorgaben zu Schnittstellen und Programmiersprachen

- Beschreibt die Gesamtstruktur und Organisation des Systems

  - hohes Abstraktionsniveau

- Identifikation wesentlicher Komponenten und deren Interaktion

- Beschreibt Schnittstellen

- Beinhaltet

  - Architekturentwurf
  - Subsystem Spezifikation
  - Schnittstellenspezifikation

- Hauptaufgaben des Architekturentwurfs

  - Aufgabe analysieren
    - Anforderungen verstehen
    - Vorhandene bzw. beschaffbare Technologien und Mittel analysieren
  - Architektur modellieren und dokumentieren
    - Grundlegende Systemarchitektur festlegen
    - Modularisierung
      - Gliederung der zu erstellenden Software in Komponenten
      - Abgrenzung der Module
      - Festlegung von Verantwortlichkeiten
    - Nebenläufige Lösungen in Prozesse gliedern
      - Analyse der zeitlich verzahnten Ausführung von Aktivitäten
      - Festlegung der Prozesse und Zuordnung zu Modulen
      - Art der Ausführung der Prozesse regeln (Priorität, Reihenfolge, Unterbrechbarkeit)
    - Zusammenarbeit festlegen
      - Kommunikationsbedürfnisse analysieren
      - Kommunikationsverfahren festlegen
      - Für jedes Bedürfnisse konkrete Verfahren wählen und Schnittstellen definieren
        - Wer kommuniziert was mit wem?
        - Wie wird kommuniziert?
  - Lösungskonzept prüfen

  

### Feinentwurf / Detailentwurf

- Beschreibt die Detailstruktur des Systems
- Beschreibt die einzelnen Komponenten, so dass die implementiert werden können
- Beschreibt Datenstrukturen und Algorithmen
- Aufgaben des Detailentwurfs:
  - Abbildung der Module und Prozesse auf die verfügbaren Konstrukte der verwendeten Programmiersprachen
  - Erstellung von Coderahmen und Implementierungsskizzen für alle Module und Prozesse
  - Detaillierte Ausarbeitung aller Aspektkonzepte
  - 
- Beinhaltet
  - Komponentenentwurf
  - Datenstrukturentwurf
  - Algorithmenentwurf



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
  - Domain Model (Software Architekturen kompakt ab S.43)
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

[1] [Software Architekturen: Grundlagen - Theorie - Praxis](https://www.springer.com/de/book/9783827419330)

[2] [Software Architektur kompakt (Gernot Starke)](https://www.springer.com/de/book/9783827428349#otherversion=9783827428356)

[3] [Eddiziente Softwarearchitekturen (Gernot Starke)](https://www.hanser-fachbuch.de/buch/Effektive+Softwarearchitekturen/9783446452077)

[4] [Documenting Software Architecture](https://herbertograca.com/2019/08/12/documenting-software-architecture/)

[5] [Unterschiedliche Sichten auf Architekturen](https://entwickler.de/online/unterschiedliche-sichten-auf-architekturen-116073.html)

[6] [Was ist eigentlich Architekturbewertung](https://www.informatik-aktuell.de/entwicklung/methoden/was-ist-eigentlich-architekturbewertung.html)

[7] [Architektur Reviews](https://www.embarc.de/themen/architekturreviews/)

[8] [Auswahl von Bewertungsmethoden für Softwarearchitekturen](https://www.softec.wiwi.uni-due.de/uploads/tx_itochairt3/publications/ICBReport14_04.pdf)

[9] [Vergleich von Qualitätsbewertungsmethoden für IT-Architekturen]([http://bauhaus.cs.uni-magdeburg.de:8080/miscms.nsf/FEA8C8150500AA14C1257449004F79A9/739B0C874E72E513C1257651002C9086/$FILE/Studienarbeit%20Frank%20Eichler.pdf](http://bauhaus.cs.uni-magdeburg.de:8080/miscms.nsf/FEA8C8150500AA14C1257449004F79A9/739B0C874E72E513C1257651002C9086/$FILE/Studienarbeit Frank Eichler.pdf))

[10] [Qualitätsanforderungen konkret formulieren](https://jaxenter.de/stakeholder-qualitaetsanforderungen-konkret-formulieren-86582)