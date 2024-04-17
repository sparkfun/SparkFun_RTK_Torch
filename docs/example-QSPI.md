---
icon: simple/arduino
---

## MX25L12833F
The Renesas-Arduino core includes a built-in [FATFileSystem library](https://github.com/arduino/ArduinoCore-renesas/tree/main/libraries/FATFilesystem) to control the QSPI flash memory. This example code demonstrates how to initialize the flash memory, a file is written, and data is read from the file. *Users can also find other example sketches in the **File** > **Examples** > **Storage** drop-down menu.*

??? code "`QSPI_Flash_FileSystem_Test.ino`"
	--8<-- "https://raw.githubusercontent.com/arduino/docs-content/main/content/hardware/04.pro/boards/portenta-c33/tutorials/user-manual/content.md:1236:1321"


--8<-- "https://raw.githubusercontent.com/arduino/docs-content/main/content/hardware/04.pro/boards/portenta-c33/tutorials/user-manual/content.md:1325:1325"

	??? code
		```cpp
		--8<-- "https://raw.githubusercontent.com/arduino/docs-content/main/content/hardware/04.pro/boards/portenta-c33/tutorials/user-manual/content.md:1272:1283"
		```

--8<-- "https://raw.githubusercontent.com/arduino/docs-content/main/content/hardware/04.pro/boards/portenta-c33/tutorials/user-manual/content.md:1326:1326"

	??? code
		```cpp
		--8<-- "https://raw.githubusercontent.com/arduino/docs-content/main/content/hardware/04.pro/boards/portenta-c33/tutorials/user-manual/content.md:1285:1299"
		```

--8<-- "https://raw.githubusercontent.com/arduino/docs-content/main/content/hardware/04.pro/boards/portenta-c33/tutorials/user-manual/content.md:1327:1327"

	??? code
		```cpp
		--8<-- "https://raw.githubusercontent.com/arduino/docs-content/main/content/hardware/04.pro/boards/portenta-c33/tutorials/user-manual/content.md:1301:1317"
		```
