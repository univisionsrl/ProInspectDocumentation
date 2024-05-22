TInspect
========

![](../../../../img/x_Graphics/Tools/UvfUITInspect-0.png)

Overview
--------

The purpose of the Template Inspection tool is to detect defects on a surface. TInspect needs to be pre-aligned by other tools providing a Fixture that arranges its run time position. The tool creates the template model image of an object statistically, from a set of training images and then compares run-time images of the object with it. A defect is any region that differs from model more than an expected tolerated variation given by the training images set. A defect can be a dark or bright spot on an object, an incorrectly shaped feature, or the absence of a shape. Basically, TInspect preprocesses image, computes difference with threshold image, applies some morphology filtering, and runs blob analysis.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Geometry | Defines tool model region by contour shape. <ud> <li>General rectangle (default)<br>Rectangular shape.</li>  <li>Circle<br>Circular shape.</li>  <li>Annulus<br>Annulus shape.</li>  <li>General polygon<br>General polygon shape.</li> </ud> |

| Tolerances and limits | |
| --- | --- |
| Min. Area | Blobs smaller than value are ignored for the result evaluation. |
| Blobs number | Enables or disables Blob number limit. <blockquote> **max. Blob number**<br>Maximum number of blobs that can be found. (default = 0)<br>  **minor defects**<br>Enable this condition for minor defects evaluation. (default = No)<br> </blockquote> |
| Single Blob area | Enables or disables Single Blob area limit.<blockquote> **single Blob area limit**<br>Maximum area for a single blob. (default = 100)<br>  **minor defects**<br>Enable this condition for minor defects evaluation. (default = No)<br> </blockquote> |
| Sum of all Blobs area | Enables or disables Sum of all Blobs area.<blockquote> **sum of all Blobs area limit**<br>Maximum value for the sum of the blobs' areas. (default = 500)<br>  **minor defects**<br>Enable this condition for minor defects evaluation.(default = No)<br> </blockquote> |
| Sum of all Blobs area (%) | Enables or disables Sum of all Blobs area as percentage of ROI.<blockquote> **sum of all Blobs area limit (%)**<br>Maximum value (%) for the sum of the blobs' areas. (default = 0)<br>  **minor defects**<br>Enable this condition for minor defects evaluation. (default = No)<br> </blockquote> |
| Model image average | Enable or disable gray model image average tolerance limits. (default = No)<blockquote> **Specification**<br>Nominal value. (default = 100.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 10.00)<br>  **Tolerance-**<br>Positive tolerance. (default = 10.00)<br> </blockquote> |

| Analysis | |
| --- | --- |
| Intensity sensitivity | This parameter represents an index of the sensitivity of the tool to variations of brightness. The higher the value the smaller will be the intensity difference considered as a defect. Intensity sensitivity modifies the threshold image used to filter runtime image. Its range varies from 0 (low sensitivity) to 99 (high sensitivity). Every value drives a pair of parameters (#Proportional and #Constant) that define how the threshold image is modified.  I(x, y) = Proportional \ SDev + Constant At every position (x, y) threshold image intensity I is the sum of a constant value and a scaling value of standard deviation of training samples at that point. (default = 25)<blockquote> **Proportional**<br>Scaling factor for the sensitivity function. (default = 8.0)<br>  **Constant**<br>Offset level for the sensitivity function. (default = 15.5)<br> </blockquote> |
| Dimension sensitivity | This parameter represents an index of the sensitivity of the tool to the area of defects. The higher the value the smaller will be the area of a region considered as a defect. Dimension sensitivity is the minimum area of blob analysis after thresholding. (default = 25)<blockquote> **Area min. (pixel)**<br>Minimum area that can be considered as a defect. (default = 75)<br> </blockquote> |
| Defect mode | | Dark and White objects (default) | Looks for defects with both polarities. It means that difference between run time image and threshold image is unsigned. | | --- | --- | | White objects (default) | Looks for defects with white polarity. Dark differences are clamped. | | Dark objects | Looks for defects with black polarity. White differences are clamped. | |
| Normalization | Normalization to apply to runtime image before preprocessing.<ud> <li>None<br>Normalization is not performed.</li>  <li>Mean & StDev<br>Normalization is applied by mean and standard deviation.</li>  <li>Mean<br>Normalization is applied by mean.</li> </ud> |
| Sobel image | Sobel Image used to highlight borders and edges of template image.   | None | Do not use | | --- | --- | | Add image to samples | Add this image to threhold image to make tools less sensitive in that regions (around borders or edges). |     | Magnitude scaling factor | Sobel parameter to magnify edges. | | --- | --- | | Magnitude threshold | Threshold for Sobel's edges. | |
| Blank scene | Enable or disable TInspect working mode. If enabled, no template model is required but a uniform image of blank scene gray value. (default = 25)<blockquote> **blank scene value**<br>Template image gray value. (default = 128)<br> </blockquote> |
| Erode difference image | Morfology to apply to difference image. (default = false)<blockquote> **Filter size**<br>Size of erosion operator. (default = 1)<br> </blockquote> |
| St.Dev threshold | Pixel in the intermediate threshold image with a gray value bigger than this threshold will be mapped to 255. (default = 180) |
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
| Inspected | Runtime image |
| Threshold image | Threshold Image result of statistical training. Every pixel value of the image is the threshold of the difference between run-time image and template image. Sensitivity modifies this threshold. |
| Difference | Difference image between runtime minus template and threshold image. |
| Model | Template image. |
| Sobel | Sobel image. |
| Mask | Mask image: care pixels are white; don't care pixels are black. |
| Threshold with extra mask | Threshold image with runtime movable masks |
| St.Dev threshold | Standard deviation Image |

Configuration
-------------

This tool is included into the library UvfCvl.
