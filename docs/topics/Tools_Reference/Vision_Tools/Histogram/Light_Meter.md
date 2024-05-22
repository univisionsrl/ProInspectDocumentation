Light Meter
===========


![](../../../../img/x_Graphics/Tools/UvfStdToolsLightmeter-0.png)


Overview
--------


Light Meter lets you calculate gray level distribution and statistics of the selected image area. It is based on the histogram of the image it processes.


Settings
--------





| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Geometry | Defines tool's region shape. Pixels outside of the shape region are treated as dont' care pixels<blockquote> **Circle**<br>Circular shape.<br>  **General rectangle (default)**<br>Rectangular shape.<br>  **Annulus**<br>Annulus shape.<br>  **General polygon**<br>General polygon shape.<br>  **Affine rectangle**<br>Rectangular shape with rounded corners.<br> </blockquote> |





| Tolerances and limits | |
| --- | --- |
| Specification mode | Enabling automatic mode, specification values are automatically generated. (default = Automatic) |
| Mean | Enable or disable histogram mean limits check. (default = No)<blockquote> **Specification**<br>Nominal value. (default = 100.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 10.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 10.00)<br> </blockquote> |
| Standard deviation | Enable or disable histogram standard deviation limits check. (default = No)<blockquote> **Specification**<br>Nominal value. (default = 1.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 1.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 1.00)<br> </blockquote> |
| Variance | Enable or disable histogram variance limits check. (default = No)<blockquote> **Specification**<br>Nominal value. (default = 1.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 1.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 1.00)<br> </blockquote> |
| Left tail | Enable or disable histogram left tail limits check. (default = No)<blockquote> **Percentage**<br>Percentage value that define the left tail. (default = 0)<br>  **Specification**<br>Nominal value. (default = 0)<br>  **Tolerance+**<br>Positive tolerance. (default = 5)<br>  **Tolerance-**<br>Positive tolerance. (default = 5)<br> </blockquote> |
| Right tail | Enable or disable histogram right tail limits check. (default = No)<blockquote> **Percentage**<br>Percentage value that defines right tail. (default = 0)<br>  **Specification**<br>Nominal value. (default = 0)<br>  **Tolerance+**<br>Positive tolerance. (default = 5)<br>  **Tolerance-**<br>Positive tolerance. (default = 5)<br> </blockquote> |
| Mode | Enable or disable histogram mode limits check. (default = No)<blockquote> **Specification**<br>Nominal value. (default = 128.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 10.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 10.00)<br> </blockquote> |
| Median | Enable or disable histogram median limits check. (default = No)<blockquote> **Specification**<br>Nominal value. (default = 128.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 10.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 10.00)<br> </blockquote> |
| Minimum value | Enable or disable minimum gray value limits check. (default = No)<blockquote> **Specification**<br>Nominal value. (default = 0.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 5.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 5.00)<br> </blockquote> |
| Maximum value | Enable or disable maximum gray value limits check. (default = No)<blockquote> **Specification**<br>Nominal value. (default = 255.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 5.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 5.00)<br> </blockquote> |
| Dark value | Range of validity of darker peak of the histogram. (default = No)<blockquote> **Specification**<br>Nominal value. (default = 0)<br>  **Tolerance+**<br>Positive tolerance. (default = 5.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 5.00)<br> </blockquote> |
| Bright value | Range of validity of brighter peak of the histogram.. (default = No)<blockquote> **Specification**<br>Nominal value. (default = 0.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 5.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 5.00)<br> </blockquote> |
| Distance peak to peak | Range of validity of the distance between the darker histogram peak and the brighter histogram peak. (default = No)<blockquote> **Specification**<br>Nominal value. (default = 0)<br>  **Tolerance+**<br>Positive tolerance. (default = 5.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 5.00)<br> </blockquote> |





| Analysis | |
| --- | --- |
| Partial range | Only a range of values of the histogram are taken into account. (default = No)<blockquote> **Min value**<br>Lower end of the range of values. (default = 0)<br>  **Max value**<br>Upper end of the range of values. (default = 255)<br> </blockquote> |


### More


Click More... to access the More section description.


Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool. |
| Processing time | Tool processing time in msec. |
| Mean | Mean value. |
| Standard deviation | Standard deviation value. |
| Variance | Variance value. |
| Left tail | Left tail value. |
| Right tail | Right tail value. |
| Mode | Mode value. |
| Median | Median value. |
| Minimum value | Minimum value. |
| Maximum value | Maximum value. |
| Dark value | Value of the darker peak of the resulting histogram. |
| Bright value | Value of the brighter peak of the resulting histogram. |
| Distance peak to peak | Distance between first and last peak of the histogram. |


Configuration
-------------


This tool is included into the library UvfStdTools.



