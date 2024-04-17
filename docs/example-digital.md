---
icon: simple/arduino
---

## Digital Output
LEDs are a perfect visual indicator for the operation of a digital output.

### LED - Blink

Below, is one of the simplest built-in examples of the Arduino IDE. Users can find this sketch in the **File** > **Examples** > **01.Basics** > **Blink** drop-down menu. The example toggles the digital output of the GPIO pin connected to the blue, `STAT` *(status)* LED.


!!! tip
	Users do not have to worry about modifying the sketch for the GPIO pin that is connected to the `STAT` LED. The pin is already defined in the Arduino core with the `LED_BUILTIN` variable. Therefore, no adjustments are necessary to utilize this example code.


??? code "`Blink.ino`"
	--8<-- "https://raw.githubusercontent.com/arduino/docs-content/main/content/built-in-examples/01.basics/Blink/Blink.md:89:89"



### LED - PWM
LEDs are also great visual indicators for PWM outputs.

On the RA6M5 Thing Plus, the GPIO pin connected to the `STAT` LED is also capable of generating a PWM output. There are two built-in examples in the Arduino IDE for operating a PWM output on an LED. The sketches operate by oscillating the duty cycle of the PWM signal from the GPIO pin so that the LED appears to be dimming or *fading*.


!!! tip
	Users will need to modify the sketches below, for the GPIO pin that is connected to the `STAT` LED. As mentioned in the example above, they can use the predefined `LED_BUILTIN` variable. Users will need to {--replace the highlighted line--} with the {++modification using the `LED_BUILTIN` variable++} to define the GPIO pin connected to the `STAT` LED.


	<div class="grid" markdown>

	<div markdown>

	!!! code "`Fade.ino`"
				int led = {--9;         // the PWM pin the LED is attached to--}
				int led = {++LED_BUILTIN; // the PWM pin the LED is attached to++}

	</div>


	<div markdown>

	!!! code "`Fading.ino`"
				int ledPin = {--9;  // LED connected to digital pin 9--}
				int ledPin = {++LED_BUILTIN;  // LED connected to digital pin 14++}

	</div>

	</div>


=== "`Fade.ino`"
	Users can find this sketch in the **File** > **Examples** > **01.Basics** > **Fade** drop-down menu.

	??? code "`Fade.ino`"
		--8<-- "https://raw.githubusercontent.com/arduino/docs-content/main/content/built-in-examples/01.basics/Fade/Fade.md:52:52"


=== "`Fading.ino`"
	Users can find this sketch in the **File** > **Examples** > **03.Analog** > **Fading** drop-down menu.


	!!! warning "PWM &ne; Analog"
		Although this example is listed under the **03.Analog** menu, users should keep in mind that a PWM output is not a **true** analog signal. PWM signals can only *emulate an analog output*, based on the average voltage output of their square waveform.


	??? code "`Fading.ino`"
		<iframe class='arduino-sketch-iframe' src='https://create.arduino.cc/example/builtin/03.Analog%5CFading/Fading/preview?embed&snippet' style='height:752px;width:100%;margin:10px 0' frameborder='0'></iframe>



### LED - WS2812
!!! warning
	Support for the new Renesas Arduino boards has not been officially released for the FastLED Arduino library. Users should follow the [installation steps](../software_overview-arduino/#ws2812-rgb-led) documented in the **Software Overview**.


The **WS2812** is an addressable RGB LED that operates with a digital signal that stacks frames of 24-bit data, per LED in a chain. We recommend that the [FastLED Arduino library](https://github.com/FastLED/FastLED/) be utilized in the Arduino IDE, to control the RGB LED on the RA6M5 Thing Plus. Once the [library is installed in the Arduino IDE](../software_overview-arduino/#ws2812-rgb-led), users will find several example sketches listed in the **File** > **Examples** > **FastLED** > drop-down menu. We recommend the following examples for users to get started:

- `Blink.ino`
- `ColorTemperature.ino`
- `ColorPalette.ino`

!!! tip
	Below, are a few tips for users to start working with the FastLED Arduino library. However, for more details, users should refer to the [documentation for the FastLED Arduino library](https://fastled.io/docs/index.html).

	??? code "Define Parameters"
		When utilizing the examples in the FastLED Arduino library, users may need to define and/or modify a few parameters:


		```cpp
		// GPIO pins connected to the LED
		#define LED_PIN      LED_RGB // (1)!
		// #define CLOCK_PIN      13 (2)

		// Information about the LED (strip)
		#define NUM_LEDS    1        // (3)!
		#define CHIPSET     WS2812   // (4)!
		#define COLOR_ORDER GRB      // (5)!

		// Define the array of leds
		CRGB leds[NUM_LEDS];

		// 
		#define BRIGHTNESS  40       // (6)!
		```
	
		1. For the RA6M5 Thing Plus, users can either refer to the predefined variable `LED_RGB` or define the pin as `13` *(`D13`)* for the RGB LED
		1. A **clock pin is not required** for the WS2812 LED on the RA6M5 Thing Plus; comment out any mentions of it
		1. On the RA6M5 Thing Plus, there is only **one** RGB LED included on the board
		1. The RGB LED on the RA6M5 Thing Plus is a **WS2812** LED
		1. The format of the color order in the WS2812's data frames is Green, Red, Blue *(**GRB**)*
		1. Some of the examples may define an LED brightness; this should be an 8-bit value *(`0`-`255`)*. Below, is a table of reference values for users to get started with:
	
			| Environment     | Description | Value |
			| :-------------: | :---------- | :---: |
			| Dark Room       | Start to see primary colors | `5` - `12`    |
			| Direct Sunlight | Start to see primary colors | **>** `60`    |
			| Direct Sunlight | Start to see color blending | `100` - `180` |
			| Direct Sunlight | Decent color blending       | **>** `230`   |


	??? code "Instantiate LED Controller"
		Most of the examples in the FastLED library predefine parameters for the LED *(strip)*, as shown above. Later in the sketches, an instance of the [LED controller](https://fastled.io/docs/class_c_l_e_d_controller.html) is created; therefore, if users have already modified all the parameters above, no other modifications should be necessary:


		```cpp
		FastLED.addLeds<CHIPSET, LED_PIN, COLOR_ORDER>(leds, NUM_LEDS);
		```


		Otherwise, users will need to locate where the instance of the [LED controller](https://fastled.io/docs/class_c_l_e_d_controller.html) is created and provide the required values. Users will also need to [configure the LED brightness](https://fastled.io/docs/class_c_fast_l_e_d.html#a730ba7d967e882b4b893689cf333b2eb) later in the sketch, if that predefined variable isn't provided either:


			FastLED.addLeds<{==WS2812==}, {==13==}, GRB>(leds, {==1==});
			FastLED.setBrightness({==<value>==});


		The example code should still [enumerate the order of the RGB color channels](https://fastled.io/docs/group___pixel_types.html#ga3c26d076773aa0f331d3066b46dbc6a4), required for the data frames of the LED chipset. However, users may need to modify the enumerator to `GRB`:


		```cpp	
		#define COLOR_ORDER GRB
		```



=== "`Blink.ino`"
	Users can find this sketch in the **File** > **Examples** > **FastLED** > **Blink** drop-down menu.

	??? code "`Blink.ino`"
		```cpp
		--8<-- "https://raw.githubusercontent.com/FastLED/FastLED/master/examples/Blink/Blink.ino"
		```


=== "`ColorTemperature.ino`"
	Users can find this sketch in the **File** > **Examples** > **FastLED** > **ColorTemperature** drop-down menu.

	??? code "`ColorTemperature.ino`"
		```cpp
		--8<-- "https://raw.githubusercontent.com/FastLED/FastLED/master/examples/ColorTemperature/ColorTemperature.ino"
		```


=== "`ColorPalette.ino`"
	Users can find this sketch in the **File** > **Examples** > **FastLED** > **ColorPalette** drop-down menu.

	??? code "`ColorPalette.ino`"
		```cpp
		--8<-- "https://raw.githubusercontent.com/FastLED/FastLED/master/examples/ColorPalette/ColorPalette.ino"
		```


=== "Sunlight Test"
	This sketch allows users to test the brightness of the WS2812 RGB LED on the RA6M5 Thing Plus in direct sunlight. The sketch implements an interrupt on the ++"USRBTN"++ button to increase the brightness of the LED in increments. The brightness value is then displayed on the [Qwiic OLED Display](https://www.sparkfun.com/products/24606), which is connected by a [Qwiic cable](https://www.sparkfun.com/products/17260).

	??? note "Optional Hardware"
		<div class="grid cards" markdown>

		-   <a href="https://www.sparkfun.com/products/17260">
			<figure markdown>
			![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/6/2/4/7/17260-Flexible_Qwiic_Cable_-_50mm-01.jpg)
			</figure>

			---

			**Flexible Qwiic Cable - 50mm**<br>
			PRT-17260</a>


		-   <a href="https://www.sparkfun.com/products/24606">
			<figure markdown>
			![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/4/9/6/3/LCD-24606-Qwiic-OLED-Display-Feature-Screen.jpg)
			</figure>

			---

			**SparkFun Qwiic OLED Display (0.91 in., 128x32)**<br>
			LCD-24606</a>

		</div>


	The example code can be found in the [GitHub repository](https://github.com/sparkfun/SparkFun_Thing_Plus_RA6M5/tree/main/docs/assets/arduino_examples/RGB_sunlight/RGB_sunlight.ino). However, users can simply click the button to download the code or expand the box *(below)* to copy the code.


	??? code "`RGB_sunlight.ino`"
		```cpp
		--8<-- "./assets/arduino_examples/RGB_sunlight/RGB_sunlight.ino"
		```


	<center>
	[:octicons-download-16:{ .heart } Download the Example Sketch](./assets/arduino_examples/RGB_sunlight/RGB_sunlight.ino){ .md-button .md-button--primary }
	</center>


*For more information, please refer to the [WS2812 datasheet](./assets/component_documentation/WS2812C-2020.pdf) and [FastLED Arduino library](https://github.com/FastLED/FastLED/).*




## Digital Input
Buttons are great for learning about digital inputs; and are often paired with LEDs, as a visual indicator for their operation.

### Button - ++"USRBTN"++
On the RA6M5 Thing Plus, the ++"USRBTN"++ button is the perfect component for operating a digital input. There are several built-in examples in the Arduino IDE for the basic use of a button as an input device. These examples utilize a digital intput to toggle an LED and/or generate an output text on the USB serial port. Users can find these sketches in the **File** > **Examples** > **01.Basics** > **DigitalReadSerial**  and **File** > **Examples** > **02.Digital** drop-down menus.

- `DigitalReadSerial.ino`
- `Button.ino`
- `Debounce.ino`
- `InputPullupSerial.ino`


!!! tip
	Users will need to modify the sketches below, for the GPIO pin that is connected to the `STAT` LED and ++"USRBTN"++. As previously, they can use the predefined `LED_BUILTIN` variable for the GPIO pin that is connected to the `STAT` LED. For the GPIO pin that is connected to the ++"USRBTN"++, users till need to modify the pin to `D31`.

	For more details, expand the boxes below to see the {++modifications++} that required to {--replace the highlighted values--}, in order to define the GPIO pins connected to the `STAT` LEDand ++"USRBTN"++


	<div class="grid" markdown>

	<div markdown>

	??? code "++"USRBTN"++"
		`DigitalReadSerial.ino`

		---

			int pushButton = {--2--};
			int pushButton = {++31++};

		`Button.ino` and `Debounce.ino`

		---

			const int buttonPin = {--2--};  // the number of the pushbutton pin
			const int buttonPin = {++31++};  // the number of the pushbutton pin

		`InputPullupSerial.ino`

		---

			pinMode({--2--}, INPUT_PULLUP);
			pinMode({++31++}, INPUT_PULLUP);

			int sensorVal = digitalRead({--2--});
			int sensorVal = digitalRead({++31++});

	</div>


	<div markdown>

	??? code "`STAT` LED"
		`Button.ino` and `Debounce.ino`

		---

			const int ledPin = {--13--};    // the number of the LED pin
			const int ledPin = {++LED_BUILTIN++};    // the number of the LED pin

		`InputPullupSerial.ino`

		---

			pinMode({--13--}, OUTPUT);
			digitalWrite({--13--}, value);

			pinMode({++LED_BUILTIN++}, OUTPUT);
			digitalWrite({++LED_BUILTIN++}, value);

	</div>

	</div>



=== "`DigitalReadSerial.ino`"
	Users can find this sketch in the **File** > **Examples** > **01.Basics** > **DigitalReadSerial** drop-down menu.

	??? code "`DigitalReadSerial.ino`"
		--8<-- "https://raw.githubusercontent.com/arduino/docs-content/main/content/built-in-examples/01.basics/DigitalReadSerial/DigitalReadSerial.md:65:65"


=== "`Button.ino`"
	Users can find this sketch in the **File** > **Examples** > **02.Digital** > **Button** drop-down menu.

	??? code "`Button.ino`"
		--8<-- "https://raw.githubusercontent.com/arduino/docs-content/main/content/built-in-examples/02.digital/Button/Button.md:45:45"


=== "`Debounce.ino`"
	Users can find this sketch in the **File** > **Examples** > **02.Digital** > **Debounce** drop-down menu.

	??? code "`Debounce.ino`"
		--8<-- "https://raw.githubusercontent.com/arduino/docs-content/main/content/built-in-examples/02.digital/Debounce/Debounce.md:41:41"


=== "`InputPullupSerial.ino`"
	Users can find this sketch in the **File** > **Examples** > **02.Digital** > **InputPullupSerial** drop-down menu.

	??? code "`InputPullupSerial.ino`"
		--8<-- "https://raw.githubusercontent.com/arduino/docs-content/main/content/built-in-examples/02.digital/InputPullupSerial/InputPullupSerial.md:68:68"



### Interrupts
The RA6M5 provides IRQ support on several of its digital input pins. This feature is great for creating an instantaneous response to a digital input, without having to wait for the MCU to complete its current task.


<div class="grid" markdown>

<div markdown>

!!! code
	```cpp
	const byte ledPin = LED_BUILTIN;
	const byte interruptPin = 31;
	--8<-- "https://raw.githubusercontent.com/arduino/reference-en/master/Language/Functions/External%20Interrupts/attachInterrupt.adoc:108:122"
	```

</div>


<div markdown>

!!! arduino
	In the Arduino IDE, interrupt requests are configured using the [`#!cpp attachInterrupt(digitalPinToInterrupt(pin), ISR, mode)` function](https://www.arduino.cc/reference/en/language/functions/external-interrupts/attachinterrupt/), where:

	- `pin` - The GPIO pin
	- `ISR` -	The interrupt service routine to call/execute when the interrupt occurs
	- `mode` - Defines how the interrupt should be triggered:
		- `LOW` - When the pin is **LOW**
		- `CHANGE` - Whenever the pin changes value
		- `RISING` - When the pin changes from **LOW** to **HIGH**
		- `FALLING`- When the pin changes from **HIGH** to **LOW**

</div>

</div>


!!! warning
	When utilizing an interrupt on a digital GPIO, the attached interrupt service routine should be able to execute within the shortest, possible time frame. Otherwise, the suspended task could trigger various faults or errors.
