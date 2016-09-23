1. ¿Cuándo es de utilidad ejecutar el comando **kafka-preferred-replica-election.sh**?
  * Cada cierto tiempo.
  * Al crear un topic.
  * Al añadir o eliminar algun broker.
  * Todas son ciertas.

2. ¿Cuál es el uso del comando **kafka-mirror-maker.sh**?
  * Copiar un topic en otro.
  * Crear replicas de una partición.
  * Copiar datos entre clusters.
  * Copiar datos de un broker a otro.

3. ¿Cuál herramienta usariamos si queremos verificar que todas las replicas de un topic tienen los mismos datos?
  * kafka-offsets-checker.sh
  * kafka-replica-verification.sh
  * kafka-offsets-verification.sh
  * kafka-replica-checker.sh

4. ¿La herramienta **kafka-replica-verification.sh** nos permite verificar los datos desde un instante de tiempo?
  * No, podemos indicar desde que offset queremos realizar la verificación.
  * Si utilizando la opción --time y indicando la fecha en formato ISO.
  * Si utilizando la opción --time y indicando la fecha en formato timestamp milisegundos.
  * Ninguna de las anteriores.

5. ¿Cuál es la necesidad de utilizar el comando **kafka-reassign-partitions.sh**?
  * Kafka no asigna particiones a los topics nuevos de manera automatica.
  * Para poder crear replicas de las particiones.
  * Para elegir donde asignar las particiones de cada topic.
  * Todas las anteriores son correctas.

6. ¿Cuál es la utilidad de la propiedad **controlled.shutdown.enable**?
  * Evitar perdidas de datos.
  * Reducir el tiempo de no disponibilidad de las particiones.
  * Escribir los mensajes pendintes al disco y asegurar que otro nodo obtiene el líder de sus particiones.
  * Todas las afirmaciones son correctas.

7. Si tenemos un fichero en formato json con el siguiente contenido:
```json
{"topics":[{"topic":"topic1"},{"topic":"topic2"}], "version":1}
```
y ejecutamos el comando:
```
bin/kafka-reassign-partitions.sh --zookeeper localhost:2181 --topics-to-move-json-file topics-move.json --broker-list "2" --generate
```
  * Los topics (*topic1* y *topic2*) moveran sus particiones al broker con id 2.
  * Los topics (*topic1* y *topic2*) moveran sus replicas al broker con id 2.
  * Se generará un json que nos servira para mover todas las particiones del topic al broker 2.
  * Se generará un json que nos servira para mover todas las replicas del topic al broker 2.

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
  {"version":1, "partitions":[{"topic":"topic1", "partition":0, "replicas":[0,1]}]}
  ```
  *
  ```json
  {"version":1, "partitions":[{"topic":"topic1", "partition":0, "replicas":[2]}]}
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

10. Si quisieramos crear una replica de la particion 0 del topic1 que se ya encontraba en el broker con id 0, en el broker con id 1. ¿Cual sería el JSON que debemos utilizar?
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
  * balance
  * elect
  * set-partitions
  * set-replication-factor

12. ¿Cuál es la utilidad del modulo reorder?
  * Elegir una partición líder.
  * Ordena las particiones asegurandose que todos los brokers tengan el mismo número de replicas.
  * Ordena las particiones asegurandose que todos los brokers tenga el mismo número de particiones líderes.
  * Ninguna de las anteriores.

13. ¿Cuándo no podemos usar la opción **even** del módulo balance?
  * Cuando el número de los brokers es impar.
  * Cuando el número de particiones no es un múltiplo de los brokers.
  * Cuando el número de particiones es impar.
  * Todas son correctas.

14. ¿Cuál es el módulo correcto para borrar un broker del cluster?
  * trim
  * remove
  * delete
  * Todos son validos.

15. ¿Qué diferencia existe entre el módulo **reorder** y **elect**?
  * **reorder** reordena las particiones para conseguir el mejor balance entre los líderes, mientras que **elect** ejecuta una elección de líderes en el orden que Kafka haya decidido.
  * **elect** reordena las particiones para conseguir el mejor balance entre los líderes, mientras que **reorder** ejecuta una elección de líderes en el orden que Kafka haya decidido.
  * **reorder** y **elect** realizan la misma función.
  * Ninguna de las anteriores es correcta.
