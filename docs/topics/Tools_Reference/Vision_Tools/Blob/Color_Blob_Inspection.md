Color Blob Inspection
=====================

![](../../../../img/x_Graphics/Tools/UvfColorToolsStdBlob-0.png)

Overview
--------

Color Blob inspection is a tool that performs blob analysis on color images. User defines a color representation (RGB or HIS) and which color ranges to accept or refuse. Color Blob tool merges color ranges settings to get a new image for standard blob analysis.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enable or disable the tool. (default = Yes) |
| Geometry | Defines tool's region shape.<ud> <li>Circle<br>Circular shape.</li>  <li>General rectangle (default)<br>Rectangular shape.</li>  <li>Annulus<br>Annulus shape.</li>  <li>General polygon<br>General polygon shape.</li>  <li>CAD (Closed ROI)<br>Closed shape imported from a CAD file.</li> </ud> |
| CAD file | CAD file name. |
| Layer name | Lists the layer names defined in the selected CAD file.<blockquote> **Connection tolerance**<br>Distance between close segment points to be considered as connected.. (default = 0)<br> </blockquote> |
| User calibration | If checked user defines parameters for CAD shapes calibration. Otherwise tool calibration is used.<blockquote> **Axes X rotation**<br>Rotation in the X axes to be applied to the CAD shape. (default = 0; min = -360; max = 360)<br>  **Axes Y rotation**<br>Rotation in the Y axes to be applied to the CAD shape. (default = 0; min = -360; max = 360)<br>  **Scale X**<br>Scale variation in the X axes to be applied to the CAD shape. You express scale value as a multiplier value. (default = 1)<br>  **Scale Y**<br>Scale variation in the Y axes to be applied to the CAD shape. You express scale value as a multiplier value. (default = 1)<br> </blockquote> |

| Tolerances and limits | |
| --- | --- |
| Min. Area | Blobs smaller than value are ignored for the result evaluation. |
| Blobs number | Enables or disables Blob number limit. <blockquote> **max. Blob number**<br>Maximum number of blobs that can be found. (default = 0)<br>  **minor defects**<br>Enable this condition for minor defects evaluation. (default = No)<br> </blockquote> |
| Single Blob area | Enables or disables Single Blob area limit.<blockquote> **single Blob area limit**<br>Maximum area for a single blob. (default = 100)<br>  **minor defects**<br>Enable this condition for minor defects evaluation. (default = No)<br> </blockquote> |
| Sum of all Blobs area | Enables or disables Sum of all Blobs area.<blockquote> **sum of all Blobs area limit**<br>Maximum value for the sum of the blobs' areas. (default = 500)<br>  **minor defects**<br>Enable this condition for minor defects evaluation.(default = No)<br> </blockquote> |
| Min. Area | Blobs smaller than value are ignored for the result evaluation. |

| Analysis | |
| --- | --- |
| Color space | Reference color space.   | HSI (default) | Hue-Saturation-Intensity color space. | | --- | --- | | RGB | Red-Green-Blue color space. | |
| Hue / Red | Range of validity of Hue/Red value. This color range forces a segmentation of the Hue (HIS) or Red (RGB) image plane. All pixels out of (into) this range are masked in Alike mode (Unlike mode). (default = Yes)<blockquote> **Specification**<br>Nominal value. (default = 0)<br>  **Tolerance+**<br>Positive tolerance. (default = 5.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 5.00)<br> </blockquote> |
| Saturation / Green | Range of validity of Saturation/Green value. This color range forces a segmentation of the Saturation (HIS) or Green (RGB) image plane. All pixels out of (into) this range are masked in Alike mode (Unlike mode). (default = No)<blockquote> **Specification**<br>Nominal value. (default = 0)<br>  **Tolerance+**<br>Positive tolerance. (default = 5.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 5.00)<br> </blockquote> |
| Intensity / Blue | Range of validity of Intensity/Blue value. This color range forces a segmentation of the Intensity (HIS) or Blue (RGB) image plane. All pixels out of (into) this range are masked in Alike mode (Unlike mode). (default = No)<blockquote> **Specification**<br>Nominal value. (default = 0)<br>  **Tolerance+**<br>Positive tolerance. (default = 5.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 5.00)<br> </blockquote> |
| Color Selection | Color selection for binarization.<ud> <li>Alike<br>Pixels with value outside the color ranges are masked.</li>  <li>Unalike<br>Pixels with value inside the color ranges are masked.</li> </ud> |
| Min. Area (pixel) | Area must be greater than this limit to be recognized as blob. |

### More

Click [here](../../../Windows/dialog_settings.md) to access the More section description.

Results
-------
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| --- | --- |
| Processing time | Tool processing time in msec. |
| Max. blobs number | Number of blobs found. |
| Total area (pixel) | Sum of the areas of all found blobs, in pixel. |
| All Blobs area (%) | Sum of the areas of all found blobs, percentage of ROI area. |
| Max. area (pixel) | Greatest blob area, in pixel. |
| Min. area (pixel) | Smallest blob area, in pixel. |
| Result | Selection of i-th found blob.<blockquote> **Area**<br>Area, in pixel.<br>  **Center X**<br>Center of mass X position.<br>  **Center Y**<br>Center of mass X position.<br> </blockquote> |

Images
------

| Binary | Segmented runtime image. |
| --- | --- |
| Hue / Red | Hue/Red plane color before segmentation. |
| Saturation / Green | Saturation/Green plane color before segmentation. |
| Intensity / Blue | Intensity/Blue plane color before segmentation. |
| Mask | Mask image to apply. White pixels are care pixels. Black pixels are don't care. |

Configuration
-------------
This tool is included into the library UvfColorToolsStd and UvfColorToolsCvl.



