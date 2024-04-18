# Hardware Assembly

![RTK Torch on a Prism Pole with Bipod](GPS-24672-Action-4.jpg)

*RTK Torch on a Prism Pole with Bipod*

The RTK Torch has a standard 5/8" 11-TPI threaded base and is compatible with most equipment including surveying poles and equipment.

Users can elect to connect to the RTK Torch from a phone, laptop, or tablet. Any device with Bluetooth is compatible. See [Connecting Bluetooth](https://docs.sparkfun.com/SparkFun_RTK_Everywhere_Firmware/connecting_bluetooth/) for more information.

## Tilt Compensation

The RTK Torch benefits from an internal IMU that can allow a user to take very accurate location readings even if the pole is not completely vertical.

The IM19 inertial module fuses MEMS sensor and GNSS RTK positioning data to deliver low-cost, high-precision attitude measurement, delivering corrected RTK position data adding as little as 1cm inaccuracy to the position of the *point* of the surveying pole.

IM19 Features

* Extremely fast initializations, within 1~2s (95%)
* Accuracy 1 cm up to 30° tilt angle, 2 cm up to 60°
* Very fast calibration
* Reduces overall mapping inaccuracies and increases productivity by not requiring pole leveling in the field

In Rover mode with Tilt Compensation, once RTK Fix is achieved, tilt compensation can be enabled by tilting the unit back and forth on a surveyor's pole. Once the IMU is activated, the outputted NMEA sentences will be modified to output the location of the *tip* of the pole (not the location of the receiver). This allows taking measurements near trees, structure corners, even underwater topographies with accuracies of +1cm when the tilt is less than 30 degrees, and +2cm when the tilt is less than 60 degrees.

For more information, see the [Tilt Compensation](https://docs.sparkfun.com/SparkFun_RTK_Everywhere_Firmware/menu_tilt/) feature in the product manual.