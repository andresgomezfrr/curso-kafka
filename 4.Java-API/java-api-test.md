1.  En la dependencia que añadimos al pom.xml del proyecto. ¿Cuál es el artifacId?
  * kafka
  * kafka_2.0.11
  * kafka-clients
  * apache-kafka

2. Cuando se crea un JAR con un proyecto con maven, utilizamos el comando:
  * mvn package
  * maven package
  * mvn compile
  * maven compile

3. ¿Qué clase se utiliza para crear un nuevo mensaje para su envío?
  * ProducerRecord
  * KafkaMessage
  * KafkaRecord
  * ProducerMessage

4. A la hora de enviar un mensaje podemos indicar:
  * topic, clave, valor
  * topic, partición, clave, valor
  * topic, valor
  * Todas son correctas.

5. Cuándo leemos un mensaje. ¿Cuál es la clase que usamos para procesarlo?
  * ConsumerMessage
  * ConsumerRecord
  * KafkaMessage
  * KafkaRecord

6. ¿Qué método de clase *KafkaConsumer** utilizamos cuando queremos leer de un topic?
  * read
  * seek
  * subscribe
  * assign

7. ¿Qué método de la clase *KafkaConsumer* debemos utilizar para obtener el mapa de particionado?
  * partitionsMap
  * listTopics
  * partitions
  * listPartitions

8. ¿Qué método de la clase *KafkaConsumer* debemos utilizar si queremos consumir de algunas particiones específicamente?
  * read
  * seek
  * subscribe
  * assign

9. ¿Cuál es la utilidad del método **seek** de la clase *KafkaConsumer*?
  * Especificar de que partición queremos leer.
  * Indicar el offset de cada partición por el que el consumidor comenzara a leer.
  * Se podría coincidir la misma utilidad con el método **assign**.
  * Todas las afirmaciones son correctas.

10. ¿Para que sirve el método **committed** de la clase *KafkaConsumer*?
  * Para hacer commits manualmente.
  * Para consultar el último commit para una partición de un topic.
  * Para borrar el último commit para una partición de un topic.
  * Ninguna de las anteriores.

11. El método **commitSync** de la clase *KafkaConsumer*:
  * Se utiliza para hacer commit manuales, de todas las particiones.
  * Se utiliza para hacer commit manuales de un offset en concreto.
  * Realiza commits de forma sincronía antes de continuar leyendo.
  * Todas son correctas.

13. ¿Qué clase debemos usar para implementar un productor que transforme de Map a Json String?
  * Serializer<Map<String, Object>>
  * Serializer<String>
  * Deserializer<Map<String, Object>>
  * Deserializer<String>

14. ¿Qué clase debemos usar para implementar un consumidor que transforme de Json String a Map?
  * Serializer<Map<String, Object>>
  * Serializer<String>
  * Deserializer<Map<String, Object>>
  * Deserializer<String>

15. ¿Qué clase se usa dentro de un **Partitioner** para descubrir las particiones de un topic?
  * Topic
  * Cluster
  * El método KafkaConsumer.listTopics()
  * Ninguna de las anteriores.
