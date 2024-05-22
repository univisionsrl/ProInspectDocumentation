TInspect Color (3P)
===================

![](../../../../img/x_Graphics/Tools/UvfColorToolsStdTCInspect-0.png)

Overview
--------

The purpose of the Template Color Inspection tool is to detect defects on a surface. TColorInspect is a TInspect that works on RGB images or HSI images. So you can select the image planes of a color representation and tune grey TInspect processing.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Geometry | Defines tool model shape.<ud> <li>General rectangle (default)<br>Rectangular shape.</li>  <li>Circle<br>Circular shape.</li>  <li>Annulus<br>Annulus shape.</li>  <li>General polygon<br>General polygon shape.</li> </ud> |

| Tolerances and Limits | |
| --- | --- |
| Min. Area | Blobs smaller than value are ignored for the result evaluation. |
| Blobs number | Enables or disables Blob number limit. <blockquote> **max. Blob number**<br>Maximum number of blobs that can be found. (default = 0)<br>  **minor defects**<br>Enable this condition for minor defects evaluation. (default = No)<br> </blockquote> |
| Single Blob area | Enables or disables Single Blob area limit.<blockquote> **single Blob area limit**<br>Maximum area for a single blob. (default = 100)<br>  **minor defects**<br>Enable this condition for minor defects evaluation. (default = No)<br> </blockquote> |
| Sum of all Blobs area | Enables or disables Sum of all Blobs area.<blockquote> **sum of all Blobs area limit**<br>Maximum value for the sum of the blobs' areas. (default = 500)<br>  **minor defects**<br>Enable this condition for minor defects evaluation.(default = No)<br> </blockquote> |
| Sum of all Blobs area (%) | Enables or disables Sum of all Blobs area as percentage of ROI.<blockquote> **sum of all Blobs area limit (%)**<br>Maximum value (%) for the sum of the blobs' areas. (default = 0)<br>  **minor defects**<br>Enable this condition for minor defects evaluation. (default = No)<br> </blockquote> |

| Analysis | |
| --- | --- |
| Color space | Reference color space representation.   | HSI (default) | Hue-Saturation-Intensity color space. | | --- | --- | | RGB | Red-Green-Blue color space. | |
| Hue / Red | Enable or disable TInspect on Hue / Red color plane. (default = Yes)<blockquote> **Intensity sensitivity**<br>This parameter represents an index of the sensitivity of the tool to variations of brightness. The higher the value the smaller will be the intensity difference considered as a defect. Intensity sensitivity modifies the threshold image used to filter runtime image. Its range varies from 0 (low sensitivity) to 99 (high sensitivity). Every value drives a pair of parameters (#Proportional and #Constant) that define how the threshold image is modified.  I(x, y) = Proportional \ SDev + Constant  At every position (x, y) threshold image intensity I is the sum of a constant value and a scaling value of standard deviation of training samples at that point. (default = 25)            Proportional      Scaling factor for the sensitivity function. (default = 8.0)          Constant      Offset level for the sensitivity function. (default = 15.5)<br>  **Proportional**<br>Read only value. Scaling factor for the sensitivity function. (default = 8.0)<br>  **Constant**<br>Read only value. Offset level for the sensitivity function. (default = 15.5)<br>  **Dimension sensitivity**<br>This parameter represents an index of the sensitivity of the tool to the area of defects. The higher the value the smaller will be the area of a region considered as a defect. Dimension sensitivity is the minimum area of blob analysis after thresholding. (default = 25)            Area min. (pixel)      Minimum area that can be considered as a defect. (default = 75)<br>  **Area min. (pixel)**<br>Read only value. Minimum area that can be considered as a defect. (default = 75)<br>  **Saturation value**<br>This parameter, available only in HSI color space, masks all pixels in the saturation plane with a higher grey value. (default = 10)<br> </blockquote> |
| Saturation / Green | Enable or disable TInspect on Saturation/Green color plane. (default = Yes)<blockquote> **Intensity sensitivity**<br>see Intensity sensitivity<br>  **Proportional**<br>Read only value. Scaling factor for the sensitivity function. (default = 8.0)<br>  **Constant**<br>Read only value. Offset level for the sensitivity function. (default = 15.5)<br>  **Dimension sensitivity**<br>see Dimension sensitivity<br>  **Area min. (pixel)**<br>Read only value. Minimum area that can be considered as a defect. (default = 75)<br> </blockquote> |
| Intensity / Blue | Enable or disable TInspect on Intensity/Blue image plane. (default = Yes)<blockquote> **Intensity sensitivity**<br>see Intensity sensitivity<br>  **Proportional**<br>Read only value. Scaling factor for the sensitivity function. (default = 8.0)<br>  **Constant**<br>Read only value. Offset level for the sensitivity function. (default = 15.5)<br>  **Dimension sensitivity**<br>see Dimension sensitivity<br>  **Area min. (pixel)**<br>Read only value. Minimum area that can be considered as a defect. (default = 75)<br> </blockquote> |
| Defect mode | | Dark and White objects (default) | Looks for defects with both polarities. It means that difference between run time image and threshold image is unsigned. | | --- | --- | | White objects (default) | Looks for defects with white polarity. Dark differences are clamped. | | Dark objects | Looks for defects with black polarity. White differences are clamped. | |
| Normalization | Normalization to apply to runtime image before preprocessing.<ud> <li>None<br>Normalization is not performed.</li>  <li>Mean & StDev<br>Normalization is applied by mean and standard deviation.</li>  <li>Mean<br>Normalization is applied by mean.</li> </ud> |
| Sobel image | Sobel Image used to highlight borders and edges of template image.<ud> <li>None<br>Do not use</li>  <li>Add image to samples<br>Add this image to threshold image to make tools less sensitive in that regions (around borders or edges).</li> </ud><blockquote> **Magnitude scaling factor**<br>Sobel parameter to magnify edges.<br>  **Magnitude threshold**<br>Threshold for Sobel's edges.<br> </blockquote> |
| Blank scene | Enable or disable TInspect working mode. If enabled, no template model is required but a uniform image of blank scene grey value. (default = 25)<blockquote> **blank scene value**<br>Template image gray value. (default = 128)<br> </blockquote> |
| Erode difference image | Morphology to apply to difference image. (default = false)<blockquote> **Filter size**<br>Size of erosion operator. (default = 1)<br> </blockquote> |
| Use train image as sample | Includes the train image in the training images set. (default = No) |
| Use custom samples | Uses a different training images set instead of usual. All tools in a View that needs statistical training use the same set. If this flag is set the tool must be trained alone. default = No)<blockquote> **Samples folder**<br>Specifies the folder containing training specific images set to use.<br> </blockquote> |

### More

Click More... to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| Processing time | Tool processing time in msec. |
| Max blobs number | Found blobs count. |
| Total area (pixel) | Sum of the areas of all found blobs, in pixel. |
| Sum of all Blobs area (%) | Sum of the areas of all found blobs, in %. |
| Max. area (pixel) | Greatest area of all found blobs, in pixel. |
| Min. area (pixel) | Smallest area of all found blobs, in pixel. |
| Result | Select the index of the blob to show information about.<blockquote> **Area**<br>Area of the selected blob, in pixel.<br>  **Center X**<br>Position X of the center of mass of the selected blob.<br>  **Center Y**<br>Position Y of the center of mass of the selected blob.<br> </blockquote> |

Images
------

| Images | |
| --- | --- |
| Inspected Hue/Red Saturation/Green Intensity/Blue | Run time Hue/red image |
| Threshold Hue/Red Saturation/Green Intensity/Blue | Threshold Image result of statistical training. Every pixel value of the image is the threshold of the difference between run-time image and template image. Sensitivity modifies this threshold. |
| Difference Hue/Red Saturation/Green Intensity/Blue | Difference image between runtime minus template and threshold image. |
| Model Hue/Red Saturation/Green Intensity/Blue | Template image. |
| Sobel Hue/Red Saturation/Green Intensity/Blue | Sobel image. |
| Mask | Mask image: care pixels are white; don't care pixels are black. |
| Threshold with extra mask | Threshold image with runtime movable masks |

Configuration
-------------

This tool is included into the library UvfColorToolsStd and UvfColorToolsCvl.

