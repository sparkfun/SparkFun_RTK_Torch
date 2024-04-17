While an Arduino library isn't necessary to utilize the [CodeLess™ AT commands](https://www.renesas.com/us/en/software-tool/smartbond-codeless-commands) for the DA14531MOD Bluetooth module, we have created an *unofficial* Arduino library to help users get started. As an official library, users will need to manually download and install the library into the Arduino IDE; it will not be available through the **Library Manager**.


<div class="grid" markdown>

<div markdown>

!!! tip "Manually Download the Arduino Library"
	To manually download and install the library, the files can be accessed from our [GitHub repository](https://github.com/sparkfun/SparkFun_Thing_Plus_RA6M5/tree/main/Firmware/CodelessBLE) or the `*.zip` can be downloaded by clicking the button below.

	<center>
	[:octicons-download-16:{ .heart } Download the Arduino Library](./assets/CodelessBLE.zip){ .md-button .md-button--primary }
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


!!! tip
	In this Arduino library, there are several examples for configuring the Bluetooth connectivity of the DA14531MOD.

	However, we also include a `SerialPassThrough` example. Once programmed on the RA6M5 Thing Plus, it allows users to directly interface with the DA14531MOD's UART port through the board's USB connection using a [serial terminal](https://learn.sparkfun.com/tutorials/112). Therefore, enabling users to experiment with the CodeLess AT commands and develop their own BLE connectivity solution.