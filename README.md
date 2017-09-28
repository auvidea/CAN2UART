# Project CAN2UART 


***Version: v.1.0*** 

***Authors: Daniel Wahl, Florian Dederichs***

***Environment  : Atollic TrueSTUDIO(R)***

***COPYRIGHT(C) : 2017 Auvidea GmbH***
   
   ***CAN2UART** is free software: you can redistribute it and/or modify*
   *it under the terms of the GNU General Public License as published by*
   *the Free Software Foundation, either version 3 of the License, or*
   *(at your option) any later version.*
   
   ***CAN2UART** is distributed in the hope that it will be useful,*
   *but **WITHOUT ANY WARRANTY**; without even the implied warranty of*
   *MERCHANTABILITY or FITNESS FOR A **PARTICULAR PURPOSE**.  See the*
   *GNU General Public License for more details.*
   
   *You should have received a copy of the GNU General Public License*
   *along with AutoQuad.  If not, see (http://www.gnu.org/licenses/).*
   
   ***Copyright (C) 2017 Auvidea GmbH***
   
   
   ***Copyright � 2015 STMicroelectronics International N.V.. All rights reserved.***

   *Redistribution and use in source and binary forms, with or without modification,
   *are permitted, provided that the following conditions are met:

   *1.	Redistribution of source code must retain the above copyright notice,*
        *this list of conditions and the following disclaimer.
   *2.	Redistributions in binary form must reproduce the above copyright notice,*
        *this list of conditions and the following disclaimer in the documentation*
        *and/or other materials provided with the distribution.*
   *3.	Neither the name of STMicroelectronics nor the names of other contributors*
        *to this software may be used to endorse or promote products derived from* 
        *this software without specific written permission.*
   *4.	This software, including modifications and/or derivative works of this*
        *software, must execute solely and exclusively on microcontroller or* 
        *microprocessor devices manufactured by or for STMicroelectronics.*
   *5.	Redistribution and use of this software other than as permitted under*
        *this license is void and will automatically terminate your rights under*
        *this license.* 

   ***THIS SOFTWARE IS PROVIDED BY STMICROELECTRONICS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS,***
   ***IMPLIED OR STATUTORY WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF***
   ***MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NON-INFRINGEMENT OF THIRD PARTY***    
   ***INTELLECTUAL PROPERTY RIGHTS ARE DISCLAIMED TO THE FULLEST EXTENT PERMITTED BY LAW.*** 
   ***IN NO EVENT SHALL STMICROELECTRONICS OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT,*** 
   ***INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,*** 
   ***PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;***
   ***OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,***
   ***WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)***
   ***ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY***
   ***OF SUCH DAMAGE.***
   
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




