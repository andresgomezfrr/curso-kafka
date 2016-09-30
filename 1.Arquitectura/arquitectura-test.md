1. ¿Cuál es la utilidad de ZooKeeper en un cluster de Kafka?
  * Almacenar los mensajes enviados a Kafka.
  * Autodescubrimiento de los productores y consumidores.
  * Sincronización de los brokers, elección de líder de las particiones y almacenamiento de configuración especifica.
  * Balancear el envío de mensajes sobre los distintos Brokers.

2. ¿Dónde guardan los consumidores los offsets que ya han procesado?
  * Los consumidores guardan sus offsets en ZooKeeper.
  * Los consumidores guardan sus offsets localmente.
  * Los consumidores no guardan sus offsets.
  * Los consumidores guardan los offsets en un topic especial.

3. ¿Cuántas instancias con el mismo **group.id** se pueden tener simultáneamente?
  * Todas las que se quieran.
  * El número máximo es igual al número de replicas de un topic.
  * El número máximo es igual al número de particiones de un topic.
  * El número máximo es igual al número total de particiones de todos los topic de los que consuma.

4. Cuando el productor envía un mensaje ...

  * Lo envía a todas las particiones.
  * Lo envía a todas las replicas.
  * Lo envía únicamente a la partición líder.
  * Lo envía a todos los brokers.

5. Si tenemos un cluster formado por 5 brokers. ¿Cuál es el número de topics máximo que podemos tener?

  * 5, uno por cada broker.
  * Depende del número de particiones por topic.
  * Depende del número de replicas de cada partición.
  * El número de brokers no es un limitante para la creación de topics.

6. Si tenemos un cluster formado por 5 brokers. ¿Cuál es el número máximo de particiones que podemos tener?

  * Depende del número de topics.
  * Depende del factor de replicación.
  * El número de particiones no esta relacionado con el número de broker.
  * 1 partición por cada broker, ya que los líderes tienen que estar repartidos.

7. Si tenemos un cluster formado por 5 broker. ¿Cuál es el factor de replicación máximo?

  * Igual al número de broker.
  * Depende del número de topics.
  * El factor de replicación no esta relacionado con el número de brokers.
  * Depende del número de las particiones que se van a replicar.

8. Los mensajes en Kafka estan formado principalmente por ...
  * Unicamente un payload, ya que es lo que se envía al broker, la clave sola es usada para particionar.
  * Una clave y un payload.
  * Ninguna de las anteriores es correcta.
  * Un timestamp, una clave y un payload.

9. Si tenemos un topic con un factor de replicación de 3 y tenemos un total de 10 brokers. ¿Cuántos brokers podemos perder antes de no poder utilizar el topic?
  * Deberíamos de perder los 10 brokers, ya que las replicas se mueven de un broker a otro automáticamente.
  * Deberíamos perder los brokers donde se encuentran las replicas. Un total de 3 brokers.
  * Deberíamos perder el broker donde se encuentra la partición leader. Un total de 1 broker.
  * Ninguna de las anteriores.

10. En Kafka un offset ...
  * Es un identificador único que identifica a un mensaje en todo el cluster.
  * Es único en todo el cluster y nunca se repite.
  * Identifican a un mensaje en una partición.
  * Todas son correctas.

11. Un mensaje con una misma clave siempre es enviado a la misma partición.
  * La afirmación es correcta.
  * Depende del particionado que se este utilizando.
  * Depende de en que broker se encuentra la partición.
  * La afirmación es correcta siempre que únicamente exista un cliente produciendo esa clave.

12. En un cluster:
  * Se deberían de tener tantos servidores de ZooKeeper como brokers.
  * Los brokers pueden tener identificadores iguales.
  * Siempre hay que tener un número impar de brokers.
  * Ninguna es correcta.

13. En un cluster de Kafka:
  * El número de ZooKeeper no debería ser mayor de 5, ya que a mayor número empeora el rendimiento.
  * El número de ZooKeeper debe ser impar para asegurar quorum.
  * El número de ZooKeeper no esta relacionado con el número de brokers.
  * Todas las afirmaciones son correctas.

14. Los topics con log compaction activado son de gran utilidad para:
  * Hacer backups de caches del tipo clave/valor.
  * Reducir el tamaño de los topics, ya que crecerían indefinidamente.
  * Ninguna de las anteriores es correcta.
  * Mejoran el rendimiento a la hora de producir mensajes debido a que esta compactado.

15. Si tenemos un topic que tiene configurado el parámetro **cleanup.policy=compact** y sabemos que el topic contiene los mensajes que están en la tabla. Cuando se ejecuta la política de limpiado, ¿cuál es el resultado del topic?
  * El topic es borrado por completo.
  * Se mantienen todos los valores.
  * Se quedan los offsets: 4,5,6
  * Se quedan los offsets: 5,8,9

| Offset         | Clave          |      Mensaje  |
| :------------- | :------------- |:------------- |
| 4              | K1             | V1            |
| 5              | K2             | V2            |
| 6              | K3             | V1            |
| 7              | K1             | V5            |
| 8              | K3             | V6            |
| 9              | K1             | V4            |
