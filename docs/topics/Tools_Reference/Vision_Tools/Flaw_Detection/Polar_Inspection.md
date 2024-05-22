Polar Inspection
================

![](../../../../img/x_Graphics/Tools/UvfCTStdUnwrapInspect-0.png)

Overview
--------

Polar inspection lets you inspect an annulus region. In Area mode non uniform areas (blobs) are extracted. In Edges mode edges that usually correspond to surface defects of a part are detected. Both modes can be selected separately. PolarInspection tools before performing blob analysis and/or edge checking unwraps the image region of the shape. 

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Geometry | Defines tool's region shape.<ud> <li>Annulus<br>Annulus shape.</li>  <li>Annulus section<br>Section of an annulus</li>  <li>General thick polygon<br>General polygon shape with significant thickness.</li> </ud> |

| Analysis | |
| --- | --- |
| Overlapping (deg) | Size (in degrees) of image. (default = 0) |
| Scale X | A scaling factor can be applied to the unwrapped region. X direction correspond to the radial direction. (default = 1.00) |
| Scale Y | A scaling factor can be applied to the unwrapped region. Y direction correspond to the radial direction. (default = 1.00) |
| Areas mode | Enables or disables error area detection. (default = Yes)<blockquote> **Adaptive sensitivity**<br>Threshold for segmentation is a value that follows the variation of histogram mean between training and inspected ROI image. Threshold is shifted according.(default = No)<br>  **Automatic**<br>Threshold is automatically calculated as the optimum value that divides the histogram in two groups such that each group has the minimum with-in group variance. For any given threshold, the within-group variance is defined by the weighted sum of the variances of the two groups.(default = no)<br>  **First threshold**<br>Mode standard:  If polarity is Dark objects, pixels with grey-scale value below the threshold are considered as foreground, while all pixels with value above the threshold are assigned as background pixels. The opposite for White objects. (default = 0 | min = 0 | max = 255)    Mode percentage:  Same, but with values are expressed as percentage. (default = 50 | min = 0 | max = 100)<br>  **Second threshold**<br>Mode standard:  If polarity is Dark objects, pixels with grey-scale value below the threshold are considered as foreground, while all pixels with value above the threshold are assigned as background pixels. The opposite for White objects. (default = 0 | min = 0 | max = 255)<br>  **Softness**<br>In case of large transitions with low slope between the levels of background and blobs the measured area becomes inaccurate. Therefore the width of the transition can be entered. Value are internally weighted and a linear slope is calculated for the transition.<br>  **Polarity**<br>Polarity of the object to consider as blob (defects).              White objects (default)      Finds objects that are brighter than the background.          Dark objects      Finds dark objects on a light background.          Dark and White objectsDisplayed only when threshold mode "Standard" is selected.      Uses the parameters First threshold and Second threshold.  Finds objects that are darker than the First threshold or brighter than the Second threshold.          Grey objectsDisplayed only when threshold mode "Standard" is selected.      Uses the parameters First threshold and Second threshold  Finds objects that are brighter than the First threshold and darker than the Second threshold.<br>  **Min. Area (pixel)**<br>Blobs with an area value smaller than this limit will be neglected in the evaluation.<br>  **Number of accepted defects**<br>The result will be good if the number of defect areas extracted is less than this value. (default = 0)<br> </blockquote> |
| Preprocessing | If necessary a preprocessing filter can be selected, operation or not, as default no filtering is done<ud> <li>None<br>No preprocessing needed. (default)</li>  <li>Median Difference<br>Median difference filtering preprocess.</li>  <li>XY Median Difference<br>Median difference filtering mainly in X and Y direction.</li>  <li>Sobel<br>Used to improve contrast changes</li>  <li>Average Difference<br>Average difference filtering preprocess.</li> </ud> |
| Edges mode | Enables or disables edge detection. (default = Enable)<blockquote> **Contrast threshold**<br>The contrast, in gray levels, above which a transition is considered an edge. (default = 5.00)<br>  **First edge polarity**<br>The expected polarity of the first edge.             Dark to light      Transition from darker region to lighter one.          Light to dark      Transition from lighter region to darker one.          Don't care (default)      Any polarity.<br>  **Filter size**<br>The filter width for edge extraction. (default = 2)<br>  **Max number of results**<br>Maximum number of edges to be found.<br>  **Number of accepted defects**<br>The result will be good if the detected defects count are less than this value. (default = 0)<br> </blockquote> |

### More

Click More... to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| Processing time | Tool processing time in msec. |
| Blobs number | Found blobs' count. |
| Total area (pixel) | Sum of the areas of all found blobs, in pixel. |
| Sum of all Blobs area (%) | Sum of the areas of all found blobs, in %. |
| Max. area (pixel) | Greatest area of all found blobs, in pixel. |
| Min. area (pixel) | Smallest area of all found blobs, in pixel. |
| Result | Select the index of the blob to show information about.<blockquote> **Area**<br>Area of the selected blob, in pixel.<br>  **Center X**<br>Position X of the center of mass of the selected blob.<br>  **Center Y**<br>Position Y of the center of mass of the selected blob.<br> </blockquote> |
| Edges number | Found edges count. |
| Edge | Select the index of the edge to show information about.<blockquote> **Position X**<br>X coordinate of the edge central point.<br>  **Position Y**<br>X coordinate of the edge central point.<br>  **Edge contrast**<br>Contrast measured for the founded edge transition's value.<br> </blockquote> |

Images
------

| Images | |
| --- | --- |
| Model | Unwrapped image of reference image used to train the tool. |
| Last | Run time unwrapped image. |

Configuration
-------------

This tool is included into the library UvfCTStd and UvfCTCvl.
