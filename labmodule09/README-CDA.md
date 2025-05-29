# Constrained Device Application (Connected Devices)

## Lab Module 09

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Crea un cliente CoAP en Python que puede enviar solicitudes CoAP estándar (GET, PUT, POST, DELETE) a un servidor CoAP (por ejemplo, la GDA). Además, puede usar la funcionalidad OBSERVE para suscribirse a cambios en recursos remotos. Todo esto permite que el CDA se comunique eficientemente con la GDA a través del protocolo CoAP, integrándose dentro del sistema como una capa de cliente para manejar las peticiones y respuestas CoAP.

How does your implementation work?

La implementación funciona creando una clase CoapClientConnector que encapsula la lógica para enviar solicitudes CoAP usando una biblioteca Python (como CoAPthon3 o aiocoap). Esta clase implementa la interfaz IRequestResponse que define métodos para enviar cada tipo de solicitud (GET, PUT, POST, DELETE) y para iniciar observaciones en recursos del servidor. Cuando se invoca un método, la clase construye y envía la solicitud CoAP apropiada al servidor GDA y maneja la respuesta o notificaciones de observación. Además, esta clase se integra con el DeviceDataManager para que otras partes de la aplicación puedan usar fácilmente las capacidades CoAP.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/braisIA/python-components/commit/194b2ee71ea6df272327e1f40c72d5384ca29e94



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
