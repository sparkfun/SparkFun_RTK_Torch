---
icon: simple/arduino
---

## Feedback Loop
The simplest way to test the SPI interface is with just a jumper *(wire)* and looping a data transmission from the **PICO** GPIO pin; back into the **POCI** GPIO pin. For this example, users are free to utilize any method or hardware they have to connect the **PICO** and **POCI** GPIO pins together. However, we recommend some IC hooks for a temporary connection.


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



??? code "`SPI_Loopback.ino`"
	```cpp
	--8<-- "./Firmware/Tests/SPI_Loopback/SPI_Loopback.ino"
	```



## Peripheral Device
A more direct method for testing the SPI interface is with an actual SPI device.

### BME688 Environmental Sensor
Users are free to utilize any hardware they already have; however, we recommend the [BME688 environmental sensor](https://www.sparkfun.com/products/19096), below. Its SPI pins are broken out on the edge of the board and can be easily connected to the RA6M5 Thing Plus. In addition, a [hookup guide](https://learn.sparkfun.com/tutorials/1168) and [Arduino library](https://github.com/BoschSensortec/Bosch-BME68x-Library) for the sensor are available.


??? note "Optional Hardware"
	<div class="grid cards" markdown>

	-   <a href="https://www.sparkfun.com/products/19096">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/8/6/9/6/19096-SparkFun_Environmental_Sensor_Breakout_-_BME688__Qwiic_-01.jpg)
		</figure>

		---

		**SparkFun Environmental Sensor - BME688 (Qwiic)**<br>
		SEN-19096</a>


	-   <a href="https://www.sparkfun.com/products/501">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/3/4/1/00501-1.jpg)
		</figure>

		---

		**IC Hook Test Leads**<br>
		CAB-00501</a>


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


	-   <a href="https://www.sparkfun.com/products/9200">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/6/4/6/09200-Hobby_Knife-01.jpg)
		</figure>

		---

		**Hobby Knife**<br>
		TOL-09200</a>

	</div>


??? arduino "Install Arduino Library"
	Users will need to install the [Bosch BME68x Arduino library](https://github.com/BoschSensortec/Bosch-BME68x-Library) for the sensor. In the Arduino IDE, users can install it by searching for `BME68x Sensor Library`, in the **Library Manager**:

		BME68x Sensor Library



Users can find this sketch in the **File** > **Examples** > **BME68x Sensor library** > **forced_mode** drop-down menu. *For more details on utilizing the BME68x breakout board, please refer to our [hookup guide](https://learn.sparkfun.com/tutorials/1168) for the sensor.*



??? code "`forced_mode.ino`"
	```cpp
	--8<-- "https://raw.githubusercontent.com/boschsensortec/Bosch-BME68x-Library/master/examples/forced_mode/forced_mode.ino"
	```
