# Gateway Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Asegura que cada uno de estos datos esté correctamente encapsulado en sus respectivas clases (ActuatorData, SensorData, SystemPerformanceData), con los métodos adecuados para obtener, establecer y manipular estos valores. Además, he creado las pruebas unitarias para verificar que:

Los valores por defecto de cada clase son correctos.

Los valores se pueden modificar correctamente.

El comportamiento de los métodos es adecuado y se ajusta a lo esperado (por ejemplo, la correcta serialización a formato CSV).

En resumen, mi implementación crea y prueba las clases para manejar los datos esenciales de los sensores y actuadores en un entorno IoT, lo cual es el objetivo principal del Lab 5.


How does your implementation work?

Cada clase de datos tiene atributos privados que almacenan la información. Estos atributos incluyen valores como el comando en el caso de ActuatorData, o la utilización de CPU, disco y memoria en SystemPerformanceData. Las clases proporcionan métodos getter y setter para acceder y modificar estos valores. En algunas clases, también hay una bandera booleana que indica si los datos corresponden a una respuesta, y el método toString() convierte los datos a un formato legible.
BaseIotData:
Las clases mencionadas anteriormente heredan de BaseIotData, que proporciona funcionalidades comunes como un nombre para el objeto y un código de estado. La clase BaseIotData tiene un método toString() que se sobrescribe en las clases hijas para añadir los detalles específicos de cada clase.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/braisIA/java-components/commit/9374a3c7c649231b710ac7374d95ce2f7d11c463


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
