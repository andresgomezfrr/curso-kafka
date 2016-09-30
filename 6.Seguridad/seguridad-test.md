1. ¿Cúal de las siguientes medidas no proporciona Kafka para conseguir seguridad?
  * Autenticación usando SSL.
  * Encriptación usando SSL.
  * Encriptación usando HTTPS.
  * Autorización de lecturas y escrituras.

2. ¿Dónde se almacena la clave privada del broker?
  * truststore del broker.
  * keystore de todos los brokers.
  * keystore del broker.
  * truststore de todos los brokers.

3. ¿Cuántas claves privadas se necesitan?
  * Una por cada maquina donde se encuentre un broker.
  * Una para todas las maquinas.
  * Una por cada cliente.
  * Ninguna de las anteriores.

4. ¿El certificado del CA donde se almacena?
  * truststore del broker.
  * keystore de todos los brokers.
  * keystore del broker.
  * truststore de todos los brokers.

5. ¿Qué necesitamos para generar el certificado firmado?
  * Certificate-Request, CA-Key, CA-Certificate
  * Private-Key, CA-Key, CA-Certificate
  * Private-Key, Certificate-Request, CA-Key, CA-Certificate
  * CA-Key, CA-Certificate

6. Finalmente en el keystore y truststore del broker tendremos:
  * **Keystore:** CA-Cert, Cert-Signed. **Truststore:** CA-Cert
  * **Keystore:** CA-Cert, Cert-Signed, Private-Key **Truststore:** CA-Cert
  * **Keystore:** CA-Cert, Cert-Signed.
  * **Keystore:** CA-Cert, Cert-Signed, Private-Key. **Truststore:** CA-Cert, Cert-Signed

7. Para conseguir encriptación entre los brokers y los clientes, en el lado del cliente únicamente debemos tener:
  *  **Truststore:** CA-Cert
  *  **Truststore:** CA-Cert, Cert-Signed
  *  **Keystore:** CA-Cert
  *  No necesitamos nada.

8. Como podemos configurar en un broker varios métodos de conexión:
  * No es posible configurar varios métodos de conexión.
  * Usando la propiedad **advertised.listeners**.
  * Usando la propiedad **listeners**.
  * Usando ambas propiedades.

9. Qué propiedad es necesario configurar en los brokers para requerir la autenticación de los clientes:
  * security.protocol=requested
  * security.protocol=required
  * ssl.client.auth=requested
  * Ninguna de las anteriores.

10. ¿Dónde se debe almacenar el certificado firmado del cliente para conseguir un correcta autenticación?
  * En el truststore de los brokers.
  * En el keystore de los brokers.
  * En ambos.
  * No hace falta el certificado firmado del cliente.
