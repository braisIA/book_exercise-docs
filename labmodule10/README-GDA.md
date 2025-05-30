# Gateway Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

How does your implementation work?

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: 



### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- MqttClientPerformanceTest
  GDA MQTT Client Performance Test Results
  Tiempo de conexión y desconexión: 304 ms

  Prueba de Publicación con 10,000 mensajes

  - QoS 0: 0.846 s

  - QoS 1: 1.057 s → diferencia del 25% respecto a QoS 0

  - QoS 2: 1.956 s → diferencia del 131% respecto a QoS 0

  QoS más rápido: QoS 0

  QoS más lento: QoS 2
  
- CoapClientPerformanceTest

  CDA CoAP Client Performance Test Results (Java)


    POST - CON: 15866 ms  
    POST - NON: 16727 ms  
    
    Diferencia porcentual (CON vs NON): ≈ 5.42%  
    Más rápido: CON  
    Más lento: NON
  
-  DeviceDataManagerWithCommsTest.java
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
