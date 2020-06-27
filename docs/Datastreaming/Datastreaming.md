# Data Streaming

*Malte Riechmann*

## Was ist Data Streaming

Um Data Streaming zu beschreiben wird oft die Analogie eine

## Warum Data Streaming?

*was ist der Vorteil*

*Wo kommt es zum einsatz*

## Eigenschaften

* kontinuierlicher Datenfluss an Datensätzen (sehr klein)
* Können mehrere Datenquellen besitzen
* mit der Verarbeitung muss nicht auf die vollständige Übertragung der daten gewartet werden 
* Ende des Flusses muss während der Übertragung noch nicht bekannt sein
  * Daten können auch kontinuierlich generiert werden
* Datenrate kann variieren
  * Muss bei der Verarbeitung/Speicherung beachtet werden
* Sequenzieller Zugriff
  * Daten werden fortlaufend verarbeitet

## Abgrenzung

* Batch-Verarbeitung vs. Stream-Verarbeitung
  * Batch: Verarbeitung eines Datenbündels, generiert Ergebnisse zu Kompletten Datensatz
  * Stream: Mini Datenbündel, Ergebnisse müssen für jeden Datensatz angepasst werden 
* Messaging vs. Streaming
  * Abgrenzung zu Messaging Systemen
    *  https://www.theseattledataguy.com/kafka-vs-rabbitmq-why-use-kafka/
  * Strategien zur Verarbeitung von Message Queues
    * http://www.doxsey.net/blog/strategies-for-working-with-message-queues

## Use Cases

* Allgemein
* Konkrete Anwendungsfälle
  * Darstellung des Themengebiets "Big Data" / Stream Processing
    * https://www.confluent.io/wp-content/uploads/2016/08/Making_Sense_of_Stream_Processing_Confluent_1.pdf
  * Internet of Things (Übertragung von Sensor Daten zur Analyse)
  * Audio-/Video-Streaming
  * Marketing (Werbung basierend auf den Nutzer-Aktionen)
  * Verteiltes Maschinelles Lernen

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
3. Und das Prozessieren von Streams sobald sie auftauchen

### Aufbau

*TODO:* Bild einfügen

Wie im vorherigen erwähnt läuft Kafka als Cluster auf einem oder mehreren Servern. Das Cluster speichert Ströme von Datensätzen unter sogenannten Topics. Diese Topics sind des Weiteren 

* ist eine verteilte Streaming Plattform
  * Es läuft als ein Cluster auf einem oder mehreren Servern
  * 

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