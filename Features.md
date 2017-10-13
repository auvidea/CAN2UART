**Current features** <br />
  - canmode 0: <br />
    Loopback mode (only for test purposes) <br />
    Sends received messages from can back to sender in reverted letters <br />   
    
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

**How to set up UART on a Ubuntu Distribution using PUTTY** <br />

```
apt install putty
sudo putty
```

- the configuration window of putty will open
- make sure that it is set up as follows:
  - serial line: /dev/<uart port> (e.g. ttyUSB0)
  - Speed: 115200
  - connection type: Serial
- 

*canmode 0* <br />

- was implemented only for test purposes, but may be used as pleased <br />
- This mode sets CAN2UART into a loopback mode. So that all messages send from can will be mirrored and send back to the sender. <br />
- e.g. <br />
  ```
  cansend can0 123#abcdef001122
  ```
  ```
  candump can0
  can0 [6] AB CD EF 00 11 22
  can0 [6] 22 11 00 EF CD AB 
  ```
<br />
*canmode 1* <br />

- can be used with a sender either connected to CAN or UART interface <br />
- make sure you enabled canmode 1, by default CAN2UART is set to canmode 0 <br />
  ```
  canmode 1
  ```
- once set, you can enter messages into putty console <br />
- a cansend command is created as follows: <br />
  ```
  cansend 291 4 0x4f 0x0b 0xca 0x87
  ```
  - messages send from UART are received on CAN interface
- it is also possible to receive messages, you will see only the last messages sent <br />
  ```
  candump
  ```
  - this command gets can messages from a buffer, so it is possible that the command needs to be used multiple times before the last message is seen. <br />
  - it may only receive messages from CAN interface
  
    
