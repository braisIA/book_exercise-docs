# Constrained Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Integramos funcionalidades de monitoreo del rendimiento del sistema. Específicamente, hemos creado y conectado el SystemPerformanceManager a la aplicación principal del CDA, permitiéndole iniciar y detener tareas de monitoreo del rendimiento. Además, hemos implementado la clase base para las tareas de utilización del sistema y clases específicas para monitorear el uso de la CPU y la memoria.

How does your implementation work?

La implementación comienza inicializando el SystemPerformanceManager dentro de ConstrainedDeviceApp. Este administrador es responsable de programar y gestionar las tareas de monitoreo del rendimiento del sistema. Dos tareas de utilidad principales, SystemCpuUtilTask y SystemMemUtilTask, recopilan métricas de utilización de la CPU y la memoria, respectivamente. Estas tareas heredan de BaseSystemUtilTask, que proporciona funcionalidades comunes. El SystemPerformanceManager inicia y detiene estas tareas como parte del ciclo de vida del CDA.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/braisIA/python-components/commit/a6f989334970771b60058aed1d2e93996225746f

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- SystemPerformanceManagerTest
- SystemCpuUtilTaskTest
- SystemMemUtilTaskTest

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- ConstrainedDeviceAppTest
- 
- 

EOF.
