---
icon: material/bluetooth
---

## AT Commands
To help users get started with the [CodeLess™ AT commands](https://www.renesas.com/us/en/software-tool/smartbond-codeless-commands) for the DA14531MOD Bluetooth module, we have provided an `SerialPassthrough` example in our [*unofficial* Arduino library](../software_overview-arduino/#da14531mod-ble-module). Once programmed on the RA6M5 Thing Plus, the example allows users to directly interface with the DA14531MOD's UART port through the board's USB connection using a [serial terminal](https://learn.sparkfun.com/tutorials/112). Thereby, enabling users to experiment with the CodeLess AT commands and develop their own BLE connectivity solution. Users can find this sketch in the **File** > **Examples** > **SparkFun Renesas Codeless BLE** > **SerialPassthrough** drop-down menu.


??? code "`SerialPassthrough.ino`"
	```cpp
	--8<-- "https://raw.githubusercontent.com/sparkfun/SparkFun_Thing_Plus_RA6M5/main/Firmware/CodelessBLE/examples/SerialPassthrough/SerialPassthrough.ino"
	```


!!! serial "Serial Monitor"
	Users should configure the serial port with a baud rate at **57600 bps** and **enable the carriage return** on the transmissions.



## Demo - BLE Solution
While an Arduino library isn't necessary to utilize the [CodeLess™ AT commands](https://www.renesas.com/us/en/software-tool/smartbond-codeless-commands) for the DA14531MOD Bluetooth module, we have created an [*unofficial* Arduino library](./Firmware/CodelessBLE) to help users get started. Once the [library is installed in the Arduino IDE](../software_overview-arduino/#da14531mod-ble-module), users will find several example sketches listed in the **File** > **Examples** > **SparkFun Renesas Codeless BLE** drop-down menu. We recommend users check out the following examples that demonstrate a basic BLE connectivity solution:


- `codelessBLE_peripheral.ino`
- `codelessBLE_central.ino`


In order to operate the `codelessBLE_peripheral.ino` and `codelessBLE_central.ino` examples, users will need two [RA6M5 Thing Plus boards](https://www.sparkfun.com/products/24243), [Qwiic OLED Display](https://www.sparkfun.com/products/24606), [Qwiic BME280 sensor](https://www.sparkfun.com/products/15440), and some [Qwiic cables](https://www.sparkfun.com/products/15081).

??? note "Required Hardware"
	<div class="grid cards" markdown>

	-   <a href="https://www.sparkfun.com/products/24243">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/4/5/3/4/WRL-24243-Thing-Plus-RA6M5-Feature.jpg)
		</figure>

		---

		**RA6M5 Thing Plus**<br>
		WRL-24243</a>

	-   <a href="https://www.sparkfun.com/products/15081">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/3/4/3/1/15081-_01.jpg)
		</figure>

		---

		**SparkFun Qwiic Cable Kit**<br>
		KIT-15081</a>


	-   <a href="https://www.sparkfun.com/products/24606">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/4/9/6/3/LCD-24606-Qwiic-OLED-Display-Feature-Screen.jpg)
		</figure>

		---

		**SparkFun Qwiic OLED Display (0.91 in., 128x32)**<br>
		LCD-24606</a>


	-   <a href="https://www.sparkfun.com/products/15440">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/4/0/1/4/15440-SparkFun_Atmospheric_Sensor_Breakout_-_BME280__Qwiic_-04a.jpg)
		</figure>

		---

		**SparkFun Atmospheric Sensor Breakout - BME280 (Qwiic)**<br>
		SEN-15440</a>

	</div>


=== "`codelessBLE_peripheral.ino`"
	This sketch requires a [Qwiic BME280 sensor](https://www.sparkfun.com/products/15440), connected by a [Qwiic cable](https://www.sparkfun.com/products/17260), to be connected the RA6M5 Thing Plus. The sketch demonstrates a basic BLE solution, by transmitting data from the BME280 to another BLE device. Users can find this sketch in the **File** > **Examples** > **SparkFun Renesas Codeless BLE** > **codelessBLE_peripheral** drop-down menu.


	??? arduino "Install Arduino Library"
		For this example, the [SparkFun BME280 Arduino Library](https://github.com/sparkfun/SparkFun_BME280_Arduino_Library) will need to be installed. In the Arduino IDE, users can install it by searching for `SparkFun BME280 Arduino Library`, in the **Library Manager**:

			SparkFun BME280 Arduino Library


	??? code "`codelessBLE_peripheral.ino`"
		```cpp
		--8<-- "https://raw.githubusercontent.com/sparkfun/SparkFun_Thing_Plus_RA6M5/main/Firmware/CodelessBLE/examples/codelessBLE_peripheral/codelessBLE_peripheral.ino"
		```


	!!! tip "BME688 Replacement"
		Users can also modify this example to utilize the [Qwiic BME688 sensor](https://www.sparkfun.com/products/19096) that is mentioned in some of the other examples. *For more details on utilizing the BME68x breakout board, please refer to our [hookup guide](https://learn.sparkfun.com/tutorials/1168) for the sensor.*


		<div class="grid cards" markdown>

		-   <a href="https://www.sparkfun.com/products/19096">
			<figure markdown>
			![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/8/6/9/6/19096-SparkFun_Environmental_Sensor_Breakout_-_BME688__Qwiic_-01.jpg)
			</figure>

			---

			**SparkFun Environmental Sensor - BME688 (Qwiic)**<br>
			SEN-19096</a>


		-   <a href="https://www.sparkfun.com/products/17260">
			<figure markdown>
			![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/6/2/4/7/17260-Flexible_Qwiic_Cable_-_50mm-01.jpg)
			</figure>

			---

			**Flexible Qwiic Cable - 50mm**<br>
			PRT-17260</a>

		</div>


		??? arduino "Install Arduino Library"
			Users will need to install the [Bosch BME68x Arduino library](https://github.com/BoschSensortec/Bosch-BME68x-Library) for the sensor. In the Arduino IDE, users can install it by searching for `BME68x Sensor Library`, in the **Library Manager**:

				BME68x Sensor Library


		??? code "Modifications"
			- Link the BME68x Arduino library:

					{--#include "SparkFunBME280.h"--}
					{++#include "bme68xLibrary.h"++}

			- Create an instance of the `Bme68x` class:

					{--BME280 myBME280;--}
					{++Bme68x bme;++}

			- Initialize and configure the sensor in the `setup()`:

					{--if(!myBME280.beginI2C())
					{
						Serial.println("Sensor didn't respond. Check wiring!");
						while(1);
					}

					Serial.println("Connected to BME280.");--}

					{++bme.begin(BME68X_I2C_ADDR_LOW, Wire)

					if(bme.checkStatus())
					{
						if (bme.checkStatus() == BME68X_ERROR)
						{
							Serial.println("Sensor error:" + bme.statusString());
							return;
						}
						else if (bme.checkStatus() == BME68X_WARNING)
						{
							Serial.println("Sensor Warning:" + bme.statusString());
						}
					}
					
					/* Set the default configuration for temperature, pressure and humidity */
					bme.setTPH();

					/* Configure the sensor to forced mode */
					bme.setOpMode(BME68X_FORCED_MODE);++}

			- Update the `loop()` to retrieve data from the BME688

					{--if((loop_start_time - millis()) > 100) // If it's been more than 100ms
					{
						reset_loop = true;
						if(bleConnected)
						{
							digitalWrite(LED_BUILTIN, HIGH);
							printstring = "|"+String(myBME280.readTempC())+","+String(myBME280.readFloatHumidity())+","+String(myBME280.readFloatPressure());
							Serial.print(myBLEPeripheral.sendCommand(printstring));
							digitalWrite(LED_BUILTIN, LOW);
						}--}

					{++bme68xData data;

					if((loop_start_time - millis()) > 100)    // If it's been more than 100ms
					{
						reset_loop = true;
						if(bleConnected)
						{
							digitalWrite(LED_BUILTIN, HIGH);

							delayMicroseconds(bme.getMeasDur());  // Wait for measurement data

							/* Retrieve data from BME688 sensor*/
							if (bme.fetchData())
							{
								bme.getData(data);
								printstring = "|"+String(data.temperature)+","+String(data.humidity)+","+String(data.pressure);
							}

							Serial.print(myBLEPeripheral.sendCommand(printstring));
							digitalWrite(LED_BUILTIN, LOW);
						}++}



=== "`codelessBLE_central.ino`"
	This sketch requires a [Qwiic OLED Display](https://www.sparkfun.com/products/24606) to be connected the RA6M5 Thing Plus, by a [Qwiic cable](https://www.sparkfun.com/products/17260). The sketch receives data transmitted from a RA6M5 Thing Plus, programmed with the `codelessBLE_peripheral.ino` sketch, and displays that data on the OLED display. Users can find this sketch in the **File** > **Examples** > **SparkFun Renesas Codeless BLE** > **codelessBLE_central** drop-down menu.

	??? code "`codelessBLE_central.ino`"
		```cpp
		--8<-- "https://raw.githubusercontent.com/sparkfun/SparkFun_Thing_Plus_RA6M5/main/Firmware/CodelessBLE/examples/codelessBLE_central/codelessBLE_central.ino"
		```
