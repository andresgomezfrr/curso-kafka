1. ¿Cuándo es de utilidad ejecutar el comando **kafka-preferred-replica-election.sh**?
  * Todas son ciertas.
  * Cada cierto tiempo.
  * Al crear un topic.
  * Al añadir o eliminar algún broker.

2. ¿Cuál es el uso del comando **kafka-mirror-maker.sh**?
  * Copiar datos entre clusters.
  * Copiar un topic en otro.
  * Crear réplicas de una partición.
  * Copiar datos de un broker a otro.

3. ¿Cuál herramienta usaríamos si queremos verificar que todas las replicas de un topic tienen los mismos datos?
  * kafka-replica-verification.sh
  * kafka-offsets-checker.sh
  * kafka-offsets-verification.sh
  * kafka-replica-checker.sh

4. ¿La herramienta **kafka-replica-verification.sh** nos permite verificar los datos desde un instante de tiempo?
  * Si utilizando la opción --time y indicando la fecha en formato timestamp milisegundos.
  * No, podemos indicar desde que offset queremos realizar la verificación.
  * Si utilizando la opción --time y indicando la fecha en formato ISO.
  * Ninguna de las anteriores.

5. ¿Cuál es la necesidad de utilizar el comando **kafka-reassign-partitions.sh**?
  * Todas las anteriores son correctas.
  * Kafka no asigna particiones a los topics nuevos de manera automática.
  * Para poder crear replicas de las particiones.
  * Para elegir donde asignar las particiones de cada topic.

6. ¿Cuál es la utilidad de la propiedad **controlled.shutdown.enable**?
  * Todas las afirmaciones son correctas.
  * Evitar pérdidas de datos.
  * Reducir el tiempo de no disponibilidad de las particiones.
  * Escribir los mensajes pendientes al disco y asegurar que otro nodo obtiene el líder de sus particiones.

7. Si tenemos un fichero en formato json con el siguiente contenido:
```json
{"topics":[{"topic":"topic1"},{"topic":"topic2"}], "version":1}
```
y ejecutamos el comando:
```
bin/kafka-reassign-partitions.sh --zookeeper localhost:2181 --topics-to-move-json-file topics-move.json --broker-list "2" --generate
```
  * Se generará un json que nos servirá para mover todas las particiones del topic al broker 2.
  * Los topics (*topic1* y *topic2*) moverán sus particiones al broker con id 2.
  * Los topics (*topic1* y *topic2*) moverán sus replicas al broker con id 2.
  * Se generará un json que nos servirá para mover todas las replicas (sin la leader) del topic al broker 2.

8. Si tenemos un topic (*topic1*) que tiene una única partición y utilizamos el siguiente comando:
```
bin/kafka-reassign-partitions.sh --zookeeper localhost:2181 --topics-to-move-json-file topics-move.json --broker-list "2" --generate
```
Utilizando el json:
```json
{"topics":[{"topic":"topic1"}], "version":1}
```
La salida en JSON del comando será la siguiente:
  *
  ```json
  {"version":1, "partitions":[{"topic":"topic1", "partition":0, "replicas":[2]}]}
  ```
  *
  ```json
  {"version":1, "partitions":[{"topic":"topic1", "partition":0, "replicas":[0,1]}]}
  ```
  *
  ```json
  {"version":1, "partitions":[{"topic":"topic1", "partition":0, "replicas":[0,1,2]}]}
  ```
  * Ninguna de las anteriores

9. ¿Cuál es la funcionalidad del siguiente JSON?
```json
{"version":1, "replicas":[
      {"topic":"topic1", "partition":0, "replicas":[5,6]},
      {"topic":"topic1", "partition":1, "replicas":[5,6]}
]}
```
  * El JSON no es correcto.
  * El JSON moverá las particiones 0 y 1 del topic (*topic1*) a los brokers con id: 5 y 6.
  * El JSON creará dos replica de las particiones 0 y 1 en los brokers 5 y 6.
  * Ninguna de las anteriores.

10. Si quisiéramos crear una replica de la partición 0 del topic1 que se ya encontraba en el broker con id 0, en el broker con id 1. ¿Cual sería el JSON que debemos utilizar?
  *
  ```json
  {"version":1, "partitions":[{"topic":"topic1", "partition":0, "replicas":[0,1]}]}
  ```
  *
  ```json
  {"version":1, "partitions":[{"topic":"topic1", "partition":0, "replicas":[1]}]}
  ```
  *
  ```json
  {"version":1, "partitions":[{"topic":"topic1", "partition":1, "replicas":[0]}]}
  ```
  *
  ```json
  {"version":1, "partitions":[{"topic":"topic1", "partition":0, "replicas":[0]}]}
  ```  
11. ¿Cuál no es un  módulo de la herramienta de LinkedIn **kafka-assigner**?
  * set-partitions
  * balance
  * elect
  * set-replication-factor

12. ¿Cuál es la utilidad del modulo reorder?
  * Ordena las particiones asegurando que todos los brokers tenga el mismo número de particiones líderes.
  * Elegir una partición líder.
  * Ordena las particiones asegurando que todos los brokers tengan el mismo número de replicas.
  * Ninguna de las anteriores.

13. ¿Cuándo no podemos usar la opción **even** del módulo balance?
  * Cuando el número de particiones no es un múltiplo de los brokers.
  * Cuando el número de los brokers es impar.
  * Cuando el número de particiones es impar.
  * Todas son correctas.

14. ¿Cuál es el módulo correcto para borrar un broker del cluster?
  * remove
  * trim
  * delete
  * Todos son validos.

15. ¿Qué diferencia existe entre el módulo **reorder** y **elect**?
  * **reorder** reordena las particiones para conseguir el mejor balance entre los líderes, mientras que **elect** ejecuta una elección de líderes en el orden que Kafka haya decidido.
  * **elect** reordena las particiones para conseguir el mejor balance entre los líderes, mientras que **reorder** ejecuta una elección de líderes en el orden que Kafka haya decidido.
  * **reorder** y **elect** realizan la misma función.
  * Ninguna de las anteriores es correcta.
