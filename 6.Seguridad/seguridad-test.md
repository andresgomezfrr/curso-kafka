1. ¿Cúal de las siguientes medidas no proporciona Kafka para conseguir seguridad?
  * Encriptación usando HTTPS.
  * Autenticación usando SSL.
  * Encriptación usando SSL.
  * Autorización de lecturas y escrituras.

2. ¿Dónde se almacena la clave privada del broker?
  * keystore del broker.
  * truststore del broker.
  * keystore de todos los brokers.
  * truststore de todos los brokers.

3. ¿Cuántas claves privadas se necesitan?
  * Una por cada maquina donde se encuentre un broker.
  * Una para todas las maquinas.
  * Una por cada cliente.
  * Ninguna de las anteriores.

4. ¿El certificado del CA dónde se almacena?
  * truststore de todos los brokers.
  * truststore del broker.
  * keystore de todos los brokers.
  * keystore del broker.

5. ¿Qué necesitamos para generar el certificado firmado?
  * Certificate-Request, CA-Key, CA-Certificate
  * Private-Key, CA-Key, CA-Certificate
  * Private-Key, Certificate-Request, CA-Key, CA-Certificate
  * CA-Key, CA-Certificate

6. Finalmente en el keystore y truststore del broker tendremos:
  * **Keystore:** CA-Cert, Cert-Signed, Private-Key **Truststore:** CA-Cert
  * **Keystore:** CA-Cert, Cert-Signed. **Truststore:** CA-Cert
  * **Keystore:** CA-Cert, Cert-Signed.
  * **Keystore:** CA-Cert, Cert-Signed, Private-Key. **Truststore:** CA-Cert, Cert-Signed

7. Para conseguir encriptación entre los brokers y los clientes, en el lado del cliente únicamente debemos tener:
  *  **Truststore:** CA-Cert
  *  **Truststore:** CA-Cert, Cert-Signed
  *  **Keystore:** CA-Cert
  *  No necesitamos nada.

8. ¿Cómo podemos configurar en un broker varios métodos de conexión?
  * Usando la propiedad **listeners**.
  * Usando ambas propiedades.
  * No es posible configurar varios metodos de conexión.
  * Usando la propiedad **advertised.listeners**.

9. Qué propiedad es necesario configurar en los brokers para requerir la autenticación de los clientes:
  * security.protocol=required
  * security.protocol=requested
  * ssl.client.auth=requested
  * Ninguna de las anteriores.

10. ¿Dónde se debe almacenar el certificado firmado del cliente para conseguir un correcta autenticación?
  * En el truststore de los brokers.
  * En el keystore de los brokers.
  * En ambos.
  * No hace falta el certificado firmado del cliente.

11. ¿Qué comando podemos usar para comprobar que Kafka esta usando SSL?
  * openssl s_client -debug -connect ${BROKER_KAFKA} -tls1
  * openssl s_server -debug -connect ${BROKER_KAFKA} -tls1
  * curl --flag=SSL -connect ${BROKER_KAFKA} -tls1
  * Ninguna de los anteriores.

12. ¿Qué configuración deberiamos aplicar en el broker para abrir una conexión SSL en el puerto 7777?
  * listeners=SSL://:7777
  * advertised.listeners=SSL://:7777
  * ssl.port=7777
  * Ninguno de los anteriores.

13. ¿Qué propiedad debemos configurar para habilitar el cifrado entre los Brokers?
  * security.inter.broker.protocol=SSL
  * security.broker.protocol=SSL
  * broker.protocol=SSL
  * broker.inter.protocol=SSL

14. ¿Qué propiedad debemos usar en los clientes para habilitar SSL?
  * security.protocol=SSL
  * No hace falta habilitar nada, el broker impone el protocolo a los clientes.
  * Unicamente es encesario indicar el keystore y se activara el SSL.
  * Ninguna de las anteriores.

15. ¿Porporciona Kafka una opción para controlar la autorización de lecturas y escrituras por clientes?
  * Si.
  * Si, pero unicamente si se usa una Kerberos.
  * No.
  * Si, pero los clientes deben usar SASL en lugar de SSL.
