# Gateway Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-GDA-* issues.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
Mi implementación gestiona el monitoreo del rendimiento del sistema, específicamente la utilización de la CPU y la memoria. En ella, se han creado clases para obtener estos valores de manera periódica, usando hilos programados que ejecutan tareas a intervalos regulares. La clase principal, SystemPerformanceManager, coordina el proceso, programando la obtención de la información sobre la CPU y la memoria a través de las clases SystemCpuUtilTask y SystemMemUtilTask, respectivamente. Los valores de utilización se registran mediante logs para su seguimiento y análisis.

How does your implementation work?

En el constructor de SystemPerformanceManager, se obtiene el intervalo de tiempo entre cada lectura de métricas desde un archivo de configuración. Se crean dos instancias de las clases SystemCpuUtilTask y SystemMemUtilTask, que se encargan de obtener los valores de utilización de la CPU y la memoria, respectivamente, utilizando la ejecución periódica del método handleTelemetry(), que obtiene los valores llamando a los métodos getTelemetryValue() de ambas clases.
Los valores obtenidos se registran en el log con un nivel de detalle adecuado, lo que permite hacer seguimiento del rendimiento del sistema. El método startManager() inicia la programación de las tareas periódicas, mientras que stopManager() detiene el servicio y cancela la tarea programada.

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
