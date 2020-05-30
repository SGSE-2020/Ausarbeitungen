# Softwarequalität

André Matutat

## Motivation

Die Konzeptionierung und Entwicklung von Software ist ein komplexes Unterfangen bei denen eine Vielzahl an unterschiedlichen Faktoren und Stakeholder Einfluss nehmen. Oft wird Software über Jahre hinweg eingesetzt und erweitert. Um sowohl die Kosten der Wartung und Entwicklung niedrig zu halten als auch die Performance und Stabilität der Software zu gewährleisten, ist es besonders wichtig auf eine hohe Softwarequalität zu achten. 

## Was ist Softwarequalität

Der Begriff Softwarequalität wird meist wie folgt definiert:

>Software-Qualität ist die Gesamtheit der Merkmale und Merkmalswerte eines Softwareprodukts, die sich auf dessen Eignung beziehen, festgelegte oder vorausgesetzte Erfordernisse zu erfüllen. 

[ glossar.hs-augsburg.de]

### ISO 25010 

Die ISO 25010 definiert acht verschiedene Faktoren, die für das Erreichen qualitativer Software nötig sind.

![ISO25010](./img/iso25010.png) [ https://iso25000.com/index.php/en/iso-25000-standards/iso-25010 ] 

**Funktionalität**: Beschreibt den Grad der funktionalen Vollständigkeit, Korrektheit und Angemessenheit, also ob die Software alle geforderten Aufgaben korrekt lösen kann.

**Performance/Effizienz**: Beschreibt die Leistung im Verhältnis zu den eingesetzten Ressourcen. Dabei spielen vor allem Zeitverhalten, Ressourcennutzung (z. B. Speicher oder Rechenleistung) und die Kapazität (Höchstgrenzen der Software), unter Betrachtung der Anforderungen, eine Rolle.

**Kompatibilität**: Beschreibt den Grad in welchem Software innerhalb einer Umgebung mit anderer Software arbeiten, bzw. koexistieren kann, ohne an Effizienz zu verlieren.

**Bedienbarkeit/Benutzerfreundlichkeit**: Beschreibt wie zufriedenstellend die Benutzerschnittstelle ist. Dabei ist neben einen optisch Ansprechenden und verständliches Designs, auf einfache Erlernbarkeit der Software sowie auf Absicherung vor Benutzerfehler zu achten. Je nach Anforderungen müssen auch unterschiedliche Faktoren betrachtet werden, welche ein Barrierefreies benutzten möglich machen.

**Zuverlässigkeit**: Beschreibt den Grad in dem Software bestimmte Funktionen unter bestimmten Umständen ausführt. Dabei ist es wichtig, dass die Software ihre Aufgabe unter normalen Umständen fehlerfrei und verlässlich ausführt. Auch die Verfügbarkeit der Software und die Toleranz gegen Hardware/Software Fehlern spielt eine Rolle.

**Sicherheit**: Beschreibt wie Sicher ein System im technischen Bezug ist. Dabei ist es wichtig darauf zu achten, dass Daten nur von berechtigten Personen eingesehen werden dürfen (Vertraulichkeit, Integrität), Änderungen nachvollzogen und bewiesen werden können (Unleugbarkeit) und alle Aktivitäten sicher auf die dafür verantwortliche Person zurückverfolgt werden können (Verantwortlichkeit, Authentizität).

**Wartbarkeit**: Beschreibt wie gut ein Softwareprodukt modifiziert werden kann, um es zu verbessern, zu korrigieren oder an neue Anforderungen anzupassen. Dabei ist vor allem auf eine hohe Modularität, also die Verwendung von kleineren Modulen, zu achten. Zusätzlich ist es gut, wenn Teile der Software für andere Bereiche oder andere Projekte wiederverwendet werden können, daher flexibel und nicht statisch sind. Zu einer guter Wartbarkeit gehören auch Faktoren wie, eine hohe Testabdeckung und gute Analysierbarkeit, um Fehler bei Modifizierungen erkennen und beheben zu können.

**Übertragbarkeit**: Beschreibt wie einfach es ist, ein Softwaresystem in eine neue Umgebung zu installieren und an wechselnde Hardware oder andere, sich verändernde, Nutzungsumgebungen angepasst werden kann.  

## Technische Schulden

Leider ist es, trotz großer Bemühungen, nicht immer Möglich zu jeder Zeit auf qualitative Softwareentwicklung zu achten bzw. es können auch unwissentlich Entscheidungen getroffen werden, welche zu einer schlechteren Softwarequalität führen.
Der Begriff **technische Schulden** beschreibt die Konsequenzen die aufgrund von schlechter, technischer, Umsetzung innerhalb von Softwareprojekten entstehen. Ebenso wie wirtschaftliche Schulden müssen auch technische Schulden zurückgezahlt werden. 

Technische Schulden sind meist die Konsequenz von Entscheidung für den kurzfristigen Erfolg. 

**Technische Schulden sind nicht sichtbar und haben negativen Einfluss auf das Geschäft.**

Der Begriff technische Schulden ist von Begriffen wie *Anti-Pattern* oder *Code Smells* abzugrenzen, da diese, im Gegensatz zu technische Schulden, eine Konsequenz aus Faulheit und Unprofessionalität des Entwicklers sind.


>"In software-intensive systems, technical debt is the collection of design or implementation constructs that are expedient in the short term, but set up a technical context that can make future changes more costly or impossible. Technical debt presents an actual or contingent liability that impacts internal system qualities, primarily maintainability and evolvability."

[https://www.dagstuhl.de/en/program/calendar/semhp/?semnr=16162]




Man kann technische Schulden grob in folgende Kategorien aufteilen

- Implementationsschulden	
  - entstehen durch schlecht umgesetzten Code (siehe auch Vortrag "Clean Code") 
- Architekturschulden
  - entstehen, wenn Architekturmodelle falsch verwendet/umgesetzt werden. 
- Testschulden
  - entstehen, wenn keine, wenige und/oder mangelhafte Testabdeckung vorhanden ist.
- Dokumentationsschulden
  - entstehen, wenn die Dokumentationen nicht gepflegt werden oder gar nicht erst angefertigt werden. 



### Taxonomie

Technische Schulden lassen sich bei Bedarf auch detaillierter Klassifizieren. Folgende Taxonomie stammt aus *[An empirical assessment of technical debt practices in industry](<https://www.researchgate.net/publication/319294348_An_empirical_assessment_of_technical_debt_practices_in_industry>)* 

![Detaillierte Taxonomie von technischen Schulden](./img/tax.png)

| Types of technical | Definition |
| ---------------- | ---------- |
| Software                     | Categories of technical debt related to software |
| Requirements                 | Tradeoffs made with respect to what requirements the development team need to implement. This category can also include delayed or wrong features. |
| Architecture/ design         | Refers to software design no longer fits its intended purpose |
| Code                         | Refers to violations of design principles in production code |
| Usability                    | Refers to technical debt associated with difficult to user interfaces resulting in inconsistent or poor user experience |
| Defect                       | Refers to known defects that are not yet fixed |
| Internal                     | Refers to defect uncovered by the development team |
| External                     | Refers to defect uncovered by the customer |
| Test                         | Refers test plan is not completely carried out |
| Test cases                   | Refers to test cases being no longer relevant to the software functionality or missing |
| Automation                   | Refers to unacceptable level of test automation or technical debt in the test automation code or unoptimized existing tests |
| Coverage                     | Refers to lack of test coverage |
| Build                        | Refers to flaws in the build system or build process of a software |
| Documentation                | Refers to missing or inadequate or outdated documentation |
| Missing                      | Refers to documentation which is missing or outdated |
| Drift                        | Refers to documentation which does not reflect the functionality of the software anymore |
| Classification               | Categories of technical debt as intentional or nonintentional |
| Intentional                  | Refers to technical debt taken on voluntarily |
| Unintentional                | Refers to technical debt taken on involuntarily |
| Reckless                     | Refers to debt taken on that has an overall negative impact with time (eg, increased interest payments) |
| Prudent                      | Refers to conscious debt taken on for short term benefits based on a decision<br/>that is not sustainable in the long term |
| Organizational               | Categories of technical debt related to the organization |
| Data                         | Refers to technical debt associated with poor quality data |
| Infrastructure               | Refers to delaying an upgrade or infrastructure fix |
| People                       | Refers to lack of skills, experience in technology, tools, and techniques to build better quality software. Also known as knowledge debt. |
| Skill                        | Refers to lacking knowledge of the right solution or tool and technology to build quality software |
| Experience                   | Refers to lack of relevant experience required to achieve quality software |
| Process                 | Refers to inefficient processes related to the code development<br/>And test environment |
| Social                       | Refers to unforeseen project costs connected to a sub‐optimal development community |


### Wie entstehen technische Schulden

Für die Entstehung von technischen Schulden gibt es eine Vielzahl von Ursachen und nicht immer liegt die Schuld bei den Softwareentwicklern selbst. Oft spielen Finanzziele oder zeitliche Vorgaben von "oben" eine große Rolle in der Softwareentwicklung. Die Software soll möglichst schnell und möglichst günstig ausgeliefert werden. 

Unter Zeitdruck entstehen viele Fehler und oft werden Probleme *quick and dirty* gelöst. So werden eine menge technischer Schulden aufgenommen welche eigentlich später abbezahlt werden müssten, doch meist müssen dann schon neue Features Implementiert oder Fehler beseitigt werden, durch die eh schon hohen Schulden sinkt die Produktivität und es entsteht erneut Zeitdruck. Ein Teufelskreis.

![Kreislauf von Schulden](./img/kreislauf.png)

Aber auch das Arbeiten mit, für das Team, unbekannten Technologien, Architekturen etc. führen zu technischen Schulden, welche sich kaum vermeiden lassen.
Unverständliche, unrealistische oder sich ständig ändernde Anforderungen können auch Ursache für technische Schulden sein.

Übersicht der gängigsten Ursachen für technische Schulden: 

- Technologie
  - Technologische Limitationen
  - Legacy code
  - COTS
  - Veränderungen in Technologien
  - Projektreife
- Prozess
  - schlechte Codepflege
  - unklare Anforderungen
  - Prozess einschränken (code reviews)
  - keine Wissen über best practices
- Menschen
  - Aufschieben von Aufgaben
  - Machen von schlechte Annahmen
  - Unerfahrenheit
  - Unprofessionalität 
  - Schlechte Teamleitung/Teamdynamic
  - Kein Durchsetzungsvermögen gegenüber Kunden
  - Ego steht im Weg
  - Wisse wie Code "sicher" geändert werden kann
  - Subunternehmer
- Produkt
  - Zeit- und Gelddruck 
  - Schlechte Kommunikation zwischen Entwickler und Management
  - Ändern der Prioritäten
  - Fehlende Vision/Plan/Strategie
  - Unklare Ziele und Prioritäten
  - Versuch jeden Kunden zufriedenzustellen
  - Unklare Entscheidungen 






### Folgen von technischen Schulden
Unbezahlte Schulden erschaffen Software welche unübersichtlich und ineffizient ist. Änderungen an der Software vorzunehmen wird immer Zeit intensiver, je mehr Schulden angesammelt werden. Durch fehlende/mangelhafte Tests sind die Auswirkungen von Änderungen an der Software nicht nachvollziehbar und die Chance, dass neue Fehler entstehen steigt dramatisch.

Außerdem steigt die "Angst" der Entwickler Quellcode zu ändern, sie fangen an, um problematische Stellen herum zu programmieren, so entsteht noch mehr unübersichtlicher Code*. Durch fehlende oder veraltetet Dokumentationen ist es, selbst bei großen Bemühungen, sehr schwer, den Quellcode und die (geplante) Architektur nachvollziehen zu können, dass demotiviert und sorgt wieder für weitere Schulden. Technische Schulden verhalten sich also äquivalent zu wirtschaftlichen Schulden und vermehren sich mit der Zeit (der Zinseszins Effekt).

Unbezahlte Schulden vermehren sich so lange, bis die Software unwartbar und unprofitabel wird.

Der Graph unten zeigt wie sich Schulden mit der Zeit vermehren, wenn sie nicht abgezahlt werden (rot), Ziel sollte es sein, seine Schulden regelmäßig abzubezahlen (grün).  

 ![Verlauf von technischen Schulden](./img/schuldenverlauf.png)



### Schulden sind Zeit und Geld

Den wirtschaftlichen Schaden von technischen Schulden zu bestimmen ist sehr schwierig, über Schätzungen lassen sich Tendenzen herleiten.

Die Kosten um eine technische Schuld zu bezahlen, lassen sich von erfahrenen Entwicklern meist gut einschätzen und können ähnlich geschätzt werden wie die kosten eines neuen Features.

Die Kosten, die eine Schuld erzeugt, wenn sie nicht abbezahlt wird, lässt sich hingegen nur sehr schwer schätzen. In SCRUM Teams können Entwickler oft gut schätzen wie viel kleiner ihr Backlog wird, wenn bestimmte Schulden beseitigt sind, daraus lässt sich dann der wirtschaftliche Schaden ableiten.  

Es gibt auch weitere Ansätze die mehrere Faktoren in die Berechnung der Schätzung mit aufnehmen. Empfehlenswert ist [An Empirical Model of Technical Debt and Interest](https://www.researchgate.net/publication/228684782_An_Empirical_Model_of_Technical_Debt_and_Interest).



### Bewusste Schulden

Da sich einige Ursachen von technischen Schulden nicht vermeiden lassen, ist es wichtig mit den entstandenen Schulden verantwortungsvoll umzugehen.

Dazu ist es wichtig zwischen bewussten und unbewussten Schulden zu unterscheiden. 

|  | Rücksichtslos |Umsichtig |
|---|---|---|
|**Bewusst**|"Wir haben keine Zeit für Design!"|„Wir müssen schnell liefern und kümmern uns später um die Konsequenzen“|
|**Unbewusst**|"Was ist eine Schichtenarchitektur?"|"Jetzt wissen wir, was wir hätten tun sollen"|

In Softwareprojekten muss man Prioritäten setzten und das führt zu Aufnahme von Schulden. Man sollte aber immer versuchen alle Schulden bewusst aufzunehmen und sich über die Bedeutung und Auswirkung dieser Schuld im Klaren zu sein. Bewusste Schulden sollten mit dem Team besprochen und dokumentiert werden. Sollten unbewusste Schulden sichtbar werden, ist es wichtig sich mit den Ursachen dafür Auseinanderzusetzen um diese beim nächsten Mal zu vermeiden.

Technische Schulden können auch als Investment betrachtet werden. Eventuell lohnt sich eine Verschuldung, um sein Produkt schneller auf den Markt zu werfen, um schneller Feedback zu bekommen und Geld einzunehmen. Sollte das Produkt keinen Erfolg haben, kann man sich ggf. auch von den Schulden lösen.  

### Gute Schulden

Wie in der Finanzwelt kann es auch in der Softwareentwicklung manchmal schlau sein Schulden aufzunehmen. Dabei ist zu beachten, dass "gute Schulden" IMMER auch bewusste Schulden sind.

Vor allem, wenn das Entwicklerteam mit neuen Technologien arbeiten muss/soll oder die Komplexität des Projektes noch nicht eingeschätzt werden kann, kann es Sinnvoll sein einen "kleinen" Prototypen zu entwickeln, dessen einziger Verwendungszweck das experimentieren und ausprobieren ist und welcher am Ende bewusst verworfen wird. Man nimmt zwar am Anfang Schulden auf, da so ein Prototyp "dirty" sein kann/soll, vermindert aber durch die gesammelte Erfahrung weitere technische Schulden, wenn es um die Entwicklung der "richtigen" Software geht.

Manchmal kann das Beheben eines Fehlers zu technischen Schulden führen. Es könnte eventuell sinnvoll sein einen Fehler, und somit Schulden, bewusst in kauf zunehmen, um weitere Schulden zu vermeiden. Dabei ist natürlich zu beachten um was für eine Art von Fehler es sich handelt, wie oft er auftritt, wie "gefährlich" erst ist und wie komplex die Behebung der Lösung wäre.  



### Conceptual Model of Technical Debt

![Conceptual Model of Technical Debt](./img/cm.png)



Das *Conceptual Model of Technical Debt* gewährt eine gute Einsicht in die Zusammenhänge von technischen Schulden und den Geschäftsziele. Es stellt die bisher erläuterten Informatioen grafisch dar.  

### Schulden Managen

#### "Nicht-Informatiker" überzeugen

Um technische Schulden managen zu können, wird Zeit benötigt. In der Wirtschaft bedeutet Zeit aber auch Geld, und viele Stakeholder ohne technischen Hintergrund fehlt das Verständnis für die Bedeutung von hoher Softwarequalität, daher ist es wichtig die entscheidenden Personen überzeugen zu können.

Der Begriff *Schulden* ist in der Wirtschaft kein unbekannte und der Begriff *technische Schulden* wurde gezielt gewählt um die Kommunikation zwischen Informatiker und Manager zu erleichtern. Die meisten werden Verstehen, dass es Teilweise nötig ist Schulden aufzunehmen um dann eine verbesserte Produktion fahren zu können, ähnlich wie die Anschaffung einer neuen Maschine.

Es hilft Beispielrechnungen vorzubringen das Zeigen, dass das jetzige Handeln deutlich günstiger sein wird, als das späte Handeln. Sagt man einem Manager er könne jetzt 10.000€ investieren oder später womöglich 50.000€, kann dieser selbst eine Entscheidung treffen.

Es kann auch Hilfreich sein den Begriff "Schulden" gegen "Verschleiß" auszutauschen, da es so schwieriger ist den Entwickler vorzuwerfen etwas falsch gemacht zu haben, da verschleiß in der Industrie etwas vollkommen normales und verständliches ist an den niemand Schuld hat. 


#### Schulden vermeiden 

Schulden lassen sich durch unterschiedliche Methoden vermeiden. 

- Der Quellcode sollte Regelmäßig refactored werden
- Dokumente sollten immer auf den neusten Stand gebracht werden
- Code sollte gereviewed werden bevor er deploit wird. 
- Pair Programming hilft dabei sauberen und fehlerfreien Code zu schreiben
- Es sollte Richtlinien zum Coden geben (Namen etc.) und eingehalten werden
-  Bewusst aufgenommene Schulden sollten verstanden und dokumentiert werden
- Es sollte eine ausreichende Testabdeckung geben (Stichwort Test Driven Development)
  - Sollten im Laufe des Softwarezyklus Fehler gefunden werden, diese beheben und Tests anfertigen.

##### How to Review

- AD-Hoc Review vermeiden (Review durch spontane Gespräche)
- sollte gemacht werden aber NICHT THE WAY TO GO sein
- Review von Erfahren Entwicklern machen lassen und dafür Zeit geben
- Code regelmäßig reviewen damit die zu überprüfenden Codezeilen gering bleiben
- Review Kommentare sollen Konstruktiv sein und den Autor des Codes nicht persönlich treffen
- Bugs, Codestyle etc. über automatische Tests prüfen lassen
- 200 bis 400 Zeilen Code in 60 bis 90 Minuten
  - nach ca 60-90min Pause machen
- Checkliste erstellen
- Entwickler reviewt sich zuerst selbst
- Review Bereiche Festlegen (z.B Fokus auf Performance, Clean Code etc.)


#### Schulden erkennen

Technische Schulden zu erkennen ist gar nicht mal so einfach. Einzelne Indizien, wie die Testabdeckung lassen sich zwar recht gut erahnen, Bad-Smells oder verwaschene Architekturmuster lassen sich hingegen nur schwer erkennen. Indizien für schlecht designte Software sind unter anderem niedrige Kohäsion innerhalb von Modulen oder hohe Kopplungen zwischen Modulen oder Module/Klassen die den Großteil des Codes beinhalten.

Schulden zu finden und zu beseitigen kann sehr zeitaufwendig und kostspielig werden, da oft ein Voranschreiten ohne externe Qualitäts-Experten kaum möglich ist. Schulden lassen sich daher am besten erkennen bevor sie gemacht werden.

Es gibt einige (kostenfreie) Tools, die dabei helfen können, eine grobe Analyse der Codebase durchzuführen um zu große Klassen oder verschwommene Architekturmuster zu erkennen.  


- [Sonarqube](<https://www.sonarqube.org/>) 
- [Jdepend](<https://github.com/clarkware/jdepend>)
- [Ndepend](<https://www.ndepend.com/>)
- [Cdepend](<http://billauer.co.il/cdepend.html>)

#### Kategorisieren und Entscheiden

Es gibt verschiedene Herangehensweisen an technische Schulden. Man kann sie ignorieren (nicht empfohlen), versuchen alle Schulden zu beseitigen (aufwändig, teuer, Kampf gegen Windmühlen) oder Schulden identifizieren, bewerten und dann entscheiden, ob sie behalten werden oder abbezahlt werden. 

Da Systeme nie perfekt sind und immer verbessert werden können, sollten Schulden nur dann abbezahlt werden, wenn eine Verbesserung mehr Produktivität erzeugt als die Optimierung an Aufwand kostet.

Bill Clark von Riot Games beschreibt in einem [Blog]( <https://technology.riotgames.com/news/taxonomy-tech-debt>) Eintrag sein Vorgehen im Umgang mit technischen Schulden bei den *Champions* des Spiels *League of Legends*

Clark bewertet den **Impact**, die **Fix Kosten**, und den **Contagion** jeder Schuld auf die er stößt auf einer Scala von bis zu 5 Punkten und entscheidet dann, ob eine Schuld beglichen wird oder bewusst behalten wird. 

Hinter den Begriff Impact versteckt sich die Auswirkung des Problems, sowohl auf die Spielerfahrung (Bugs, fehlende Features etc.) als auch auf den Workflow der Entwickler.

Unter Fix Kosten versteht Clark die vermutlich auftretenden Kosten, wenn der Fehler behoben werden soll, auch unter Betrachtung der Risiken möglicher (unvorhergesehener) Komplikationen mit anderen teilen des Codes.

Der letzte, laut Clark oft vernachlässigte, Punkt ist die Frage der "Contagion" also der Ansteckung/Ausbreitung des Problems, wenn es weiter bestehen bleibt. Hat es Einfluss auf die Entwicklung neuer Features? Besteht die Gefahr das sich die Schuld durch "Copy-and-paste" weiterverbreitete?  

Bewertet man seine Schulden mit diesem Schema ergeben sich einige Entscheidungsmöglichkeiten. Schulden mit hohem Impact, niedrigen Fixkosten und hoher Verbreitungsgefahr sollten so schnell wie möglich beseitigt werden. Fehler mit niedrigem Impact und geringer Verbreitung können auch später behoben werden, da sich die Kosten wohl nicht vergrößern werden. 


#### Schulden bezahlen

Entscheidet man sich dafür eine Schuld zu bezahlen, sollte dies auch ordentlich gemacht werden. Es sollte darauf geachtet werden bei der Bezahlung keine neuen Schulden aufzunehmen. Dabei helfen die oben genannten Vorgehensweisen. 
Schulden sollten nach ihrer Dringlichkeit und ihren Schadensfaktor Priorisiert und bezahlt werden. 

##### Schulden und Legacy Code
Schulden und Legacy Code sind nochmal eine ganz neue Herausforderung.
Meist ist es nicht möglich den alten Code "mal gründlich aufzuräumen", daher sollte ab sofort versucht werden den Legacy Code Schritt für Schritt zu isolieren. Änderungen am Legacy Code sollten den Code besser zurücklassen als er vorher war.
So wird, mit genügen Zeit, der Legacy Code verschwinden bzw. zu Non-Legacy Code.

## Tldr
- Technische Schulden
	- entstehen bei "schlampiger" Umsetzung
	- lassen sich selten vermeiden
	- sind nicht nur auf Code beschränkt
	- können bewusst und unbewusst gemacht werden
	- vermehren sich
	- kosten (richtig viel) Geld
	- lassen sich durch gutes Management reduzieren   

      **Arbeitet ordentlich sonst fällt es euch auf die Füße.**


## Quellen
- [ISO25010](https://iso25000.com/index.php/en/iso-25000-standards/iso-25010)

- [Wikipedia](https://de.wikipedia.org/wiki/Technische_Schulden)

- [Technische Schulden erkennen und reduzieren](https://www.youtube.com/watch?v=aT6TGc_cGUg)

- [Technical Debt from metaphor to theory and practice](https://pkruchten.files.wordpress.com/2012/08/kruchten-120821-techdebt.pdf)

- [3 Kinds of Good Tech Debt](https://engineering.squarespace.com/blog/2019/three-kinds-of-good-tech-debt)

- [Softwareverschleiß vs technische Schulden](https://www.wps.de/aktuelles_events/blog/softwareverschleiss-vs-technische-schulden/)

- [A TAXONOMY OF TECH DEBT](https://technology.riotgames.com/news/taxonomy-tech-debt)

- [Code Cleanupt - Using Agile Techniques to Pay Back Technical Debt](https://docs.microsoft.com/en-us/archive/msdn-magazine/2009/december/code-cleanup-using-agile-techniques-to-pay-back-technical-debt)

- [Technical debt: managing code quality](https://www.kenneth-truyers.net/2016/04/13/technical-debt-managing-code-quality/)

- [5 arguments to make managers care about technical debt](https://understandlegacycode.com/blog/5-arguments-to-make-managers-care-about-technical-debt/)

- [Messen und Steuern von Softwarequalität](https://jaxenter.de/kontinuierliche-inspektion-wie-sie-interne-softwarequalitaet-objektiv-messen-und-steuern-24180)

- [Messen und verbessern von Softwarequalität](https://entwickler.de/online/agile/softwarequalitaet-so-misst-und-verbessert-man-software-114867.html)

- [Qualitätsmetriken mit VS-Code](https://www.aitgmbh.de/blog/tfsblog/qualitt-als-konzept-qualittsmetriken-in-visual-studio/)

- [Abschlussarbeit Thema: Entwicklung eines Werkzeuges zur Bestimmung von Qualitätskriterien und Metriken für sicherheitsrelevante Industriesoftware in der Hochsprache C](https://www.h-brs.de/files/informatik/maurer.pdf)

- [Die Sicht des Architekten auf Softwarequalität in Unternehmen](https://m.heise.de/developer/artikel/Die-Sicht-des-Architekten-auf-Softwarequalitaet-in-Unternehmen-3338611.html?seite=all)

- [Der Kampf gegen technische Schulden](<https://www.richard-seidl.com/kampf-gegen-technische-schulden/>)

- [Technische Schulden entstehen einfach so](<https://www.heise.de/developer/artikel/Technische-Schulden-entstehen-einfach-so-3969279.html>)

- [A Systematic Mapping Study on Technical Debt and Its Management](<https://www.researchgate.net/publication/269396520_A_Systematic_Mapping_Study_on_Technical_Debt_and_Its_Management>)

- [An empirical assessment of technical debt practices in industry](<https://www.researchgate.net/publication/319294348_An_empirical_assessment_of_technical_debt_practices_in_industry>)

- [The Future of Managin Technical Debt](<https://insights.sei.cmu.edu/sei_blog/2016/08/the-future-of-managing-technical-debt.html>)

- [An Empirical Model of Technical Debt and Interest](<https://www.researchgate.net/publication/228684782_An_Empirical_Model_of_Technical_Debt_and_Interest>)

  

