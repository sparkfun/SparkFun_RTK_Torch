---
icon: simple/arduino
---

## Feedback Loop
The simplest way to test the UART interface is with just a jumper *(wire)* and looping transmission data from the **TX** GPIO pin; back into the **RX** GPIO pin. For this example, users are free to utilize any method or hardware they have to connect the **RX** and **TX** GPIO pins together. However, we recommend some IC hooks for a temporary connection.


??? note "Optional Hardware"
	<div class="grid cards" markdown>

	-   <a href="https://www.sparkfun.com/products/501">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/3/4/1/00501-1.jpg)
		</figure>

		---

		**IC Hook Test Leads**<br>
		CAB-00501</a>


	-   <a href="https://www.sparkfun.com/products/9741">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/3/6/9/6/09741-01.jpg)
		</figure>

		---

		**IC Hook with Pigtail**<br>
		CAB-09741</a>


	-   <a href="https://www.sparkfun.com/products/9194">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/6/3/4/JumperWire-Female-01-L.jpg)
		</figure>

		---

		**Jumper Wires Premium 6" Mixed Pack of 100**<br>
		PRT-09194</a>


	-   <a href="https://www.sparkfun.com/products/116">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/0/6/00116-02-L.jpg)
		</figure>

		---

		**Break Away Headers - Straight**<br>
		PRT-00116</a>


	-   <a href="https://www.sparkfun.com/products/9044">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/4/0/7/09044-02-L.jpg)
		</figure>

		---

		**Jumper - 2 Pin**<br>
		PRT-09044</a>

	</div>


After users have jumpered the GPIO pins and uploaded the example code, they will need to open the [**Serial Monitor**](https://docs.arduino.cc/software/ide-v2/tutorials/ide-v2-serial-monitor/) in the Arduino IDE. Any entries that are sent through the message textbox, should be re-transmitted back into the **Serial Monitor** by the jumpered GPIO pins.


=== "`MultiSerial.ino`"
	Users can find this sketch in the **File** > **Examples** > **04.Communication** > **MultiSerial** drop-down menu.

	??? code "`MultiSerial.ino`"
		<iframe class='arduino-sketch-iframe' src='https://create.arduino.cc/example/builtin/04.Communication%5CMultiSerial/MultiSerial/preview?embed&snippet' style='height:752px;width:100%;margin:10px 0' frameborder='0'></iframe>


=== "`SerialPassthrough.ino`"
	Users can find this sketch in the **File** > **Examples** > **04.Communication** > **SerialPassthrough** drop-down menu.

	??? code "`SerialPassthrough.ino`"
		<iframe class='arduino-sketch-iframe' src='https://create.arduino.cc/example/builtin/04.Communication%5CSerialPassthrough/SerialPassthrough/preview?embed&snippet' style='height:752px;width:100%;margin:10px 0' frameborder='0'></iframe>



## Peripheral Device


### GNSS/GPS Module
For GNSS receivers, we recommend that the [TinyGPSPlus Arduino library](https://github.com/mikalhart/TinyGPSPlus) be utilized to parse the NMEA sentences from the module. Once the [library is installed in the Arduino IDE](https://docs.arduino.cc/software/ide-v2/tutorials/ide-v2-installing-a-library/), users will find several example sketches listed in the **File** > **Examples** > **TinyGPSPlus** > drop-down menu. We recommend the following examples for getting started with a GNSS receiver:

- `DeviceExample.ino`
- `FullExample.ino`


!!! tip
	Below, are a few tips for users to start working with the TinyGPSPlus Arduino library. However, for more details, users should refer to the [documentation for the TinyGPSPlus Arduino library](http://arduiniana.org/libraries/tinygpsplus/).

	??? code "Define Parameters"
		When utilizing the examples in the TinyGPSPlus Arduino library, users may need to define and/or modify a few parameters. The baud rate for the GNSS receiver should be configured based upon the information presented in the datasheet.

		For the RA6M5 Thing Plus, users have two options for configuring the serial port on the `RX` and `TX` GPIO pins:

		- In the examples, they can continue to implement the SoftwareSerial library and update the values of `RX` and `TX` GPIO pins in the code
		- Otherwise, users can remove the SoftwareSerial library implementation; and replace it with `Serial1` UART port


		<div class="grid cards" markdown>

		-   **Baud Rate**

			---

			Check the datasheet or product manual for the default baud rate of the GPS receiver; if necessary, replace the value in the example:


				static const uint32_t GPSBaud = {==4800==};
				static const uint32_t GPSBaud = {++115200++};


			In some cases, the datasheet may be inaccurate or the module's configuration was previously changed. In which case, the most common rates to try are:

			- `4800` bps
			- `9600` bps
			- `115200` bps


		-   **Update GPIO Pins**

			---

			Replace the values for the `RX` (`D20`) and `TX` (`D21`) GPIO pins for those on the RA6M5 Thing Plus:

				static const int RXPin = {--4--}, TXPin = {--3--};
				static const int RXPin = {++20++}, TXPin = {++21++};


		-   **Utilize `Serial1` Port**

			---

			Remove the implementation of the SoftwareSerial library implementation


				{--#include <SoftwareSerial.h>--}

				{--static const int RXPin = 4, TXPin = 3;--}
				{--SoftwareSerial ss(RXPin, TXPin);--}


			Then, replace the SoftwareSerial objects with `Serial1` class


				void setup()
				{
					Serial.begin(115200);
					{--ss--}{++Serial1++}.begin(GPSBaud);


				void loop()
				{
					while ({--ss--}{++Serial1++}.available() > 0)
						if (gps.encode({--ss--}{++Serial1++}.read()))
							displayInfo();

		</div>


	??? abstract "Hardware Assembly"
		Connecting a GNSS receiver to a microcontroller is relatively straight forward. Users must provide power to the module through the `PWR`/`VCC` and `GND` pins on the board. Additionally, the `TX` pin from the GNSS receiver, should be connected to the `RX` pin of the microcontroller. This will allow the module to transmit the NMEA sentences to the microcontroller.

		<center>

		| Thing Plus | GPS Module |
		| :---: | :-------------: |
		| `3V3` | `VCC` or `PWR`  |
		| `GND` | `GND`           |
		| `RX` (`D21`)  | `TX`    |
		| `TX` (`D20`)  | ---     |

		</center>


	??? question "Satellite Fix"
		As with all GNSS receivers, the module's antenna must have a clear view of the sky *(it can't operate inside a building)* to receive signal from the GNSS constellation. In addition, the GNSS receiver must acquire a fix on its position, before it starts transmitting complete NMEA sentences *(with all the data)*.




??? note "Optional Hardware"
	<div class="grid cards" markdown>

	-   <a href="https://www.sparkfun.com/products/14414">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/2/3/4/0/14414-SparkFun_GPS_Breakout_-_XA1110__Qwiic_-01.jpg)
		</figure>

		---

		**SparkFun GPS Breakout - XA1110 (Qwiic)**<br>
		GPS-14414</a>


	-   <a href="https://www.sparkfun.com/products/19166">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/8/7/8/8/19166-GPS_Module_-_GP1818MK__56_Channel_-04.jpg)
		</figure>

		---

		**GPS Module - GP1818MK (56 Channel)**<br>
		GPS-19166</a>


	-   <a href="https://www.sparkfun.com/products/9741">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/3/6/9/6/09741-01.jpg)
		</figure>

		---

		**IC Hook with Pigtail**<br>
		CAB-09741</a>


	-   <a href="https://www.sparkfun.com/products/11375">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/7/1/2/0/11375-Hook-Up_Wire_-_Assortment__Solid_Core__22_AWG_-01.jpg)
		</figure>

		---

		**Hook-Up Wire - Assortment (Stranded, 22 AWG)**<br>
		PRT-11375</a>


	-   <a href="https://www.sparkfun.com/products/9325">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/8/7/3/09325_9161-Solder_Lead_Free_-_100-gram_Spool-01.jpg)
		</figure>

		---

		**Solder Lead Free - 100-gram Spool**<br>
		TOL-09325</a>


	-   <a href="https://www.sparkfun.com/products/24063">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/4/3/8/5/KIT-24063-PINECIL-Soldering-Iron-Kit-Feature.jpg)
		</figure>

		---

		**PINECIL Soldering Iron Kit**<br>
		KIT-24063</a>

	</div>



After users have connected their GNSSS module and uploaded the example code, they will need to open the [**Serial Monitor**](https://docs.arduino.cc/software/ide-v2/tutorials/ide-v2-serial-monitor/) in the Arduino IDE to view the data. Users should begin to see the data parsed by the TinyGPSPlus Arduino library, from the NMEA sentences transmitted from the GNSS receiver.



=== "`DeviceExample.ino`"
	Users can find this sketch in the **File** > **Examples** > **TinyGPSPlus** > **DeviceExample** drop-down menu.

	??? code "`DeviceExample.ino`"
		```cpp
		--8<-- "https://raw.githubusercontent.com/mikalhart/TinyGPSPlus/master/examples/DeviceExample/DeviceExample.ino"
		```


=== "`FullExample.ino`"
	Users can find this sketch in the **File** > **Examples** > *TinyGPSPlus** > **FullExample** drop-down menu.

	??? code "`FullExample.ino`"
		```cpp
		--8<-- "https://raw.githubusercontent.com/mikalhart/TinyGPSPlus/master/examples/FullExample/FullExample.ino"
		```



### DA14531MOD
For the DA14531MOD, users can interface with the module through the `Serial2` UART port of the RA6M5 Thing Plus. The firmware on the module implements the CodeLess AT command platform. This means, users can easily configure the BLE connectivity of the board with a few AT commands. *For more details, please refer to the [section with the DA14531MOD examples](../example-codeless/).*

