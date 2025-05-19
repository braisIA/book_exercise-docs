# Gateway Device Application (Connected Devices)

## Lab Module 07

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do?

Mi implementación crea un cliente MQTT que puede conectarse y desconectarse de un broker MQTT local. Además, permite suscribirse a tópicos, publicar mensajes con diferentes niveles de calidad de servicio (QoS 1 y QoS 2), y manejar la comunicación completa de control de paquetes MQTT (como PUBACK, PUBREC, PUBREL y PUBCOMP). También implementa un mecanismo para enviar y recibir pings al broker para mantener viva la conexión. Finalmente, incluye pruebas automatizadas que verifican que estas funcionalidades básicas operan correctamente.

How does your implementation work?

La implementación utiliza la clase MqttClientConnector que encapsula la lógica para interactuar con un broker MQTT usando la librería cliente MQTT de Java. El cliente primero intenta conectarse al broker en tcp://localhost:1883. Una vez conectado, puede suscribirse a un tópico específico para recibir mensajes publicados ahí. También puede publicar mensajes en ese tópico usando diferentes QoS, lo que asegura la entrega con distintos niveles de garantía (QoS 1 asegura entrega al menos una vez, QoS 2 asegura entrega exactamente una vez). Durante la conexión, el cliente envía automáticamente paquetes ping (PINGREQ) para mantener la conexión activa y recibir respuestas (PINGRESP). La implementación maneja internamente la recepción y procesamiento de mensajes entrantes y la confirmación de entrega mediante los paquetes de control MQTT. Las pruebas automatizadas ejecutan estos pasos y validan que cada función (conexión, publicación, suscripción, desconexión y ping) se ejecute correctamente sin errores.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/braisIA/java-components/commit/9a72ed985ae90a2a4c7823ccde3d87fb0c64e733


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- MqttClientControlPacketTest
- MqttClientConnectorTest
- 

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- MqttClientConnectorTest/testPublishAndSubscribe
- MqttClientConnectorTest/testConnectAndDisconnect
- 

EOF.
