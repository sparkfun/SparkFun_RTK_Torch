---
icon: material/book-open-page-variant
---

# Introduction
<div class="grid cards desc" markdown>

-   <a href="https://www.sparkfun.com/products/24243">
	**RA6M5 Thing Plus**<br>
	**SKU:** WRL-24243

	---

	<figure markdown>
	![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/4/5/3/4/WRL-24243-Thing-Plus-RA6M5-Feature.jpg)
	</figure></a>


	<center>

	<article class="video-container">
	<iframe src="https://www.youtube.com/embed/A9NTdowiY_o" title="Product Showcase Video" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	![QR code to product video](./assets/img/qr_code/product_video.png){ .qr width=100 }
	</article>

	[&nbsp;![QR code to product page](./assets/img/qr_code/product-low.png){ .tinyqr }&nbsp;&nbsp;Purchase from SparkFun :fontawesome-solid-cart-plus:{ .heart }&nbsp;&nbsp;&nbsp;](https://www.sparkfun.com/products/24243){ .md-button .md-button--primary }
	</center>


-	Clocking in at 200MHz, the RA6M5 is a high-performance microcontroller from [Renesas](https://www.renesas.com/) that is perfect for real-time applications. The [SparkFun Thing Plus - RA6M5](https://www.sparkfun.com/products/24243), is our latest [Thing Plus board](https://www.sparkfun.com/thing_plus) featuring the standard Qwiic connector, JST LiPo battery connector, 21 GPIO pins broken out in a Feather footprint, and status indicator LEDs. At the core is the RA6M5 microcontroller, a low-power Arm^®^ Cortex^®^-M33 processor with an available 512kB of SRAM and 2MB of Flash and an extensive list of peripheral capabilities. Additionally, we have included 16MB of QSPI Flash and an SD card slot on the board, so users won't have to worry about running out of memory space or data storage options.

	The SparkFun RA6M5 Thing Plus also features Bluetooth® Low Energy connectivity, thanks to the provided DA14531MOD module *(also from Renesas)*. When actively transmitting, the DA14531MOD sips a mere 4mA and is capable of operating from a small coin-cell battery. The firmware provided on the module features Renesas' [SmartBond™ - CodeLess™ AT command](https://lpccs-docs.renesas.com/UM-140-DA145x-CodeLess/index.html) set. Therefore, users only need to send AT commands to configure a Bluetooth connection; without the need to reprogram the module.

	!!! note
		While the Thing Plus - RA6M5 does include some 5V tolerant pins, it is primarily a **3.3V** *logic-level* board.

		While the full capabilities of the RA6M5 support a broad range of features, only a limited set may be implemented, by default, in the [Renesas-Arduino core](https://github.com/arduino/ArduinoCore-renesas). However, the capabilities of the Thing Plus - RA6M5 should be comparable to the [Arduino Portenta C33](https://store.arduino.cc/collections/portenta-family/products/portenta-c33); with the exclusion of WiFi connectivity.

</div>


## :fontawesome-solid-list-check:&nbsp;Required Materials
To get started, users will need a few items. Some users may already have a few of these items, feel free to adjust accordingly.

<div class="annotate" markdown>

* Computer with an operating system (OS) that is compatible with all the software installation requirements
* [USB 3.1 Cable A to C - 3 Foot](https://www.sparkfun.com/products/14743) - Used to interface with the RA6M5 Thing Plus (1)
* [SparkFun RA6M5 Thing Plus](https://www.sparkfun.com/products/24243)

</div>

1. If your computer doesn't have a USB-A slot, then choose an appropriate cable or adapter.


<div class="grid cards col-4" markdown>

-   <a href="https://www.sparkfun.com/products/14743">
	<figure markdown>
	![USB 3.1 Cable A to C - 3 Foot](https://cdn.sparkfun.com/assets/parts/1/2/9/7/2/14743-USB_3.1_Cable_A_to_C_-_3_Foot-01.jpg)
	</figure>

	---

	**USB 3.1 Cable A to C - 3 Foot**<br>
	CAB-14743</a>

-   <a href="https://www.sparkfun.com/products/24243">
	<figure markdown>
	![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/4/5/3/4/WRL-24243-Thing-Plus-RA6M5-Feature.jpg)
	</figure>

	---

	**RA6M5 Thing Plus**<br>
	WRL-24243</a>

</div>



??? note "Data Logging"
	This board is capable of logging data to an &micro;SD card. Please check out the [memory cards and accessories](https://www.sparkfun.com/categories/351) in our product catalog.

	<div class="grid cards col-4" markdown>

	-   <a href="https://www.sparkfun.com/products/15107">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/3/4/7/0/15107-microSD_Card_-_1GB__Class_4_-01.jpg)
		</figure>		

		---

		**microSD Card - 1GB (Class 4)**<br>
		COM-15107</a>

	-   <a href="https://www.sparkfun.com/products/13004">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/9/9/5/8/13004-03.jpg)
		</figure>		

		---

		**microSD USB Reader**<br>
		COM-13004</a>

	</div>



??? note "Headers and Wiring"
	To add headers or hookup wires, users will need [soldering equipment](https://www.sparkfun.com/categories/49) and [headers](https://www.sparkfun.com/categories/381)/[wires](https://www.sparkfun.com/search/results?term=hook-up+wire).


	!!! tip "New to soldering?"
		Check out our [How to Solder: Through-Hole Soldering](https://learn.sparkfun.com/tutorials/5) tutorial for a quick introduction!

		<div class="grid cards col-4" markdown align="center">

		-   <a href="https://learn.sparkfun.com/tutorials/5">
			<figure markdown>
			![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/e/3/9/9/4/51d9fbe1ce395f7a2a000000.jpg)
			</figure>

			---
	
			**How to Solder: Through-Hole Soldering**</a>

		</div>


	<div class="grid cards col-4" markdown>

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

	-   <a href="https://www.sparkfun.com/products/14579">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/2/7/2/5/14579-Chip_Quik_No-Clean_Flux_Pen_-_10mL-01.jpg)
		</figure>

		---

		**Chip Quik No-Clean Flux Pen - 10mL**<br>
		TOL-14579</a>

	-   <a href="https://www.sparkfun.com/products/15187">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/3/6/0/4/15187-Feather_Stackable_Header_Kit-01.jpg)
		</figure>

		---

		**Feather Stackable Header Kit**<br>
		PRT-15187</a>

	-   <a href="https://www.sparkfun.com/products/116">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/0/6/00116-02-L.jpg)
		</figure>

		---

		**Break Away Headers - Straight**<br>
		PRT-00116</a>

	-   <a href="https://www.sparkfun.com/products/11375">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/7/1/2/0/11375-Hook-Up_Wire_-_Assortment__Solid_Core__22_AWG_-01.jpg)
		</figure>

		---

		**Hook-Up Wire - Assortment (Stranded, 22 AWG)**<br>
		PRT-11375</a>

	</div>



??? note "Li-Po Battery"
	For mobile applications, users will want to pick up a [single-cell LiPo battery](https://www.sparkfun.com/categories/54) from our catalog.

	<div class="grid cards col-4" markdown>

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



??? note "Qwiic Devices and Cables"
	Our Qwiic connect system is a simple solution for daisy chaining I^2^C devices without the hassle of soldering or checking wire connections. Check out other [Qwiic devices](https://www.sparkfun.com/categories/399) from our catalog.

	<div class="grid cards col-2" markdown>

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

	!!! tip "What is Qwiic?"

		<div class="grid" markdown>

		<div markdown>

		<!-- Qwiic Banner -->
		<center>
		[![Qwiic Logo - light theme](./assets/img/qwiic_logo-light.png#only-light){ width=400 }](https://www.sparkfun.com/qwiic)
		[![Qwiic Logo - dark theme](./assets/img/qwiic_logo-dark.png#only-dark){ width=400 }](https://www.sparkfun.com/qwiic)
		</center>

		---

		The [Qwiic connect system](https://www.sparkfun.com/qwiic) is a solderless, polarized connection system that allows users to seamlessly daisy chain I^2^C boards together. Play the video, to learn more about the Qwiic connect system or click on the banner above to learn more about [Qwiic products](https://www.sparkfun.com/qwiic).

		</div>

		<div style="max-height=400px;" markdown>

		<center>
		<div class="video-container">
		<iframe src="https://www.youtube.com/embed/x0RDEHqFIF8" title="SparkFun's Qwiic Connect System" frameborder="0" allow="accelerometer; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

		![QR code to instructional video](./assets/img/qr_code/qwiic_video.png){ .qr width=100 }
		</div>
		</center>

		</div>

		</div>


		!!! info "Features of the Qwiic System"

			=== "No Soldering"

				![no soldering - light theme](./assets/img/no_soldering-light.png#only-light){ align="left" width="90" }
				![no soldering - dark theme](./assets/img/no_soldering-dark.png#only-dark){ align="left" width="90" }

				Qwiic cables (4-pin JST) plug easily from development boards to sensors, shields, accessory boards and more, making easy work of setting up a new prototype.

			=== "Polarized Connector"

				![polarized connector - light theme](./assets/img/polarized_connector-light.png#only-light){ align="left" width="90" }
				![polarized connector - dark theme](./assets/img/polarized_connector-dark.png#only-dark){ align="left" width="90" }

				There's no need to worry about accidentally swapping the `SDA` and `SCL` wires on your breadboard. The Qwiic connector is polarized so you know you’ll have it wired correctly every time.

				The part numbers for the PCB connector is `SM04B-SRSS` ([Datasheet](https://cdn.sparkfun.com/assets/parts/1/2/2/8/9/Qwiic_Connector_Datasheet.pdf)) and the mating connector on the cables is `SHR04V-S-B`; or an equivalent *1mm pitch, 4-pin JST connection*.

			=== "Daisy Chain-able"

				![daisy chainable - light theme](./assets/img/daisy_chainable-light.png#only-light){ align="left" width="90" }
				![daisy chainable - dark theme](./assets/img/daisy_chainable-dark.png#only-dark){ align="left" width="90" }

				It’s time to leverage the power of the I^2^C bus! Most Qwiic boards will have two or more connectors on them, allowing multiple devices to be connected.



??? note "Jumper Modification"
	To modify the [jumpers](../hardware_overview/#jumpers), users will need [soldering equipment](https://www.sparkfun.com/categories/49) and/or a [hobby knife](https://www.sparkfun.com/categories/379).


	!!! tip "New to jumper pads?"
		Check out our [Jumper Pads and PCB Traces Tutorial](https://learn.sparkfun.com/tutorials/664) for a quick introduction!

		<div class="grid cards col-4" markdown align="center">

		-   <a href="https://learn.sparkfun.com/tutorials/664">
			<figure markdown>
			![Tutorial thumbnail](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/6/4/PCB_TraceCutLumenati.jpg)
			</figure>

			---
			
			**How to Work with Jumper Pads and PCB Traces**</a>

		</div>


	<div class="grid cards col-4" markdown>

	-   <a href="https://www.sparkfun.com/products/22265">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/2/2/0/2/TOL-22265-Beginner-Tool-Kit-Feature.jpg)
		</figure>		

		---

		**SparkFun Beginner Tool Kit**<br>
		TOL-22265</a>

	-   <a href="https://www.sparkfun.com/products/9200">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/6/4/6/09200-Hobby_Knife-01.jpg)
		</figure>

		---

		**Hobby Knife**<br>
		TOL-09200</a>

	-   <a href="https://www.sparkfun.com/products/14579">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/2/7/2/5/14579-Chip_Quik_No-Clean_Flux_Pen_-_10mL-01.jpg)
		</figure>

		---

		**Chip Quik No-Clean Flux Pen - 10mL**<br>
		TOL-14579</a>

	</div>




## :material-bookshelf:&nbsp;Suggested Reading

As a more sophisticated product, we will skip over the more fundamental tutorials (i.e. [**Ohm's Law**](https://learn.sparkfun.com/tutorials/voltage-current-resistance-and-ohms-law) and [**What is Electricity?**](https://learn.sparkfun.com/tutorials/what-is-electricity)). However, below are a few tutorials that may help users familiarize themselves with various aspects of the board.


<div class="grid cards col-4" markdown align="center">

-   <a href="https://learn.sparkfun.com/tutorials/61">
	<figure markdown>
	![Installing the Arduino IDE](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/1/arduinoThumb.jpg)
	</figure>

	---

	**Installing the Arduino IDE**</a>

-   <a href="https://learn.sparkfun.com/tutorials/15">
	<figure markdown>
	![Installing an Arduino Library](https://cdn.sparkfun.com/c/264-148/assets/b/e/4/b/2/50f04b99ce395fd95e000001.jpg)
	</figure>

	---

	**Installing an Arduino Library**</a>

-   <a href="https://learn.sparkfun.com/tutorials/1265">
	<figure markdown>
	![Installing Board Definitions in the Arduino IDE](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/1/2/6/5/sparkfun_boards.PNG)
	</figure>

	---

	**Installing Board Definitions in the Arduino IDE**</a>

-   <a href="https://learn.sparkfun.com/tutorials/62">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/2/Input_Output_Logic_Level_Tolerances_tutorial_tile.png)
	</figure>

	---

	**Logic Levels**</a>

-   <a href="https://learn.sparkfun.com/tutorials/89">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/3/7/6/6/0/51c48875ce395f745a000000.png)
	</figure>

	---

	**Analog vs. Digital**</a>

-   <a href="https://learn.sparkfun.com/tutorials/35">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/d/d/5/c/4/5114013ece395f527e000000.jpg)
	</figure>

	---

	**Analog to Digital Conversion**</a>

-   <a href="https://learn.sparkfun.com/tutorials/51">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/f/9/c/8/a/512e869bce395fbc64000002.JPG)
	</figure>

	---

	**Pulse Width Modulation**</a>

-   <a href="https://learn.sparkfun.com/tutorials/8">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/7/d/f/9/9/50d24be7ce395f1f6c000000.jpg)
	</figure>

	---

	**Serial Communication**</a>

-   <a href="https://learn.sparkfun.com/tutorials/112">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/1/1/2/thumb.jpg)
	</figure>

	---

	**Serial Terminal Basics**</a>

-   <a href="https://learn.sparkfun.com/tutorials/114">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/1/1/4/dddtt.jpg)
	</figure>

	---

	**Data Types in Arduino**</a>

-   <a href="https://learn.sparkfun.com/tutorials/82">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/8/2/I2C-Block-Diagram.jpg)
	</figure>

	---

	**I2C**</a>

-   <a href="https://learn.sparkfun.com/tutorials/16">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/1/6/spiThumb_Updated.jpg)
	</figure>

	---

	**SPI**</a>

-   <a href="https://learn.sparkfun.com/tutorials/316">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/3/1/6/LED_Demo_1.gif)
	</figure>

	---

	**Processor Interrupts with Arduino**</a>

-   <a href="https://learn.sparkfun.com/tutorials/5">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/e/3/9/9/4/51d9fbe1ce395f7a2a000000.jpg)
	</figure>

	---

	**How to Solder: Through-Hole Soldering**</a>

-   <a href="https://learn.sparkfun.com/tutorials/664">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/6/4/PCB_TraceCutLumenati.jpg)
	</figure>

	---

	**How to Work with Jumper Pads and PCB Traces**</a>

-   <a href="https://learn.sparkfun.com/tutorials/80">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/8/3/6/3/b/51dc6e21ce395f0807000000.png)
	</figure>

	---

	**Integrated Circuits**</a>

</div>
