Modified Arduino Ethernet Library
==========

Modified [Arduino](http://arduino.cc) Ethernet v1.1.0 library. This modification adds EthernetClent.remoteIP() and EthernetClient.setClientTimeout() functions and removes the delay from Ethernet.begin().

This library supports Wiznet W5100, W200, and W500 Ethernet controllers with automatic detection. Thanks to [Fede85](https://github.com/Fede85).


<a id="installation"></a>
#### Installation
- This library is only compatible with Arduino versions 1.5 and up. If you are using Arduino IDE 1.0.x then select the Arduino-IDE-1.0.x branch instead.
- Download the most recent version of the modified Ethernet library here: https://github.com/per1234/EthernetMod/archive/W5x00.zip
- Open the Arduino IDE
- Sketch > Include Library > Add ZIP Library... > select the downloaded file > Open

<a id="usage"></a>
#### Usage
`EthernetClient.remoteIP()` - See examples/ChatServer.ino for demonstration of using remoteIP. Thanks to [Philgaskin on the Arduino forum](http://forum.arduino.cc/index.php?topic=82416.0).
- Returns: The IP address of the remote connection.
  - Type: IPAddress

I have removed the delay in Ethernet.begin() so you may need to add a delay in your sketch if it is not reliably initializing the Ethernet controller.

For all the standard functions included in the library see the official Arduino Ethernet documentation: http://arduino.cc/en/reference/ethernet
The read() function in the Client class inherits from Stream so the stream functions are also available, see the Arduino Stream documentation: http://arduino.cc/en/Reference/Stream


#### License
This library is free software; you can redistribute it and/or
modify it under the terms of the GNU Lesser General Public
License as published by the Free Software Foundation; either
version 2.1 of the License, or (at your option) any later version.

This library is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
Lesser General Public License for more details.

You should have received a copy of the GNU Lesser General Public
License along with this library; if not, write to the Free Software
Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA 02110-1301 USA

