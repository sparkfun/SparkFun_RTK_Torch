---
icon: simple/arduino
---

!!! warning "Data Corruption"
	To avoid any data loss or corrupting the SD card, users should disable all activity with the SD card before removing it from the RA6M5 Thing Plus.

	The [FATFileSystem library](https://github.com/arduino/ArduinoCore-renesas/tree/main/libraries/FATFilesystem) built into the Renesas-Arduino core, supports &micro;SD cards with a **FAT32** file system *(i.e. SD cards **up to 32GB** in size)*.

	- While users may be able to use cards with a higher storage capacity, we highly advise against it. As users may experience data loss due to a corrupt file system *(i.e. SD cards with a storage capacity greater than 32GB are not meant to be formatted with a FAT32 file system)*.


## SD Card - Test
The Renesas-Arduino core includes a built-in [FATFileSystem library](https://github.com/arduino/ArduinoCore-renesas/tree/main/libraries/FATFilesystem) that controls the SD host interface. The library that supports SD cards with a **FAT32** file system *(i.e. SD cards **up to 32GB** in size)*. Users can find an example sketch in the **File** > **Examples** > **Storage** > **TestSDCARD** drop-down menu.

??? note "Optional Hardware"
	<div class="grid cards" markdown>

	-   <a href="https://www.sparkfun.com/products/15107">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/3/4/7/0/15107-microSD_Card_-_1GB__Class_4_-01.jpg)
		</figure>

		---

		**microSD Card - 1GB (Class 4)**<br>
		COM-15107</a>


	-   <a href="https://www.sparkfun.com/products/19041">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/8/6/5/3/19041-microSD_Card_-_32GB__Class_10_-02.jpg)
		</figure>

		---

		**microSD Card - 32GB (Class 10)**<br>
		COM-19041</a>


	-   <a href="https://www.sparkfun.com/products/13004">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/9/9/5/8/13004-02.jpg)
		</figure>

		---

		**microSD USB Reader**<br>
		COM-13004</a>

	</div>


<!-- 
=== "`TestSDCARD.ino`"
	Users can find this sketch in the **File** > **Examples** > **Storage** > **TestSDCARD** drop-down menu.

	??? code "`TestSDCARD.ino`"
		```cpp
		--8<-- "https://raw.githubusercontent.com/arduino/ArduinoCore-renesas/main/libraries/Storage/examples/TestSDCARD/TestSDCARD.ino"
		```


=== "`SD_Test.ino`"
	Users can find this sketch in the **File** > **Examples** > **02.Digital** > **InputPullupSerial** drop-down menu.

	??? code "`SD_Test.ino`"
		```cpp
		--8<-- "./Firmware/Tests/SD_Test/SD_Test.ino"
		```
-->


??? code "`TestSDCARD.ino`"
	```cpp
	--8<-- "https://raw.githubusercontent.com/arduino/ArduinoCore-renesas/main/libraries/Storage/examples/TestSDCARD/TestSDCARD.ino"
	```
