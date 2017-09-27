# README

/src/

main

can
used for transmitting messages over can

uart
same as can but for uart

i2c
handle i2c messages 

Current features
  - canmode 0:
    Loopback mode 
    Sends received messages from can back to sender in reverted letters
    e.g:
    ID: 123 DLC: 8 DATA: aa bb cc dd ee ff 00 11 99
    ID: 123 DLC: 8 DATA: 99 11 00 ff ee dd cc bb aa
    (this is a simplyfied output, yours may differ from what you use as a interpreter)
    
 - canmode 1:
    Normal mode
    Sends messages from UART to CAN
    
 - LED default mode: flashing LED

Planned features
