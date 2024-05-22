
Blob Measure
============


![](../../../../img/x_Graphics/Tools/UvfUIBlobMeasure-0.png)


Overview
--------


Blob measure works like the Blob inspect tool but returns several details about each blob found. These details give features of the blob that can be controlled.


Settings
--------





| Options | |
| --- | --- |
| Enable | Enable or disable the tool. (default = Yes) |
| User origin | Enable or disable the user defined origin. (default = No) |
| Geometry | Defines tool's region shape.<ud> <li>Circle<br>Circular shape.</li>  <li>General rectangle (default)<br>Rectangular shape.</li>  <li>Annulus<br>Annulus shape.</li>  <li>General polygon<br>General polygon shape.</li>  <li>CAD (Closed ROI)<br>Closed shape imported from a CAD file.</li> </ud> |
| CAD file | CAD file name. |
| Layer name | Lists the layer names defined in the selected CAD file.<blockquote> **Connection tolerance**<br>Distance between close segment points to be considered as connected.. (default = 0)<br> </blockquote> |
| User calibration | If checked user defines parameters for CAD shapes calibration. Otherwise tool calibration is used.<blockquote> **Axes X rotation**<br>Rotation in the X axes to be applied to the CAD shape. (default = 0; min = -360; max = 360)<br>  **Axes Y rotation**<br>Rotation in the Y axes to be applied to the CAD shape. (default = 0; min = -360; max = 360)<br>  **Scale X**<br>Scale variation in the X axes to be applied to the CAD shape. You express scale value as a multiplier value. (default = 1)<br>  **Scale Y**<br>Scale variation in the Y axes to be applied to the CAD shape. You express scale value as a multiplier value. (default = 1)<br> </blockquote> |





| Tolerances and limits | |
| --- | --- |
| Check results count | Enables or disables blobs count condition. Condition fails if number of number of blobs in tolerance found don't agree with settings.   | None | Disabled | | --- | --- | | Expected number | The expected number of blobs found. | | Less than | Less than number of blobs found | | Greater than | More than number of blobs found | | Number of results to find | Enter number of expected blobs. (default = 1) | |
| Position offset | Enables or disables position tolerance limits. Specification position is the center of mass of the greatest blob found in the reference image .<blockquote> **Elliptical Region**<br>Use an elliptical region area instead of a rectangular one. Position XY tolerances are the semi-axes the ellipse or the semi-size of rectangle.<br>  **Position X tolerance**<br>Position tolerance in the X axes. (default = 10)<br>  **Position Y tolerance**<br>Position tolerance in the Y axes. (default = 10)<br> </blockquote> |
| Angle offset | Enables or disables orientation tolerance limits. Specification orientation is the angle of the primary inertia axes of the greatest blob found in the reference image. <blockquote> **Angle+**<br>Tolerance for positive angles. (default = 360; min = 0; max = 360)<br>  **Angle-**<br>Tolerance for negative angles. (default = 360; min = 0; max = 360)<br> </blockquote> |
| Specification mode | In the automatic mode, specification values are automatically set. Otherwise specification values need to bi set. |
| Area | Enables or disables Blob area limit.<blockquote> **Specification**<br>Expected blob area. (default = 0)<br>  **Tolerance+**<br>Positive tolerance. (default = 0)<br>  **Tolerance-**<br>Negative tolerance. (default = 0)<br> </blockquote> |
| Perimeter | Enables or disables Blob perimeter limit.<blockquote> **Specification**<br>Expected blob perimeter. (default = 0)<br>  **Tolerance+**<br>Positive tolerance. (default = 0)<br>  **Tolerance-**<br>Negative tolerance of the measured perimeter. (default = 0)<br> </blockquote> |
| Width | Enables or disables Blob width limit. Blob width is the width of bounding box around the principal axes.<blockquote> **Specification**<br>Expected width value. (default = 0)<br>  **Tolerance+**<br>Positive tolerance. (default = 0)<br>  **Tolerance-**<br>Negative tolerance. (default = 0)<br> </blockquote> |
| Height | Enables or disables Blob height limit. Blob width is the height of bounding box around the principal axes.<blockquote> **Specification**<br>Expected height value. (default = 0)<br>  **Tolerance+**<br>Positive tolerance. (default = 0)<br>  **Tolerance-**<br>Negative tolerance. (default = 0)<br> </blockquote> |
| Holes count | Enables or disables Blob holes count limit.<blockquote> **Specification**<br>Expected height value. (default = 0)<br>  **Tolerance+**<br>Positive tolerance. (default = 0)<br>  **Tolerance-**<br>Negative tolerance. (default = 0)<br> </blockquote> |
| Holes max area | Enables or disables Blob holes maximum area limit.<blockquote> **Specification**<br>Expected hole area. (default = 0)<br>  **Tolerance+**<br>Positive tolerance. (default = 0)<br>  **Tolerance-**<br>Negative tolerance. (default = 0)<br> </blockquote> |
| Elongation | Enables or disables Blob elongation limit. Elongation is the ratio between inertia principal axes.<blockquote> **Specification**<br>Expected elongation. (default = 0)<br>  **Tolerance+**<br>Positive tolerance. (default = 0)<br>  **Tolerance-**<br>Negative tolerance. (default = 0)<br> </blockquote> |





| Analysis | |
| --- | --- |
| Max number of results | Number of blob to find. |
| Adaptive sensitivity | Threshold is a value that follows the variation of histogram mean between training and inspected ROI image. Threshold is shifted according. |
| Automatic | Threshold is automatically calculated as the optimum value that divides the histogram in two groups such that each group has the minimum with-in group variance. For any given threshold, the within-group variance is defined by the weighted sum of the variances of the two groups |
| First threshold | Mode standard: If polarity is Dark objects, pixels with grey-scale value below the threshold are considered as foreground, while all pixels with value above the threshold are assigned as background pixels. The opposite for White objects. (default = 0 | min = 0 | max = 255)   Mode percentage: Same, but with values are expressed as percentage. (default = 50 | min = 0 | max = 100) |
| Second threshold | Mode standard: If polarity is Dark objects, pixels with grey-scale value below the threshold are considered as foreground, while all pixels with value above the threshold are assigned as background pixels. The opposite for White objects. (default = 0 | min = 0 | max = 255) |
| Softness | In case of large transitions with low slope between the levels of background and blobs the measured area becomes inaccurate. Therefore the width of the transition can be entered. Value are internally weighted and a linear slope is calculated for the transition. |
| Polarity | Polarity of the object to consider as blob (defects).   | White objects (default) | Finds objects that are brighter than the background. | | --- | --- | | Dark objects | Finds dark objects on a light background. | | Dark and White objectsDisplayed only when threshold mode "Standard" is selected. | Uses the parameters First threshold and Second threshold. Finds objects that are darker than the First threshold or brighter than the Second threshold. | | Grey objectsDisplayed only when threshold mode "Standard" is selected. | Uses the parameters First threshold and Second threshold Finds objects that are brighter than the First threshold and darker than the Second threshold. | |
| Min. Area (pixel) | Area must be greater than this limit to be labeled as blob. |
| Calibrated results | Show results in calibrated units, e.g. mm. (default = no) |
| Preprocessing | If necessary a # Pre-processing filter can be applied before blob analysis.   | None (default) | No preprocessing. | | --- | --- | | Median difference | Median difference filter. | | XY median difference | Median difference filter only in X and Y direction. | | Sobel | Sobel filter. | | Average difference | Average difference filter. |  <blockquote> **X (pixel)**<br>Filter width.<br>  **Y (pixel)**<br>Filter height.<br>  **Magnitude scaling factor**<br>Sobel filter parameter.<br>  **Magnitude threshold**<br>Sobel filter parameter.<br> </blockquote> |


### More


Click [here](../../../Windows/dialog_settings.md) to access the More section description.


Results
-------







| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| --- | --- |
| Processing time | Tool processing time in msec. |
| Results count | Number of found blobs. |
| Position X | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset between the tool's specification X position and tool's result X position (specification reference system).<br> </blockquote> |
| Position Y | Y position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset Y**<br>Offset between the tool's specification Y position and tool's result Y position (specification reference system).<br> </blockquote> |
| Offset length | Distance between specification and result points. |
| Angle | Angle of the tool.<blockquote> **Angle offset**<br>Offset between the tool's specification orientation angle and tool's result orientation angle.<br> </blockquote> |
| Area | Area of the selected blob, in pixel.<blockquote> **Difference with specification**<br>Difference between result and specified value.<br> </blockquote> |
| Perimeter | Perimeter of the selected blob, in pixel.<blockquote> **Difference with specification**<br>Difference between result and specified value.<br> </blockquote> |
| Width | Width of the selected blob, in pixel.<blockquote> **Difference with specification**<br>Difference between result and specified value.<br> </blockquote> |
| Height | Height of the selected blob, in pixel.<blockquote> **Difference with specification**<br>Difference between result and specified value.<br> </blockquote> |
| Hole count | Holes count of the selected blob. |
| Hole max area | Hole maximum area of the selected blob, in pixel.<blockquote> **Difference with specification**<br>Difference between result and specified value.<br> </blockquote> |
| Elongation | Elongation of the selected blob.<blockquote> **Difference with specification**<br>Difference between result and specified value.<br> </blockquote> |


Images
------







| Mask | Mask image to apply. White pixels are care pixels. Black pixels are don't care. |
| --- | --- |
| Preprocessing | Image processed through filter (if any) before blob analysis. |


Configuration
-------------


This tool is included into the library UvfCvl.



