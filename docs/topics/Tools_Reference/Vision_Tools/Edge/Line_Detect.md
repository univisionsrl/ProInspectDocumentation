
Line Detect
===========


![](../../../../img/x_Graphics/Tools/UvfCvlHoughLine-0.png)


Overview
--------


Line Detect lets you find linear scratches in the selected search area. It uses basically the Hough algorithm to extract desired linear features.


Settings
--------





| Options | |
| --- | --- |
| Enable | Enable or disable the tool. (default = Yes) |
| Geometry | Defines tool's region shape.<ud> <li>Circle<br>Circular shape.</li>  <li>General rectangle (default)<br>Rectangular shape.</li>  <li>Annulus<br>Annulus shape.</li>  <li>General polygon<br>General polygon shape.</li>  <li>CAD (Closed ROI)<br>Closed shape imported from a CAD file.</li> </ud> |
| CAD file | CAD file name. |
| Layer name | Lists the layer names defined in the selected CAD file.<blockquote> **Connection tolerance**<br>Distance between close segment points to be considered as connected.. (default = 0)<br>  **Normalize XY weight**<br>If checked weight is distributed for 50% to X features and for 50% to Y features. If unchecked all features have the same weight. (default = No)<br> </blockquote> |
| User calibration | If checked user defines parameters for CAD shapes calibration. Otherwise tool calibration is used.<blockquote> **Axes X rotation**<br>Rotation in the X axes to be applied to the CAD shape. (default = 0; min = -360; max = 360)<br>  **Axes Y rotation**<br>Rotation in the Y axes to be applied to the CAD shape. (default = 0; min = -360; max = 360)<br>  **Scale X**<br>Scale variation in the X axes to be applied to the CAD shape. You express scale value as a multiplier value. (default = 1)<br>  **Scale Y**<br>Scale variation in the Y axes to be applied to the CAD shape. You express scale value as a multiplier value. (default = 1)<br> </blockquote> |





| Tolerances and limits | |
| --- | --- |
| Number of shapes not matched | Enables or disables check on the number of linear scratches found. (default = Yes)<blockquote> **Max number of shapes**<br>Maximum allowed number.  (default = 0)<br> </blockquote> |
| Length of each shape | Enables or disables check on scratch's length limit. (default = No)<blockquote> **Single shape length limit**<br>Maximum value of shapes' length. (default = 10.00)<br> </blockquote> |
| Sum of all shapes length | Enables or disables check on the sum of all scratches' length limit. (default = No)<blockquote> **Sum of all shapes length limit**<br>Maximum value of shapes' length sum. (default = 50.00)<br> </blockquote> |





| Analysis | |
| --- | --- |
| Magnitude threshold | Magnitude threshold above which a feature is considered in the Hough space. (default = 20) |
| Max. num. of lines | Maximum number of scratches to find. (default = 10000) |
| Minimum length (pixel) | Minimum length (pixels) of valid scratches. (default = 10) |
| Minimum density | The density is computed as the ratio of the number of contributing featurelets divided by the length. A low density threshold may cause colinear line segments to merge into one longer segment. A high density threshold may break up an otherwise longer line segment into multiple shorter colinear pieces. Very high density threshold may exceed the density of all line segments in the image data, and cause the tool to report no line segment. (default = 0.8) |
| Diagnostic | Enable extended diagnostic. (default = No) |


### More


Click [here](../../../Windows/dialog_settings.md) to access the More section description.


Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool. |
| Processing time | Tool processing time in msec. |
| Num of shapes not matched | Found shapes count. |
| Sum of shapes length | Sum of shapes length. |
| Max length | Maximum length of all founded shapes. |
| Min length | Minimum length of all founded shapes. |
| Result | Select the index of the line to show information about.<blockquote> **Length**<br>Measured length of the selected shape.<br>  **Start point X**<br>X coordinate of the starting point.<br>  **Start point Y**<br>Y coordinate of the starting point.<br> </blockquote> |


Configuration
-------------


This tool is included into the library UvfCvl.



