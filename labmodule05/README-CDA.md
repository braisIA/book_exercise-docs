# Constrained Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
Permite convertir los objetos de datos del sistema como SensorData, ActuatorData y SystemPerformanceData a formato JSON y viceversa. Esto facilita el intercambio de datos entre el CDA y otros componentes del sistema (como el GDA), utilizando un formato estandarizado y fácil de interpretar.

How does your implementation work?
Utilizo la clase DataUtil en el CDA para manejar la transformación de objetos a JSON y de JSON a objetos. Específicamente, se usan funciones que aprovechan la librería json de Python para serializar los atributos del objeto (__dict__) y reconstruirlos luego a partir de un string JSON. Esto garantiza que los datos puedan ser enviados, almacenados o leídos por otros servicios que también comprendan el mismo formato.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/braisIA/python-components/commit/0d2005f9ee8ded6e41b0786053ff0ab261450001


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
