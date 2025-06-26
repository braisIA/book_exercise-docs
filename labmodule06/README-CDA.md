# Constrained Device Application (Connected Devices)

## Lab Module 06

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Permite que el componente DeviceDataManager se conecte y se comunique con un broker MQTT utilizando la clase MqttClientConnector. Esto habilita la funcionalidad de publicar y suscribirse a mensajes MQTT, permitiendo enviar datos desde el dispositivo y recibir comandos para los actuadores. También maneja correctamente la conexión y desconexión del cliente MQTT al iniciar y detener el sistema, respectivamente.

How does your implementation work?

Inicialización Condicional de MQTT:

En el constructor de DeviceDataManager, se verifica una configuración (ENABLE_MQTT_CLIENT_KEY). Si está habilitada, se instancia un MqttClientConnector y se configura con un listener de mensajes de datos.

Conexión y Suscripción al Iniciar:

En el método startManager(), si MQTT está habilitado, el cliente MQTT se conecta al broker y se suscribe al tópico CDA_ACTUATOR_CMD_RESOURCE, que recibe comandos para actuadores.

Publicación de Datos:

Cuando se reciben datos de sensores o del sistema, se publican aguas arriba a través del cliente MQTT usando publishMessage().

Desconexión y Cancelación de Suscripción al Detener:

En stopManager(), el cliente MQTT se desuscribe del tópico de comandos y se desconecta del broker, liberando recursos.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/braisIA/python-components/commit/ecbc2967d4029d6d1e10671238ab827225cc4472


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

- MqttClientConnectorTest
- MqttClientControlPacketTest
- 

EOF.
