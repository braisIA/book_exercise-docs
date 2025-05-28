# Gateway Device Application (Connected Devices)

## Lab Module 08

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Mi implementación crea un servidor CoAP en el Gateway Device App (GDA) que permite manejar comunicaciones CoAP con otros componentes del sistema IoT, específicamente con el Client Device App (CDA). Para ello:

Implementa una clase CoapServerGateway que aloja y gestiona varios recursos CoAP.

Crea tres controladores de recursos CoAP especializados:

UpdateSystemPerformanceResourceHandler para recibir datos de rendimiento del sistema mediante solicitudes PUT.

UpdateTelemetryResourceHandler para recibir datos de telemetría de sensores también vía PUT.

GetActuatorCommandResourceHandler para enviar comandos de actuadores al CDA usando el mecanismo CoAP OBSERVE.

Actualiza el DeviceDataManager para que pueda registrar listeners para manejar eventos de actuadores, facilitando así la interacción entre los datos gestionados y las peticiones CoAP.

Permite que el servidor CoAP gestione tanto recursos creados internamente como recursos proporcionados externamente (por ejemplo, desde DeviceDataManager).

En resumen, la implementación proporciona un servidor CoAP funcional y extensible que conecta el GDA con el CDA a través de recursos CoAP para la gestión de datos y comandos.



How does your implementation work?

El servidor CoAP (CoapServerGateway) se inicializa y arranca, agregando a su estructura varios recursos CoAP basados en clases handler específicas.

Cada recurso handler extiende un recurso genérico (GenericCoapResourceHandler) y está especializado para procesar mensajes CoAP de tipos concretos (PUT para actualizar datos o GET/OBSERVE para comandos).

Cuando el servidor recibe una solicitud CoAP para alguno de estos recursos:

El handler correspondiente procesa la solicitud, extrae los datos (por ejemplo, SensorData o SystemPerformanceData).

Invoca métodos en DeviceDataManager para almacenar o actualizar la información recibida o para registrar observadores.

En el caso del recurso de comandos, el handler usa el mecanismo OBSERVE para notificar eventos al CDA cuando hay nuevos comandos de actuadores.

DeviceDataManager mantiene referencias a listeners que reciben estos eventos o datos para reaccionar o propagar la información a otros componentes.

Esto permite una comunicación bidireccional y basada en eventos entre el GDA y el CDA, usando el protocolo ligero CoAP, ideal para IoT.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: 


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
