# Constrained Device Application (Connected Devices)

## Lab Module 04

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
Mi implementación permite la integración de emuladores de sensores en el sistema de gestión de sensores. Dependiendo de una configuración, que se obtiene desde un archivo de configuración, el sistema puede operar utilizando datos simulados o utilizando emuladores para simular el comportamiento de los sensores reales.

Si el emulador está habilitado, el sistema carga dinámicamente los módulos de emuladores de los sensores de humedad, presión y temperatura. Si el emulador no está habilitado, la implementación generará datos simulados a través de un generador de datos (SensorDataGenerator), creando una representación artificial de los valores de los sensores.

How does your implementation work?

En la inicialización de la clase SensorAdapterManager, se lee un valor de configuración llamado ENABLE_EMULATOR_KEY desde un archivo de configuración para determinar si se deben utilizar emuladores o no. Esto se guarda en la variable self.useEmulator.
Si self.useEmulator es True, el sistema carga dinámicamente los emuladores de sensores (humedad, presión y temperatura) usando la función import_module. Esto se realiza dentro del método _initEnvironmentalSensorTasks().
Para cada tipo de sensor, se importa el módulo correspondiente y se crea una instancia del emulador de ese sensor.
Si self.useEmulator es False, se generan datos simulados utilizando la clase SensorDataGenerator. Los rangos de valores para cada sensor (humedad, presión y temperatura) se obtienen de la configuración.
Se utilizan estos rangos para generar datos de sensores simulados. Luego, se instancian los adaptadores de los sensores simulados (como HumiditySensorSimTask, PressureSensorSimTask y TemperatureSensorSimTask) con los datos generados.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/braisIA/python-components/commit/a5463cd1c77bdb4a1244a5fbd01acbbd82755c7a


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.



### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- HumidityEmulatorTaskTest.py
- PressureEmulatorTaskTest.py
- TemperatureEmulatorTaskTest.py
- SenseHatEmulatorQuickTest.py
- HumidifierEmulatorTaskTest.py
- HvacEmulatorTaskTest.py
- LedDisplayEmulatorTaskTest.py
- SensorEmulatorManagerTest.py
- ActuatorEmulatorManagerTest.py
  

EOF.
