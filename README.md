#Project CAN2UART 

**--Version: v.1.0
Authors: Daniel Wahl, Florian Dederichs
Environment  : Atollic TrueSTUDIO(R)
COPYRIGHT(C) : 2017 Auvidea GmbH--**
   *
   CAN2UART is free software: you can redistribute it and/or modify
   it under the terms of the GNU General Public License as published by
   the Free Software Foundation, either version 3 of the License, or
   (at your option) any later version.
   
   CAN2UART is distributed in the hope that it will be useful,
   but WITHOUT ANY WARRANTY; without even the implied warranty of
   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
   GNU General Public License for more details.*
   
   You should have received a copy of the GNU General Public License
   along with AutoQuad.  If not, see (http://www.gnu.org/licenses/).
   
   Copyright (C) 2017 Auvidea GmbH
   
   Third-party software is not provided by AUVIDEA GmbH and must be aquired seperatly. 
   This includes libraries providied by micro controllers to be used for can or uart.
   In this case STM32F0xx libraries. (http://www.st.com/content/st_com/en.html)
   
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

  /src/

  ../main: main part of can2uart software 

  ../can: used for transmitting messages over can

  ../i2c: handle i2c messages 

  ../rcc: handles system messages

  ../usart: same as can but for uart




