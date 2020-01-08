![Actions Status](https://github.com/Landoop/kafka-connect-common/workflows/CI/badge.svg)
[<img 
src="https://img.shields.io/badge/latest%20release-v01.1.9-blue.svg?label=latest%20release"/>](http://search.maven.org/#search%7Cga%7C1%7Cg%3A%22com.datamountaineer%22%20AND%20a%3A%22kafka-connect-common%22)
Kafka Connect Common is in Maven, include it in your connector.


# Releases


| Version | Confluent Version |Kafka| Kcql Version |
| ------- | ----------------- |-----|--------------|
|1.1.9|5.0.0|1.1.0|2.8.4
|1.1.8|5.0.0|1.1.0|2.8.4
|1.1.5|5.0.0|1.1.0|2.8.2
|1.1.5|4.1.0|1.1.0|2.8.2
|1.1.4|4.1.0|1.1.0|2.8.2
|1.1.3|4.1.0|1.1.0|2.8
|1.1.2|4.1.0|1.1.0|2.7
|1.1.1|4.1.0|1.1.0|2.5.1
|1.1.0|4.1.0|1.1.0|2.5.1
|1.0.9|4.0.0|1.0.0|2.5.1
|1.0.8|4.0.0|1.0.0|2.5.1
|1.0.7|4.0.0|1.0.0|2.5.1
|1.0.6|4.0.0|1.0.0|2.5.1
|1.0.5|4.0.0|1.0.0|2.5.1
|1.0.4|4.0.0|1.0.0|2.5.1
|1.0.3|4.0.0|1.0.0|2.4
|1.0.2|4.0.0|1.0.0|2.4
|1.0.1|4.0.0|1.0.0|2.4
|1.0.2|4.0.0|1.0.0|2.4
|1.0.1|4.0.0|1.0.0|2.4
|1.0.0|4.0.0|1.0.0|2.4

```bash
#maven
<dependency>
	<groupId>com.datamountaineer</groupId>
	<artifactId>kafka-connect-common</artifactId>
	<version>1.1.9</version>
</dependency>

#sbt
libraryDependencies += "com.datamountaineer" % "kafka-connect-common" % "1.1.9"

#gradle
'com.datamountaineer:kafka-connect-common:1.1.9'
```

# kafka-connect-common
Common components used across the datamountaineer kafka connect connectors.

## Packages

### Config

#### SSLConfigConext
Contains class for SSL Context configuration for supplied trust and keystores.

### Offsets

The offset handler retrieves, from Kafka the stored offset map per source partition.

### Queues

Helper methods to drain LinkedBlockingQueues.

### Sink

Contains Writer and KeyBuilder classes.

### DbWriter

Defines the contract for inserting a new row for the connect sink record.

#### KeyBuilder

* Builds the new record key for the given connect SinkRecord.
* Builds a new key from the payload fields specified.

### Schemas

* RestService to integrate with the Schema Registry

#### PayloadFields
Works out the fields and their mappings to be used when inserting a new row.

### ConvertUtil

Converts source and sink records to JSON and Avro and back.

### StructFieldsExtractor

Extracts fields from a SinkRecord Struct based on a specified set of provided columns.
