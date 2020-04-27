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
Komplexität, was es schwieriger macht den Code nachvollziehen zu können.

### Open Closed Principle
Das Open Closed Principle, OCP, verlangt, das Klassen offen für Erweiterungen sind, aber geschlossen gegenüber Modifikation.
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

### Interface Segregation Principle

Bei dem Interface Segregation Principle (ISP) geht es um die Abtrennung von Interfaces. So ist es für einen 
Client nicht notwendig alle Details eines Services zu wissen, sondern nur die für den CLient relevanten. Wird das Prinzip
befolgt, wird die Kopplung zwischen Koponenten geringer, was zu einfachere Wartung und Erweiterbarkeit führt. 

### Dependency Inversion Priciple

Das Depndency Inversion Principle (DIP) setzt vorraus, dass High-Level Klassen nicht von Low-Level Klassen abhängig sein 
sollen, sondern beide von Interfaces. Außerdem sollen Interfaces nicht von Details abhängig sein, sondern von Details von
anderen Interfaces. Wird dieses Prinzip befolgt ist die Kopplung zwischen Klassen geringer und es ist einfacher einzelne
Komponenten zu testen. 

## Dirty Code Beispiele

## Maßnahmen

## Prinzipien

## Praktiken

## Clean Code Controlling

## Vorteile und Ziele von Clean Code

## Nachteile von Clean Code