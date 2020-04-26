# Softwarequalität

André Matutat

## Motivation

Die Konzeptionierung und Entwicklung von Software ist ein komplexes Unterfangen bei denen eine Vielzahl an unterschiedlichen Faktoren und Steakholder Einfluss nehmen. Oft wird Software über Jahre hinweg eingesetzt und erweitert. Um sowohl die Kosten der Wartung und Entwicklung niedrig zu halten als auch die Performance und Stabilität der Software zu gewährleisten, ist es besonders wichtig auf eine hohe Softwarequalität zu achten. 

## Was ist Softwarequalität

Der Begriff Softwarequalität wird meist wie folgt definiert:
```
>>Software-Qualität ist die Gesamtheit der Merkmale und Merkmalswerte eines Softwareprodukts, die sich auf dessen Eignung beziehen, festgelegte oder vorausgesetzte Erfordernisse zu erfüllen.<< 
glossar.hs-augsburg.de
```
### ISO 25010 

Die ISO 25010 definiert acht verschiedene Faktoren, die für das Erreichen qualitativer Software nötig sind.

![ISO25010](/img/iso25010.png)

**Funktionalität**: Beschreibt den Grad der Funktionalen -Vollständigkeit, Korrektheit und Angemessenheit, also ob die Software alle geforderten Aufgaben korrekt lösen kann.

**Performance/Effizienz**: Beschreibt die Leistung im Verhältnis zu den eingesetzten Ressourcen. Dabei spielen vor allem Zeitverhalten, Ressourcennutzung (z. B. Speicher oder Rechenleistung) und die Kapazität (Höchstgrenzen der Software), unter Betrachtung der Anforderungen, eine Rolle.

**Kompatibilität**: Beschreibt den Grad in welchem Software innerhalb einer Umgebung mit anderer Software arbeiten bzw. koexistieren kann, ohne an Effizienz zu verlieren.

**Bedienbarkeit/Benutzerfreundlichkeit**: Beschreibt wie zufriedenstellend die Benutzerschnittstelle ist. Dabei ist neben einen optisch Ansprechenden und Verständliches Designs, auf einfache Erlernbarkeit der Software sowie auf Absicherung vor Benutzerfehler zu achten. Je nach Anforderungen müssen auch unterschiedliche Faktoren betrachtet werden, welche ein Barrierefreies benutzten möglich machen.

**Zuverlässigkeit**: Beschreibt den Grad in dem Software bestimmte Funktionen unter bestimmten Umständen ausführt. Dabei ist es wichtig, dass die Software ihre Aufgabe unter normalen Umständen fehlerfrei und verlässlich ausführt. Auch die Verfügbarkeit der Software und die Toleranz gegen Hardware/Software Fehlern spielt eine Rolle.

**Sicherheit**: Beschreibt wie Sicher ein System im technischen Bezug ist. Dabei ist es wichtig darauf zu achten, dass Daten nur von berechtigten Personen eingesehen werden dürfen (Vertraulichkeit, Integrität),  Änderungen nachvollzogen und bewiesen werden können (Unleugbarkeit) und alle Aktivitäten sicher auf die dafür verantwortliche Person zurückverfolgt werden können (Verantwortlichkeit, Authentizität).

**Wartbarkeit**: Beschreibt wie gut ein Softwareprodukt modifiziert werden kann, um es zu verbessern, zu korrigieren oder an neue Anforderungen anzupassen. Dabei ist vor allem auf eine hohe Modularität, also die Verwendung von kleineren Modulen, zu achten. Zusätzlich ist es gut, wenn Teile der Software für andere Bereiche oder andere Projekte wiederverwendet werden können, daher flexibel und nicht statisch sind. Zu einer guter Wartbarkeit gehören auch Faktoren wie, eine hohe Testabdeckung und gute Analysierbarkeit, um Fehler bei Modifizierungen erkennen und beheben zu können.

**Übertragbarkeit**: Beschreibt wie einfach es ist, ein Softwaresystem in eine neue Umgebung zu installieren und an wechselnde Hardware oder andere, sich verändernde, Nutzungsumgebungen angepasst werden kann. 

## Technische Schulden

Leider ist es, trotz großer Bemühungen, nicht immer Möglich zu jeder Zeit auf qualitative Softwareentwicklung zu achten bzw. es können auch unwissentlich Entscheidungen getroffen werden, welche zu einer schlechteren Softwarequalität führen.
Der Begriff **technische Schulden** beschreibt die Konsequenzen die aufgrund von schlechter, technischer, Umsetzung innerhalb von Softwareprojekten entstehen. Der Begriff technische Schulden ist von Begriffen wie *Anti-Pattern* oder *Code Smells* abzugrenzen, da diese, im Gegensatz zu technische Schulden, eine Konsequenz aus Faulheit und Unprofessionalität des Entwicklers sind.

Man kann Schulden grob in folgende Kategorien aufteilen

- Implementationsschulden	
  - entstehen durch schlecht umgesetzten Code (siehe auch Vortrag "Clean Code") 
- Architekturschulden
  - entstehen, wenn Architekturmodelle falsch verwendet/umgesetzt werden. 
- Testschulden
  - entstehen, wenn keine, wenige und/oder mangelhafte Testabdeckung vorhanden ist.
- Dokumentationsschulden
  - entstehen, wenn die Dokumentationen nicht gepflegt werden oder gar nicht erst angefertigt werden. 

### Folgen von technischen Schulden

Technische Schulden sorgen, wenn sie nicht abbezahlt werden, dafür das Modifizierungen an Software nur langsam und kostspielig umgesetzt werden können. Auch gibt es sowas wie den "Zinses Zins" Effekt: je länger technische Schulden bestehen, desto höher steigt die Anzahl der Schulden, wenn neue Features oder Bugfixes in die Software implementiert werden. Auf Dauer führen technische Schulden zu Softwareerosion bis hin zu kompletten Ausfall von Software und vollständiger Unwirtschaftlichkeit.

Der Graph unten zeigt wie sich Schulden mit der Zeit vermehren, wenn sie nicht abgezahlt werden (rot), Ziel sollte es sein, seine Schulden regelmäßig abzubezahlen (grün).  

 ![Verlauf von technischen Schulden](/img/schuldenverlauf.PNG)

### Wie enstehen technische Schulden

Für die Entstehung von technischen Schulden gibt es eine Vielzahl von Ursachen und nicht immer liegt die Schuld bei den Softwareentwicklern selbst. Oft spielen Finanzziele oder zeitliche Vorgaben von "oben" eine große Rolle in der Softwareentwicklung. Die Software soll möglichst schnell und möglichst günstig ausgeliefert werden. 

Unter Zeitdruck entstehen viele Fehler und oft werden Probleme "quick and dirty" gelöst. So werden eine menge technischer Schulden aufgenommen welche eigentlich später abbezahlt werden müssten, doch meist müssen dann schon neue Features Implementiert oder Fehler beseitigt werden, durch die eh schon hohen Schulden sinkt die Produktivität und es entsteht erneut Zeitdruck. Ein Teufelskreis.

![Kreislauf von Schulden](/img/kreislauf.PNG)

Aber auch das Arbeiten mit, für das Team, unbekannten Technologien, Architekturen etc. führen zu technischen Schulden, welche sich kaum vermeiden lassen.
Unverständliche, unrealistische oder sich ständig ändernde Anforderungen können auch Ursache für technische Schulden sein. Folgende Abbildung zeigt einige Ursachen für technische Schulden.

 ![Cause of Technical Debt ](/img/ursachen.PNG)

### Bewusste Schulden

Da sich einige Ursachen von technischen Schulden nicht vermeiden lassen, ist es wichtig mit den entstandenen Schulden verantwortungsvoll umzugehen.

Dazu ist es wichtig zwischen bewussten und unbewussten Schulden zu unterscheiden. 

|  | Rücksichtslos |Umsichtig |
|---|---|---|
|**Bewusst**|"Wir haben keine Zeit für Design!"|„Wir müssen schnell liefern und kümmern uns später um die Konsequenzen“|
|**Unbewusst**|"Was ist eine Schichtenarchitektur?"|"Jetzt wissen wir, was wir hätten tun sollen"|

In Softwareprojekten muss man Prioritäten setzten und das führt zu Aufnahme von Schulden. Man sollte aber immer versuchen alle Schulden bewusst aufzunehmen und sich über die Bedeutung und Auswirkung dieser Schuld im Klaren zu sein. Bewusste Schulden sollten mit dem Team besprochen und dokumentiert werden. Sollten unbewusste Schulden sichtbar werden, ist es wichtig sich mit den Ursachen dafür Auseinanderzusetzen um diese beim nächsten Mal zu vermeiden.

### Gute Schulden

Wie in der Finanzwelt kann es auch in der Softwareentwicklung manchmal schlau sein Schulden aufzunehmen. Dabei ist zu beachten das "gute Schulden" IMMER auch bewusste Schulden sind.

Vor allem, wenn das Entwicklerteam mit neuen Technologien arbeiten muss/soll oder die Komplexität des Projektes noch nicht eingeschätzt werden kann, kann es Sinnvoll sein einen "kleinen" Prototypen zu entwickeln, dessen einziger Verwendungszweck das experimentieren und ausprobieren ist und welcher am Ende bewusst verworfen wird. Man nimmt zwar am Anfang Schulden auf, da so ein Prototyp "dirty" sein kann/soll, vermindert aber durch die gesammelte Erfahrung weitere technische Schulden, wenn es um die Entwicklung der "richtigen" Software geht.

Manchmal kann das Beheben eines Fehlers zu technischen Schulden führen. Es könnte eventuell sinnvoll sein einen Fehler, und somit Schulden, bewusst in kauf zunehmen, um weitere Schulden zu vermeiden. Dabei ist natürlich zu beachten um was für eine Art von Fehler es sich handelt, wie oft er auftritt, wie "gefährlich" erst ist und wie komplex die Behebung der Lösung wäre.  

### Schulden erkennen

Technische Schulden zu erkennen ist gar nicht mal so einfach. Einzelne Indizien, wie die Testabdeckung lassen sich zwar recht gut erahnen, Bad-Smells oder verwaschene Architekturmuster lassen sich hingegen nur schwer erkennen. Indizien für schlecht Designte Software sind unter anderen niedrige Kohäsion innerhalb von Modulen oder hohe Kopplungen zwischen Modulen oder Module/Klassen die den Großteil des Codes beinhalten.

Schulden zu finden und zu beseitigen kann sehr zeitaufwendig und Kostspielig werden, da oft ein Voranschreiten ohne externe Qualitäts-Experten kaum möglich ist. Schulden lassen sich daher am besten erkennen bevor sie gemacht werden.

Es gibt einige kostenfreie Tools, die dabei helfen können, eine grobe Analyse der Codebase durchzuführen um zu große Klassen oder verschwommene Architekturmuster zu erkennen.  

- [Sonarqube](<https://www.sonarqube.org/>) 
- [Jdepend](<https://github.com/clarkware/jdepend>)
- [Ndepend](<https://www.ndepend.com/>)
- [Cdepend](<http://billauer.co.il/cdepend.html>)

### Kategorisieren und Entscheiden

Es gibt verschiedene Herangehensweisen an technische Schulden. Man kann sie ignorieren (nicht empfohlen), versuchen alle Schulden zu beseitigen (aufwändig, teuer, Kampf gegen Windmühlen) oder Schulden identifizieren, bewerten und dann entscheiden, ob sie behalten werden oder abbezahlt werden.

Bill Clark von Riot Games beschreibt in einem [Blog]( <https://technology.riotgames.com/news/taxonomy-tech-debt>) Eintrag sein vorgehen im Umgang mit technischen Schulden bei den *Champions* des Spiels *League of Legends*

Clark bewertet den **Impact**, die **Fix Kosten**, und den **Contagion** jeder Schuld auf die er stößt auf einer Scala von bis zu 5 Punkten und entscheidet dann, ob eine Schuld beglichen wird oder bewusst behalten wird. 

Hinter den Begriff Impact versteckt sich die Auswirkung des Problems, sowohl auf die Spielerfahrung (Bugs, fehlende Features etc.) als auch auf den Workflow der Entwickler.

Unter Fix Kosten versteht Clark die vermutlich auftretenden Kosten, wenn der Fehler behoben werden soll auch unter Betrachtung der Risiken möglicher (unvorhergesehener) Komplikationen mit anderen teilen des Codes.

Der letzte, laut Clark oft vernachlässigte, Punkt ist die Frage der "Contagion" also der Ansteckung/Ausbreitung des Problems, wenn es weiter bestehen bleibt. Hat es Einfluss auf die Entwicklung neuer Features? Besteht die Gefahr das sich die Schuld durch "Copy-and-paste" weiterverbreitete?  

Bewertet man seine Schulden mit diesem Schema ergeben sich einige Entscheidungsmöglichkeiten. Schulden mit hohem Impact, niedrigen Fixkosten und hoher Verbreitungsgefahr sollten so schnell wie möglich beseitigt werden. Fehler mit niedrigem Impact und geringer Verbreitung können auch später behoben werden, da sich die Kosten wohl nicht vergrößern werden.

Clark gibt auch ein Beispiel, indem er sich die Verbreitungsgefahr zum Vorteil nimmt. Das Team von Riot Games hat eine eigene Implementation der String Klasse von C++ entwickelt, welche deutlich Speicher sparender ist und zusätzlich einfacher zu verwenden ist. Durch "Copy-and-paste" soll sich die eigens Entwickelte Implementation langsam über das gesamte Projekt verteilen.  

## Wie lassen sich technische Schulden managen?

Schulden lassen sich durch unterschiedliche Methoden vermeiden und abbauen. 

- Der Quellcode sollte Regelmäßig refactored werden
- Dokumente sollten immer auf den neusten Stand gebracht werden
- Code sollte gereviewed werden bevor er deploit wird. 
- Paar Programming hilft dabei sauberen und Fehlerfreien Code zu schreiben
- Es sollte Richtlinien zum Coden geben (Namen etc.) und eingehalten werden
-  Bewusst aufgenommene Schulden sollten verstanden und dokumentiert werden
- Es sollte einige ausreichende Testabdeckung geben (Stichwort Test Driven Development)
  - Sollten im Laufe des Softwarezyklus Fehler gefunden werden, diese beheben und Tests anfertigen.

So lassen sich bereits viele Schulden im Vorfeld verhindern.  

## "Nicht-Informatiker" überzeugen

Um technische Schulden managen zu können, wird Zeit benötigt. In der Wirtschaft bedeutet Zeit aber auch Geld, und viele Steakholder ohne technischen Hintergrund fehlt das Verständnis für die Bedeutung von hoher Softwarequalität, daher ist es wichtig die entscheidenden Personen überzeugen zu können.

Der Begriff *Schulden* ist in der Wirtschaft kein unbekannte und der Begriff *technische Schulden* wurde gezielt gewählt um die Kommunikation zwischen Informatiker und Manager zu erleichtern. Die meisten werden Verstehen, dass es Teilweise nötig ist Schulden aufzunehmen um dann eine verbesserte Produktion fahren zu können, ähnlich wie die Anschaffung einer neuen Maschine.

Es hilft Beispielrechnungen vorzubringen das Zeigen, dass das jetzige Handeln deutlich günstiger sein wird, als das späte Handeln. Sagt man einem Manager jetzt 10.000€ investieren oder später womöglich 50.000€, kann dieser selbst eine Entscheidung treffen.

Es kann auch Hilfreich sein den Begriff "Schulden" gegen "Verschleiß" auszutauschen, da es so schwieriger ist den Entwickler vorzuwerfen etwas falsch gemacht zu haben, da verschleiß in der Industrie etwas vollkommen normales und verständliches ist an den niemand Schuld hat.  


## TlDr

Ziel jedes Softwareprojektes sollte es sein, ein möglichst Qualitativ hochwertiges Produkt anzufertigen. Dazu sollten die Faktoren Funktionalität, Effizienz, Wartbarkeit, Benutzerfreundlichkeit, Übertragbarkeit, Sicherheit, Zuverlässigkeit und Kompatibilität beachtet werden. Durch die teilweise hohe Anforderungen, komplexe Projekte oder unerfahrene Entwickler werden im Laufe des Entwicklungsprozesses technische Schulden aufgenommen. Wichtig ist technische Schulden zu erkennen, zu bewerten und entsprechende Handlungen in die Wege zuleiten. Manchmal kann es Sinnvoll sein, kurzfristig Schulden aufzunehmen und diese später abzuzahlen um größere Schulden zu vermeiden. Schulden sollten immer bewusst und umsichtig gemacht werden. Technische Schulden im Nachhinein zu erkennen und zu beheben kann Zeit- und kostspielig sein.

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
