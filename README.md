Parts Required:
1 esp32 30pin
2 Taxnele DDS669 Bidirectional meter
2 TTL to RS485
1 SSD1306 128x64 oled display
2 momentary push buttons

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
    
RS485 Connections:
TTL to RS485 module(1) -> DDS669(1)Loads -> DDS669(2)Solar
TTL to RS485 module(2) -> Soyosource Inverter

note: you need to change the address of one of the dds669 meter to 2 used for metering solar Inverter and Load... solar to address 2 and load to address 1 since they share one rs485 connection in parallel...
