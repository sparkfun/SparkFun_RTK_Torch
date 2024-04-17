---
icon: simple/arduino
---

## Device Scan
This sketch allows users to scan for devices connected to the primary I^2^C bus of the RAM5 Thing Plus. The example code can be found in the [GitHub repository](https://github.com/sparkfun/SparkFun_Thing_Plus_RA6M5/tree/main/docs/assets/arduino_examples/i2c_scanner/i2c_scanner.ino). However, users can also simply click on the button *(below)*, to download the code; or expand the box *(below)*, to copy the code.


??? code "`i2c_scanner.ino`"
	```cpp
	--8<-- "./assets/arduino_examples/i2c_scanner/i2c_scanner.ino"
	```


<center>
[:octicons-download-16:{ .heart } Download the Example Sketch](./assets/arduino_examples/i2c_scanner/i2c_scanner.ino){ .md-button .md-button--primary }
</center>



## Peripheral Devices
The RA6M5 Thing Plus features a Qwiic connector to seamlessly integrate with devices from [SparkFun's Qwiic Ecosystem](https://www.sparkfun.com/qwiic). While users are free to utilize any I^2^C device, we recommend the [Qwiic devices](https://www.sparkfun.com/categories/399) from our catalog.


??? note "Optional Hardware"
	<div class="grid cards" markdown>

	-   <a href="https://www.sparkfun.com/products/15081">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/3/4/3/1/15081-_01.jpg)
		</figure>

		---

		**SparkFun Qwiic Cable Kit**<br>
		KIT-15081</a>


	-   <a href="https://www.sparkfun.com/products/15109">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/3/4/7/5/15109-Qwiic_Cable_-_Grove_Adapter__150mm_-01.jpg)
		</figure>

		---

		**Qwiic Cable - Grove Adapter (100mm)**<br>
		PRT-15109</a>


	-   <a href="https://www.sparkfun.com/products/23453">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/3/7/6/0/23453-Qwiic-OLED-Feature-WithDisplay.jpg)
		</figure>

		---

		**SparkFun Qwiic OLED - (1.3in., 128x64)**<br>
		LCD-23453</a>


	-   <a href="https://www.sparkfun.com/products/14414">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/2/3/4/0/14414-SparkFun_GPS_Breakout_-_XA1110__Qwiic_-01.jpg)
		</figure>

		---

		**SparkFun GPS Breakout - XA1110 (Qwiic)**<br>
		GPS-14414</a>


	-   <a href="https://www.sparkfun.com/products/15168">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/3/5/5/8/15168-SparkFun_Qwiic_Joystick-01.jpg)
		</figure>

		---

		**SparkFun Qwiic Joystick**<br>
		COM-15168</a>


	-   <a href="https://www.sparkfun.com/products/16784">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/5/6/8/9/16784-SparkFun_Qwiic_Mux_Breakout_V2_-_8_Channel__TCA9548A_-01.jpg)
		</figure>

		---

		**SparkFun Qwiic Mux Breakout - 8 Channel (TCA9548A)**<br>
		BOB-16784</a>


	-   <a href="https://www.sparkfun.com/products/19096">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/8/6/9/6/19096-SparkFun_Environmental_Sensor_Breakout_-_BME688__Qwiic_-01.jpg)
		</figure>

		---

		**SparkFun Environmental Sensor - BME688 (Qwiic)**<br>
		SEN-19096</a>


	-   <a href="https://www.sparkfun.com/products/19013">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/8/6/1/2/19013-SparkFun_Qwiic_Mini_ToF_Imager_-_VL53L5CX-01.jpg)
		</figure>

		---

		**SparkFun Qwiic Mini ToF Imager - VL53L5CX**<br>
		SEN-19013</a>

	</div>



### MAX17048 Fuel Gauge
The MAX17048 fuel gauge measures the approximate charge/discharge rate, state of charge, and voltage of a connected LiPo battery. We recommend the [SparkFun MAX1704x Arduino library](https://github.com/sparkfun/SparkFun_MAX1704x_Fuel_Gauge_Arduino_Library) be utilized in the Arduino IDE, to connect to the MAX17048 on the RA6M5 Thing Plus. Once the [library is installed in the Arduino IDE](../software_overview-arduino/#max17048-fuel-gauge), users will find several example sketches listed in the **File** > **Examples** > **SparkFun MAX1704x Fuel Gauge Arduino Library** > drop-down menu. We recommend the following examples for users:


- `Example1_Simple.ino`
- `Example4_MAX17048_KitchenSink.ino`


??? note "Optional Hardware"
	<div class="grid cards" markdown>

	-   <a href="https://www.sparkfun.com/products/13855">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/r/140-140/assets/parts/1/1/4/6/2/13855-01.jpg)
		</figure>		

		---

		**Lithium Ion Battery - 2Ah**<br>
		PRT-13855</a>


	-   <a href="https://www.sparkfun.com/products/13851">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/r/140-140/assets/parts/1/1/4/5/8/13857-01.jpg)
		</figure>		

		---

		**Lithium Ion Battery - 400mAh**<br>
		PRT-13851</a>


	-   <a href="https://www.sparkfun.com/products/13813">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/r/140-140/assets/parts/1/1/4/0/1/13813-01.jpg)
		</figure>		

		---

		**Lithium Ion Battery - 1Ah**<br>
		PRT-13813</a>


	-   <a href="https://www.sparkfun.com/products/13853">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/r/140-140/assets/parts/1/1/4/6/0/13853-01.jpg)
		</figure>		

		---

		**Lithium Ion Battery - 110mAh**<br>
		PRT-13853</a>

	</div>



=== "`Example1_Simple.ino`"
	Users can find this sketch in the **File** > **Examples** > **SparkFun MAX1704x Fuel Gauge Arduino Library** > **Example1_Simple** drop-down menu.

	??? code "`Example1_Simple.ino`"
		```cpp
		--8<-- "https://raw.githubusercontent.com/sparkfun/SparkFun_MAX1704x_Fuel_Gauge_Arduino_Library/main/examples/Example1_Simple/Example1_Simple.ino"
		```


=== "`Example4_MAX17048_KitchenSink.ino`"
	Users can find this sketch in the **File** > **Examples** > **SparkFun MAX1704x Fuel Gauge Arduino Library** > **Example4_MAX17048_KitchenSink** drop-down menu.

	??? code "`Example4_MAX17048_KitchenSink.ino`"
		```cpp
		--8<-- "https://raw.githubusercontent.com/sparkfun/SparkFun_MAX1704x_Fuel_Gauge_Arduino_Library/main/examples/Example4_MAX17048_KitchenSink/Example4_MAX17048_KitchenSink.ino"
		```



### BME688 Environmental Sensor
Users are free to utilize any hardware they already have; however, we recommend the [BME688 environmental sensor](https://www.sparkfun.com/products/19096). The board includes a Qwiic connector on the edge of the board and can be easily attached to the RA6M5 Thing Plus with a [Qwiic cable](https://www.sparkfun.com/products/17260). In addition, a [hookup guide](https://learn.sparkfun.com/tutorials/1168) and [Arduino library](https://github.com/BoschSensortec/Bosch-BME68x-Library) for the sensor are available.


??? note "Optional Hardware"
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



Users can find this sketch in the **File** > **Examples** > **BME68x Sensor library** > **forced_mode** drop-down menu. *For more details on utilizing the BME68x breakout board, please refer to our [hookup guide](https://learn.sparkfun.com/tutorials/1168) for the sensor.*



??? code "`forced_mode.ino`"
	!!! warning "I^2^C Modifications"
		By default, this example utilizes the SPI bus; therefore, some modifications must be made:

		- The chip select pin no longer needs to be defined:

				{--#ifndef PIN_CS
				#define PIN_CS SS
				#endif--}

		- The I^2^C bus must be initialized, instead of the SPI bus:

				{--SPI.begin();--}
				{++Wire.begin();++}

		- The sensor must be initialized with the Wire class, instead of the SPI class:

				/* initializes the sensor based on {--SPI--}{++Wire++} library */
				{--bme.begin(PIN_CS, SPI);--}
				{++bme.begin(BME68X_I2C_ADDR_LOW, Wire)++}


	```cpp
	--8<-- "https://raw.githubusercontent.com/boschsensortec/Bosch-BME68x-Library/master/examples/forced_mode/forced_mode.ino"
	```
