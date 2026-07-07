Parts Required:
1 esp32 30pin
2 Taxnele DDS669 Bidirectional meter
2 TTL to RS485

Connection:
    SOYOSOURCE
        |
     DDS669(2)
        |
Grid  <- ->  DDS669(1)  <--> LOADS

UART pins of ESP32 -> TTL to RS485 module then RS485's to Meter and Inverter :
  - id: uart_meter
    tx_pin: GPIO26 
    rx_pin: GPIO27 

  - id: uart_inverter
    tx_pin: GPIO33 
    rx_pin: GPIO32

