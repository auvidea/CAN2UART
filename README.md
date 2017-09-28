# Project CAN2UART <br /> 


***Version: v.1.0*** <br />

***Authors: Daniel Wahl, Florian Dederichs*** <br />

***Environment  : Atollic TrueSTUDIO(R)*** <br />

***COPYRIGHT(C) : 2017 Auvidea GmbH*** <br />
   
   ***CAN2UART** is free software: you can redistribute it and/or modify* <br />
   *it under the terms of the GNU General Public License as published by* <br />
   *the Free Software Foundation, either version 3 of the License, or* <br />
   *(at your option) any later version.* <br />
   
   ***CAN2UART** is distributed in the hope that it will be useful,* <br />
   *but **WITHOUT ANY WARRANTY**; without even the implied warranty of* <br />
   *MERCHANTABILITY or FITNESS FOR A **PARTICULAR PURPOSE**.  See the* <br />
   *GNU General Public License for more details.* <br />
   
   *You should have received a copy of the GNU General Public License* <br />
   *along with AutoQuad.  If not, see (http://www.gnu.org/licenses/).* <br />
   
   ***Copyright (C) 2017 Auvidea GmbH*** <br />
   
   
   ***Copyright � 2015 STMicroelectronics International N.V.. All rights reserved.*** <br />

   *Redistribution and use in source and binary forms, with or without modification,* <br />
   *are permitted, provided that the following conditions are met:* <br />

   *1.	Redistribution of source code must retain the above copyright notice,* <br />
        *this list of conditions and the following disclaimer.* <br />
   *2.	Redistributions in binary form must reproduce the above copyright notice,* <br />
        *this list of conditions and the following disclaimer in the documentation* <br />
        *and/or other materials provided with the distribution.* <br />
   *3.	Neither the name of STMicroelectronics nor the names of other contributors* <br />
        *to this software may be used to endorse or promote products derived from* <br />
        *this software without specific written permission.* <br />
   *4.	This software, including modifications and/or derivative works of this* <br />
        *software, must execute solely and exclusively on microcontroller or* <br />
        *microprocessor devices manufactured by or for STMicroelectronics.* <br />
   *5.	Redistribution and use of this software other than as permitted under* <br />
        *this license is void and will automatically terminate your rights under* <br />
        *this license.* <br />

   ***THIS SOFTWARE IS PROVIDED BY STMICROELECTRONICS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS,*** <br />
   ***IMPLIED OR STATUTORY WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF*** <br />
   ***MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NON-INFRINGEMENT OF THIRD PARTY*** <br />
   ***INTELLECTUAL PROPERTY RIGHTS ARE DISCLAIMED TO THE FULLEST EXTENT PERMITTED BY LAW.*** <br />
   ***IN NO EVENT SHALL STMICROELECTRONICS OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT,*** <br />
   ***INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,*** <br />
   ***PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;*** <br />
   ***OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,*** <br />
   ***WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)*** <br />
   ***ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY*** <br />
   ***OF SUCH DAMAGE.*** <br />
   
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
    Sends messages from UART to CAN or CAN to CAN<br />
    
 - LED default mode: flashing LED <br /> 

  /src/ <br />

  ../main: main part of can2uart software <br />

  ../can: used for transmitting messages over can <br />

  ../i2c: handle i2c messages <br />

  ../rcc: handles system messages <br />

  ../usart: same as can but for uart <br />




