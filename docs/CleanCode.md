# Clean Code

## Einleitung

Bei Clean Code handelt es sich um eine Reihe Richtlinien und Prinzipien, welche von allen Softwareentwicklern beachtet werden sollten.
Diese Prinzipien und auch der Name entstammen dem Buch "Clean Code" von Robert C. Martin. 
Dieses Buch enthält eine Menge von Best Practices, Prinzipien und Praktiken, welche zu "Clean Code" führen.

Die folgeden Kapitel werden zunächst auf ein Paar negativ Beispiele, sogenannten Dirty Code eingehen, um zu zeigen, was 
vermieden werden sollte. Danach wird auf die Clean Code Developer Bewegung eingegangen, welche die Clean Code Richtlinien so weit ausbreiten will, wie möglich.
Dabei wurde ein Wertesystem entwickelt, verschiedene Clean Code Grade, Tugenden und verschiedene Maßnahmen. Die wichtigsten
dieser Maßnahmen setzen das sogenannte SOLID Prinzip zusammen. Nachdem erklärt wurde, wie Clean Code Prinzipien theorhetisch umgesetzt
werden sollen, wird im Clean Code Controlling Kapitel erklärt, wie dies tatsächlich in Firmen angewendet wird. 
Zuletzt werden nochmal die Vorteile und Ziele und die Nachteile von Clean Code aufgelistet.

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
So beginnt ein Entwickler beispielsweise bei dem schwarzen Grad, und arbeitet sich während der Entwicklung bis zum 
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
- Separation of Concerns (SoC)
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
- Open Closed Principle
- Tell don't ask
- Interface Segregation Principle (ISP)
- Integration Operation Segregation Principle (IOSP)

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
- Continuous Delivery
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
Im folgendem wird SRP auf eine überladene Klasse angewendet:

    class Store{
        ...
        public List<Produkt> zeigeProdukte() 
        ...
        public double berechnePreis()
        ...
        public Benutzer registriereBenutzer()
        ...
    }
    
In diesem Fall hat die Store Klasse zu viele Aufgaben. Stattdessen sollten die benötigten Funktionlitäten auf verschiedene
Klassen aufgeteilt werden, welche dann miteinander Kommunizieren.  
  
    class Store{
        ...
        public List<Produkt> zeigeProdukte() 
        ...
    }
    
    class Preisrechner{
        ...
        public double berechnePreis()
        ...
    }   
    
    class LoginService{
        ...
        public Benutzer registriereBenutzer()
        ...
    }

### Open Closed Principle
Das Open Closed Principle, OCP, gehört zum grünen Grad und verlangt, das Klassen offen für Erweiterungen sind, aber geschlossen gegenüber Modifikation.
Durch dieses Prinzip soll gewährleistet werden, dass funktionierende Funktionalitäten nicht durch hinzufügen neuer 
Funktionalitäten beschädigt werden.  
Das folgende Beispiel zeigt, wie das Open-Closed Prinzip angewendet werden kann:
  
    public double Preis() {
        const decimal StammkundenRabatt = 0.95;
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

    interface IPreisRechner {
        double Preis(int menge, double einzelpreis);
    }
    
    IPreisRechner preisRechner;
    
    public double Preis() {
        return preisRechner.Preis(menge, einzelpreis);
    }
    
    class Einmalkunde implements IPreisRechner {
        public double Preis(int menge, double einzelpreis) {
            return menge * einzelpreis;
        }
    }
    
    class Stammkunde implements IPreisRechner {
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

    class Kunde{
        private String name;
        ...
        private List<Produkt> kaufhistorie;
        ...
        public List<Produkt> getKaufhistorie(){
            return kaufhistorie;
        }
        ...
    }

    class UnangemeldeterKunde extends Kunde{
        ...
        public List<Produkt> getKaufhistorie(){
            return null;
        }
        ...
    }  
    
Bei diesem Beispiel fehlen der UnangemeldeterKunde Klasse Funktionalitäten, welche in der Elternklasse enthalten sind. Um diesen
Fehler zu beheben, kann zum Beispiel die Erbstruktur geändert werden.

     class UnangemeldeterKunde{
        private List<Produkt> einkaufswagen;
        ...
     }
     
     class AngemeldeterKunde extends UnangemeldeterKunde{
         private String name;
        ...
        private List<Produkt> kaufhistorie;
        ...
        public List<Produkt> getKaufhistorie(){
            return kaufhistorie;
        }
        ...
     }

### Interface Segregation Principle

Bei dem Interface Segregation Principle (ISP), welches ebenfalls zum gelben Grad gehört, geht es um die Abtrennung von 
Interfaces. So ist es für einen Client nicht notwendig alle Details eines Services zu wissen, sondern nur die für den 
Client relevanten. Wird das Prinzip befolgt, wird die Kopplung zwischen Koponenten geringer, was zu einfachere Wartung 
und Erweiterbarkeit führt. 

    interface IKunde{
        private List<Produkt> getRabatte()
        ...
        private bool login(String username, String password)
        ...
        private void buy()
        ...
    }
    
    interface IMitarbeiter{
        ...
        private bool login(String username, String password)
        ...
    }
    
In diesem Beispiel ist das IKunde Interface sehr mächtig, und es wird Kunden geben, die nicht alle diese Funktionalitäten
benötigen. Außerdem benötigt sowohl der IKunde als auch der IMitarbeiter die login Funktion, weshalb es besser wäre, dafür
ein eigenes Interface zu erstellen. Dies könnte dann zum Beispiel so aussehen:

    interface IRegistriert{
        private bool login(String username, String password)
    }
    
    interface IKunde{
        private void buy()
    }
    
    interface IStammkunde extends IKunde{
        private List<Produkt> getRabatte()
    }
    
Nun sind die Interfaces kleiner, und ermöglichen, dass auch wirklich nur das enthalten ist, was benötigt wird. Ein
Stammkunde würde damit zum Beispiel alle drei Interfaces verwenden, wähhrend ein unagemeldeter Kunde nur IKunde verwenden
würde.

### Dependency Inversion Priciple

Das letzte Prinzip von SOLID, das Dependency Inversion Principle (DIP) setzt vorraus, dass High-Level Klassen nicht von Low-Level Klassen abhängig sein 
sollen, sondern beide von Interfaces. Außerdem sollen Interfaces nicht von Details abhängig sein, sondern von Details von
anderen Interfaces. Wird dieses Prinzip befolgt ist die Kopplung zwischen Klassen geringer und es ist einfacher einzelne
Komponenten zu testen. Diese Eigenschaften machen DIP auch Teil des gelben Grades.

In dem folgenden Beispiel wurden mehrere verschiedene Kundenarten implementiert, die von einer abstrakten Klasse ableiten.
Die beiden High-Level Klassen unterscheiden sich nur in dem Preisrechner, welcher verwendet wird um zu berechnen, wie viel 
Kunden bezahlen müssen. Damit sind diese nur von Low-Level Klassen abhängig.

    abstract class Kunde{
        public abstract double preis();
    }
    
    class Stammkunde extends Kunde{
        StammkundePreisrechner preisrechner = new StammkundePreisrechner();
        
        public override double preis(){
            return preisrechner.preis();
        }
    }

    class Neukunde extends Kunde{
        NeukundePreisrechner preisrechner = new NeukundePreisrechner();
                
        public override double preis(){
            return preisrechner.preis();
        }
    }
    
Hier wurden nun die Abhängigkeiten umgekehrt, dass heißt der Preisrechner bestimmt, um welche Art von Kunde es sich handelt.
Die verschiedenen Kundenarten konnten auch gekürzt werden, da sich diese nur durch den Preisrechner unterschieden haben, und es
wird stattdessen der Kunde verwendet, welche das IKunde Interface implementiert. 

    interface IKunde{
        public double price();
    }
    
    class Kunde implements IKunde{
        ...
    }

    main(){
        Kunde stammkunde = new Kunde(new StammkundePreisrechner())
        Kunde neukunde = new Kunde(new NeukundePreisrechner())
    }
    

## Maßnahmen
Außerhalb der bereits vorgestellten Prinzipien von SOLID beinhält jeder Grad, außer der schwarze, eine Menge an weiteren Prinzipien
und Praktiken, welche das jeweilige Ziel des Grades erfüllen. Die folgenden Unterkapitel erläutern welche der
wichtigsten und bekanntesten dieser Techniken.

### Don't Repeat Yourself (DRY)
Eine eigentlich selbstverständliche Regel, die dennoch oft Missachtet wird. Hier geht es darum, dass
man doppelten Code vermeiden sollte, und stattdessen lieber Funktionen oder andere Refaktoriserungsmuster anwenden sollte.
Das folgende Beispiel zeigt sogenannten WET (We enjoy typing) Code, welcher das Gegenteil zu DRY abbildet. 
    
    ...
    double zwischenPreis = produktPreis * menge * 0.95;
    
    double gesamtpreis = produktPreis * menge * 0.95;
    ...
    
In diesem Beispiel wird natürlich die berechnung des Preises wiederholt, aber auch die Magic Number, welche einen
Stammkundenrabatt darstellt, sollte in eine Konstante ausgelagert werden, damit diese nicht an mehreren Stellen erneut 
ausgeschrieben werden muss.  
Somit würde folgendes entstehen:
    
    const double stammkundenrabatt = 0.95;
    ...
    public double berechnePreis(double produktPreis, int menge){
        return  produktPreis * menge * stammkundenrabatt;
    }
    ...
    double zwischenPreis = berechnePreis(produktPreis, menge)
    
    double gesamtpreis = berechnePreis(produktPreis, menge)
    ...

### Keep It Simple, Stupid (KISS)
Dieses Prinzip steht dafür, dass stehts die einfachste Lösung verwendet werden soll. Wenn Code unverständlich ist, erschwert
dies, dass mehrere Personen an ihm arbeiten können. Um stehts die einfachste Lösung zu finden empfehlen sich Code Reviews 
und Pair Programming. Dieses Prinzip lässt sich auch auf Datenstrukturen anwenden. Wenn für eine Lösung nur eine
Liste nötig ist, sollte keine Map oder sonstiges verwendet werden.

    FileOutputStream stream = null;
    PrintStream out = null;
    try {
        File file = new File("Test.txt");  
        stream = new FileOutputStream(file); 
        String text = "Teststring";
        out = new PrintStream(stream);
        out.print(text);                  
    } catch (Exception ex) {
        //do something
    } finally {
        try {
            if(stream!=null) stream.close();
            if(out!=null) out.close();
        } catch (Exception ex) {
            //do something
        }
    }
    
Anstatt diese komplizierte Herangehensweise zu wählen, könnte man stattdessen mitgelieferte Methoden verwenden, solange man 
wie in diesem Fall die richtige Version von Java verwendet.

    Files.writeString(Path.of("\", "Test.txt"), "Teststring");

### Die Pfadfinderregel
Die Pfadfinderregel besagt "Hinterlasse einen Ort immer in einem besseren Zustand als du ihn vorgefunden hast" und soll 
verursachen, dass stetige kleine Verbesserungen stattfinden. So wird ein großes Projekt zum Bespiel nur an stellen aufgeräumt,
die gerade weiterentwickelt werden. Hierbei ist allerdings zu beachten, dass ein Clean Code Developer immer nur 
Prinzipien und Praktiken seines aktuellen Grades anpassen sollte, andernfalls nehmen solche Aufräumarbeiten zu viel Zeit ein und
bringen den Entwickler von seiner eigentlichen Tätigkeit ab.

### Single Level of Abstraction (SLA)
Das Single Level Of Abstraction Prinzip schreibt vor, dass Methoden auf einheitliche Abstraktionsniveus gebracht werden
sollten. Im Falle einer Methode kann dieses Abstraktionsniveau zum Beispiel stark schwanken. Währrend in einer Zeile nur eine
einfache Zuweisung stattfindet, kann in der nächsten eine komplizierte Formel auf Bittiefe stehen.  
Um einheitliche Niveaus zu erreichen sollten solche komplizierten Algorithmen ausgelagert werden, sodass die Lesbarkeit 
der Methode erhalten bleibt. Wenn der Entwickler wünscht genauer hinzusehen, kann er dazu einfach die aufgerufene Methode betrachten.  

    public double berechnePreis(double produktKosten, int produktAnzahl, UserData userdata){
        double rabattMultiplikator = 1 - (userdata.anzahlBestellungen * 0.01) - (userdata.kundenart.index * 0.1);
        
        return produktKosten * produktAnzahl * rabattMultiplikator; 
    }
    
In diesem Beispiel sind zwei verschiedene Abstraktionsebenen. Die eine behandelt nur die komplizierte Berechnung des
Rabatts anhand der Benutzerdaten, währrend der Rest eine simple Mulitplikation darstellt.

Um SLA umzusetzen, sollte die Rabatt Berechnung in eine Methode ausgelagert werden.

    private double berechneRabatt(UserData userdata){
        return 1 - (userdata.anzahlBestellungen * 0.01) - (userdata.kundenart.index * 0.1)
    }

    public double berechnePreis(double produktKosten, int produktAnzahl, UserData userdata){
        return produktKosten * produktAnzahl * berechneRabatt(userdata); 
    }
  
### Tell, Don't Ask
Bei diesem Prinzip wird verlangt, dass Objekte nicht Entscheidungen anhand von dem momentanen Zustand anderer Objekte treffen.
Es wird stattdessen verlangt, dass Objekte sich gegenseitig befehlen, was zu tun ist.  
Also wenn Objekt A eine Methode von Objekt B aufrufen will, und von Property C abhängig ist welche, dann soll A anhand von C
entschieden, und nicht B C anfragen und dann selbst entscheiden. Wenn dieses Prinzip angewendet wird, führt dies zu geringerer
Kopplung, und Objekte werden seltener zu reinen Datenhaltungsobjekten.

    class Preisrechner{
        ...
        private double berechneRabatt(UserData userdata){
            return 1 - (userdata.anzahlBestellungen * 0.01) - (userdata.kundenart.index * 0.1)
        }
    
        public double berechnePreis(double produktKosten, int produktAnzahl, UserData userdata){
            return produktKosten * produktAnzahl * berechneRabatt(userdata); 
        }
        ...
    }
     
Anstatt, dass der Preisrechner den Rabatt berechnet, welcher von Eigenschaften der User Daten abhängt, sollte dem Preisrechner
der Rabatt gesagt werden. Die Berechnung des Rabatts wäre somit Teil der USer Daten.

    class UserData{
        ...
        UserData(...){
            ...
            this.rabattMultiplikator = berechneRabatt();
        }
        
        private double berechneRabatt(){
            return 1 - (anzahlBestellungen * 0.01) - (kundenart.index * 0.1)
        }
        ...
    }
    
    class Preisrechner{
        ...
        public double berechnePreis(double produktKosten, int produktAnzahl, double rabattMultiplikator){
            return produktKosten * produktAnzahl * rabattMultiplikator; 
        }
        ...
    }

### Law Of Demeter
Der Law of Demeter handelt davon, das Zusammenspiel von Objekten zu beschränken. So soll nach dem Law of Demeter eine Methode
nur folgende andere Methoden verwenden:
- Methoden der eigenen Klasse
- Methoden der Parameter
- Methoden assoziierter Klassen
- Methoden selbst erzeugter Objekte  
Dadurch soll minimiert werden, dass Aufrufe über mehrere Objekte möglich sind, welche zu hoher Kopplung führen würden. Manchmal
sollte dieses Prinzip allerdings nicht angewendet werden, zum Beispiel bei Konfigurationsklassen.


    class Abrechnung{   
        ...
        double zwischenKosten = bisherigeKosten + neuesProdukt * auftrag.user.preisrechner.rabatt;
        ...
    }
    
In diesem Besipiel ruft die Abrechnung den Rabatt eines Auftrages über den Benutzer und dessen Preisrechner auf.
Stattdessen sollen Hilfsmethoden verwendet werden, die solche Zugriffe ermöglichen. Dadurch wird die
Kopplung verringert, da nicht mehr die Abrechnung angepasst werden muss, wenn zum Besipiel der Rabatt nicht mehr
am Preisrechner hängt, sondern direkt an den User Daten.
    
    class UserData{
        getUserRabatt(){
            return preisrechner.rabatt;
        }
    }
    
    class Auftrag{
        getAuftragRabatt(){
            return userdata.getUserRabatt();
        }
    }
    
    class Abrechnung{
        ...
        double zwischenkosten = bisherigeKosten + neuesProdukt * auftrag.getAuftragRabatt();
        ...
    }
    

### You Ain't Gonna Need It (YAGNI)
Der Grund, weshalb das eigentlich sehr einfache YAGNI Prinzip notwendig ist, ist das Anforderungen für Software oftmals sehr ungenau
und ständig wechselnd sind. Dies führt dazu, das Software oftmals sehr flexibel wird, um diesen Anforderungen zu entsprechen.
Dies klingt zwar im ersten Moment gut, führt aber auf lange Sicht zu einer Menge Features die garnicht benötigt oder verwendet werden.
Außerdem wird es schwierig den Code mit all diesen Features zu verstehen oder gar weiter zu entwickeln.  
Um den entgegen zu wirken wurde das YAGNI Prinzip entwickelt, welches sich vorallem mit den Anforderungen befasst. 
So werden nur Anforderungen implementiert die auf jedenfall benötigt werden, alle anderen werden so spät wie möglich oder
eben gar nicht implementiert. Zusammengefasst führt das YAGNI-Prinzip bei der Softwareentwicklung zu folgedem:
- Es werden ausschließlich klare Anforderungen implementiert
- Der Kunde muss seine klaren Anforderungen priorisieren
- Die Anforderungen werden nach Priorisierung implementiert
- Codestruktur wird so aufgesetzt, dass sich ändernde und neue Anfoderungen leicht umgesetzt werden können  

Diese Eigenschaften machen YAGNI ein Prinzip, was nicht nur einzelne Entwickler sondern ganze Projekte und Teams betrifft.

### Code Konformität
Es sollten Regeln für den allgemeinen Style des Codes existieren, an die sich jeder hält. Damit ist gemeint, dass sich zum Beispiel 
entweder für die underscore Schreibweise (tolle_funktion) oder camel case (tolleFunktion) entscheidet. Ist ein Code Style
festgelegt, kann dieser in Reviews überprüft werden, oder es können Tools wie Checkstyle verwendet werden, um guten
Codestyle zu prüfen.

### Refactoring Muster
Bei Refactoring handelt es sich um den Vorgang, Code neu zu strukturieren, um die Clean Code Prinzipien umzusetzen. 
Dabei gibt es verschiedene Refactoring Muster, welche häufig angewendet werden. Zum Beispiel das Rename Muster, welches
lediglich die Namen von Variablen, Funktionen und ähnlichem ändert. Dies scheint erst überflüssig, aber erhöht die Leserlichkeit
des Codes Teilweise enorm.

    public double berechne(double a, int b){
        return a * b * 0.95;
    }
    
Aus dieser Schreibweise der Funktion wird nicht deutlich, was ihre Aufgabe ist, und was welche Variable bedeutet.

    private const double stammkundenRabatt = 0.95;
    
    public double berechneStammkundenpreis(double produktPreis, int produktAnzahl){
        return produktPreis * produktAnzahl * stammkundenRabatt;
    }
    
Obwohl die Rechnung noch genau so funktioniert, wie vorher, wird durch die Benennung ein Kontext gegeben, welcher erreicht, dass
die Funktion korrekt verwendet wird, und eventuell leichter angepasst werden kann.

Ein weiteres Refaktorisierungsmuster ist das Dependecy Injection Muster, bei welchen Objekten Eigenschaften mitgegeben werden, 
von denen sie abhängen, anstelle diese pro Objekt zu definieren.

    class NeukundenPreisrechner{
         private const double neukundenRabatt = 0.9;
         ...
    }
    
    class StammkundenPreisrechner{
         private const double stammkundenRabatt = 0.95;
         ...
    }
    
Anstelle viele verschiedene Objekttypen zu haben, werden stattdessen Einheitliche Objekte verwendet, welche alle unterscheidenen
Merkmale im Build Prozess erhalten:

    class Preisrechner{
         private double rabatt;
         
         preisrechner(double rabatt){
            this.rabatt = rabatt;
         }
    }

    main(){
        Preisrechner neukundenPreisrechner = new Preisrechner(0.9);
        Preisrechner stammkundenPreisrechner = new Preisrechner(0.95);
        ...
    }     
    
Ein weiteres bekanntes Refaktorisierungsmuster ist das Extract Methode Muster. Hier werden gewissen Teile von Funktionen
in andere Funktionen ausgelagert. Dies macht den Code nicht nur leserlicher, und hält das Single Layer Of Abstraction Prinzip ein,
sondern kann auch verwendet werden, um doppelten Code zu minimieren.
        
    public void bestelleProdukte(List<Produkt> produkte, UserDaten userdaten){
        double gesamtPreis;
        
        foreach (produkt : produkte){
            gesamtPreis = gesamtPreis + produkt.preis * produkt.anzahl * userdaten.kundenart.rabatt;
        }
        ...
        erstelleRechnung(userdaten, gesamtpreis, produkte);
        ...
    }
    
Wie dieses Beispiel zeigt, wird in der bestelleProdukt Funktion der Gesamtpreis im Detail berechnet. Allerdings könnte es
sein, dass ein Kunde vorm Bestellen der Produkte seine aktuellen Kosten einsehen möchte, wofür dieser Teil der Funktion
ebenfalls benötigt wird.  
    
    public void bestelleProdukte(List<Produkt> produkte, UserDaten userdaten){
        double gesamtPreis = berechneGesamtpreis(produkte, userdaten.kundenart.rabatt)
        ...
        erstelleRechnung(userdaten, gesamtpreis, produkte);
        ...
    }

## Clean Code Controlling
Clean Code Controlling soll sicherstellen, dass sich alle Entwickler an einem Projekt an die Clean Code Richtlinien halten.
Dies kann dadurch entstehen, dass die gute Vorsätze schnell vergessen werden und unterschiedliche Meinungen zu verschiedenen 
Lösungen führen. 
Die drei Grundregeln des Clean Code Controllings sind:
1. Alle Teilnehmer an einem Projekt verpflichten sich die vereinbarten Prozesse anzuerkennen
2. Prozessen können jederzeit nach Bedarf angepasst werden
3. Es muss sich auf ein Verfahren zur Entscheidungsfindung geeinigt werden 

Um sich Clean Code Controlling besser vorstellen zu können wird es nun ähnlich einer Gewaltenteilung in Legislative, 
Exekutive und Judikative unterteilt. 

### Legislative
In der Legislativen Phase des Clean Code Controllings wird zunächst entschieden, welche Methode zur Entscheidungsfindung
verwendet werden soll. Entweder kann hierbei der Projektleiter die alleinige Entscheidungsgewalt bekommen oder das ganze Team.
Dabei können entweder Mehrheitsbeschlüsse, wie beim Abstimmen, verwendet werden oder eine Methode zur Minimierung des 
durschnittlichen Widerstands. Damit ist gemeint, dass durch Vetoabfragen oder Thumb-Voting die Entscheidung getroffen wird,
welche die wenigsten Teammitglieder abgelehnt haben.    

Sobald entschieden wurde, wie Regeln und Prozesse festgelegt werden sollen, werden grobe Fragen zur Projektentwicklung entschieden.
Dazu gehört zum Beispiel, was für das Team DONE heißt, wie mit unfertigem Code umgegangen werden soll, wie mit "fremdem Eigentum"
umgegangen werden soll und was für das Team CLEAN bedeutet.

Nachdem diese Formalitäten geklärt wurden, muss sich nun geeinigt werden, welche Form der Kontrolle verwendet werden soll.
Hier stehen Scrum ähnliche Daily Standups, regelmäßige Team-Reviews, Pair Programming oder vier Augen Reviews zur Auswahl.

### Exekutive
Bei der Exekutiven werden nun die vereinbarten Ziele mit der ausgewählten Methode kontrolliert. Hierbei ist wichtig zu beachten,
dass neue Entwicklungen erst nach Kontrolle durch andere Teammitglieder auf funktionelle Korrektheit, ausreichende Testabdeckung,
TODO Einträge und Einhaltung der abgestimmten Clean Code Maßnahmen als fertig angesehen werden dürfen. 

### Judikative
Die Judikative soll die Teammitglieder motivieren, sich an die vereinbarten Regeln zu halten und soll grobe Vergehen bestrafen.
Dies kann zum Beispiel durch die 1€-Regel umgesetzt werden. Diese schreibt vor, dass jedes Teammitglied einen Euro in eine
gemeinsame Kasse spenden muss, wenn zum Beispiel nicht kompilierender Code gepusht wurde, oder gebrochene Tests nicht korrigiert wurden.
Von dem gesammelten Geld kann am Ende der Entwicklung für das Team Kuchen oder ähnliches gekauft werden. Neben dieser materiellen
Motivation wird die Motivation natürlich auch durch erlangte Anerkennung erreicht, die ein Entwickler bekommt, wenn er sich an
alle Regeln vorbildlich hält und guten Code produziert. 

## Test Driven Developement (TDD)
Bei Test Driven Development wird, wie der Name vermuten lässt, die Entwicklung von Tests vorrangetrieben. Um dies umzusetzen
wird TDD in drei Merkregeln zusammengefasst:
1. Schreibe erst einen fehlschlagenden Test, bevor neue Funktionalität, die diesen bestehen lassen soll, entwickelt wird.
2. Passe Programmcode nur solange an, bis alle Tests erfolgreich durchlaufen.
3. Räume den Code auf. Keine neuen Verhaltensweisen hinzufügen. Wenn Tests nach Aufräumen fehlschlagen, Fehler finden und beheben.

Durch TDD wird erreicht, dass der Code eine hohe Testabdeckung hat. Oftmals werden Tests vernachlässigt, was zu Problemen bei
der Fehlerfindung führt und das hinzufügen neuer Komponenten erschwert, da nicht sichergestellt ist, dass immer noch alles
funktioniert.

Damit besteht zwischen TDD und CCD eine hohe Ähnlichkeit. Beide Vorgehensweisen setzen sich, unter anderem, als Ziel eine höhere
Testabdeckung zu erzielen. Allerdings wird bei TDD die Entwicklung mit Tests vorrangetrieben, während bei CCD Tests nachträglich hinzugefügt werden.
Hier ist allerdings zu beachten, dass TDD meist für neue Entwicklungen angewendet wird, während CCD auch auf bereits bestehende
Software angewendet wird.

## Vorteile und Ziele von Clean Code
Die Vorteile und Ziele von Clean Code lassen sich gut mit dem vorgestelltem Wertesystem zusammenfassen. Zunächst soll durch das 
Anwenden der Clean Code Prinzipien und Praktiken eine höhere Evolvierbarkeit erreicht werden. Dies bedeutet, dass auch große 
Projekte leicht mit neuen Features erweitert werden können, ohne das dabei ein schier unmöglicher Aufwand entsteht. Dies geligt
oftmals durch das reduzieren der Kopplung der einzelnen Komponenten, aber auch durch Techniken wie ausgiebiges testen, um zum 
einen sicher zu stellen, dass das neue Feature wie geplant funktioniert, aber auch bereits bestehende Funktionalitäten erhalten bleiben.  
Ein weiterer Effekt des vielen Testens ist die Erhöhung der Korrektheit, welche aber auch durch das Einfachhalten des Programms
erreicht werden kann.   
Die Produktionseffizienz wird durch die erhöhte Einfachheit, gute Dokumentation und gut Strukturierung erhöht, da auch
vorher unbeteiligte Entwickler sich schnell einarbeiten können und neue Features schnell hinzugefügt werden können.
All diese Maßnahmen und vorallem die Pfadfinderregel führen letztendlich auch zu kontinuierlicher Verbesserung. Software ist
selten abgeschlossen, weshalb es wichtig ist sie stetig zu verbessern. Ob dies nun Verbesserungen der Verständlichkeit, 
Laufzeit oder anderem ist, spielt dabei keine Rolle.  
Clean Code sorgt somit dafür, dass Software immer weiterentwicklet werden kann, und niemals der Punkt erreicht wird, an dem
die Software so komplex und verworren ist, dass es einfacher ist komplett von vorne zu beginnen.

## Nachteile von Clean Code
Um erfolgreich alle Aspekte von Clean Code durchführen zu können, ist ein hoher Aufwand nötig. Zunächst
muss sich jeder Mitarbeiter in das Thema einarbeiten, und dann die je nach aktuellen Grad verlangten Prinzipien umsetzten.
Außerdem ist es notwendig, durch Code Reviews, Pair Programming oder andere Methoden zu kontrollieren, ob die Prinzipien
korrekt umgesetzt wurden. Dieses enorme Zeitinvestment könnte natürlich dafür verwendet werden neue Features zu entwickeln.
Allerdings ist diese Betrachtungsweise sehr kurzsichtig, da unaufgeräumte Software einen Punkt erreicht, an dem die Implementation
neuer Features, durch die schlechte Struktur des Projekts, so aufwändig ist, dass es besser gewesen wäre von vornerein die Clean Code
Prinzipien umzusetzen.

## Zusammenfassung
Abschließend werden nochmals die Tugenden und die wichtigsten Prinzipien und Praktiken zusammengefasst.

| Name                                      | Bedeutung                                                                 |
|-------------------------------------------|---------------------------------------------------------------------------|
| **Prinzipielle Tugenden**                 | |
| Value Variation                           | Alternative Lösungen sind manchmal besser, nicht alles standardiesieren   |
| Do Only What's Necessary                  | Nur wirklich benötigte Dinge Implementieren, keine Zeit mit unnötigen Dingen verschwenden   |
| Isolate Aspects                           | Komponenten einzeln betrachten und weiterentwickeln                       |
| Minimize Dependencies                     | Abhängigkeiten von Komponenten minimieren, Kopplung verringern            |
| Honor Pledges                             | Funktionalität spiegelt Planung, keine Überraschungen                     |
| **Praktische Tugenden**                   | |
| Embrace Uncertainty                       | Unsicherheit führt zum sichergehen durch testen, oder nachdenken          |
| Focus                                     | Immer auf eine Sache auf einmal Konzentrieren                             |
| Value Quality                             | Nicht mit suboptimalen Lösungen zufrieden sein, keine Workarounds         |
| Get Things Done                           | Eine Sache nach der anderen, keine Sachen unfertig liegenlassen           |
| Stay Clean                                | Code einheitlich halten, Refaktorisieren, Code Styles einhalten           |
| Keep Moving                               | Wissen stehts erweitern, jede Entwicklung reflektieren, erlerntes auf weitere Teile anwenden |
| **Prinzipien**                            | |
| Single Responsibility Principle           | Jede Klasse hat eine Verantwortlichkeit                                   |
| Open Closed Principle                     | Klassen sind offen für Erweiterungen, geschlossen für Modifikation        |
| Liskov Substitution Principle             | Subtypen verhalten sich so wie Basistypen, nur Erweiterung, keine Einschränkung |
| Interface Segregation Principle           | Interfaces sind abgetrennt, geben nur so wenig preis wie nötig            |
| Dependency Inversion Principle            | High-Level Klassen sind nicht von Low-Level Klassen abhängig, beide sind von Interfaces abhängig |
| Don't Repeat Yourself                     | Wiederholungen im Code vermeiden, Magic Numbers in Konstanten packen      |
| Keep It Simple, Stupid                    | Immer die enfachste Lösung oder Datenstruktur verwenden                   |
| Single Level Of Abstraction               | Funktionen haben einheitliche Abstraktionsebenen                          |
| Tell Don't Ask                            | Objekte fragen nicht nach Zuständen anderer Objekte, sonder geben Objekten Anweisungen |
| Law Of Demeter                            | Objekte haben nur beschränkte Interaktion mit anderen Objekten            |
| You Ain't Gonna Need It                   | Nur klare Anforderungen umsetzen, alles andere später, Funktionen anhand von Priorisierung umsetzen, keinen flexiblen Code |
| **Praktiken**                             | |
| Pfadfinderregel                           | Hinterlasse einen Ort immer in einem besseren Zustand als du ihn vorgefunden hast |

## Quellen
[Clean Code Developer](!https://clean-code-developer.de/)  
[Vortrag zu Clean Code](!https://gi.de/fileadmin/RG/Dortmund/user_upload/Clean-Code-Vortrag.pdf)  
[Wikipedia](!https://de.wikipedia.org/wiki/Clean_Code)