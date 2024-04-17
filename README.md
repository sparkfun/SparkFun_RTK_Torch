SparkFun Thing Plus - RA6M5
========================================

[![SparkFun Thing Plus - RA6M5](https://cdn.sparkfun.com/assets/parts/2/4/5/3/4/WRL-24243-Thing-Plus-RA6M5-Feature.jpg)](https://www.sparkfun.com/products/24243)

[*SparkFun Thing Plus - RA6M5 (WRL-24243)*](https://www.sparkfun.com/products/24243)

Clocking in at 200MHz, the RA6M5 is a high-performance microcontroller from [Renesas](https://www.renesas.com/) that is perfect for real-time applications. The [SparkFun Thing Plus - RA6M5](https://www.sparkfun.com/products/24243), is our latest [Thing Plus board](https://www.sparkfun.com/thing_plus) featuring the standard Qwiic connector, JST LiPo battery connector, 21 GPIO pins broken out in a Feather footprint, and status indicator LEDs. At the core is the RA6M5 microcontroller, a low-power Arm^®^ Cortex^®^-M33 processor with an available 512kB of SRAM and 2MB of Flash and an extensive list of peripheral capabilities. Additionally, we have included 16MB of QSPI Flash and an SD card slot on the board, so users won't have to worry about running out of memory space or data storage options.

The SparkFun RA6M5 Thing Plus also features Bluetooth® Low Energy connectivity, thanks to the provided DA14531MOD module *(also from Renesas)*. When actively transmitting, the DA14531MOD sips a mere 4mA and is capable of operating from a small coin-cell battery. The firmware provided on the module features Renesas' [SmartBond™ - CodeLess™ AT command](https://lpccs-docs.renesas.com/UM-140-DA145x-CodeLess/index.html) set. Therefore, users only need to send AT commands to configure a Bluetooth connection; without the need to reprogram the module.

**Note:**

- While the Thing Plus - RA6M5 does include some 5V tolerant pins, it is primarily a **3.3V** *logic-level* board.
- While the full capabilities of the RA6M5 support a broad range of features, only a limited set may be implemented, by default, in the [Renesas-Arduino core](https://github.com/arduino/ArduinoCore-renesas). However, the capabilities of the Thing Plus - RA6M5 should be comparable to the [Arduino Portenta C33](https://store.arduino.cc/collections/portenta-family/products/portenta-c33); with the exclusion of WiFi connectivity.

Documentation
--------------

* **[Hookup Guide (mkdocs)](http://docs.sparkfun.com/SparkFun_Thing_Plus_RA6M5/)** - The hookup guide for the Thing Plus - RA6M5 hosted by GitHub pages.<br>
  [![Built with Material for MkDocs](https://img.shields.io/badge/Material_for_MkDocs-526CFE?logo=MaterialForMkDocs&logoColor=white)](https://squidfunk.github.io/mkdocs-material/) [![GitHub Pages Deploy](https://github.com/sparkfun/SparkFun_Thing_Plus_RA6M5/actions/workflows/mkdocs.yml/badge.svg)](https://github.com/sparkfun/SparkFun_Thing_Plus_RA6M5/actions/workflows/mkdocs.yml)
* [SparkFun Graphical Datasheets](https://github.com/sparkfun/Graphical_Datasheets) - Graphical Datasheets for various SparkFun products.


*Need to download or print our hookup guide?*

* [Print *(Print to PDF)* from Single-Page View](http://docs.sparkfun.com/SparkFun_Thing_Plus_RA6M5/print_view)

Repository Contents
-------------------

* **[/docs](/docs/)** - Online documentation files
    * [assets](/docs/assets/) - Assets files
        * [board_files](/docs/assets/board_files/) - Files for the product design
            * [Eagle design files](/docs/assets/board_files/eagle_files.zip) (.zip)
            * [Schematic](/docs/assets/board_files/schematic.pdf) (.pdf)
            * [Dimensions](/docs/assets/board_files/dimensions.pdf) (.pdf)
            * [Graphical Datasheet](/docs/assets/board_files/graphical_datasheet.pdf) (.pdf)
        * [component_documentation](/docs/assets/component_documentation/) - Datasheets for hardware components
        * [img/hookup_guide/](/docs/assets/img/hookup_guide/) - Images for hookup guide documentation
* **[/Hardware](/Hardware/)** - Eagle design files (.brd, .sch)
  * **[/Production](/Production/)** - Production files

Product Variants
----------------

* [WRL-24243](https://www.sparkfun.com/products/24243)- v1.0, Initial Release

Version History
---------------

* [v10](https://github.com/sparkfun/SparkFun_Thing_Plus_RA6M5/releases/tag/v10) - Initial Release


License Information
-------------------

This product is ***open source***!

Please review the [`LICENSE.md`](./LICENSE.md) file for license information.

If you have any questions or concerns about licensing, please contact technical support on our [SparkFun forums](https://forum.sparkfun.com/viewforum.php?f=152).

Distributed as-is; no warranty is given.

- Your friends at SparkFun.
