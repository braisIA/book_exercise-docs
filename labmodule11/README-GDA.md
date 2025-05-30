# Gateway Device Application (Connected Devices)

## Lab Module 11

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Mi implementación permite conectar un dispositivo embebido (CDA) con una aplicación de puerta de enlace (GDA) y, desde allí, transmitir datos hacia un servicio en la nube utilizando el protocolo MQTT. Específicamente, los datos generados por el CDA, como lecturas de sensores o métricas de rendimiento del sistema (CPU, memoria, etc.), se envían al GDA, que a su vez los publica en tópicos específicos del proveedor cloud.

How does your implementation work?

El flujo de funcionamiento es el siguiente:

El CDA genera datos (como temperatura, uso de CPU o memoria) y los envía al GDA mediante MQTT o CoAP.

El GDA recibe estos datos y los gestiona a través de su clase DeviceDataManager, que detecta el tipo de datos recibido.

Si el cliente cloud está habilitado (enableCloudClient = true), el GDA usa la clase CloudClientConnector, que:

Se conecta al broker MQTT del proveedor cloud (por ejemplo, Ubidots).

Publica los datos en tópicos específicos configurados en el archivo PiotConfig.props.

Los mensajes se publican en formato JSON, transformados a partir de objetos SensorData o SystemPerformanceData.

La conexión y publicación se hacen de forma robusta utilizando MqttClientConnector como backend MQTT, con soporte para autenticación, conexión segura y configuración de QoS.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/braisIA/java-components/tree/practica11


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- 
- 
- 

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- 
- 
- 

EOF.
