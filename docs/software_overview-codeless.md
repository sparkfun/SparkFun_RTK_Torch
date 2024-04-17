---
icon: material/bluetooth
---

The firmware provided with the DA14531MOD Bluetooth module on the RA66M5 Thing Plus, utilizes Renesas' [SmartBond™ - CodeLess™ AT commands](https://www.renesas.com/us/en/software-tool/smartbond-codeless-commands) platform. This platform allows users to quickly get started on developing wireless IoT applications through a set of [AT Commands *(ASCII instructions)*](https://en.wikipedia.org/wiki/Hayes_AT_command_set) without having to write a single line of source code. The basic set of AT commands provides control over the Bluetooth® LE connectivity: BLE connect/disconnect, advertise, stop advertising, change roles (central/peripheral), scan for nearby devices, report BLE address, etc.


<div class="grid" markdown>

<div markdown>

## User Manual
Renesas provides documentation for the CodeLess platform:

- [DA14531 TINY™ Module Getting Started](https://lpccs-docs.renesas.com/UM-B-139-Getting-Started-with-DA14531-TINY-Module/index.html)
- [DA145`XX` CodeLess User Manual](https://lpccs-docs.renesas.com/UM-140-DA145x-CodeLess/index.html)

</div>


<div markdown>

!!! tip "Default Configuration"
	The default serial port configuration of the DA14531MOD for AT commands:

	- BaudRate : 57600
	- DataBits : 8
	- StopBits : 1
	- Parity : None
	- Flow Control : None
	- Transmit Text: Append CR


??? info "Firmware"
	The precompiled binary from the CodeLess SDK utilized as the firmware image, on the DA14531MOD of the RA6M5 Thing Plus, is the `codeless_531_datapump.hex` *(CodeLess for DA1453x datapump)*.

</div>

</div>



## Arduino Library
--8<-- "./software-DA14531MOD.md"


### Example - SerialPassThrough
In our *unofficial* Arduino library, there are several examples for configuring the Bluetooth connectivity of the DA14531MOD. Also included, is a `SerialPassThrough` example. Once programmed on the RA6M5 Thing Plus, it allows users to directly interface with the DA14531MOD's UART port through the board's USB connection using a [serial terminal](https://learn.sparkfun.com/tutorials/112). The example, utilizes the default configuration settings for the serial port on the DA14531MOD, as [listed above](#user-manual).


!!! terminal "Serial Terminal Emulator"
	In order to configure the DA14531MOD on the RA6M5 Thing Plus, users will need access to a [serial terminal emulator](https://learn.sparkfun.com/tutorials/112) on their computer. The [**Serial Monitor** in the Arduino IDE](https://docs.arduino.cc/software/ide-v2/tutorials/ide-v2-serial-monitor/) is more than suitable for this application; however, users are also free to utilize their terminal emulator of choice. Below are a few options, outside of the Arduino IDE:

	??? tip "Serial Communication and Serial Terminal"
		Check out our hookup guides on [serial communication](https://learn.sparkfun.com/tutorials/8) and [installing a terminal emulator](https://learn.sparkfun.com/tutorials/112):

		<div class="grid cards" markdown align="center">

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

		</div>

	=== "Windows"
		For Windows computers, we highly recommend [TeraTerm](https://teratermproject.github.io/index-en.html) *(open-source development project)*.

	=== "Mac OS"
		For Mac OS, users can check out [CoolTerm](https://freeware.the-meiers.org/) *(freeware)*.

	=== "Linux"
		Some Linux operating systems will already have the `screen` terminal emulator preinstalled.

