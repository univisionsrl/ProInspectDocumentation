Color Light Meter
=================

![](../../../../img/x_Graphics/Tools/UvfColorToolsStdLightMeter-0.png)

Overview
--------

Color Light Meter calculates histogram of planes of color images and provides Hue/Saturation/Intensity (HSI Color Space) or Red/Green/Blue (RGB Color Space) statistics of the its region image area.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Geometry | Defines tool's region shape. At the moment the only available shape is Rectangle.   | Circle | Circular shape. | | --- | --- | | General rectangle (default) | Rectangular shape. | | Annulus | Annulus shape. | | General polygon | General polygon shape. | |

| Tolerances and limits | |
| --- | --- |
| Specification mode | Enabling automatic mode, specification values are automatically generated. (default = Automatic) |
| Mean H/R | Enable or disable histogram mean, of Hue/Red plane color, limits checks. (default = No)<blockquote> **Specification**<br>Nominal Hue/Red value. (default = 100.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 10.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 10.00)<br> </blockquote> |
| Dev. Std H/R | Enable or disable histogram standard deviation, of Hue/Red plane color, limits checks. (default = No)<blockquote> **Specification**<br>Nominal Hue/Red standard deviation value. (default = 1.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 1.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 1.00)<br> </blockquote> |
| Mean S/G | Enable or disable histogram mean, of Saturation/Green plane color, limits checks. (default = No)<blockquote> **Specification**<br>Nominal Saturation/Green value. (default = 100.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 10.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 10.00)<br> </blockquote> |
| Dev. Std S/G | Enable or disable histogram standard deviation, of Saturation/Green plane color, limits checks. (default = No)<blockquote> **Specification**<br>Nominal Saturation/Green standard deviation value. (default = 1.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 1.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 1.00)<br> </blockquote> |
| Mean I/B | Enable or disable histogram mean, of Intensity/Blue plane color, limits checks. . (default = No)<blockquote> **Specification**<br>Nominal Intensity/Blue value. (default = 100.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 10.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 10.00)<br> </blockquote> |
| Dev. Std I/B | Enable or disable histogram standard deviation, of Intensity/Blue plane color, limits checks (default = No)<blockquote> **Specification**<br>Nominal Intensity/Blue standard deviation value. (default = 1.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 1.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 1.00)<br> </blockquote> |

| Analysis | |
| --- | --- |
| Color space | Reference color space.   | HSI (default) | Hue-Saturation-Intensity color space. | | --- | --- | | RGB | Red-Green-Blue color space. | |

### More

Click More... to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool. |
| Processing time | Tool processing time in msec. |
| Mean H/R | Hue/Red mean value. |
| Dev. Std. H/R | Hue/Red standard deviation value. |
| Mean S/G | Saturation/Mean value. |
| Dev. Std. S/G | Saturation/Mean standard deviation value. |
| Mean I/B | Intensity/Blue mean value. |
| Dev. Std. I/B | Intensity/Blue standard deviation value. |

Configuration
-------------

This tool is included into the library UvfColorToolsStd and UvfColorToolsCvl.



