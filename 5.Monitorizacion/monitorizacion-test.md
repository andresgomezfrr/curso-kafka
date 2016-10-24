1. ¿Qué métricas son críticas a nivel de host en un Broker?
  * Ninguna de las anteriores es correcta.
  * % espacio en disco y % páginas cacheadas
  * % espacio en disco y % número de hist en la caché
  * número de hits en la caché y % páginas cacheadas

2. Si queremos solucionar problemas con el % de ocupación del espacio en disco, debemos:
  * Todas las afirmaciones son correctas.
  * Configurar correctamente las propiedades de las políticas de limpiado.
  * Añadir nuevos brokers al sistema y repartir las particiones.
  * Añadir nuevos discos duros a la maquina donde se encuentra el Broker.

3. ¿Cuando el sistema es estable y se encuentra en estado estacionario, que representación debe tener el % de espacio en disco en una gráfica temporal?
  * Creciente y decreciente.
  * Decreciente.
  * Creciente.
  * Constante.

4. ¿Cual es el valor ideal de páginas en la caché?
  * El valor ideal es próximo a 100.
  * El valor ideal es próximo a 0.
  * El valor debe estar oscilando continuamente entre 0 y 100.
  * Ninguna de las anteriores.

5. Un descenso de los hist en la cache puede indicar:
  * Todas las anteriores son correctas.
  * Una mayor tasa de producción.
  * Existen consumidores releyendo algún topic desde el principio.
  * Los consumidores tienen LAG.

6. Cual de las siguientes métricas nos indican que existen replicas que están fuera de sincronía:
  * UnderReplicatedPartitions
  * ReplicasOutSync
  * OfflinePartitionsCount
  * OutOfSyncReplicatedPartitions

7. ¿Dónde deberíamos buscar la métrica **OfflinePartitionsCount**?
  * En el broker que es controller.
  * En cualquier Broker de Kafka.
  * En algún broker que no sea un controller.
  * En los consumidores.

8. ¿Qué valor indica una alerta para la métrica **ActiveControllerCount**?
  * Un valor igual a 0.
  * Un valor inferior a 0.
  * Un valor superior a 1.
  * Un valor igual a 1.

9. ¿Cuál de las siguientes métricas nos muestra una posible perdida de datos?
  * UncleanLeaderElectionPerSec
  * ActiveControllerCount
  * OfflinePartitionsCount
  * UnderReplicatedPartitions

10. ¿Qué representa el LAG en un consumidor?
  * El número de mensajes que le quedan por leer de una partición.
  * El tiempo en ms que tarda en recibir los mensajes desde el Broker.
  * El tiempo que tarda en asentir que un mensaje ha sido procesado.
  * El número de mensajes que le quedan por leer de un topic.

11. ¿Qué podemos hacer descender el LAG de un grupo de consumidores?
  * Todas las afirmaciones son correctas.
  * Incrementar el número de particiones.
  * Levantar más instancias con el mismo grupo de consumidores.
  * Incrementar el número de bytes consumidos por nuestra aplicación.

12. ¿Qué herramienta proporciona Kafka para determinar el LAG de un consumidor?
  * kafka-consumer-groups.sh
  * kafka-consumer-offset.sh
  * kafka-topics.sh
  * kafka-console-consumer.sh

13. ¿Que variable de entorno debemos exportar si queremos que el Broker configure automáticamente los flags de JMX?
  * JMX_PORT
  * JMX_FLAGS
  * JMX_METRICS
  * BROKER_JMX

14. Si queremos que el broker active el servicio de JMX en una dirección IP concreta que flag debemos utilizar:
  * -Djava.rmi.server.hostname
  * -Djava.jmx.server.hostname
  * -Djava.rmi.server.address
  * -Djava.jmx.server.address

15. ¿Qué es lo que no podemos hacer con Yahoo Kafka Manager UI?
  * JMX polling de los consumidores.
  * Crear topics con configuración.
  * JMX polling de los brokers.
  * Comprobar el LAG de los consumidores.
