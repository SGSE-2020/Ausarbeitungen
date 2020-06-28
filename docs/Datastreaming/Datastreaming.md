# Data Streaming

*Malte Riechmann*

## Was ist Data Streaming?

https://www.ververica.com/blog/continuous-queries-on-dynamic-tables-analyzing-data-streams-with-sql

![img](img/datastreaming.png)

Um Data Streaming zu beschreiben wird oft die Analogie eines Flusses verwendet. Wichtig ist dabei der Fokus auf die Strömung, die wie der Name *Streaming* schon verrät, im Vordergrund steht. Beim Data Streaming spielt der Anfang oder das Ende des Stroms erstmal keine Rolle. Die Daten die durch diesen Strom fließen sind kontinuierlich und haben keinen eindeutig definierten Start- und Endpunkt. Ein Beispiel für solch einen Datenstrom wäre zum Beispiel ein Smartes Thermometer, welches kontinuierlich die Temperatur an einen Server sendet, der darauf hin die Heizung steuert. Hier spielt der Start oder das Ende des Temperatur Datenstromes keine Rolle, wichtig ist nur der permanente Eingang neuer Daten.

Data Streaming ist auch nicht auf eine Datenquelle begrenzt. Wie das Bild zeigt, können die Daten aus tausenden verschiedenen Datenquellen kommen. Dabei ist der Typ der Datenquelle nicht wichtig und kann für jede Datenquelle unterschiedlich sein. Die Daten werden von der Quelle kontinuierlich als kleine Pakete verschickt, die von der Größe her im Kilobytebereich liegen. Die einkommenden Daten aus dem Strom werden dann sequentiell und inkrementell verarbeitet.

## Warum Data Streaming?

Nun stellt sich allerdings die Frage, was der Vorteil von Data Streaming und warum es verwendet werden sollte. Der Vorteil von Streaming wird schnell klar, wenn man den Bereich von Big Data betrachtet. Durch die kleinen Pakete, die aus viele verschiedene Quellen kommen, können Ereignisse aus diese Quellen quasi **simultan** verarbeitet werden. Dies ist wichtig um schnell auf verschiedene zusammenhängende Ereignisse zu reagieren.

Ein weiterer wichtiger Vorteil ist die **Echtzeitfähigkeit** des Streamings. Die kleinen Pakete können mit wenig Verzögerung verschickt werde. Außerdem gibt es kein Overhead für das Sammeln von Daten, wie es bei der Batch Verarbeitung üblich ist. Die kleinen Pakete können auch erheblich schneller verarbeitet werden als große Datenbündel, wodurch auf solche Ereignisse schneller reagiert werden kann.

Darüber besitzt Streaming eine gewisse **Fehlertoleranz**. Der Verlust einen wenige Kilobyte großen Paketes lässt sich in vielen Fällen bessere verkraften als zum Beispiel der Verlust eines ganzen Datenpaketes bei der Batch Verarbeitung. Und obwohl ein Datenpaket fehlt, kann der Datenstrom normal weiterverarbeitet werden.

Ein weiterer großer Vorteil von Data Streaming ist, dass das **Ende der Daten nicht bekannt sein muss**. Durch die Sequentielle Verarbeitung der kleinen Datenpakete wird immer nur in Ausschnitt des Datenstroms betrachtet. Dieses Fenster wird über die Daten geschoben, ohne das eine Ende bekannt sein muss. So können die kontinuierlichen Daten eines Sensors verarbeitet werden ohne sie vorher in Start- und Endpunkte aufzuteilen.

## Wo kommt Data Streaming zum Einsatz?

**Internet of Things**

Aufgrund der geringen Kosten von Sensoren und neuen Entwicklungen um Bereich Internet of Things (IoT) werden neue Produkte oft mit ihnen vollgepackt. Diese Sensoren zeichnen kontinuierlich Daten auf, die verarbeitet werden müssen. Die Daten an sich sind meisten kleine, wie zum Beispiel eine Temperaturwert oder eine Geschwindigkeit. Nichts desto trotz kommt es allein durch die Menge an Sensoren zu einem riesigen Strom an Daten. Das ist zum Beispiel der Fall in Transportfahrzeugen. Die Sensoren sollen dazu dienen die Leistung zu überwachen und gegebenenfalls Defekte möglichst schnell zu erkennen.

Ein weiteres Beispiel ist das Smart Home. Auch hier zeichnen zahlreiche Sensoren kontinuierlich Daten auf. Abhängig von den eingehenden Daten können dann Aktionen ausgeführt werden. Wenn zum Beispiel der CO2 Gehalt zu hoch ist können Fenster geöffnet und Heizungen ausgeschaltet werden. So kann der Komfort in dem Haus erhöht werden und außerdem Energie und Geld gespart werden.

**Finanzen**

Der Finanzbereich ist ein sehr typischer Bereich für Data Streaming, da hier tausende von verschieden Informationen kommen, die sich ständig ändern. So kann an dem Börsenmarkt Data Streaming zum Einsatz kommen um in Echtzeit Value-at-Risk-Berechnungen durchzuführen. So können Portfolios direkt angepasst und an den Börsenmarkt ausgerichtet werden.

**Aktivitätsverfolgung**

Aktivitätsverfolgung kommt in vielen Bereichen zum Einsatz, wie zum Beispiel Social Media Plattformen. Hier werden die einzelnen Aktivitäten der Nutzer verwendet um den Nutzungskomfort zu erhöhen. Basierend auf der Aktivität eines Nutzer und anderer vergleichbarer Nutzer werden dann bestimmte Vorschläge gemacht, die sich der Nutzer ansehen kann. Durch Data Streaming können diese Dienste besser auf den einzelnen Nutzer zugeschnitten werden und es kann schneller auf bestimmte Trends reagiert werden.

## Eigenschaften

In den vorherigen Kapiteln wurden einige Eigenschaften von Data Streaming erwähnt. An dieser Stelle werden alle noch einmal zusammengeführt und übersichtlich dargestellt.

* Ein Datenstrom kann mehrere unterschiedliche Quellen besitzen
* Es herrscht ein kontinuierlicher Datenfluss
* Der Datenfluss besteht aus kleinen Paketen im Kilobyte Bereich
* Ende des Flusses muss während der Übertragung nicht bekannt sein, wie im Beispiel der kontinuierlich generierten Daten eines Sensors
* Auf die Daten wird sequenziell zugegriffen (ggf. über ein Sliding Window)
* Datenrate kann variieren was bei der Verarbeitung/Speicherung beachtet werden

## Abgrenzung

* Batch-Verarbeitung vs. Stream-Verarbeitung
  
  * https://aws.amazon.com/de/streaming-data/
  
  Streaming besitzt nun drei wichtige Vorteil im Kontext von Big Data. Der erste ist die **Simultanität**. Dies spielt vor allem bei mehreren Datenquellen eine Rolle. Durch das Sammeln der Daten und das verschicken in größeren Datenbündeln geht Zeit verloren. Auch dauert das verarbeiten eine Batches länger und die Daten stehen erst später zur Verfügung. So ist die Differenz mit der Daten die aus verschieden Quellen stammen, aber zeitgleich passiert sind größer. Beim Streaming hingegen sind Pakete viel kleiner, sie können schneller verschickt und verarbeitet werden, sodass die Differenz mit der zeitgleiche Ereignisse verarbeitet werden geringer ist. Durch Verzögerungen in der Übertragung kann es auch beim Streaming zu größeren Differenzen kommen, allerdings sind diese Aufgrund der geringeren Paketgröße immer noch kleiner als bei der Batch Verarbeitung.  Im folgenden Bild ist diese Fall vereinfach dargestellt. Es wird davon ausgegangen, dass nur einen gemeinsamen Buffer für die Verschiedenen Sensoren gibt. Der Fall trifft aber ähnlich zu, wenn es verschiedene Buffer gibt
  
  ![img](img/simultan.png)
  
  * vorteil batchverarbeitung
  * vorteil streaming
  * Batch: Verarbeitung eines Datenbündels, generiert Ergebnisse zu Kompletten Datensatz
  * Stream: Mini Datenbündel, Ergebnisse müssen für jeden Datensatz angepasst werden 
  
* Messaging vs. Streaming
  * Abgrenzung zu Messaging Systemen
    *  https://www.theseattledataguy.com/kafka-vs-rabbitmq-why-use-kafka/
  * Strategien zur Verarbeitung von Message Queues
    * http://www.doxsey.net/blog/strategies-for-working-with-message-queues

## Genereller Aufbau

* Data Lakes / Streaming Data Tools & Techniques
  * https://developer.sh/posts/delta-lake-and-iceberg
  * https://developer.sh/posts/streaming-data-overview
* Speicherebene (Ordnen und Aufzeichnen von Daten)
* Verarbeitungsebene (Daten aus der Speicherebene verarbeiten)
* Beide Ebenen beeinflussen sich gegenseitig
* Die Infrastruktur wird durch die im Folgenden genannten Tools festgelegt

## Tools

* **Kafka**
* Kinesis Firehose
* Strom

## Kafka

https://kafka.apache.org/intro

Kafka ist einer verteilte Streaming Plattform. Verteilt bedeutet in diesem Kontext, dass es als Cluster auf einem oder mehreren Servern läuft. Was das für Vorteile mit sich bringt wird im folgenden nach und nach deutlich. Grundsätzlich bietet Kafka bietet drei Hauptfunktionen an:

1. Einen *Publish und Subscribe* Mechanismus an einen Strom an Datensätzen (Stream of records), vergleichbar zu Messaging Systemen
2. Ein fehlertolerantes Speichern von Datenströmen (Streams)
3. Und das Verarbeiten von Streams sobald sie auftauchen

Kafka kommt für häufig für zwei Hauptaufgaben zum Einsatz. Die erste ist als Datapipline die zuverlässig Daten zwischen Systemen in Echtzeit austauscht und die zweite ist zum Transformieren und und reagieren auf Datenströmen. Das heißt Kafka arbeitet nur auf dem Stream und hat keinen direkten Bezug zu dem Empfänger.

### Hauptkonzepte

Bevor es an die verschiedenen Streaming Architekturen geht müssen einige Grundbausteine und Konzepte von Kafka im Folgenden erklärt werden.

![concepts](img/concepts.png)

**Record**

Eine Record oder Datensatz stellt ein kleines Datenpaket dar, welches der Producer als eine Einheit schreibt. Jeder Datnsatz besteht aus einem Schlüssel, einem Wert und einem Timestamp.

**Topics and Logs**

Topics sind die Kernbestandteile von Kafka. Sie stellen die Kategorien dar unter denen Ströme von Datensätzen veröffentlicht werden. Wie in einer Log-Datei, werden alle eingehenden Datensätze gespeichert und neue Daten werden kontinuierlich an das Ende der Sequenz angehängt. Die Sequenz ist  dabei immutable und die Reihenfolge der Daten kann nicht geändert werden. Jeder Datensatz bekommt eine aufsteigende Nummer zugewiesen, dem sogenannten Offset. Dieser Offset identifiziert einen eine Datensatz eindeutig innerhalb einer Sequenz. Eine Topic unterstütz immer multi-subscriber, was bedeutet, dass ein Topic keinen, einen oder mehrere Subscriber haben kann

Unter einem Topic werden alle Daten erstmal dauerhaft gespeichert, unabhängig davon ob sie gelesen wurde oder nicht. Es kann eine Speicher-Periode eingestellte werden. Eingehende Datensätze werden dann für genau diese Zeitspanne gespeichert und nach Ablauf gelöscht unabhängig davon ob sie verarbeitet wurden.

**Partitions**

Ein weiterer wichtiger Punkt ist, dass ein Topic  aus mehren besteht Partitionen. Jede Partition ist eine solche geordnete Sequenz von Datensätzen. Die einzelnen Partition sind über das Cluster verteilt und jeder Server behandelt die Anfragen für einen Teil der Partitionen. Diese Aufteilung erlaubt eine nahe zu unbegrenzten Menge an Datensätzen zu speichern. Die Größe einer Partition ist begrenzt durch den Speicher des Servers, aber verschiedenen Partitionen liegen auf mehreren Servern und die Datensätze können aufgeteilt werden. Ein weiterer Vorteil ist, dass diese Aufteilung parallelisierte Verarbeitung unterstützt. *Wichtig anzumerken im Kontext der Offset ist, das dieser nur die Reihenfolge innerhalb einer Partition speichert und nicht für das gesamte Topic über alle Partitionen hinweg. Wenn eine solche übergeordnete Reihenfolge benötigt wird, darf nur eine Partition für das Topic verwendet werden.*

**Replicas**

Für jede Partition mehrere Kopien für eine höherer Fehler Toleranz. Dabei gibt es einen Server der als *Leader* agiert, der verantwortlich für alle Lese- und Schreibzugriffe auf die Partition ist. Die anderen Server der Kopien agieren als *Follower* und kopieren den Leader. Wenn einer der Leader ausfällt wird automatische einer der Follower zum neuen Leader. Um die Auslastung gleichmäßig über das Cluster aufzuteilen, agiert jeder Server als Leader für ein paar Partitionen und Follower für die Anderen.

**Producer**

Producer publishen Records an Topics ihrer Wahl. Dabei ist der Producer verantwortlich dafür welchen Datensatz er in welche Partition eines Topics schreibt. Dies Strategie hierfür kann jeder Producer frei wählen. Vorstellbar ist zum Beispiel ein Round-Robin vorgehen um die Auslastung der einzelnen Partitionen zu reduzieren, oder auch eine semantische Aufteilung der Datensätze, zum Beispiel nach dessen Schlüssel.

**Consumer**

Ein Consumer liest die verschiedenen Datensätze einer Partition, üblicherweise -aber nicht zwingend- in einer sequentiellen Reihenfolge. Für jeden Consumer wird ein Offset gespeichert, der angibt an welcher Stelle innerhalb des  Datenstromes er sich gerade befindet. Die Kontrolle über dem Offset liegt dabei bei dem jeweiligen Consumer. Deswegen muss dieser die Daten auch nicht sequentiell abarbeiten, sondern kann den Offset anpassen, um Daten wiederholt einzulesen oder Daten zu überspringen.

**Consumer Groups**

Jeder Consumer ist einer Gruppe von Consumern zugeordnet. Ein Datensatz eines Topics wird dann an genau einen Consumer innerhalb einer Consumer Gruppe geschickt. Wenn alle Consumer eines Topics als die gleiche Gruppe besitzen werden die Datensätze gleichmäßig aufgeteilt und wenn alle eine unterschiedliche Gruppe besitzen, wird der Datensatz an jeden Consumer geschickt. Diese beiden Fälle sind allerdings Spezialfälle, im Normalfall gibt wenige Consumer Groups (eine Gruppe = ein logischer Subscriber) mit jeweils mehreren Subscribern.

Bei Topics mit mehreren Partitionen und mehreren Consumer einer Gruppe werden die Partitionen auf die Consumer aufgeteilt. Das bedeutet, das ein Consumer immer die Datensätze von der gleichen Subgruppe an Partitionen bekommt. Diese Aufteilung wird von Kafka dynamisch verwaltet, sodass wenn neue Consumer dazu kommen, die Partitionen in kleinere Gruppen aufgeteilt werden, oder anders herum, wenn eine Instanz wegfällt, dass zu größeren Gruppen zusammengefasst werden.

**Broker**

Der Broker ist ein Kafka Server, der innerhalb des Clusters läuft. Er ist verantwortlich für das verwalten und weiterleiten der eingehenden Datensätze. Die Partitionen eines Topics werden gleichmäßig auf alle verfügbaren Broker aufgeteilt

**Zookeeper**

Der Zookeeper verwaltet und Koordiniert die verschiedenen Broker. Seine Hauptaufgabe ist es die Producer uns Consumer darüber zu informieren, dass ein neuer Broker verfügbar ist bzw. dass ein Broker ausgefallen ist. Die Producer und Consumer nutzen diese Information, um ihrer Aufgaben über andere Broker zu koordinieren 

**Cluster**

Sobald Kafka mehr als einen Broker besitzt spricht man von einem Cluster. Da Broker dynamisch dazu kommen oder verschwinden können, kann eine Cluster dynamisch wachsen oder schrumpfen. In dem Cluster wird die Persistenz und Kopien der Datensätze verwaltet.

### Kern APIs

Kafka bietet 5 API an, die Nutzer für ihre Software nutzen können.

**Producer API**

Die Producer API erlaubt es einer Applikation einen Datenstrom an ein oder mehr Topics zu veröffentlichen.  Im folgenden ist eine Beispiel eines Producers, der Nummern als String als Schlüssel-Wert-Paar schickt an ``"my-topic"`` schickt. Der Producer hält eine Buffer für jede Partition.

````java
Properties props = new Properties();
props.put("bootstrap.servers", "localhost:9092");
props.put("acks", "all");
props.put("key.serializer", "org.apache.kafka.common.serialization.StringSerializer");
props.put("value.serializer", "org.apache.kafka.common.serialization.StringSerializer");

Producer<String, String> producer = new KafkaProducer<>(props);
for (int i = 0; i < 100; i++)
     producer.send(new ProducerRecord<String, String>("my-topic", Integer.toString(i), Integer.toString(i)));

producer.close();
````

**Consumer API**

Die Consumer API erlaubt es Applikationen ein oder mehr Topics zu subscriben. Die so eingehenden Datensätze bestehend aus Schlüssel-Wert-Paaren und dem Offset können dann verarbeitet werden. Im folgenden ist ein Beispiel für ein Consumer.  Dieser Consumer gehört zur Consumer-Gruppe ``"test"`` und erwartet String Schlüssel-Werte-Paare. Der Consumer liest die Nachrichten aus dem Topic ``"my-topic"``.  An dieser Stelle können auch mehrere Topics angegeben werden.

````java
Properties props = new Properties();
props.setProperty("bootstrap.servers", "localhost:9092");
props.setProperty("group.id", "test");
// ... some more settings ...
props.setProperty("key.deserializer", "org.apache.kafka.common.serialization.StringDeserializer");
props.setProperty("value.deserializer", "org.apache.kafka.common.serialization.StringDeserializer");

KafkaConsumer<String, String> consumer = new KafkaConsumer<>(props);
consumer.subscribe(Arrays.asList("my-topic"));
while (true) {
    ConsumerRecords<String, String> records = consumer.poll(Duration.ofMillis(100));
    for (ConsumerRecord<String, String> record : records)
        System.out.printf("offset = %d, key = %s, value = %s%n", record.offset(), record.key(), record.value());
}
````

**Streams API**

Über die Streams API kann eine Applikation als Stream Processor fungieren. Es holt sich den Input-Stream aus einem oder mehreren Topics, verarbeitet sie und schreibt den Output in ein oder mehrere Topics. Auf die genau Architektur für Stream Processing wird nochmal unter **Streaming Architektur** eingegangen. Im folgenden ist ein sehr einfaches Beispiel gegeben.  Hier wird der Wert des eingehenden Schlüssel-Werte-Paars so umgewandelt, dass er nun die länge des Strings ursprünglichen Wertes als String enthält. Input für diesen Stream ist ``"my-topic"`` und der umgewandelte Datensatz wird an das Topic ``"my-output-topic"`` verschickt.

````java
Properties props = new Properties();
props.put(StreamsConfig.APPLICATION_ID_CONFIG, "my-stream-processing-application");
props.put(StreamsConfig.BOOTSTRAP_SERVERS_CONFIG, "localhost:9092");
props.put(StreamsConfig.DEFAULT_KEY_SERDE_CLASS_CONFIG, Serdes.String().getClass());
props.put(StreamsConfig.DEFAULT_VALUE_SERDE_CLASS_CONFIG, Serdes.String().getClass());

StreamsBuilder builder = new StreamsBuilder();
builder.<String, String>stream("my-topic").mapValues(value -> String.valueOf(value.length())).to("my-output-topic");

KafkaStreams streams = new KafkaStreams(builder.build(), props);
streams.start();
````

**Connector API**

Die Connector API ermöglicht es wieder verwendbare Consumer und Publisher zu schreiben, die Topics mit existierenden Applikationen oder Datensystemen verbindet. Es gibt beispielsweise Connectors zu Datenbanken wie Mongo DB, die jede Änderung in der Datenbank erfassen.

**Admin API**

Die Admin API erlaubt das verwalten und betrachten der verschiedenen Topics, Partitionen und Broker und anderer Kafka Objekte.

### Streaming Architektur

Die Streaming Architektur im Kontext von Kafka dreht sich um die **Stream API**. 

### Kafka und Microservices



### Use Cases

* Use Cases
  * https://kafka.apache.org/uses
  * 
* Darstellung der wesentlichen Konzepte von Kafka
  * Producer, Consumer, Cluster, Topics, Partition, Broker
* Was ist im Zusammenhang mit Kafka die "Streaming Architecture"?
* Was ist KSQL?
  * https://www.confluent.io/product/ksql/
* Was ist Avro?
  *  https://www.confluent.io/blog/avro-kafka-data/
* Abgrenzung zu Big Data Science Software 
  * Apache Spark Streaming
  * Apache Hadoop
  * Apache HiveApache Cassandra
  * Apache Flink
  * Apache Beam
* Kafka in Microservice-Architekturen zur asynchronen Kommunikation