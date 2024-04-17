---
icon: simple/arduino
---

!!! tip
	For first-time users, who have never programmed before and are looking to use the Arduino IDE, we recommend beginning with the [SparkFun Inventor's Kit (SIK)](https://www.sparkfun.com/products/15631), which is designed to help users get started programming with the Arduino IDE.

Most users should already be familiar with the Arduino IDE and its use. However, for those of you who have never heard the name *Arduino* before, feel free to check out the [Arduino website](https://www.arduino.cc/en/Guide/HomePage). To get started with using the Arduino IDE, check out our tutorials below:


<div class="grid cards" markdown align="center">

-   <a href="https://learn.sparkfun.com/tutorials/50">
	<figure markdown>
	![What is an Arduino?](https://cdn.sparkfun.com/c/264-148/assets/3/b/6/e/b/512e66bece395f492b000000.jpg)
	</figure>

	---

	**What is an Arduino?**</a>

-   <a href="https://learn.sparkfun.com/tutorials/61">
	<figure markdown>
	![Installing the Arduino IDE](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/1/arduinoThumb.jpg)
	</figure>

	---

	**Installing the Arduino IDE**</a>

-   <a href="https://learn.sparkfun.com/tutorials/1265">
	<figure markdown>
	![Installing Board Definitions in the Arduino IDE](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/1/2/6/5/sparkfun_boards.PNG)
	</figure>

	---

	**Installing Board Definitions in the Arduino IDE**</a>

-   <a href="https://learn.sparkfun.com/tutorials/15">
	<figure markdown>
	![Installing an Arduino Library](https://cdn.sparkfun.com/c/264-148/assets/b/e/4/b/2/50f04b99ce395fd95e000001.jpg)
	</figure>

	---

	**Installing an Arduino Library**</a>

</div>


## Arduino Core

### Installation
!!! success "Installing the *Ported* Renesas-Arduino Core"
	In order to program the RA6M5 Thing Plus in the Arduino IDE, users will need to install the **Renesas-Arduino core**. However, until the [RA6M5 Thing Plus is officially adopted into the Renesas-Arduino core](https://github.com/arduino/ArduinoCore-renesas/pull/290), users need to utilize [our port of the **Renesas-Arduino core**](./assets/SFE-Renesas-Arduino_core.zip).

	1. Before users can install our ported version of the Renesas-Arduino core, they should first install the [*official* Renesas-Arduino core](https://github.com/arduino/ArduinoCore-renesas) in the Arduino IDE.
		- This will ensure that any required compilation and upload tools are installed for the Arduino core.
	2. Once installed, users will need to locate the `packages` directory for the Arduino cores in the Arduino IDE:

		<div class="grid cards" markdown>

		-   **Windows**

			---

			On Windows, the directory location may vary based on whether the Arduino IDE was installed for an individual user or all users:

			- The user's `AppData` directory *(hidden folder)*:

					C:\Users\{==<insert username>==}\AppData\Local\Arduino15\packages

			- The user's `ArduinoData` directory:

					C:\Users\{==<insert username>==}\Documents\ArduinoData

			- The `Program Files` or `Program Files(x86)` directories:

					C:\Program Files{++(x86)++}\Arduino IDE


		-   **MacOS**

			---

			With Mac OS, users should check the `Applications` and `Library` directories:

			- `Applications` directory:

					/Applications/Arduino.app/

			- `Library` directory:

					~/Library/Arduino15/packages/


		-   **Linux**

			---

			For Linux, this may be located in the following directories:

			- Local:

					/home/$USER/Arduino

			- Downloaded:

					/home/$USER/.arduino15/packages


		</div>

	3. After the `packages` directory has been located, users will need to navigate to the Renesas Arduino core. It is usually located in the `./arduino/hardware/{==renesas_portenta==}/{++<version number>++}/` directory of the `packages` folder.
	4. The Arduino core is followed by a directory, named after the Arduino core's release `{++<version number>++}`. From there, users will need to create a new directory/folder in the `renesas_portenta` directory with the `version number` bumped up.
		- *For example, if the current version is `1.1.0`, users can name the new directory `1.2.0`.*
	4. Next, users will need to download and extract the files from [our ported version of the Renesas-Arduino core](./assets/SFE-Renesas-Arduino_core.zip):
		<center>
		[:material-download:{ .heart }&nbsp;&nbsp;Download our Renesas-Arduino Core *(Ported)*](./assets/SFE-Renesas-Arduino_core.zip "Click to download the ported Arduino core"){ .md-button .md-button--primary }
		</center>
	4. Once extracted, users will need to copy over the files from [our ported version of the Renesas-Arduino core](./assets/SFE-Renesas-Arduino_core.zip)into the new directory that was created earlier:
		<figure markdown>
		[![Extracted files](./assets/img/hookup_guide/arduino-extracted_files.png){ width=500 }](./assets/img/hookup_guide/arduino-extracted_files.png "Click to enlarge")
		<figcaption markdown>The files extracted from [our ported version of the Renesas-Arduino core](./assets/SFE-Renesas-Arduino_core.zip).</figcaption>
		</figure>
	5. Once the extracted files have been copied into the new directory, users will need to install the USB drivers for the board by executing the `post-install.*` script:
		- Windows: `post-install.bat`
		- Mac/Linux: `post-install.sh`

	!!! info
		This information is accurate as of April 2024; however, it may become irrelevant in the future *(once the [RA6M5 Thing Plus is included in the Renesas-Arduino core](https://github.com/arduino/ArduinoCore-renesas/pull/290))*. At which point, users may disregard this note and/or request for this information to be updated by [filing an issue](../github/file_issue).



??? failure "Do Not Use - *Hardware Not Officially Supported (yet)*"
	!!! warning
		The instructions below are invalid; theRA6M5 Thing Plus has not been [officially added into the Renesas-Arduino core](https://github.com/arduino/ArduinoCore-renesas/pull/290). In the meantime, users will need to utilize [our port of the **Renesas-Arduino core**](./assets/SFE-Renesas-Arduino_core.zip) *(see instructions above)*.


	{--

	In order to program the RA6M5 Thing Plus in the Arduino IDE, users will need to install the [Renesas-Arduino core](https://github.com/arduino/ArduinoCore-renesas). The Arduino core can be found by searching for `Arduino Renesas Portenta Boards` in the **Board Manager** of the Arduino IDE. Once installed, the RA6M5 Thing Plus will become available in the **Board Manager**.

		Arduino Renesas Portenta Boards

	<div class="grid" markdown>

	<div markdown>

	For users who are unfamiliar with this process, please check out our tutorial on [installing an Arduino core](https://learn.sparkfun.com/tutorials/installing-board-definitions-in-the-arduino-ide/installing-an-arduino-board-definition).

	<div class="grid cards" markdown align="center">

	-   <a href="https://learn.sparkfun.com/tutorials/1265">
		<figure markdown>
		![Installing Board Definitions in the Arduino IDE](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/1/2/6/5/sparkfun_boards.PNG)
		</figure>

		---

		**Installing Board Definitions in the Arduino IDE**</a>

	</div>

	</div>

	<div markdown>

	<figure markdown>
	[![Install the Renesas-Arduino Core](./assets/img/hookup_guide/arduino-renesas_core.png){ width="400" }](./assets/img/hookup_guide/arduino-renesas_core.png "Click to enlarge")
	<figcaption markdown>Installing the [Renesas-Arduino core](https://github.com/arduino/ArduinoCore-renesas) in the Arduino IDE.</figcaption>
	</figure>

	</div>

	</div>

	--}



### Programming a Board
In order to upload a sketch from the Arduino IDE onto the RA6M5 Thing Plus, users will need to select the `SparkFun Thing Plus RA6M5` from the **Tools** > **Board** > **Arduino Renesas Portenta Boards** > **SparkFun Thing Plus RA6M5** drop-down menu. Users will also need to select the serial port from the **Tools** > **Port** drop-down menu; the port should be automatically labeled, based upon the PID/VID of board in the USB driver.


<div class="grid" markdown>

<div markdown>

<figure markdown>
[![Select the RA6M5 Thing Plus](./assets/img/hookup_guide/arduino-select_board.png){ width="400" }](./assets/img/hookup_guide/arduino-select_board.png "Click to enlarge")
<figcaption markdown>Selecting the `SparkFun Thing Plus RA6M5` from the **Tools** drop-down menu in the Arduino IDE.</figcaption>
</figure>

</div>


<div markdown>

<figure markdown>
[![Select the RA6M5 Thing Plus](./assets/img/hookup_guide/arduino-select_board_alt.png){ width="400" }](./assets/img/hookup_guide/arduino-select_board_alt.png "Click to enlarge")
<figcaption markdown>Searching for the `SparkFun Thing Plus RA6M5` in the **Select Other Board and Port** menu in the Arduino IDE.</figcaption>
</figure>

</div>

</div>


Alternatively, in the Arduino IDE *(v2.`x`.`x`)*, users can also search for the board and serial port in the **Select Other Board and Port** menu. Once the appropriate board and serial port have been selected in the Arduino IDE, users can click the ++"&rarr;"++ *(upload)* button to begin the compilation and upload process.


??? success "DFU Mode"
	If users are having issues uploading code to the board, the RA6M5 can be manually forced into DFU mode. This issue, often occurs when the USB connection is busy and a reset can't be triggered on the RA6M5, to initialize the upload process. To force the RA6M5 Thing Plus into DFU mode:

	1. Double-tap the ++"RST"++ button
		- The `STAT` LED should be fading in/out very slowly
	1. Users should now, be able to upload a new program
		- It shouldn't be necessary to select a COM port in the Arduino IDE; only the board needs to be selected
	1. Once programming is complete, the MCU should reboot on its own. Otherwise:
		- Press the ++"RST"++ button
		- Power cycle the board



## Arduino Libraries
In order to utilize some of the peripherals of the RA6M5 Thing Plus with the Arduino IDE, users will need to [install Arduino libraries](https://learn.sparkfun.com/tutorials/15) for the peripheral devices/interfaces. For users who are unfamiliar with this process, please check out our tutorial below:

<div class="grid cards" markdown align="center">

-   <a href="https://learn.sparkfun.com/tutorials/15">
	<figure markdown>
	![Installing an Arduino Library](https://cdn.sparkfun.com/c/264-148/assets/b/e/4/b/2/50f04b99ce395fd95e000001.jpg)
	</figure>

	---

	**Installing an Arduino Library**</a>

</div>



### MAX17048 Fuel Gauge
While users are free to choose any Arduino library that provides support for MAX17048 fuel gauge, we recommend the [SparkFun MAX1704x Arduino library](https://github.com/sparkfun/SparkFun_MAX1704x_Fuel_Gauge_Arduino_Library); as it has been tested and verified to work with the MAX17048 on the RA6M5 Thing Plus. The [SparkFun MAX1704x Fuel Gauge Arduino library](https://github.com/sparkfun/SparkFun_MAX1704x_Fuel_Gauge_Arduino_Library) can be installed from the **Library Manager** in the Arduino IDE by searching for:

	SparkFun MAX1704x Fuel Gauge Arduino Library


<div class="grid" markdown>

<div markdown>

<figure markdown>
[![Install the SparkFun MAX1704x Arduino library](./assets/img/hookup_guide/arduino-MAX1704x_library.png "Click to enlarge"){ width="400" }](./assets/img/hookup_guide/arduino-MAX1704x_library.png)<figcaption markdown>SparkFun MAX1704x Fuel Gauge Arduino library in the library manager of the Arduino IDE.</figcaption>
</figure>

</div>

<div markdown>

!!! tip "Manually Download the Arduino Library"
	For users who would like to manually download and install the library, the `*.zip` file can be accessed from the [GitHub repository](https://github.com/sparkfun/MAX1704x_Fuel_Gauge_Arduino_Library) or downloaded by clicking the button below.

	<center>
	[:octicons-download-16:{ .heart } Download the Arduino Library](https://github.com/sparkfun/SparkFun_MAX1704x_Fuel_Gauge_Arduino_Library/archive/refs/heads/main.zip){ .md-button .md-button--primary }
	</center>

</div>

</div>



### WS2812 RGB LED
Users are free to choose any Arduino library that provides support for WS2812 LEDs. However, we recommend the [FastLED Arduino library](https://github.com/FastLED/FastLED/); as it has been tested and verified to work with the RGB LED on the RA6M5 Thing Plus.


!!! warning
	While support for the new Renesas Arduino boards has not been officially released for the FastLED Arduino library, the hardware modifications have been integrated into the GitHub repository. Therefore, users can manually download and install the FastLED Arduino library for *unofficial* support of the Renesas Arduino boards.


<div class="grid" markdown>

<div markdown>

!!! tip "Manually Download the Arduino Library"
	For users who would like to manually download and install the library, the `*.zip` file can be accessed from the [GitHub repository](https://github.com/FastLED/FastLED/) or downloaded by clicking the button below.

	<center>
	[:octicons-download-16:{ .heart } Download the Arduino Library](https://github.com/FastLED/FastLED/archive/refs/heads/master.zip){ .md-button .md-button--primary }
	</center>

</div>


<div class="grid cards" markdown align="center">

-   <a href="https://learn.sparkfun.com/tutorials/15">
	<figure markdown>
	![Installing an Arduino Library](https://cdn.sparkfun.com/c/264-148/assets/b/e/4/b/2/50f04b99ce395fd95e000001.jpg)
	</figure>

	---

	**Installing an Arduino Library**</a>

</div>

</div>


!!! abstract "Add Support for the RA6M5 Thing Plus"
	In addition to manually installing the Arduino library, users will also need to integrate the RA6M5 Thing Plus into the FastLED Arduino library with the [porting instructions](https://github.com/FastLED/FastLED/blob/master/PORTING.md). This requires users to include the {++highlighted lines++} before {==line 94==} in the [`fastpin_arm_renesas.h`](https://github.com/FastLED/FastLED/blob/master/src/platforms/arm/renesas/fastpin_arm_renesas.h#L94) file of the FastLED Arduino library:


	??? code "Code Modification"

		<div class="language-cpp highlight" markdown>

			--8<-- "https://raw.githubusercontent.com/FastLED/FastLED/master/src/platforms/arm/renesas/fastpin_arm_renesas.h:90:92"
			{++
			#elif defined(ARDUINO_THINGPLUS_RA6M5)

			#define MAX_PIN 24
			// D0-D06
			_FL_DEFPIN( 0, BSP_IO_PORT_01_PIN_12, R_PORT1_BASE ); _FL_DEFPIN( 1, BSP_IO_PORT_04_PIN_06, R_PORT4_BASE ); _FL_DEFPIN( 2, BSP_IO_PORT_04_PIN_05, R_PORT4_BASE );
			_FL_DEFPIN( 3, BSP_IO_PORT_04_PIN_04, R_PORT4_BASE ); _FL_DEFPIN( 4, BSP_IO_PORT_04_PIN_03, R_PORT4_BASE ); _FL_DEFPIN( 5, BSP_IO_PORT_04_PIN_02, R_PORT4_BASE );
			_FL_DEFPIN( 6, BSP_IO_PORT_02_PIN_07, R_PORT2_BASE );

			// D07-D12 (A0-A5)
			_FL_DEFPIN( 7, BSP_IO_PORT_00_PIN_14, R_PORT0_BASE ); _FL_DEFPIN( 8, BSP_IO_PORT_00_PIN_15, R_PORT0_BASE ); _FL_DEFPIN( 9, BSP_IO_PORT_05_PIN_05, R_PORT5_BASE );
			_FL_DEFPIN(10, BSP_IO_PORT_05_PIN_04, R_PORT5_BASE ); _FL_DEFPIN(11, BSP_IO_PORT_05_PIN_03, R_PORT5_BASE ); _FL_DEFPIN(12, BSP_IO_PORT_05_PIN_02, R_PORT5_BASE );

			// D13-D21
			_FL_DEFPIN(13, BSP_IO_PORT_01_PIN_05, R_PORT1_BASE ); _FL_DEFPIN(14, BSP_IO_PORT_01_PIN_06, R_PORT1_BASE ); _FL_DEFPIN(15, BSP_IO_PORT_04_PIN_01, R_PORT4_BASE );
			_FL_DEFPIN(16, BSP_IO_PORT_04_PIN_00, R_PORT4_BASE ); _FL_DEFPIN(17, BSP_IO_PORT_01_PIN_10, R_PORT1_BASE ); _FL_DEFPIN(18, BSP_IO_PORT_01_PIN_09, R_PORT1_BASE );
			_FL_DEFPIN(19, BSP_IO_PORT_01_PIN_11, R_PORT1_BASE ); _FL_DEFPIN(20, BSP_IO_PORT_04_PIN_09, R_PORT4_BASE ); _FL_DEFPIN(21, BSP_IO_PORT_04_PIN_08, R_PORT4_BASE );

			// D30-31
			_FL_DEFPIN(30, BSP_IO_PORT_03_PIN_04, R_PORT3_BASE ); _FL_DEFPIN(31, BSP_IO_PORT_04_PIN_15, R_PORT4_BASE );
			++}
			{==#elif defined(ARDUINO_ARCH_RENESAS_PORTENTA)==}

			--8<-- "https://raw.githubusercontent.com/FastLED/FastLED/master/src/platforms/arm/renesas/fastpin_arm_renesas.h:96:99"


		</div>


	!!! info
		This information is accurate as of April 2024; however, it may become irrelevant in the future *(once a release is published, with support for the Renesas Arduino boards and RA6M5 Thing Plus)*. At which point, users may disregard this note and/or request for this information to be removed by [filing an issue](../github/file_issue).



!!! tip "How to Define Parameters"
	While using the FastLED Arduino library, users need to define the following parameters to the **WS2812 RGB LED** included on the board. However, if additional LEDs are connected externally to the board, then the appropriate values should be provided for the Arduino library.

	**`#define NUM_LEDS 1`**
	:	There is only one WS2812 LED on the board

	**`#define DATA_PIN LED_RGB`**
	:	Declare which pin is connected to the WS2812 LED. On the RA6M5 Thing Plus, it is defined as `D13` or `RGB_LED` in the Arduino core for GPIO `P105`.

	**`#define LED_TYPE WS2812`**
	:	Declare the LED type for the library; the RA6M5 Thing Plus only includes `WS2812` RGB LED on the board.


<!-- Original Instructions (adjust snippet in "software_overview-codeless" when restoring)
### WS2812 RGB LED
While users are free to choose any Arduino library that provides support for WS2812 LEDs, we recommend the [FastLED Arduino library](https://github.com/FastLED/FastLED/). It has been tested and verified to work with the RGB LED on the RA6M5 Thing Plus. The [FastLED Arduino library](https://github.com/FastLED/FastLED/) can be installed from the **Library Manager** in the Arduino IDE by searching for:

	FastLED Arduino Library


<div class="grid" markdown>

<div markdown>

<figure markdown>
[![Install the FastLED Arduino library](./assets/img/hookup_guide/arduino-FastLED_library.png "Click to enlarge"){ width="400" }](./assets/img/hookup_guide/arduino-FastLED_library.png)
<figcaption markdown>FastLED Arduino library in the library manager of the Arduino IDE.</figcaption>
</figure>

</div>

<div markdown>

!!! tip "Manually Download the Arduino Library"
	For users who would like to manually download and install the library, the `*.zip` file can be accessed from the [GitHub repository](https://github.com/FastLED/FastLED/) or downloaded by clicking the button below.

	<center>
	[:octicons-download-16:{ .heart } Download the Arduino Library](https://github.com/FastLED/FastLED/archive/refs/heads/master.zip){ .md-button .md-button--primary }
	</center>

</div>

</div>
-->



### DA14531MOD BLE Module
--8<-- "./software-DA14531MOD.md"
