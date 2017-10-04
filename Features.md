**Current features** <br />
  - canmode 0: <br />
    Loopback mode (only for test purposes) <br />
    Sends received messages from can back to sender in reverted letters <br />
    e.g: <br />
    ID: 123 DLC: 8 DATA: aa bb cc dd ee ff 00 11 99 <br />
    ID: 123 DLC: 8 DATA: 99 11 00 ff ee dd cc bb aa <br />
    (this is a simplyfied output, yours may differ from what you use as a interpreter) <br />
    
 - canmode 1: <br />
    Normal mode <br />
    Sends messages from UART to CAN or CAN to CAN <br />
    
 - LED default mode: flashing LED <br /> 

  /src/ <br />

  ../main: main part of can2uart software <br />

  ../can: used for transmitting messages over can <br />

  ../i2c: handle i2c messages <br />

  ../rcc: handles system messages <br />

  ../usart: same as can but for uart <br />
  
  **How to use:** <br />
 <br />
- Any software to send messages over UART or CAN may be used <br />

- In our example we tested CAN2UART as follows: <br />
  - We tested our device on Ubuntu 16.04 in combination with a TX1. <br />
  - PUTTY was used to send messages over UART or to set canmode. <br />
  - We used cansend and candump commands from CAN-UTILS for CAN. <br />


-canmode 0- <br />

- was implemented only for test purposes, but may be used as pleased <br />
- This mode sets CAN2UART into a loopback mode. So that all messages send from can will <br />
  be mirrored and send back to the sender. <br />
- E.g. <br />
  ```
  cansend can0 123#abcdef001122
  ```
  ```
  candump can0
  can0 [6] 22 11 00 ef cd ab 
  ```
