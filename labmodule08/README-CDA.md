# Constrained Device Application (Connected Devices)

## Lab Module 08

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Mi implementación configura y ejecuta un servidor CoAP personalizado utilizando Python, específicamente con la biblioteca CoAPthon3. Este servidor expone varios recursos que representan dispositivos IoT simulados, como sensores y actuadores. También desarrollé pruebas automatizadas e integración con el cliente Californium, permitiendo enviar solicitudes CoAP (como GET o POST) desde un cliente externo para probar el comportamiento del servidor.

En resumen, mi implementación permite enviar y recibir mensajes CoAP entre un cliente y un servidor para simular la comunicación en un entorno IoT.

How does your implementation work?

La implementación se basa en una clase CoapServerAdapter que extiende y configura un servidor CoAP utilizando la librería CoAPthon3. Dentro de esta clase, se registran recursos con rutas específicas como:

/PIOT/ConstrainedDevice/SystemPerfMsg para mensajes de rendimiento del sistema,

/PIOT/ConstrainedDevice/ActuatorCmd/HumidifierActuator para comandos a actuadores.

Cada recurso tiene un handler que gestiona peticiones GET o POST, según el caso.

Durante las pruebas, se puede arrancar el servidor usando unittest, lo cual también permite automatizar su verificación. Luego, el cliente Californium, construido y ejecutado por separado en Java, envía solicitudes CoAP que son recibidas y procesadas por mi servidor Python.

Esto demuestra la interoperabilidad entre distintos entornos y lenguajes de programación mediante el protocolo CoAP.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/braisIA/python-components/commit/b713bb531deb1dc424d9fc9a9a26158c8c7a093c



### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- CoapClientToServerConnectorTest
- 
- 

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- CoapClientToServerConnectorTest/testConnectAndGetCon
- 
- 

EOF.
