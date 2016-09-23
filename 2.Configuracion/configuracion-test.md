1. Si quisieramos cambiar la dirección del puerto donde ofrece el servicio el broker deberiamos modificar la propiedad:
  * advertised.port
  * listeners
  * advertised.listeners
  * listen.port

2. El espacio de los log se puede controlar en base a el:
  * Tiempo
  * Tamaño
  * Tiempo y Tamaño
  * Numero de mensajes

3. La propiedad **log.segment.bytes** es utilizada para:
  * Indicar el número maximo de bytes que se almacenan de una partición entre todos los ficheros de logs.
  * Indicar el tamaño máximo de un fichero de log.
  * Indicar el tamaño máximo de un topic.
  * Ninguna de las anteriores.

4. La propiedad **log.retention.bytes** es utilizada para:
  * Indicar el número maximo de bytes que se almacenan de una partición entre todos los ficheros de logs.
  * Indicar el tamaño máximo de un fichero de log.
  * Indicar el tamaño máximo de un topic.
  * Ninguna de las anteriores.

5. Si se configuran las propiedades **log.retention.hours** y **log.retention.bytes**:
  * Unicamente tiene efecto **log.retention.bytes**.
  * Unicamente tiene efecto **log.retention.hours**.
  * Ninguna de las dos tiene efecto y se utiliza la configuración por defecto.
  * Ambas tienen efecto y se aplicara la primera que se cumpla.

6. Las principales propiedades de un productor son:
  * bootstrap.server, key.serializer, value.serializer
  * bootstrap.server, key.deserializer, value.deserializer
  * zookeeper.server, key.serializer, value.serializer
  * zookeeper.server, key.deserializer, value.deserializer

7. Las principales propiedades de un consumidor son:
* bootstrap.server, key.serializer, value.serializer
* bootstrap.server, key.deserializer, value.deserializer
* zookeeper.server, key.serializer, value.serializer
* zookeeper.server, key.deserializer, value.deserializer

8. Si quisieramos que el broker nos devuelva el asentimiento cuando la partición haya escrito el mensaje debemos configurar:
  * La propiedad **ack** con valor **all**.
  * La propiedad **ack** con valor **1**.
  * La propiedad **ack** con valor **0**.
  * Ninguna de las anteriores es correcta.

9. Las opciones de compresión que proporciona Kafka son:
  * none, gzip, snappy y lz4
  * none, zip, snappy y lz4
  * none, gzip, snappy y tar
  * none, gzip y lz4

10. Si utilizamos la interfaz *Partitioner* para implementar un particionado personalizado, tendremos disponible para realizar el particionado:
  * El topic, la clave y el valor.
  * El topic y la clave.
  * La clave y la información del cluster.
  * El topic, la clave, el valor y la información del cluster.

11. Si quisieramos configurar Quotas de bytes leidos por cliente:
  * Deberiamos configurar correctamente el **cliend.id**
  * Deberiamos aplicar la configuración utilizando el script **kafka-configs.sh**
  * Añadir la configuración **consumer_byte_rate**.
  * Todas las afirmaciones son correctas.

12. Cuando se crea un topic sin indicar el número de particiones, ni el factor de replicación:
  * Se utiliza los valores 1 partición y factor de replicación igual a 1.
  * Se utilizan las propiedades por defecto definidas en la configuración a nivel de topic.
  * Se utilizan las propiedades por defecto configuradas en el fichero server.properties
  * Ninguna de las anteriores es correcta.

13. Para configurar las replicas de una partición:
  * Se utiliza el script **kafka-reassign-partitions.sh**
  * Hay que crear un fichero indicando en que brokers se quiere replicar cada partición.
  * Es necesario saber la dirección de ZooKeeper.
  * Todas las afirmaciones son correctas.

14. Para activar el log compaction:
  * Hay que activar unicamente la propiedad **log.cleaner.enable**
  * Hay que configurar la propiedad anterior e indicar a nivel de topic **cleanup.policy=compaction**
  * Hay que configurar la propiedad anterior e indicar a nivel de topic **cleanup.policy=compact**
  * Hay que configurar la propiedad anterior, pero no es necesario indicar la propiedad **cleanup.policy** ya que el valor por defecto es el de compactación.

15. Una vez se ha creado un topic:
  * No se puede aplicar nueva configuraciones.
  * Hay que recrear el topic para aplicar nuevas configuraciones.
  * Se pueden borrar configuraciones pero no añadir.
  * Las configuraciones se pueden añadir, cambiar y borrar.
