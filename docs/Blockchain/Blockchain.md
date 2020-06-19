# Blockchain

## 1 Einleitung

### 1.1 Motivation

Bei der Blockchain handelt es sich um eine Technologie zur speicherung von Daten, die über Schnittstellen gelesen und bearbeitet werden können. Im gegensatz zu Datenbanken, die in der Regel über eine Client-Server-Architektur verfügen, bestehen Blockchain-Netzwerke aus meheren Gleichberechtigten Knoten, die ein Peer-to-Peer Netzwerk bilden und unabhänging voneinader eine gemeinsame Datenbasis pflegen.

Die Blockchain dient als grundlegende Technologie des Bitcoin und wurde erstmals in dem Paper "Bitcoin: A Peer-to-Peer Electronic Cash System" unter dem Pseudonym Satoshi Nakamoto veröffentlicht. Mit dem Bitcoin konnte erstmals die Machbarkeit eine elektronischen Währung ohne zentrale Kommunikationsstelle  bestätigt werden. Durch die Blockchain wird hier ein vertrauenswürdiger austausch zwischen zwei Parteien ermöglicht.

Während der Einsatz der Blockchain für digitale Währungen immer noch die zentrale Anwendung ist, gibt es mittlerweile auch andere Anwendungsbereiche in denen die Blockchain eingesetzt wird, wie zum Beispiel dem maschinellen lernen.

### 1.2 Umfang

Im folgenden Teil der Einleitung werden zunächst die der Blockchain zugrundeliegenden Technologien erläutert. Daraufhin wird die funktionsweise der Blockchain selbst beschrieben und abschließend werden Smart Contracts vorgestellt, die es ermöglichen Operationen in Form von Algorithmen in der Blockchain zu hinterlegen. In Kapitel 2 werden verscheidene Anwendungsfälle der Blockchain dargestellt. In Kapitel 3 folgt eine Darstellung der Punkte in denen sich Verschiedene Blockchain Anwendungen voneinander abgrenzen lassen. In Kapitel 4 die Architektur von Blockchain basierten Anwendung vorgestellt. Anschließend folgt in Kapitel 5 eine kurze Darstellung der Auswirkungen der Verwendung einer Blockchain. In Kapitel 6 folgt die Darstellung bereits existierender Blockchain Anwendeungen, wie Bitcoin und Ethereum. Abschließend folgt in Kapitel 7 Darstellung von Beispielen für Smart Contracts.

### 1.3 Grundlegende Technologien

Die der Blockchain zugrundeliegenden Technologien sind bereits gut erforscht und stammen aus der Informatik beziehungsweise der Kryptographie. Konkret handelt es sich bei diesen Technologien um Hash-Funktionen, kryptographische Puzzles, Hash-Bäume und digitale Signaturen für Nachrichten.

#### 1.3.1 Hash-Funktionen

Bei Hash-Funktionen handelt es sich um funktionen, die ine menge an Informationenbeliebieger größe als Eingabemenge auf einen Zielbereich fixer größe abbilden können. Der Zeilbereich ist dabeiwesentlich kleiner als der Eingabereich und die Hash-Funktion soll so gestalltet sein, das es möglichst zu keinen kollisionen im Zielbereich kommt. Die Hash-Funktion muss daher den Zielbereich möglichst gut ausnutzen können und dementsprechend für ähnliche Eingabewerte komplett unterschiedliche Zielwerte errechnen. Zusätzlich soll man aus dem Zielwert keine Rückschlüsse auf den Eingabewert ziehen können. Diese eigenschaft Ermöglicht es, mithilfe des Zielwertes die korrektheit des Einagbewertes sicherzustellen.

Sogennante kryptographische Hash-Funktionen, die bei der Blockchain zum einsatz kommen müssen zusätzlich unter anderem die folgenden Eigenschaften erfüllen:

- starke Kollisionsresistenz
- praktisch unmöglich von Zielwert auf Eingabewert zu schließen
- unmöglich durch Variation des Eingabewertes einen bestimmten Zielwert zu erzeugen

Eine Hash-Funktion, die diese Eigenschaften bietet der SHA-256-Hash-Algorithmus. In der folgenden Tabelle werden Beispielhaft zwei Hash werte darsgestellt, die mit diesem Algorithmus berechnet wurden. Dabei ist zu sehen, dass obwohl die Eingabewerte sich nur in einer Stelle unterscheiden nahezu komplett unterschiedliche Hash-Werte generiert wurden

| Eingabewert             | SHA-256-Hash-Wert                                            |
| ----------------------- | ------------------------------------------------------------ |
| A bezahlt B 10 Bitcoin. | 30AF6E0870081E16E20BEC0923DF8CB3A0D49EB29CFB772B2DD6377CCBCB71B4 |
| A bezahlt B 11 Bitcoin. | 4AEFD39DA0278DA3383D67AC30E8CD0E53ACD7114DCA6337750EBE58E0999789 |

#### 1.3.2 Kryptographische Puzzle

In der Blockchain werden die oben beschriebenen Eigenschaften von Hash-Funktionen genutzt um kryptographische Puzzle zu erzeugen. Dabei geht es daraum einen gegebenen Eingabewert so zu variieren, das der Ausgabewert in einem bestimmten Wertebereich liegt. Beispielswiese soll in der Eingabe "A bezahlt B 11 Bitcoin. XXXX" die stelle XXXX so ersetzt werden, das ein SHA-256-Hash-Wert mit sieben führenden Nullen entsteht. Dies ist allerdings nur durch reines Ausprobieren verschiedener Möglichkeiten realisierbar.

Durch die kryptographischen Puzzle lässt sich eine zufällige Auswahl in einer Menge an Teilnehmern eines Netzwerkes  treffen, ohne die notwendigkeit einer zentralen Stelle. Dazu wir das Puzzle im Netzwerk Veröffentlicht und der Teilnehmer, der das Puzzle als erstes löst wird ausgewählt. Da jeder Teilnehmer nur verschiedenene Möglichkeiten durchprobieren kann, hängt die Auswahl vom Zufall ab.

#### 1.3.3 Hash-Bäume

Hash-Bäume, oder auch Merkle-Bäume genannt, dienen zur Überprüfung ob bestimmte Informationen innerhalb einer Ansammlung von Daten vorhanden sind. Dabei wird, wie in der unteren Abbildung gezeigt, für jde Information ein Hashwert berechnet, welche anschließend immer weiter zu einem Root-Hash kombiniert werden. Mithilfe des Root-Hashes lässt sich anschließend überprüfen, ob die zugrundeliegenden Informationen verändert wurden. Um zu überprüfen, ob eine Information in den Daten vorhanden ist, muss ihr Hash-Wert berechnet werden und in kombination mit den anderen Hash-Werten anschließend der Root-Wert berechnet werde. Gelingt die berechnung des Root-Wertes, ist die Information Teil der Daten. 

![Hash-Baum](img/Hash-Baum.png)

#### 1.2.4 Digitale Signaturen

Eine weitere Grundlegende Technologie der Blockchain, ist die der Digitalen Signaturen. Diese basiert auf asymetrischen Verschlüsselungsverfahren. Bei diesen Verschlüsselungsverfahren verfühgen die einzelnen Kommunikationspartner über jeweils einen öffentlichen und einen privaten Schlüssel. Der üffentliche Schlüssel ist dabei frei für jeden zugänglich und der private Schlüssel wird lokal gesichert. Nachrichten, die mit dem öffentlichen Schlüssel einer Person verschlüsselt werden, können von dieser Person mit dem privaten Schlüssel wieder entschlüsselt werden und umgekert. 

In der unten stehenden Abbildung wird der vorgang einer Digitalen Signatur beschrieben. Dabei wird der Hash der zu übertragenen Nachricht von Alice mit ihrem privaten Schlüssel verschlüsselt beziehungsweise signiert. Anschließend kann der Empänger der Nachricht, in diesem Falle Bob die Nachricht mit Alice öffentlichen Schlüssel wieder entschlüsseln und so sicherstellen, dass Alice der tatsächliche Sender der Nachricht ist.

![Digitale_Signaturen](img/Digitale_Signaturen.png)

### 1.4 Aufbau und Funktionsweise von Blockchains

Mithilfe der Vorherigen Abschitt vorgetstellten Technologient lässt sich nun eine Blockchain aufbauen. Da es noch keinen einheitlichen Standart für Blockchains gibt muss jede Blockchain seperat beschrieben werden. Im folgenden wird der Aufbau und die Funktionsweise der Blockchain am Beispiel des Bitcoin vorgestellt.

In der unteren Abbildung ist dabei der Aubau der einzelnen Blöcke zu sehen. Auf der untersten Ebene des Blockes befinden sich dabei die Daten zu einzelnen Transaktionen in der Blockchain. Im Falle des Bitcoin handelt es sich hierbei um die Übertragung der digitalen Währung, die als Übertragung von öffentlichen Schlüsseln der Teilnehmer dargestellt werden.

Aus diesen Transaktionen wird mithilfe der Hash-Bäume ein Root-Hash berechnet und in dem Block-Header gespeichert. ZUdem befindet sich im Block-Header ein Zeitstemple, die Version der Blockchain implementierung, den Hasch des vorherigen Blockes ,ein Traget Wert und ein Nonce-Wert. Über den Target Wert wird die Schwierigkeit eines kryptogradischen Puzzles angegeben. Die Schwierigkeit wird dabei an die im Netzwerk zur verfühgung stehenden Rechenleistung angepasst. Bei dem Nonce-Wert handelt es sich um einen Zahlenwert, durch dessen Variation die einzelnen Knoten des Netzwerkes versuchen das kryptographische Puzzle zu lösen. Wenn ein Knoten eine Lösung des Problems findet sendet er diese an alle anderen Knoten im Netzwerk. Diese können durch angabe des Nonce Wertes die korrektheit der Lösung prüfen und den Block zu ihrer Blockchain hinzufügen. Dieses Verfahren zum generieren neuer Blöcke wird *proof-of-work* genannt.

Die Blockchain bildet sich dabei durch die Angabe des Hash-Wertes des vorherigen Blockes. Dadurch muss man, um die Transaktionen in einem Block zu verändern auch die Werte des Nachfolgenden Blöcke neu berechnen. Da dies surch die kryptographischen Puzzle mit einem hohen Rechenaufwand verbunden ist, können die Daten nicht manipuliert werden, solange ein Großteil der Rechenleistung des Netzes bei korrekt arbeitenden Knoten liegt.

![Blockchain_Aufbau](img/Blockchain_Aufbau.png)

### 1.5 Smart-Contracts

Neben Tarnsaktionen lassen sich in der Blockchain auch andere Informationen speichern. Bei Smart-Contracts war zunächst die erfassung von digitalen Vertragsbedingungen vorgesehen, die ohne einflussnahme Dritter algorithmisch ausgeführt werden. Heute können über Smart-Contrats Anweisungen hinterlegt werden, die bei ausführung weiterer Transaktionen überprüft beziehungsweise Ausgeführt werden. So lassen sich komplexe Abläufe beschreiben, die auf den aktuellen Zustand der Blockchain reagieren. Die mögliche kompläxität der Anweisung hängt dabei allerdings startk von der zugrunde liegenden Blockchain-Platform ab.

## 2 Anwendungsfälle

### 2.1 Landwirtschaftliche Wertschöpfungskette

In einer Wertschöphungskette kann der Austausch von Informationen genauso wichtig sein, wie der Austausch der Waren selbst. In der landwirtscahftlichen Wertschöphungskette für Nahrung ist es wichtig festzuhalten wo die Bestandteile Angebaut, verarbeitet und wie sie Verteilt wurden, um eine Lebesmittelsicherheit zu erreichen. Die Informationssysteme zur Unterstützung einer Wertschöpfungskette, werden normalerweise von den einzelnen Teilnehmern seperat gepflegt. So kann jeder Teilnehmer der Kette nur die Informationen zu dem Schritt sehen, an dem er direkt beteiligt ist. Im zuge der Digitalisierung wurde die Vereilung von Information geleufiger. Ein Möglichkeit zum Verteilen der Informationen ist das Einrichten eines Zentralen Servers in dem wichtige Ereignisse in der Wertschöpfungskette für alle Teilnehmer zentral gespeichert werden.

Eine alternative Lösung mit der Verwendung einer Blockchain, ist die Kontrolle des Wertschöpfungskette mithlife von Smart-Contracts. Die Teilnehmer der gemeinsamen Wertschöpfungskette legen zunächst ein Design für den gemeinsamen Prozess fest und legen fest wie die Interaktionen untereinander ablaufen sollen. Die Kontrolle des Prozesses wird in Smart-Contracts implementiert und wird koordiniert, idem die Teilnehmer die Smart-Contracts abwechselnd aufrufen. Smart-Contracts den Prozess wie folgt stützen:

- Nachrichten werden abgewiesen, wenn sie an der falschen stelle des Prozesses stehen
- Nachrichten werden nur von dem Teilnehmer angenommen, der autorisiert ist sie zu senden
- Bedingungen können im Prozess Model aufgeführt werden und direkt durch Smart-Contract-Code ausgeführt werden

Auf diese weise können Prozesszweige automatisch angestoßen werden, wenn die dafür nötigen bedingungen erfüllt sind. In dem daraus resultierenden System kommunizieren dei einzelnen Teilnehmer der Wertschöpfungskette durch senden von Nachrichten über die Blockchain. Um die Kommunikation über die Blockchain zu erleichtern werden "Trigger" Komponenenten verwendet, die konventionelle service Aufrufe in Blockchain Transaktionen umwandeln können und umgekehrt.

### 2.2 Open Data Registry

Register sind Sammlungen von Informationen, die Zentral, meist von Regierungseinheiten, verwaltet werden. In einem Register werden dabei Informationen zu einer bestimmte Klasse von Entitäten gespeichert. Hierbei kann es sich Besipielsweise um Personen oder Unternehmen handeln. Manche Regierungregister sidn öffentlcih und können von jedem eingesehen werden, wie zum Beispiel das Handelsregister.

Bei Daten Portalen wie zum Beipiel data.gov.au wird einen Daten Register mit konventionelen Methoden implementiert. Das Register wird dabei zentral von der Regierung verwaltet und kann den Zugang auf die daten individuell einstellen. Die Konsumenten der Daten können über das Register die verschiedenen Datensätze finden. Das Anfordern der eigentlichen Daten erfolgt anschließend direkt vom Data Provider. Die folgende Abbildung zeigt die grundelgende Architektur dieses Aufbaus

![Data_registry](img/Data_registry.png)

Eine mögliche Verwendungsmöglichkeit der Blockchein ist es nun, dass zentral Verwaltetete Register durch eine Blockchain zu ersetzen. Die daraus entstehende Architektur wird in der folgenden Abbildung grob dargestellt. Statt einer zentrallen Verwaltungsstelle verwalten hier die Data Provider individuell den Datenzugang.

![Data_registry_blockchain](img/Data_registry_blockchain.png)

### 2.3 Blockchain und maschinelles Lernen

Die Blockchain und maschinelles lernen sind zwei der aktuell Erfolgversprechendsten Technologien. Wobei jede neue Technologien auch neue Herausvorderungen mit sich bringt. Beim maschinellen Lernen liegt die Herausvorderung im hohen Bedarf an Daten, Hardware-Ressourcen und menschlicher Expertise. Das zentrale verschprechen der Blockchain ist es nun gerade diese Ressourcen zu demokratisieren. Im folgenden wird gezeigt, wie maschinelles Lernen genutzt werden kann um die Blockchain zu unterstützen und wie die Blockchain wiederum maschinelles Lernen unterstützen kann.

#### 2.3.1 Maschinelles Lernen zur Unterstützung der Blockchain

Da alle Transaktionen innerhalb der Blockchain öffentlich sind, kann maschinelles Lernen verwnedet werden, um unnatürliches Verhalten frühzeitig zu erkennen. So lassen sich Angriffe auf die Blockchain vereiteln, die mögliche Fehler in Smart-Contarcts oder anderen Bereichen ausnutzen.

Auch lässt sich mit maschinellem Lernen eine Admistartion einrichten, die Komponeneten der Blockchain verändern kann. Auf diese wiese können Probleme in der Skalierung behoben werden, indem die Blockgröße auf die aktuelle Menge an Transaktionen angepasst werden kann. Nach aktuellem Stand, sond die Werte, in welcher Rate ein neuer Block erstellt wird und wie viele Transaktionen ein Block beinhaltet von der jeweiligen Blockchainplattform konstant festgelegt sind. Wenn man mschinelles Lernen in die Software an jedem Knoten eingebettet wird, könnte eine dynamische transparente Anpassung erfolgen.

Eine andere möglcihkeit zum Einsatz des maschinellen Lernend auf die Blockchain, ist es bei Kryptowährungen verhaltensmuster zu erkennen und so zusammenhängende Gruppierungen bilden zu können. Auf diese weise kann Untersucht werden, wie Anonym die Transaktionen tatsächlich sind.

#### 2.3.2 Blockchain zur Unterstützung des maschinellen Lernens

Während der Einsatz des maschinellen Lernens zur Unterstützung der Blockchain am naheliegensten ist, gibt es deutlich mehr Literatur für den umgegehrten Fall.

Zum einen lässt sich die Blockchain zur sicherstellung der Integrität, Verfügbarkeit und Vertraulichkeit sicherstellen.Die eigentlichen Daten werden dabei ausserhalb der Blockchain gespeichert und können über eine Blockchain verwaltet werden. Auf die Wiese können Nutzer Daten anbieten, ohne die Kontrolle über diese zu verlieren. Die Blockchain dient in diesem Fall als eine Identifizierungs- und
Authentifizierungsplattform.

Mithilfe von Smart-Contracts lässt sich eine Automatisierung im Lernprozess erreichen.  Da es sich bei Smart-Contarcts um transparente automatisierte Sktipte handelt, kann das Auftreten mesnchlicher Fehler reduziert werden.

Die Blockchain kann asl Speicherung von Metadaten der eigentlichen Dateien dienen, die lokal gespeichert werden. In Branchen, wie dem medizinischen Bereich, wo es für Dritte schwierig ist auf diese Dateien zuzugreifen, könne dezentarle Blockchain Lösungen verwendet werden. Die Auwertung dezentarl Verügbarer Daten war bisher aus den folgenden Gründen erschwert:

- Fehlende Austauschmechanismen 
- Mangelnde Sicherheit und Schutz der Privatsphäre 
- Mangelnde Datenintegrität 
- Dateneigentum 
- Hohe Kosten für die zentrale Datenspeicherung 

Für ersten vier Punkte kann hierbei mit der Blockchain-Technologie und einer dezentralen Datenspeicherung eine gut Grundlage geschaffen werden.

## 3 Variationen der Blockchain

Seit der Entstehung von Bitcoin 2008 entstanden viele verscheidene Blockchains.  Da Blockchaisn sich noch in einer frühen Phase der Entwicklung befinden, gibt es wenig verlässliche Technologien, um verschiedene Blockchains zu vergleichen. Beim erstellen einer neuen Blockchain Anwendung, muss man zunächst die Eigenschaften herausarbeiten, die die Blockchain haben soll. In diesem Kapitel werden verscheidene Punkte vorgestellt, in denen Blockchains sich voneinander unterscheiden können.

### 3.1 Dezentralisierung

Dezentralisierung ist eine der grundlegenden Fähigkeiten der Blockchain. Allerding kann hier zwischen vercsheidenen Stufen der dezentralisierung unterschieden werden. In einem zentralen System liegt die zentrale autorität auf einem Punkt und es gibt einen single Point of Failure. Im gegensatz Dazu steht ein komplett dezentrales System, wie zum Beispiel Bitcoin, welches Personen ermöglicht festzustellen, welche Ressourcen wem gehöhren, ohne jemanden Vertrauen zu müssen. Diese Sytseme haben eine hohe verfügbarkeit, da jeder Knoten unabhängig arbeiteitet und somit eine hohe redundanz herrscht. Die folgende Tabelle zeigt ein sprektrum zwischen komplett zentralen und komplett dezentralen Systemen. In der Tabelle wird gezeigt, dass eine kombination aus einem centralen und einem dezentralen System möglich ist. So können Beispielsweise alle Knoten die Blockchain einsehen, aber nur eine bestimmte menge Knoten auf dieser schreiben.

![dezentralisierung](img/dezentralisierung.png)

### 3.2 Ledger Struktur

Bei einer distributed Ledger handelt es sich um eine Sammlung von Transaktionen, bei der es nur möglich ist neue Daten hinzuzufügen. Diese Ledger wird an viele verschiedene Rechner verteilt. Bei einer Blockchain handelt es sich nun um eine speziele Variante einer solchen distributed ledger. Es handelt sich um eine Ledger, die aus miteinader verknüften Blöcken besteht. Es gibt nun verschiedene Arten diese Ledger aufzubauen. Die folgende Tabelle gibt einen Überblick über diese Varianten. Bei Bitcoin wird hierfür eine globale Liste von Blöcken verwendet.

Andere Blockchain und distributed Ledger Sytseme verwenden andere Datenstrukturen. Beispielsweise wird bei [Hashgraph](https://www.hedera.com/) ein directed acyclic graph (DAG) statt einer Liste verwendet.

![ledger_structure](img/ledger_structure.png)

### 3.3 Consensus Protokoll

Wenn zwei Knoten gleichzeitig einen neuen Block erstellen und an die anderen Knotn im Netzwerk weiterleiten, können die Lösungen bei den einzelnen Knoten in einer unterschiedlichen Reihenfolge auftauchen. Die Entscheidung welche Lösung verwendet wird, beruht auf einem einheitlichen consensus Protokoll innerhalb des Netzwerkes. Im Gegensatz dazu gibt es bei Hyperledger Fabric einen modularen Aufbau, der einen austauschbare Implementation des Protokolls bietet.Die folgende Tabelle stellt verschiedene consnsus Protokolle und ihre Auswirkungen dar. 

Der typische Ansatz wird Nakamoto consensus genannt und beruht darauf, dass jeder Knoten immer die längste Blockkette auswählt, die er beobachtet hat. Eine alternative Nakamoto Consensus den Bitcoin verwendet, ist Beispielsweise der *proof-of-stake* Mechanismus. Hierbei wird die Lösung von dem Miner ausgewählt, der über die meisten Einheiten der digitalen Währung der Blockchain verfügt.

![consensus](img/consensus.png)

### 3.4 Block Konfiguration

Die Konfiguration eines Blockes betrifft die Anzahl und komplexität der Transaktionen, die in einem Block gespiechert werden und die Frequenz mit der neue Blöcke erstellt werden. Die Verschiedenen Konfigurationsmöglichkeiten wirken sich dabei auf die Rate aus, in der Transaktionen verarbeitet werden können. Die folgende Tabelle gibt einen Überblick darüber. Eine Konfigurationsmöglichkeit wäre es Beispielsweise die Schwierigkeit des kryptographischen Puzzle zu senken, wodurch Blöcke schneller generiert werden können. Durch vergrößern eines Blockes können mehrere Transaktionen auf einmal bearbeitet werden, allerding sind große Blöcke schwerer zu replizieren.

![block_configuration](img/block_configuration.png)

### 3.5 Anreize

Verschiedene Blockchain Plattformen bieten vercshiedene Anreitze dem Netzwek beizutreten. Bei Bitcoin zum Beispiel erhalten Knoten die einen neuen Block erstellt haben, eine Belohnung für das Erstellen in form eines neuen Coins und einen Teil der Transaktionskosten. Knoten im Ethereum Netzwerk erhalten ebenfalls einen Belohnung für das ausführen einen Smart-Contracts in for von Ether, der Währung der Ethereum Plattform.

## 4 Architektur Blockchain basierter Anwendugen

### 4.1 Blockchain in der Software Architektur

Die Architektur einer Anwendung lässt sich aus mehreren Software-Komponenten zusammensetzen. In Blockchai basierten anwendung ist die Blockchain eine solche Komponente. Wie für jede Komponente muss auch für die Blockchain entscheiden werden, welche Funktionalitäten von ihr abgedekt werden sollen. Die wichtigste Entscheidung ist dabei, welche Daten in der Kette ind er Kette gespiechert werden sollen und welche nicht. Eine Blockchain kann dabei in der Anwendung verschiedene Funktionen erfüllen.

Eine Funkrion ist es, die Blockchain als Speicherelement für Daten zu verwenden.  Auch lassen sie sich als Rechenelement verwenden. In Etherium wird Beispielweise erlaubt Smart-Contrcts in einer Turing vollständigen Sprache einzubinden, die automatisch ausgeführt werden können. Des Weiteren lässt sich die Blockchain auch als Kommunikations-Komponente verwenden.

### 4.2 Design Prozess für Blockchain Anwendungen

Zu beginn des Design Prozesses der Software Archtitektur muss entschieden werden, ob die Verwendung einer Blockchain für die Anwnedung sinnvoll ist. Dieser Entscheidungsprozesss wird in der folgenden Abbildung vereinfacht dargestellt. DLT steht dabei für Distributed Ledger Technologie. Multi-party meint dabei, ob das System von mehreren vercshieden Parteien genutzt werden soll oder von einzelnen isolierten Nutzern. Bei einzelnen Nutzern wäre der einsatz einer zentralen Datenbank deutlich einfacher umzusetzen. Auch ist es für den Einsatz einer Blockchain wichtig, dass es keine vertrauenswürdige Authorität notwednig ist und die Operation nicht zentralisiert ist. Weitere Entscheidungskriterien sind Beipielsweise notwendige Transparenz oder ob unveränderlichkeit der Daten gewünscht ist. 

![design](img/design.png)

Nach der Evaluierung ob eine Blockchain verwendet werden sollt, folgt dar design Prozess der eigentlichen Blockchain Komponente. Dieser Vorgang wird in der folgenden Abbildung dargestellt. Zunächst muss dabei entscheiden werden, wie eine Authorität dezentralisiert werden soll falls eine vorhanden ist. Anschließend muss entscheiden werde, welche Daten in der Blockchain gespeichert werden, welche Blockchain verwendet werden soll und wie die Blöcke konfiguriert werden sollen.

![design_blockchain](img/design_blockchain.png)

### 4.3 Blockchain Patterns

In diesem Kapitel erfolgt die darstellung einer Auswahl an Patterns für das Design einer neuen Blockchain Anwendung.

#### 4.3.1 Oracle Pattern

Dieses Entwurfsmuster behandelt die kommunikation der Blockchain mit der Außenwelt.

## 5 Auswirkungen der Verwendung von Blockchain

###  5.5 Kosten
### 5.6 Performance
### 5.7 Zuverlässigkeit und Sicherheit

## 6 Existierende Blockchain Plattformen

### 6.1 Bitcoin
### 6.2 Ethereum
### 6.3 Hyperledger Fabric
### 6.4 Weitere representativie Blockchain Formate

## 7 Smart Contract Beispiele

### 7.1 Ethereum Smart Contract
### 7.2 Hyperledger Chaincode
### 7.3 Facebook Libra

## 8 Quellen

[Die Vorteile der Blockchain-Technologie](https://t3n.de/news/blockchain-statt-datenbank-diese-1063641/#:~:text=Klassische Datenbanken orientieren sich typischerweise,voneinander die gemeinsame Datenbasis pflegen.)

[Bitcoin: A Peer-to-Peer Electronic Cash System](https://bitcoin.org/bitcoin.pdf)