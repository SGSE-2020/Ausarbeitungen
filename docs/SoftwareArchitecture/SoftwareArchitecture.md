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

Um zu die entwickelte Software Architektur zu validieren und zu überprüfen ob diese als Lösungskonzept für das vorhandene Problem dienen kann, ist es sinnvoll eine Bewertung durchzuführen. Diese kann helfen, potenzielle Risiken zu erkennen und die Realisierung von Qualitätsanforderungen durch die Architektur zu beurteilen. Weiterhin kann eine Bewertung dazu beitragen die Schwachstellen sowie deren Überarbeitungsaufwand zu analysieren. Im Zuge der Bewertung werden oftmals auch Möglichkeiten zur Wiederverwendung von Softwarekomponenten und anderen Artefakten erarbeitet. Dies dient dazu, sicherzustellen, dass die korrekte Software Architektur verwendet wird, da diese spätere Funktionalität sowie Kosten maßgeblich beeinflussen kann. Je später Fehler erkannt werden, desto teurer können diese werden.

Die Bewertung einer Software Architektur erfolgt grundsätzlich anhand der Erreichung bestimmter Qualitätsmerkmale. Die `ISO 25010` definiert für diesen Zweck eine Reihe von Qualitätskriterien für Software und IT-Systeme. Die in dem untenstehenden Bild sichtbaren 8 Kernkriterien werden von der Norm definiert. Alle Kernkriterien besitzen Unterkriterien, welche zu erreichen sind um das Kernziel umfassend zu erfüllen.

![Qualitätsmerkmale](img/Qualitätsmerkmale.png)

​       *Quelle: [6]*



### Qualitätsbaum

Der Qualitätsbaum ist der Ausgangspunkt für die Bewertung einer Software Architektur. Er stellt eine Beschreiung der zu erreichenden Qualitätsziele dar. Dabei wird eine hierarchische Struktur aufgestellt, welche die Qualitätsmerkmale aus der `ISO 25010` für die eigenen Bedürfnisse anpasst und nur die für spezifische Software relevanten Qualitätsmerkmale enthält. Im Qualitätsbaum können je nach Softwareanforderungen einzelne Kernkriterien oder nur einige Unterkriterien weggelassen werden. Auf Basis des Qualitätsbaums können anschließend verschiedene Bewertungsmethoden durchgeführt werden. Das untenstehende Bild verdeutlicht ein Beispiel eines Qualitätsbaums, in welchem einige Kernkriterien nicht relevant sind.

![Qualitätsbaum Beispiel](img/BeispielQualitätsbaum.jpg)

​     *Quelle: [10]*



### Qualitative Bewertung

Die qualitative Bewertung einer Softwarearchitektur setzt auf Fokussierung, die Durchsprache von Lösungsansätzen sowie auf Erfahrung und Argumente von Workshop Beteiligten. Dabei bleibt ein Restrisiko, da eine Durchsprache niemals ein Messen von Zahlen darstellen kann. Daher liefert diese Art der Bewertung keine Zahlen, sondern quantitative Aussagen. Qualitative Bewertungsmethoden überprüfen, ob die Lösungsansätze und Entscheidungen die für eine Architektur getroffen wurden, zu den Zielen des Vorhabens sowie der Anforderungen passen.

Für die qualitative Bewertung gibt es verschiedene Methoden und Ansätze wie z.B das Ausfüllen von vorgefertigten Fragebögen und Checklisten oder auch das Durchführen Szenario basierter Verfahren. Szenario basierte Verfahren agieren häufig wie eine Art Vorgehensmodell, welches zu einer Architekturbewertung führt. Dabei werden mehr oder weniger detailliert Schritte beschrieben, wie man zu einer solchen Bewertung gelangt. Die wichtigsten Schritte, welche sich in vielen dieser Vorgehensmodelle wiederfinden, sind folgende:

- Erheben und Priorisieren von Qualitätsszenarios
- Erstellen und Beschreiben der Architektur
- Bewertung der Softwarearchitektur aus dem Blickwinkel der wichtigsten erhobenen Qualitätsszenarios
- Präsentieren der Ergebnisse und Erstellen eines Berichts

Ein Qualitätsszenario stellt dabei eine beispielhafte Verwendung des zu betrachtenden Systems dar. Dies kann ein gewünschter Anwendungsfall oder auch der Auftritt eines Fehlers sein. Dabei muss ein bestimmtes Qualitätsmerkmal aus dem Qualitätsbaum im Fokus liegen. Es gibt sehr viele verschiedene Szenario basierte Verfahren. Das bekannteste Verfahren nennt sich ATAM [**A**rchitecture **t**readeoff **a**nalysis **m**ethod]. Dieses bietet eine gute Identifikation von Risiken und Nichtrisiken hinsichtlich der geforderten Qualitätsmerkmale. 

In der nachfolgenden Tabelle sind die Vor und Nachteile der qualitativen Bewertung aufgelistet:

| Vorteile                                                 | Nachteile                                                    |
| -------------------------------------------------------- | ------------------------------------------------------------ |
| Bereits früh anwendbar                                   | Durchsprache ist kein Messen (ein "Restrisiko" bleibt)       |
| Passt auf alle Qualitätsmerkmale                         | Workshops nicht trivial in der Durchführung (Planung, Moderation ... ) |
| Bindet Stakeholder optimal ein und fördert den Austausch |                                                              |

 *Quelle: [6]*

### Quantitative Bewertung

Im Gegensatz zur qualitativen Bewertung setzt die quantitative Bewertung eher auf Zahlen und Fakten. Um eine Bewertung durchzuführen, wird der Quelltext der Software sowie die Struktur der Elemente und deren Beziehungen untereinander gemessen- Dies wird toolgestützt durchgeführt mit Tools für die Code Analyse.

Ansätze für die quantitative Bewertung sind z.B. die statische oder dynamische Codeanalyse. Bei der statischen Codeanalyse werden Metrik Auswertungen durchgeführt, welche Problemgebiete innerhalb der Software identifizieren und bestehende Softwareteile zu bewerten oder Aufwände zu fokussieren. Die dynamische Codeanalyse kann dafür genutzt werden, um in den Bereichen der Performanz, Skalierung sowie Zuverlässigkeit Aufschlüsse über die Tauglichkeit der Softwarelösung zu geben. Außerdem kann eine quantitative Bewertung auch mit Hilfe einer Strukturanalyse durchgeführt werden. Dabei wird der Code in seiner Gliederung und Abhängigkeiten visualisiert und kann anschließend auf Problemherde untersucht werden. Dabei wird auch eine mögliche Abweichung der bisherigen Architekturidee sichtbar. Dies kann zur Überarbeitung von Architektur- oder Codeseite führen.

In der nachfolgenden Tabelle sind die Vor und Nachteile der quantitativen Bewertung aufgelistet:

| Vorteile                                          | Nachteile                                                  |
| ------------------------------------------------- | ---------------------------------------------------------- |
| Wenig Bauchgefühl, Zahlen sind gute Argumente     | Vergleichsweise spät einsetzbar                            |
| Messungen leicht automatisierbar und wiederholbar | Messungen können nicht alle Qualitätsmerkmale gut erfassen |
|                                                   | Gefahr der Missdeutung und Fehlleitung                     |

 *Quelle: [6]*

## Entwurf einer Software

Der Softwareentwicklungsprozess gliedert sich in vier Phasen auf. Zu Beginn wird eine Anforderungsanalyse durchgeführt, welche alle Anforderungen an die Software zusammen mit allen Rahmenbedingungen sammelt und in ein Lasten und Pflichtenheft formuliert. Anschließend folgt die Entwurfphase. Diese gliedert sich auf in Grob- und Feinentwurf. Im ersten Schritt, dem Grobentwurf oder auch Architekturentwurf wird die eine erste Klärung der Funktionalität und Systemarchitektur durchgeführt und erste Modelle werden entworfen. Anschließend werden die Ergebnisse beim Feinentwurf oder auch Detailentwurf detaillierter Ausgearbeitet und Schnittstellen sowie Datenstrukturen werden definiert. Wenn er Entwurf abgeschlossen ist beginnt die Implementierung der Software. Abschließend wird die Software getestet und integriert. Je nach Vorgehensweise werden die Phasen nacheinander abgearbeitet (klassisch) oder es besteht die Möglichkeit zu einer früheren Phase zurückzuspringen (agil / iterativ).

![Phasen Softwareentwicklung](img/PhasenSoftwareentwicklung.png)

​                                      *Quelle: [14]*



Die Software Architektur entsteht in der Entwurfphase. Wie zuvor erläutert, muss dafür die Analysephase abgeschlossen sein und die Anforderungs- und Systemspezifikation (Pflichten und Lastenheft) müssen vorliegen. Bei der Entwicklung eines Softwareentwurfs geht man meist iterativ vor und der Entwurf nimmt mit jeder Iterationsphase an Granularität zu. Ziel des Softwareentwurfs ist es, die Vorgaben der Anforderungsdefinition möglichst umfassend zu berücksichtigen.

### Grobentwurf / Architekturentwurf

Der Grobentwurf, oder auch Architekturentwurf genannt, beschreibt die Gesamtstruktur und Organisation des Systems auf einer hohen Abstraktionsebene. Dabei müssen wesentliche Komponenten und deren Interaktion untereinander identifiziert werden. Außerdem werden Randbedingungen festgelegt, wie die Vorgabe von Hardware, Betriebssystem, Middleware sowie Vorgaben zu Programmiersprachen. Die Hauptaufgaben für die Erstellung des Grobentwurfs sind:

- Aufgabe analysieren
- Architektur modellieren und dokumentieren
- Lösungskonzept prüfen

Bei der Analyse der Aufgabe ist es das Ziel die Anforderungen zu verstehen und vorhandene bzw. beschaffbare Technologien zu analysieren. In der Modellierungs- und Dokumentationsphase wird die grundlegende Systemarchitektur festgelegt. Im Rahmen dessen ist es hilfreich die Modularisierung zu definieren. Dabei wird dir zu erstellende Software in Komponenten gegliedert und Module werden voneinander abgegrenzt. Außerdem werden Verantwortlichkeiten definiert. Eine weitere Aufgabe der Phase ist es nebenläufige Lösungen in Prozesse zu gliedern. Dafür muss eine Analyse der zeitlich verzahnten Ausführung von Aktivitäten durchgeführt werden. Anschließend können die Prozesse festgelegt und zu Modulen zugeordnet werden. Weiterhin muss in dieser Phase die Zusammenarbeit festgelegt werden. Dabei werden Kommunikationsbedürfnisse analysiert und Kommunikationsverfahren festgelegt. Für jedes Bedürfnis werden konkrete Verfahren gewählt und Schnittstellen definiert. Abschließend wird das gesamte Lösungskonzept geprüft und validiert.

Der Grobentwurf beinhaltet die folgenden Artefakte:

- Architekturentwurf
- Subsystem Spezifikation
- Schnittstellenspezifikation

### Feinentwurf / Detailentwurf

Der Feinentwurf beschreibt die Detailstruktur des Systems. Dabei werden die einzelnen Komponenten so detailliert beschrieben, so dass diese implementiert werden können. Außerdem werden Datenstrukturen und Algorithmen beschrieben. Zu Hauptaufgaben für die Erstellung des Feinentwurfs gehört die Abbildung der Module und Prozesse auf die verfügbaren Konstrukte der verwendeten Programmiersprachen. Außerdem wird ein Coderahmen erstellt sowie Implementierungsskizzen für alle Module und Prozesse. 

Der Feinentwurf beinhaltet die folgenden Artefakte:

- Komponentenentwurf
- Datenstrukturentwurf
- Algorithmenentwurf



## Herangehensweise an Architektur und Design

Im Rahmen der Software Entwicklung werden für alle Schritte verschiedene Arten von Mustern eingesetzt. Es gibt Muster für die Analyse, für den Entwurf, für die Implementierung sowie für das Testen von Software. Für den Softwareentwurf unterscheidet man je nach Granularität zwischen Entwurfsmuster und Architekturmuster. Architekturmuster sind grobgranular und bieten eine Sicht auf die gesamte Anwendung. Entwurfsmuster dagegen sind eher feingranular und fokussieren sich auf die Lösung eines lokalen Problems.



### Entwurfsmuster

Entwurfsmuster sind innerhalb der Softwarearchitektur und Entwicklung allgemeine, wieder verwendbare Lösungsmuster für wiederkehrende Entwurfsprobleme. Sie bieten eine sich bereits bewährte Vorlage zur Problemlösung für bestimmte Kontexte. Weiterhin legen Entwurfsmuster eine Struktur von Subsystemen fest. Entwurfsmuster können die Kommunikation im Team verbessern, da sie eine Diskussionsgrundlage bieten um über Softwarearchitektur zu sprechen. Es gibt drei verschiedene Gruppen von Entwurfsmuster basierend auf dem Kontext in dem sie eingesetzt werden können. Folgende Arten von Erzeugungsmustern gibt es:

- Erzeugungsmuster
- Strukturmuster
- Verhaltensmuster

Das folgende Bild zeigt eine Übersicht verschiedener Entwurfsmuster und in welche Gruppe diese gehören. Die fett markierten Entwurfsmuster werden in dieser Ausarbeitung beispielhaft dargestellt.

![Entwurfsmuster Übersicht](img/Entwurfsmuster.svg)
#### Erzeugungsmuster

Erzeugungsmuster befassen sich mit der Erzeugung von Objekten. Sie entkoppeln die Objektkonstruktion von der Objektrepräsentation.



**Beispiele:**

- *Factory*

- *Singleton*

  

#### Strukturmuster

Strukturmuster beschreiben die Komposition von Klassen Objekten.

**Beispiele:**

- *Decorator*
- *Composite*



#### Verhaltensmuster

Verhaltensmuster beschreibt wie Klassen oder Objekte miteinander kommunizieren und wie die Verantwortlichkeiten verteilt sind.

**Beispiele:**

* *State*

* *Observer*



### Architekturmuster

Architekturmuster beschreiben Systemstrukturen, welche die Gesamtarchitektur eines Systems festlegen. Dabei spezifizieren sie wie die Subsysteme der Software miteinander zusammenarbeiten. Architekturmuster können mittels vier Überkategorien geordnet und zusammengefasst werden. Folgende Übergruppen gibt es:

- Chaos zu Struktur
- Muster für verteilte Systeme
- Adaptive / Anpassbare Systeme
- Interaktive Systeme



#### Chaos zu Struktur

Architekturmuster dieser Kategorie bieten eine Organisation der Vielzahl der Komponenten und Objekte eines Softwaresystems. Die Aufteilung der Funktionalität des Gesamtsystems wird dabei in kooperierende Subsysteme aufgeteilt. Die bekannteste Architektur in dieser Kategorie ist die Schichtenarchitektur. 

**Beispiele:**

- Schichtenarchitektur
- Domain Model *(Software Architekturen kompakt ab S.43)*
  - Ports and Adapters (hexagonale Architektur)
  - Onion Architecture
  - Clean Architecture
- Pipes und Filter *(evtl. nur ganz kurz oder auflisten)*
- Schwarzes Brett *(evtl. nur ganz kurz oder auflisten)*



#### Muster für verteilte Systeme

Architekturmuster in dieser Kategorie unterstützen die Verwendung verteilter Ressourcen und Dienste in Netzwerken. Um ein Softwaresystem verteilen zu können, muss es in Subsysteme strukturiert sein. Dabei ist es wichtig, dass die Subsysteme in sich stark verbunden sind. Die traditionelle Architektur in dieser Kategorie ist die Client-Server Architektur.

**Beispiele:**

-  Client-Server
- Serviceorientierte Architektur (SOA)
- Peer-to-Peer *(evtl. nur ganz kurz oder auflisten)*

#### Adaptive / Anpassbare Systeme

Architekturmuster in dieser Kategorie sind besonders anpassungsfähig und erweiterungsfähig zur Laufzeit.

**Beispiele:**

- Dependency Injection
- Reflexion 

#### Interaktive Systeme

Muster in dieser Kategorie bieten eine Strukturierungsmöglichkeit für Interaktionen von Mensch und Computer.

**Beispiele:**

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

[9] [Vergleich von Qualitätsbewertungsmethoden für IT-Architekturen](http://bauhaus.cs.uni-magdeburg.de:8080/miscms.nsf/FEA8C8150500AA14C1257449004F79A9/739B0C874E72E513C1257651002C9086/$FILE/Studienarbeit Frank Eichler.pdf)

[10] [Qualitätsanforderungen konkret formulieren](https://jaxenter.de/stakeholder-qualitaetsanforderungen-konkret-formulieren-86582)

[11] [Spezifikation und Entwurf von Software (Martin Glinz)](https://files.ifi.uzh.ch/rerg/amadeus/teaching/courses/spezifikation_und_entwurf_ws0506/kapitel_17.pdf)

[12] [Softwarearchitektur & Entwurf (Wolfgang Schramm)](http://services.informatik.hs-mannheim.de/~schramm/see/files/Kapitel04.pdf)

[13] [Lehrbuch der Softwaretechnik: Entwurf, Implementierung, Installation und Betrieb (Helmut Balzert)](https://www.springer.com/de/book/9783827417060)

[14] [Vorgehensweise zur Erstellung einer  IT-Architektur](https://www.axxessio.com/de/blog-de/axx42-erstellung-it-architektur)

[15] [Design Pattern](https://www.philipphauer.de/study/se/design-pattern.php)

[16] [Architektur und Entwurfsmuster](https://www.w3l.de/de/fileadmin/user_upload/Architektur_und_Entwurfsmuster_2012.pdf)

[17] [DDD Architekturen im Vergleich](https://www.maibornwolff.de/blog/ddd-architekturen-im-vergleich)

[18] [Von Schichten zu Ringen - Hexagonale Architekturen erklärt](https://www.maibornwolff.de/blog/von-schichten-zu-ringen-hexagonale-architekturen-erklaert)

[19] [Clean Architekture](https://www.4soft.de/blog/2019/clean-architecture/)