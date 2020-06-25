# Blockchain

## 1 Einleitung

### 1.1 Motivation

Bei der Blockchain handelt es sich um eine Technologie zur Speicherung von Daten, die über Schnittstellen gelesen und bearbeitet werden können. Im Gegensatz zu Datenbanken, die in der Regel über eine Client-Server-Architektur verfügen, bestehen Blockchain-Netzwerke aus mehreren gleichberechtigten Knoten, die ein Peer-to-Peer Netzwerk bilden und unabhängig voneinander eine gemeinsame Datenbasis pflegen.

Die Blockchain dient als grundlegende Technologie des Bitcoin und wurde erstmals in dem Paper "Bitcoin: A Peer-to-Peer Electronic Cash System" unter dem Pseudonym Satoshi Nakamoto veröffentlicht. Mit dem Bitcoin konnte erstmals die Machbarkeit eine elektronischen Währung ohne zentrale Kommunikationsstelle bestätigt werden. Durch die Blockchain wird hier ein vertrauenswürdiger Austausch zwischen zwei Parteien ermöglicht.

Während der Einsatz der Blockchain für digitale Währungen immer noch die zentrale Anwendung ist, gibt es mittlerweile auch andere Anwendungsbereiche in denen die Blockchain eingesetzt wird, wie zum Beispiel dem maschinellen lernen.

## 1.2 Umfang

Im folgenden Teil der Einleitung werden zunächst die der Blockchain zugrundeliegenden Technologien erläutert. Daraufhin wird die Funktionsweise der Blockchain selbst beschrieben und abschließend werden Smart-Contracts vorgestellt, die es ermöglichen, Operationen in Form von Algorithmen in der Blockchain zu hinterlegen. In Kapitel 2 werden verschiedene Anwendungsfälle der Blockchain außerhalb des Finanzbereiches dargestellt. In Kapitel 3 folgt eine Darstellung der Punkte in denen sich verschiedene Blockchain Anwendungen voneinander abgrenzen lassen. In Kapitel 4 die Architektur von Blockchain basierten Anwendung vorgestellt. Anschließend folgt in Kapitel 6 die Darstellung bereits existierender Blockchain Anwendungen, wie Bitcoin und Ethereum. Abschließend folgt in Kapitel 7 Darstellung von Beispielen für Smart-Contracts in Ethereum.

### 1.3 Grundlegende Technologien

Die der Blockchain zugrundeliegenden Technologien sind bereits gut erforscht und stammen aus der Informatik beziehungsweise der Kryptographie. Konkret handelt es sich bei diesen Technologien um Hash-Funktionen, kryptographische Puzzles, Hash-Bäume und digitale Signaturen für Nachrichten.

#### 1.3.1 Hash-Funktionen

Bei Hash-Funktionen handelt es sich um Funktionen, die eine Menge an Informationen beliebiger Größe als Eingabemenge auf einen Zielbereich fixer Größe abbilden können. Der Zielbereich ist dabei wesentlich kleiner als der Eingabereich und die Hash-Funktion soll so gestaltet sein, das es möglichst zu keinen Kollisionen im Zielbereich kommt. Die Hash-Funktion muss daher den Zielbereich möglichst gut ausnutzen können und dementsprechend für ähnliche Eingabewerte komplett unterschiedliche Zielwerte errechnen. Zusätzlich soll man aus dem Zielwert keine Rückschlüsse auf den Eingabewert ziehen können. Diese Eigenschaft Ermöglicht es, mithilfe des Zielwertes die Korrektheit des Eingabewertes sicherzustellen.

Sogenannte kryptographische Hash-Funktionen, die bei der Blockchain zum Einsatz kommen müssen zusätzlich unter anderem die folgenden Eigenschaften erfüllen:

- starke Kollisionsresistenz

- praktisch unmöglich von Zielwert auf Eingabewert zu schließen
- unmöglich durch Variation des Eingabewertes einen bestimmten Zielwert zu erzeugen

Eine Hash-Funktion, die diese Eigenschaften bietet der SHA-256-Hash-Algorithmus. In der folgenden Tabelle  werden Beispielhaft zwei Hash werte dargestellt, die mit diesem Algorithmus berechnet wurden. Dabei ist zu sehen, dass obwohl die Eingabewerte sich nur in einer Stelle unterscheiden nahezu komplett unterschiedliche Hash-Werte generiert wurden.

| Eingabewert             | SHA-256-Hash-Wert                                            |
| ----------------------- | ------------------------------------------------------------ |
| A bezahlt B 10 Bitcoin. | 30AF6E0870081E16E20BEC0923DF8CB3A0D49EB29CFB772B2DD6377CCBCB71B4 |
| A bezahlt B 11 Bitcoin. | 4AEFD39DA0278DA3383D67AC30E8CD0E53ACD7114DCA6337750EBE58E0999789 |

#### 1.3.2 Kryptographische Puzzle

In der Blockchain werden die oben beschriebenen Eigenschaften von Hash-Funktionen genutzt um kryptographische Puzzle zu erzeugen. Dabei geht es darum einen gegebenen Eingabewert so zu variieren, das der Ausgabewert in einem bestimmten Wertebereich liegt. Beispielswiese soll in der Eingabe "A bezahlt B 11 Bitcoin. XXXX" die Stelle XXXX so ersetzt werden, das ein SHA-256-Hash-Wert mit sieben führenden Nullen entsteht. Dies ist allerdings nur durch reines Ausprobieren verschiedener Möglichkeiten realisierbar.

Durch die kryptographischen Puzzle lässt sich eine zufällige Auswahl in einer Menge an Teilnehmern eines Netzwerkes treffen, ohne die Notwendigkeit einer zentralen Stelle. Dazu wir das Puzzle im Netzwerk Veröffentlicht und der Teilnehmer, der das Puzzle als erstes löst wird ausgewählt. Da jeder Teilnehmer nur verschiedene Möglichkeiten durchprobieren kann, hängt die Auswahl vom Zufall ab.

### 1.3.3 Hash-Bäume

Hash-Bäume, oder auch Merkle-Bäume genannt, dienen zur Überprüfung ob bestimmte Informationen innerhalb einer Ansammlung von Daten vorhanden sind. Dabei wird, wie in der unteren Abbildung gezeigt, für jede Information ein Hashwert berechnet, welche anschließend immer weiter zu einem Root-Hash kombiniert werden. Mithilfe des Root-Hash lässt sich anschließend überprüfen, ob die zugrundeliegenden Informationen verändert wurden. Um zu überprüfen, ob eine Information in den Daten vorhanden ist, muss ihr Hash-Wert berechnet werden und in Kombination mit den anderen Hash-Werten anschließend der Root-Wert berechnet werde. Gelingt die Berechnung des Root-Wertes, ist die Information Teil der Daten. 