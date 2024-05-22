Thin Finger Inspect
===================

![](../../../../img/x_Graphics/Tools/UvfCTStdThinLineInspect-0.png)

Overview
--------

Finger Inspect tool measures along lines the width of continuous objects (like fingers). The tool measures the width with a defined density, up to the pixel size, creating a profile of the width of the inspected object. The tool measures the line width and detects cuts, fat and thin sections.

The with of the line is measured using the gray level intensity of the line. This allows to measure sub-pixel width. The tool must calibrate the line width during training with a reference image.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enable or disable the tool. (default = Yes) |
| Geometry | Defines tool's model shape.<ud> <li>LineSeg (default)<br>Line segment.</li>  <li>CAD<br>Shape imported from a CAD file.</li> </ud> |
| CAD file | Defines CAD file name.<blockquote> **Layer name**<br>Lists the layer names defined in the selected CAD file.<br>  **Scale X**<br>Scale variation in the X axes to be applied to the CAD shape. You express scale value as a multiplier value.<br>  **Scale Y**<br>Scale variation in the Y axes to be applied to the CAD shape. You express scale value as a multiplier value.<br>  **Axes X rotation**<br>Rotation in the X axes to be applied to the CAD shape. (default = 0; min = -360; max = 360)<br>  **Axes Y rotation**<br>Rotation in the Y axes to be applied to the CAD shape. (default = 0; min = -360; max = 360)<br>  **Connection tolerance**<br>Distance between close segment points to be considered as connected.<br> </blockquote> |

| Tolerances and Limits | |
| --- | --- |
| Finger mean width | Enables or disables width mean measurement check. (default = No)<blockquote> **Specification**<br>Width mean specification for a single finger. (default = 0.0)<br>  **Tolerance-**<br>Positive tolerance of the measured width. (default = 0.0)<br>  **Tolerance+**<br>Negative tolerance of the measured width. (default = 0.0)<br> </blockquote> |
| Finger Std. Dev. width | Enables or disables width standard deviation measurement check. (default = No)<blockquote> **Single finger limit**<br>Tolerance of the standard deviation width for a single finger. (default = 0.0)<br>  **Global limit**<br>Tolerance of the standard deviation width for all fingers. (default = 0.0)<br> </blockquote> |
| Short interruptions | Enables or disables the defect check. (default = No)<blockquote> **max. number**<br>Maximum number of defects accepted. (default = 0.0)<br> </blockquote> |
| Medium interruptions | Enables or disables the defect check. (default = No)<blockquote> **max. number**<br>Maximum number of defects accepted. (default = 0.0)<br> </blockquote> |
| Long interruptions | Enables or disables the defect check. (default = No)<blockquote> **max. number**<br>Maximum number of defects accepted. (default = 0.0)<br> </blockquote> |
| Thin finger length | Enables or disables the thin finger measurement check (single defect). (default = No)<blockquote> **Single finger limit**<br>Maximum thin finger length for a single measure. (default = 0.0); if a finger is thin more than the limit, then is a defect<br> </blockquote> |
| Short fat sections | Enables or disables the defect check. (default = No)<blockquote> **max. number**<br>Maximum number of defects accepted. (default = 0.0)<br> </blockquote> |
| Medium fat sections | Enables or disables the defect check. (default = No)<blockquote> **max. number**<br>Maximum number of defects accepted. (default = 0.0)<br> </blockquote> |
| Long fat sections | Enables or disables the defect check. (default = No)<blockquote> **max. number**<br>Maximum number of defects accepted. (default = 0.0)<br> </blockquote> |
| Blurred finger length | Enables or disables the blurred finger measurement check (single defect). (default = No)<blockquote> **Single finger limit**<br>Maximum thin burred length for a single measure. (default = 0.0); if a finger is blurred more than the limit, then is a defect<br> </blockquote> |
| Sum of lengths of interruptions | Enables or disables broken finger measurement check. (default = No)<blockquote> **Single finger limit**<br>Maximum broken finger length for a single finger. (default = 0.0)<br>  **Global limit**<br>Maximum broken finger length for all fingers. (default = 0.0)<br> </blockquote> |
| Sum of lengths of thins | Enables or disables thin finger measurement check. (default = No)<blockquote> **Single finger limit**<br>Maximum thin finger length for a single finger. (default = 0.0)<br>  **Global limit**<br>Maximum thin finger length for all fingers. (default = 0.0)<br> </blockquote> |
| Sum of lengths of fats | Enables or disables fat  finger measurement check. (default = No)<blockquote> **Single finger limit**<br>Maximum fat finger length for a single finger. (default = 0.0)<br>  **Global limit**<br>Maximum fat finger length for all fingers. (default = 0.0)<br> </blockquote> |
| Sum of lengths of blurreds | Enables or disables blurred finger measurement check. (default = No)<blockquote> **Single finger limit**<br>Maximum blurred finger length for a single finger. (default = 0.0)<br>  **Global limit**<br>Maximum blurred finger length for all fingers. (default = 0.0)<br> </blockquote> |
| Number of missing points | Enables or disables missing points (failed measurements) check. (default = No)<blockquote> **Single finger limit**<br>Maximum number of missing point for a single finger. (default = 0.0)<br>  **Global limit**<br>Maximum number of missing point for all fingers. (default = 0.0)<br> </blockquote> |

When a single finger point is measured, the measure can be classified as an interruption, thin or fat. Then the tool starts to measure the length of the interruption or the thin or fat section, until the point measurement has the same classification.

A point measurement is considered an interruption if there is no finger to measure.  
A point measurement is considered thin, if the finger width is less than Thin finger width limit.  
A point measurement is considered fat, if the finger width is greater than Fat finger width limit.

Multiple measurements of the same class make a section; a section can be considered:  
- short, if the section is long less than the short limit  
- medium, if the section is longer than the short limit but less than the medium limit  
- long, if the section is longer than the medium limit

| Measurement classification | |
| --- | --- |
| Short interruption limit | Limit to classify an interruption as short. (default = 0) |
| Medium interruption limit | Limit to classify an interruption as medium. (default = 0) |
| Thin finger width limit | Limit to classify a finger as thin, if less than. (default = 3) |
| Fat finger width limit | Limit to classify a finger as fat, if more than. (default = 7) |
| Short fat section limit | Limit to classify an fat section as short. (default = 0) |
| Medium fat section limit | Limit to classify a fat as medium. (default = 0) |

| Analysis | |
| --- | --- |
| Density | Density of the measurement. (default = 1.00) |
| Number of measurement points | Number of points to average to get a single point measurement. (default = 1) |
| Finger search width (pixels) | Width of the caliper used to align the inspected line. (default = 50) |
| Finger search height (pixel) | Height of the caliper used to align the inspected line. (default = 5) |
| Finger search gap right (pixel) | Right don't care area for line search. (default = 0) |
| Finger search gap left (pixel) | Left don't care area for line search. (default = 0) |
| Dark back gound | Defines is the background is darker then the measured object. (default = Yes) |
| Background color limit | Defines the background gray level. (default = 128) when there is an interruption, if the gray level is less than this value, then is considered as background. |
| Mouse bites | Enables small breakage detection (advanced). (default = No) |
| Local inspection | Enable local inspection (default = Yes)<blockquote> **number of point to average**<br>Number of points used to get the local measurement. (default = 5)<br>  **only center value**<br>Enables using only the center as measurement . (default = No)<br>  **filter gray value on average**<br>Enable using the number of point to average to get the local gray value for the local inspection (default = Yes)<br>  **contrast threshold**<br>minimum contrast threshold to detect a breakage<br>  **filter size**<br>The filter width for edge extraction. (default = 2)<br>  **second edge threshold (%)**<br>Percentage change from the first breakage edge gray value to define end of the breakage<br>  **Measure don't care left**<br>Left don't care area for measurement. (default = 0)<br>  **Measure don't care right**<br>Right don't care area for measurement. (default = 0)<br> </blockquote> |

You need to provide a reference image with the finger size you want to measure and calibrate providing the right value in units. The tool calculate a linear map (slope and intercept) between the gray level and the size:

~~~
size = m \ gray\_level + q
~~~

The calibration can be:

- with absolute values (Slope an Constant)  
- local, one value per line or with a global average calibrated value, if there is more than one line

You can adjust the image with a look-up table image before calibrating.

| Finger measurement calibration | |
| --- | --- |
| Slope (m) | Slope of the line . (default = 1) |
| Constant (q) | Intercept of the line . (default = 0) |
| Use local calibration | Enable local calibration (default = No)<blockquote> **update on train**<br>Update the calibration every train operation (default = Yes)<br>  **value**<br>The reference value in units (default = 40)<br>  **finger average**<br>Use an average for all fingers, when more than one (default = No)<br>  **contrast threshold**<br>Minimum contrast threshold to detect a breakage<br>  **slope (m)**<br>Calibrated slope<br>  **constant (q)**<br>Calibrated intercept<br> </blockquote> |
| Manual map | Enable manual mapping image grey levels before calibration (default = Yes)<blockquote> **first threshold**<br>Threshold for black levels(default = 10)<br>  **second threshold**<br>Threshold for white levels(default = 220)<br> </blockquote> |

### More

Click More... to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| Processing time | Tool processing time in msec. |
| Finger(s) selection | Select the finger number (id) to see results. Result below are referred to the selected finger<ud> <li>Tools name(default)<br>Results are referred to the all fingers</li>  <li>Single finger - id<br>Results are referred to the finger id            finger id      Number of the finger</li> </ud> |
| Finger result | Pass/Fail decision of the finger. |
| Number of points | Number of measurements. |
| Number of missing points | Number of failed measurements. |
| Min contrast | Minimum contrast measured for the found transitions value edges. |
| Local inspection min contrast | Minimum contrast measured for the found transitions value edges when using local inspection |
| Finger mean width | Finger width mean measurement. |
| Finger Std. Dev. width | Finger width standard deviation measurement. |
| Finger min. width | Finger minimum width measurement. |
| Finger max. width | Finger maximum width measurement. |
| Num. of interruptions | Number of broken sections found.<blockquote> **short interruptions**<br>Number of short interruptions<br>  **medium interruptions**<br>Number of medium interruptions<br>  **long interruptions**<br>Number of long interruptions<br>  **min. length**<br>Size of the smaller interruption<br>  **max. length**<br>Size of the larger interruption<br>  **sum of lengths**<br>Total interruptions length<br> </blockquote> |
| Num. of thin sections | Number of thin sections found.<blockquote> **Min length**<br>Minimum length.<br>  **Max length**<br>Maximum length.<br>  **Sum of lengths**<br>Sum of all thin sections length.<br> </blockquote> |
| Num. of fat sections | Number of fat sections found.<blockquote> **short fat sections**<br>Number of short fat sections<br>  **medium fat sections**<br>Number of medium fat sections<br>  **long fat sections**<br>Number of long fat sections<br>  **Min length**<br>Minimum length.<br>  **Max length**<br>Maximum length.<br>  **Sum of lengths**<br>Sum of all fat sections length.<br> </blockquote> |
| Num. of blurred sections | Number of blurred sections found.<blockquote> **Min length**<br>Minimum length.<br>  **Max length**<br>Maximum length.<br>  **Sum of lengths**<br>Sum of all blurred sections length.<br> </blockquote> |
