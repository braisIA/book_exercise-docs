# Constrained Device Application (Connected Devices)

## Lab Module 03

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Crea una instancia del DeviceDataManager, el cual se encarga de manejar los datos de sensores, actuadores y rendimiento del sistema. Inicia y detiene el ciclo de funcionamiento de estos componentes utilizando los métodos startManager y stopManager. Elimina referencias directas al SystemPerformanceManager dentro de la app principal para centralizar su gestión desde DeviceDataManager.

How does your implementation work?

En la clase ConstrainedDeviceApp, se crea una instancia de DeviceDataManager durante la inicialización con self.dataMgr = DeviceDataManager().
Al ejecutar startApp(), se llama a self.dataMgr.startManager(), lo que inicia internamente los gestores de sensores, actuadores y rendimiento del sistema. Cuando se detiene la aplicación con stopApp(), se ejecuta self.dataMgr.stopManager() para detener todos los gestores.
Dentro de DeviceDataManager, se instancian y configuran los componentes SensorAdapterManager, ActuatorAdapterManager y SystemPerformanceManager.
Cada uno de estos componentes llama a setDataMessageListener(self) para que puedan enviar sus datos a DeviceDataManager, quien se encarga de procesarlos

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/braisIA/python-components/commit/ee40c48e168db9593a98960478ef0217f423ee15

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ActuatorDataTest
- SensorDataTest
- SystemPerformanceDataTest
- HumiditySensorSimTaskTest
- PressureSensorSimTaskTest
- TemperatureSensorSimTaskTest
- HumidifierActuatorSimTaskTest
- HvacActuatorSimTaskTest
- SensorAdapterManagerTest
- ActuatorAdapterManagerTest

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- DeviceDataManagerNoCommsTest
- ConstrainedDeviceAppTest
  

EOF.
