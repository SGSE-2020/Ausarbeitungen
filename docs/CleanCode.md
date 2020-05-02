# Clean Code

## Einleitung
Bei Clean Code handelt es sich um eine Reihe Richtlinien und Prinzipien, welche von allen Softwareentwicklern beachtet werden sollten.
Diese Prinzipien und auch der Name entstammen dem Buch "Clean Code" von Robert C. Martin. 
Dieses Buch enthält eine Menge von Best Practices, Prinzipien und Praktiken, welche zu "Clean Code" führen.

Die folgeden Kapitel werden zunächst auf die Clean Code Developer Bewegung eingehen, welche 
die Clean Code Richtlinien so weit ausbreiten wollen, wie möglich, das SOLID Prinzip, 

## Clean Code Developer Bewegung

Die Clean Code Developer Bewegung macht sich stark dafür, dass so viele Entwickler wie möglich die Clean Code Prinzipien
von Robert C. Marting einhalten. Dadurch soll die Allgemeine Code Qualität enorm angehoben werden, was die Software 
Entwicklung professioneller machen soll.  

### Wertesystem

Die Clean Code Developer Bewegung (CCD) orientiert sich an einem Wertesystem, welches vier Punkte umfasst.
- Wandelbarkeit
- Korrektheit
- Produktionseffizienz
- Kontinuierliche Verbesserung

#### Wandelbarkeit

Der CCD ist der Auffassung, das Wartung, wie sie bei Maschinen möglich ist, bei Software nicht möglich ist. Dies liegt
daran, dass es bei Software keinen Verschleiß gibt, Software bleibt immer so, wie sie zu Beginn war. Wenn Software 
gewartet wird, bedeutet das immer eine Änderung der Software, ob es sich nun um Erweiterungen oder Fehlerbehebungen
handelt spielt dabei keine Rolle.  
Deshalb sollte Software eine innere Struktur haben, die solche Änderungen einfach macht. Andernfalls wächst Software
über den langen Zeitraum des Betriebs so stark an, dass ein Überblick über die Software nahezu unmöglich wird. Dies
erschwert die Implementation von Änderungen enorm, was letzten Endes zu erhöhten Kosten führt.  
Um eine hohe Wandelbarkeit zu erzielen muss Software von Beginn an mit diesen Aspekten entwickelt werden. So soll
zum Beispiel die Kopplung zwischen Klassen gering gehalten werden, sodass eine Änderung an einer Klasse nicht unzählige
unerwartete Auswirkungen auf andere Klassen hat.

#### Korrektheit

Zur Korrektheit gehört nach CCD zunächst die korrekte Ausführung der gewünschtren Funktionalität. Aber es ist außerdem
wichtig für korrekte Software, dass die Software schonend mit Ressourcen, wie Speicher und Prozessorzeit umgeht, und 
Antwortzeiten in einem definierten Rahmen liegen.  
Um diese Korrektheit zu errecihen müssen neben automatiesierten Tests für alle Komponenten der Software auch genaue 
Anforderungen formuliert werden. So kann eine Komponente der Software als inkorrekt befunden werden, sobald sie 
die festgelegten Anforderungen nicht mehr einhält. 

#### Produktionseffizienz

Das Ziel der Produktionseffizienz ist es, die Entwicklungszeit und somit den Preis einer Software möglichst gering zu
halten. Diese wird vorallem durch Automatisierung und gute Strukturierung erzielt, sodass Software über lange Zeit 
weiterentwickelt werden kann, ohne dass an einem gewissen Punkt von vorne angefangen werden muss.  
Ein andere Nebeneffekt der Produtionseffizienz ist es, dass die anderen Werte in Schach gehalten werden, damit nicht
ein unverhältnismäßiger Aufwand betrieben werden muss, um zum Beispiel die Korrektheit umzusetzen.

#### Kontinuierliche Verbesserung

Unter kontinuierlicher Verbesserung versteht der CCD, dass nach jeder Entwicklung reflektiert wird, ob der gewählte Weg
gut war, oder ob es Probleme gab. Dadurch können zukünftige Entwicklungen basierend auf gemachten Erfahrungen geplant 
werden, und gemachte Fehler behoben werden.  
Um Kontinuierliche Verbesserung umzusetzen empfiehlt der CCD, dass Pair Porgramming, Code Reviews, tägliche Reflektionsmeetings
mit dem ganzen Team und ähnliches durchgeführt werden um zum Entwicklungsalltag gehören.

### Grade

Die CCD ist der Meinung, dass es Zeit und Übung benötigt das Wertesystem und alle Regeln und Prinzipien zu verinnerlichen,
deshalb wurden verschiedene Entwicklungsstufen bestimmten Graden zugeordnet.
So beginnt ein Entwickler beispielsweise bei dem schwarzen Grad, und arbeitet sich währrend der Entwicklung bis zum 
weißen Grad hoch. Um Kollegen in einem Projekt zu verdeutlichen, bei welchem Grad man sich aktuell befindet, können
Armbänder mit den verschiedenen Farben verwendet werden.

#### Schwarzer Grad

Der schwarze Grad signalisiert, dass man sich zwar für den CCD interessiert, aber noch nicht alle Vorraussetzungen für 
den nächsten Grad erfüllt hat.

#### Roter Grad

Der rote Grad stellt den Beginn zum CCD dar und umfasst daher nur unverzichtbare Elemente des CCD-Wertesystems.
So soll der rote Grad eher eine fundamentale Haltung zur Softwareentwicklung aufbauen, anstatt viele 
Softwareentwicklungsprinzipien zu enthalten.

#### Oranger Grad

Mit dem orangen Grad beginnt die Anwendung der fundamentalen Prinzipien auf den Code. Das Hauptthema des Grades ist die 
Automatiserung von Abläufen, um die Produktivität zu erhöhen. Hauptsächlich soll die Korrektheitsprüfung des Codes
automatisiert werden, zum Beispiel mit Integrationstests.

#### Gelber Grad

Der gelbe Grad behandelt hauptsächlich das Thema automatisierte Tests. Hierbei soll ermöglicht werden, dass jede 
Komponente einzeln untersucht und getestet werden kann. Dazu müssen unter anderem Prinzipien der objektorientierten
Programmierung angewendet werden. 

#### Grüner Grad

Auch der grüne Grad handelt weiterhin um die Automatisierung. Vorallem sollen Übersetzungen automatisiert werden, 
sodass Programme sich nicht nur fehlerfrei am Entwickler PC ausführen lassen, sondern auch an beliebigen anderen 
Systemen.  

#### Blauer Grad

Der blaue Grad ist der letzte, welcher sich mit der Automatisierung beschäftigt. In diesem Fall soll das Deployment
automatisiert werden. Um gute Vorrausseetzungen für diese Automatiserung zu schaffen, wird auch die Architektur und 
Strukturierung des Projekts betrachtet. 

#### Weißer Grad

Der weiße Grad führt alle vorhergegangen Grade, mit all deren Prinzipien und Praktiken zusammen. Der weiße Grad kann daher
nur von erfahrenen CCDs erreicht werden, da das komplette Wertesystem im Auge gehalten werden muss.

## SOLID
SOLID ist eine Abkürzung für fünf grundlegende Prinzipien, welche für jede Objektorientierte Software umgesetzt sein sollten.  
Das Akronym SOLID setzt sich zusammen aus:
- **S**ingle Responsibility Principle
- **O**pen Closed Principle
- **L**iskov Substitution Principle
- **I**nterface Segregation Principle
- **D**ependency Inversion Priciple

Diese Prinzipien werden in den folgenden Unterkapiteln nun genauer beschrieben und erklärt.

### Single Responsibility Principle
Das Single Responsibility Principle, kurz SRP, beschreibt das Prinzip, das jede Klasse genau eine 
Verantwortlichkeit hat. Das Ziel des Prinzips ist es bei Änderungen oder Erweiterungen der Funktionalität
so wenige Klassen wie möglich ändern zu müssen, da so unvorhersehbare Fehler an anderen Stellen des Projekts 
unwahrscheinlicher werden.  
Eine Verletzung des Prinzips führt zu höherer Kopplung und draus resultierend höhere 
Komplexität, was es schwieriger macht den Code nachvollziehen zu können. SRP ist Teil des orangenen Grades.

### Open Closed Principle
Das Open Closed Principle, OCP, gehört zum grünen Grad und verlangt, das Klassen offen für Erweiterungen sind, aber geschlossen gegenüber Modifikation.
Durch dieses Prinzip soll gewährleistet werden, dass funktionierende Funktionalitäten nicht durch hinzufügen neuer 
Funktionalitäten beschädigt werden.  
Das folgende Beispiel zeigt, wie das Open-Closed Prinzip angewendet werden kann:
  
    public double Preis() {
        const decimal StammkundenRabatt = 0.95m;`  
        switch(kundenart) {  
            case Kundenart.Einmalkunde:  
                return menge * einzelpreis;  
            case Kundenart.Stammkunde:  
                return menge * einzelpreis * StammkundenRabatt;  
            default:  
                throw new ArgumentOutOfRangeException();  
        }  
    }
    
Um eine neue Art der Preisberechnung hinzuzufügen muss die bereits verwendete Funktion modifiziert werden. Um solche
Modifikationen, welche die Funktionsweise unerwartet beeinflussen könnten, zu verhindern, können Strategien wie das 
Strategy Pattern verwendet werden.

    public interface IPreisRechner {
        double Preis(int menge, double einzelpreis);
    }
    
    private IPreisRechner preisRechner;
    
    public double Preis() {
        return preisRechner.Preis(menge, einzelpreis);
    }
    
    public class Einmalkunde : IPreisRechner {
        public double Preis(int menge, double einzelpreis) {
            return menge * einzelpreis;
        }
    }
    
    public class Stammkunde : IPreisRechner {
        const decimal StammkundenRabatt = 0.95m;
        
        public double Preis(int menge, double einzelpreis) {
            return menge * einzelpreis * StammkundenRabatt;
        }
    }
    
Durch Anwendung des Strategy Patterns können weitere Preisrechner implementiert werden, ohne bereits existierende zu 
verändern. Dadurch bleibt die Klasse erweiterbar, aber ist gleichzeitig gegen Modifikationen abgesichert.

### Liskov Substitution Principle

Das Liskov Substitution Priciple (LSP), besagt, dass sich Subtypen so verhalten müssen wie die Basistypen von denen sie
erben. Eine gute Merkregel hierbei ist, dass Subtypen die Funktionalität nur erweitern dürfen, aber nicht einschränken.  
LSP ist Bestandteil des gelben Grades.

### Interface Segregation Principle

Bei dem Interface Segregation Principle (ISP), welches ebenfalls zum gelben Grad gehört, geht es um die Abtrennung von 
Interfaces. So ist es für einen Client nicht notwendig alle Details eines Services zu wissen, sondern nur die für den 
CLient relevanten. Wird das Prinzip befolgt, wird die Kopplung zwischen Koponenten geringer, was zu einfachere Wartung 
und Erweiterbarkeit führt. 

### Dependency Inversion Priciple

Das letzte Prinzip von SOLID, das Depndency Inversion Principle (DIP) setzt vorraus, dass High-Level Klassen nicht von Low-Level Klassen abhängig sein 
sollen, sondern beide von Interfaces. Außerdem sollen Interfaces nicht von Details abhängig sein, sondern von Details von
anderen Interfaces. Wird dieses Prinzip befolgt ist die Kopplung zwischen Klassen geringer und es ist einfacher einzelne
Komponenten zu testen. Diese Eigenschaften machen DIP auch Teil des gelben Grades.

## Dirty Code Beispiele

Bei "Dirty Code" handelt es sich um Code, welcher eine Menge "Bad Smells" beinhält. Bei Bad Smells handelt es sich um 
Probleme, welche nicht die Funktionalität von Code einschränken, aber machen das Verstehen, Arbeiten und Überprüfen 
von Implementierten Code schwierig bis unmöglich. 
Dirty Code ist des weiteren oftmals schlecht optimiert, und könnte um einiges Ressourcen schonender sein oder schneller Antwortzeiten haben.
Zu den Klassikern unter den Bad Smells zählen zum Beispiel:
- Konformitätsbrüche
- Schlechte Namensgebung
- Toter Code
- Magie in Code
- Code-Verdopplung
- Fehlende Tests
- Fehlende Kommentare
- Fehlendes Logging
- Schlechte Fehlerbehandlung
- Workarounds anstatt Behebungen
- Halbfertige Refactorings
- Zu komplizierte Implementierung
- Aufgeblasene Klassen und Methoden
- Zu tiefe Verschachtelung
- Spaghetti-Code  
Clean Code versucht diese Probleme systematisch zu eliminieren, was je nach Bad Smell einen verschieden hohen Aufwand erfordert.

## Maßnahmen

Außerhalb der bereits vorgestellten Prinzipien von SOLID beinhält jeder Grad, außer der schwarze, eine Menge an weiteren Prinzipien
und Praktiken, welche das jeweilige Ziel des Grades erfüllen. Die folgenden Unterkapitel erläutern welche der
wichtigsten und bekanntesten dieser Techniken.

### Don't Repeat Yourself (DRY)

### Keep It Simple, Stupid (KISS)

### Die Pfadfinderregel


### Single Level of Abstraction (SLA)


### Tell, Don't Ask

### Law Of Demeter

### You Ain't Gonna Need It (YAGNI)

## Prinzipielle Tugenden

Die grundlegenden prinzipiellen Tugenden von Clean Code werden in fünf Hauptpunkte eingeteilt. Um diese Hauptpunkte umzusetzen können 
verschiedene Prinzipien der verschiedenen Grade umgesetzt werden.  
Die fünf Hauptprinzipien sind:
- Schätze Variation (Value Variation (VV))
- Tue nur das Nötigste (Do Only What's Necessary (DOWN))
- Isoliere Aspekte (Isolate Aspects (IA))
- Minimiere Abhängigkeiten (Minimize Dependencies (MD))
- Halte Versprechen ein (Honor Pledges (HP))  

Jeder dieser Punkte setzt einen oder mehrere der Werte von Clean Code um. Die folgenden Unterkapitel gehen nun auf die
Hauptpunkte, die Werte die umgesetzt werden und die dazugehörigen Prinzipien ein.

### Value Variation

Das Ziel von Value Variation ist es der Standardisierung und Vereinheitlichung entgegen zu wirken. Es soll erlaubt sein
auch alternative Lösungswege auszuprobieren, da dadurch bessere Lösungen gefunden werden können. Die Werte die durch
VV umgesetzt werden sind daher auch die Evolvierbarkeit und die kontinuierliche Verbesserung.

### Do Only What's Necessary

Wie der Name schon vermuten lässt, ist das Ziel von DOWN, dass nur implementiert wird, was auch tatsächlich gebraucht wird.
Wird dies umgesetzt wird sowohl die Produktionseffizienz erhöht, da keine Zeit mit unnötigen Komponenten verschwendet wird,
als auch die Evolvierbarkeit verbessert.    
Zu Prinzipien, welche diese Tugend umsetzen, gehören:
- Vorsicht vor Optimierungen
- You Ain't Gonna Need It (YAGNI)
- Keep It Simple, Stupid (KISS)

### Isolate Aspects

Diese Tugend sagt aus, dass man Aspekte eines Projekts isoliert betrachten soll. Dadurch wird die Evolvierbarkeit erhöht,
da es einfacher ist einzelne Komponenten weiter zu entwickeln, anstatt mehrere auf einmal.  
Zu dieser Tugend gehören folgende Prinzipien:
- Don't Repeat Yourself (DRY)
- Seperation of Concerns (SoC)
- Single Level of Abstraction (SLA)
- Single Responsibility Principle (SRP)
- Interface Segregation Principle (ISP)
- Entwurf und Implementation überlappen nicht
. Integration Operation Segregation Principle (IOSP)


### Minimize Dependencies

Das Ziel dieser Tugend ist es, eine möglichst geringe Kopplung der verschiedenen Komponenten zu erhalten. Dies steigert 
die Evolvierbarkeit, da Änderungen an einer Komponente nicht so viele Änderungen an anderen Komponenten nach sich ziehen.  
Prinzipien, um dies umzusetzen, sind:
- Dependency Inversion Principle
- Information Hiding Principle
- Law of Demeter
- Open CLosed Principle
- Tell don't ask
- Interface Segregation Principle (ISP)
. Integration Operation Segregation Principle (IOSP)

### Honor Pledges

Bei der Honor Pledges, oder auch Minimize Surprises, Tugend geht es darum, dass sich Implementierte Funktionalitäten so 
verhalten, wie vorher geplant. Dadurch werden natürlich auch unerwartete Überraschungen minimiert, was den alternativen 
Namen der Tugend abbildet. Hält mich an sich an diese Tugend wird die Evolvierbarkeit erhöht, da selbst wenn der Entwickler
an einer Funktionalität sich ändert, dieser schnell verstehen sollte, was bereits umgesetzt ist und dann Erweiterungen
vornehmen kann.  
Zu dieser Tugend zählne folgende Prinzipien:
- Liskov Substitution Principle
- Principle of Least Astonishment
- Implementation spiegelt Entwurf
- Favour Composition over Inheritance (FCoI)


## Praktische Tugenden

Praktische Tugenden beschreiben im Gegensatz zu Prinzipiellen Tugenden auf welche Art die Entwicklung umgesetzt werden soll,
anstatt Regeln für diese vorzuschreiben. Auch hier wurden Hauptpunkte beschrieben, an welche man sich halten soll, um einen
oder mehrere der Werte umzusetzen.  
Bei diesen sechs Hauptpunkten handelt es sich um:  
- Umarme Unsicherheit (Embrace Uncertainty (EC))
- Fokussiere (Focus (F))
- Wertschätze Qualität (Value Quality (VQ))
- Mach fertig (Get Things Done (GTD))
- Halte Ordnung (Stay Clean (SC))
- Bleib am Ball (Keep Moving (KM))

### Embrace Uncertainty

Diese Tugend beschreibt, dass es gut ist, wenn man sich unsicher ist, da durch diese Unsicherheit erreicht wird, das 
getestet wird. Durch dieses testen wird die Evolvierbarkeit erhöht, da ideallerweise bei jeder Änderungen nachvollzogen 
werden kann, ob andere Teile durch diese nicht mehr funktionieren, und sie führt zu Kontinuierlicher Verbesserung, da 
Fehler schneller auffallen und behoben werden können.  
Praktiken, welche umzusetzen sind um dies zu erreichen wären:
- Ein Versionskontrollsystem verwenden
- Automatisierte Integrationstests
- Automatisierte Unit Tests
- Mockups
- Continous Integration
- Inversion of Control Container

### Focus

Das Ziel dieser Tugend ist es, dass sich immer nur auf eine Sache konzentriert wird, und nicht mehrere Teile gleichzeitig 
entwickelt werden. Dies erhöht die Produktionseffizienz, da neue Features schneller abgeschlossen werden.  
Anwendbare Praktiken hierzu sind:
- Komponentenorientierung
- Test first
- Limit WIP
  
### Value Quality

Diese Tugend soll verhindern, dass mit Spaghetti Code oder halbfertigen Komponenten weitergearbeitet wird. Obwohl dies 
zunächst mehr Aufwand nach sich zieht wird trotzdem die Produktionseffizienz erhöht, da Code mit hoher Qualität sich besser 
weiterentwickeln und warten lässt.  
Praktiken dazu sind:
- Akzeptiere nur hohe Qualität
- Automatisierte Unit Tests
- Reviews

### Get Things Done

Bei dieser Tugend soll erreicht werden, dass neue Features oder ähnliches fertiggestellt werden, bevor andere begonnen 
werden. Dies erhöht die Produktionseffizienz, da häufiger neue Versionen erstellt werden können, welche dann ausgeliefert werden können.
Um diese Tugend zu erfüllen sollten folgende Praktiken beachtet werden:
- Iterative Entwicklung
- Continous Delivery
- Limit WIP

### Stay Clean

Diese Tugend sagt vermutlich dass aus, was der unerfahrene Entwickler sich unter Clean Code vorstellt. Hier geht es hauptsächlich
darum den Code ordentlich zu halten, sodass man selber und andere einfacher mit diesem arbeiten können. Dies führt 
zu erhöhter Korrektheit, Evolvierbarkeit und Produktionseffizienz.  
Um die Ordnung halten zu können werden folgende Praktiken empfohlen:
- Die Pfadfinderregel beachten
- Komplexe Refaktorisierungen
- Einfache Refaktorisierungsmuster anwenden
- Statische Codeanalyse
- Code Coverage Analyse
- Source Code Konventionen

### Keep Moving

Diese Tugend sagt aus, dass egal wie erfahren jemand ist, oder wie gut jemand die Clean Code Prinzipien und Praktikten umsetzt,
es immer Möglichkeiten zur Verbesserung gibt. Es werden immer neue und bessere Methoden entwickelt, die es zu erlernen gilt
um den best möglichen Code zu schreiben. Wenn man diese Tugend einhält, führt dies logischerweise zu kontinuierlicher
Verbesserung.  
Praktiken, um dies zu erreichen sind:
- Eigene Weiterbildung durch das Lesen neuer Entwicklungen
- Teilnahme an Fachveranstaltungen
- Erfahrungen weitergeben
- Täglich Reflektieren
- Root Cause Analysis
- Messen von Fehlern
- Issue Tracking
- Regelmäßige Retrospektiven

## Clean Code Controlling

## Vorteile und Ziele von Clean Code

## Nachteile von Clean Code
Um erfolgreich alle Aspekte von Clean Code durchführen zu können, ist ein hoher Aufwand nötig. Zunächst
muss sich jeder Mitarbeiter in das Thema einarbeiten, und dann die je nach aktuellen Grad verlangten Prinzipien umsetzten.
Außerdem ist es notwendig, durch Code Reviews, Pair Programming oder andere Methoden zu kontrollieren, ob die Prinzipien
korrekt umgesetzt wurden. Dieses enorme Zeitinvestment könnte natürlich dafür verwendet werden neue Features zu entwickeln.
Allerdings ist diese Betrachtungsweise sehr kurzsichtig, da unaufgeräumte Software einen Punkt erreicht, an dem die Implementation
neuer Features, durch die schlechte Struktur des Projekts, so aufwändig ist, dass es besser gewesen wäre von vornerein die Clean Code
Prinzipien umzusetzen.

## Quellen
[Clean Code Developer](!https://clean-code-developer.de/)  
[Vortrag zu Clean Code](!https://gi.de/fileadmin/RG/Dortmund/user_upload/Clean-Code-Vortrag.pdf)