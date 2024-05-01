# Operating Modes

The RTK Torch can be used in a variety of modes:

* GNSS Positioning (~800mm accuracy) - also known as 'Rover'
* GNSS Positioning with RTK (8mm accuracy) - using a local base station
* GNSS Positioning with PPP-RTK (14 to 60mm accuracy) - using PointPerfect corrections
* GNSS Positioning with Tilt Compensation
* GNSS Base Station
* GNSS Base Station NTRIP Server

## Rover

In **Rover** mode, the RTK Torch will receive L1, L2, and L5 GNSS signals from the four constellations (GPS, GLONASS, Galileo, and BeiDou) and output the devices' position with accuracies around 800mm. The device will calculate the position based on the combination of GNSS and any correction signals (primarily DGPS if available). Similar to a standard-grade GPS receiver, the RTK Torch will output industry standard NMEA sentences at 2Hz and broadcast them over any paired Bluetooth® device. The end user will need to parse the NMEA sentences using [commonly available mobile apps, GIS products](https://docs.sparkfun.com/SparkFun_RTK_Everywhere_Firmware/gis_software/), or embedded devices (there are many open source libraries).

## Rover with RTK

In **Rover with RTK** mode, the RTK Torch will receive GNSS signals and combine them with RTCM correction data to achieve accuracy of approximately 8mm horizontal positional accuracy and 15mm vertical accuracy. The RTCM correction data is most easily obtained over a cellular connection to the Internet using a free app on your phone (see SW Maps or Lefebure NTRIP) and sent over Bluetooth®. Additionally, corrections can be obtained over WiFi, or [ESP-NOW](https://docs.sparkfun.com/SparkFun_RTK_Everywhere_Firmware/menu_radios/). Correction data can come from 2nd unit setup as a base station, from a free local base station, or from a paid service. See the [Quick Start guide](https://docs.sparkfun.com/SparkFun_RTK_Everywhere_Firmware/quickstart-torch/#ntrip-example) and the [NTRIP Client](https://docs.sparkfun.com/SparkFun_RTK_Everywhere_Firmware/menu_gnss/#ntrip-client) for more information.

## Rover with PPP-RTK

In **Rover with PPP-RTK**, the RTK Torch will receive GNSS signals and combine them with correction data provided over an IP connection (usually a cell phone hotspot). The corrections are State Space Representation (SSR) based and are also known as PPP-RTK. These corrections are obtained from [ublox's PointPerfect network](https://docs.sparkfun.com/SparkFun_RTK_Everywhere_Firmware/menu_pointperfect/). Time to RTK Fix can take up to 300 seconds and has 14 to 60mm horizontal positional accuracy.

## Rover with Tilt Compensation

In **Rover with Tilt Compensation**, once RTK Fix is achieved, [tilt compensation can be enabled](https://docs.sparkfun.com/SparkFun_RTK_Everywhere_Firmware/menu_tilt/#entering-tilt-compensation-mode) by tilting the unit back and forth on a surveyor's pole. Once the IMU is activated, the outputted NMEA sentences will be modified to output the location of the tip of the pole (not the location of the receiver). This allows taking measurements near trees, structure corners, even underwater topographies with accuracies of +1cm when the tilt is less than 30 degrees, and +2cm when the tilt is less than 60 degrees.

## Base Station

In **Base Station** mode the device is mounted to a fixed position (like a tripod or roof) and will initiate a survey. After 60 to 120 seconds the survey will complete and the RTK Torch will begin transmitting RTCM correction data over the built in 2.4GHz radio (if [ESP-NOW](https://docs.sparkfun.com/SparkFun_RTK_Everywhere_Firmware/menu_radios/) is enabled). A base is often used in conjunction with a second RTK Torch unit (or [RTK Facet](https://www.sparkfun.com/products/19984), [RTK Surveyor](https://www.sparkfun.com/products/18443), [Express](https://www.sparkfun.com/products/18442), [Express Plus](https://www.sparkfun.com/products/18589), etc) set to 'Rover' to obtain the 8mm accuracy. Said differently, the Base sits still and sends correction data to the Rover so that the Rover can output a really accurate position. The relative accuracy of this mode is 8mm base-to-rover but has higher (up to a meter) of absolute inaccuracy. See [how to set up a permanent base](https://docs.sparkfun.com/SparkFun_RTK_Everywhere_Firmware/permanent_base/) to decrease the absolute inaccuracy.

## Base Station with NTRIP

In **Base Station with NTRIP** the device will enter Base Station mode. If WiFi is available, and the [NTRIP Server(s)](https://docs.sparkfun.com/SparkFun_RTK_Everywhere_Firmware/menu_base/#ntrip-server) is enabled, its corrections will be broadcast to up to four NTRIP casters and made available to any rover that also has internet access and is within 10-20km.