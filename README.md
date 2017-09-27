# README
Current features
  - Messages can be sent from UART to CAN
  - Simple Mode: messages are simply sent from UART to CAN
  - Loopback mode: messages sent to CAN2UART module will be sent back to sender in mirrored letters 
    e.g. 123 0a bb cc dd bb 0a
         123 0a bb dd cc bb 0a
  
Planned features
