1. ¿Qué métricas son críticas a nivel de host en un Broker?
  * % espacio en disco y % páginas cacheadas
  * % espacio en disco y % número de hist en la caché
  * número de hits en la caché y % páginas cacheadas
  * Ninguna de las anteriores es correcta.

2. Si queremos solucionar problemas con el % de ocupación del espacio en disco, debemos:
  * Todas las afirmaciones son correctas.
  * Configurar correctamente las propiedades de las políticas de limpiado.
  * Añadir nuevos brokers al sistema y repartir las particiones.
  * Añadir nuevos discos duros a la maquina donde se encuentra el Broker.

3. ¿Cuando el sistema es estable y se encuentra en estado estacionario, que representación debe tener el % de espacio en disco en una gráfica temporal?
  * Decreciente.
  * Creciente.
  * Constante.
  * Creciente y decreciente.

4. ¿Cual es el valor ideal de páginas en la caché?
  * El valor ideal es próximo a 0.
  * El valor ideal es prixmo a 100.
  * El valor debe estar oscilando continuamente entre 0 y 100.
  * Ninguna de las anteriores.

5. Un descenso de los hist en la cache puede indicar:
  * Una mayor tasa de producción.
  * Existen consumidores releyendo algún topic desde el principio.
  * Los consumidores tienen LAG.
  * Todas las anteriores son correctas.

6. Cual de las siguientes métricas nos indican que existen replicas que estan fuera de sincronia:
  * ReplicasOutSync
  * OfflinePartitionsCount
  * UnderReplicatedPartitions
  * OutOfSyncReplicatedPartitions

7. ¿Dónde deberiamos buscar la métrica **OfflinePartitionsCount**?
  * En cualquier Broker de Kafka.
  * En algún broker que no sea un controller.
  * En el broker que es controller.
  * En los consumidores.

8. ¿Qué valor indica una alerta para la métrica **ActiveControllerCount**?
  * Un valor inferior a 0.
  * Un valor superior a 1.
  * Un valor igual a 1.
  * Un valor igual a 0.

9. ¿Cuál de las siguientes métricas nos muestra una posible perdida de datos?
  * UncleanLeaderElectionPerSec
  * ActiveControllerCount
  * OfflinePartitionsCount
  * UnderReplicatedPartitions

10. ¿Qué representa el LAG en un consumidor?
  * El tiempo en ms que tarda en recibir los mensajes desde el Broker.
  * El número de mensajes que le quedan por leer de una partición.
  * El tiempo que tarda en asentir que un mensaje ha sido procesado.
  * El número de mensajes que le quedan por leer de un topic.

11. ¿Qué podemos hacer descender el LAG de un grupo de consumidores?
  * Incrementar el número de particiones.
  * Levantar más instancias con el mismo grupo de consumidores.
  * Incrementar el número de bytes cosumidos por nuestra aplicación.
  * Todas las afirmaciones son correctas.

12. ¿Qué herramienta proporciona Kafka para determinar el LAG de un consumidor?
  * kafka-consumer-groups.sh
  * kafka-consumer-offset.sh
  * kafka-topics.sh
  * kafka-console-consumer.sh

13. ¿Que variable de entorno debemos exportar si queremos que el Broker configure automaticamente los flags de JMX?
  * JMX_FLAGS
  * JMX_METRICS
  * JMX_PORT
  * BROKER_JMX

14. Si queremos que el broker active el servicio de JMX en una dirección IP concreta que flag debemos utilizar:
  * -Djava.rmi.server.hostname
  * -Djava.jmx.server.hostname
  * -Djava.rmi.server.address
  * -Djava.jmx.server.address

15. ¿Qué es lo que no podemos hacer con Yahoo Kafka Manager UI?
  * Crear topics con configuración.
  * JMX polling de los brokers.
  * JMX polling de los consumidores.
  * Comprobar el LAG de los consumidores.
