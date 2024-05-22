RSI Search
==========

![](../../../../img/x_Graphics/Tools/UvfUIRsi-0.png)

Overview
--------

The RSI Search tool is a specialized search tool that combines features of both PatMax and Search. Like those tools, RSI Search lets you train a model of the image features that you are looking for, then find instances of the trained features in a run-time image.

For most applications that require the ability to find scaled and rotated feature instances, PatMax will be faster and more accurate than RSI Search. But in a number of cases, RSI Search can solve applications that PatMax cannot:

- When using color images
- When the run-time images exhibit shear with respect to the trained model
- When using small models or model images (PatMax may be unable to train patterns from small images because they don’t contain enough features)
- When run-time images contain significant texture (PatMax may run slowly if images have too many features)

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Search area | Select the area where search for a model.<ud> <li>All Image (default)<br>Search area agrees with overall image area.</li>  <li>Centered<br>Search area is the model area enlarged by a symmetrical frame.</li>  <li>Free<br>Search area is defined by the user.</li> </ud><blockquote> **Frame X**<br>Frame width. (default = 20)<br>  **Frame Y**<br>Frame height. (default = 20)<br> </blockquote> |
| Model | Defines tool's model shape.<ud> <li>Circle<br>Circular shape.</li>  <li>General rectangle (default)<br>Rectangular shape.</li>  <li>Annulus<br>Annulus shape.</li>  <li>General polygon<br>General polygon shape.</li> </ud> |
| User origin | Allows to set the model origin in an arbitrary position, instead of the center of the model area. |
| Synthetic model | Model is created using a synthetic image shapes instead of using the reference image.<blockquote> **Model polarity**<br>Polarity of the shapes represented in the synthetic model            White on black background (default)      White foreground (pixels within the shape) on black background.          Black on white background      Black foreground (pixels within the shape) on white background.<br>  **Model frame X (pixel)**<br>symmetrical X frame to add to the width of the model shape.<br>  **Model frame Y (pixel)**<br>symmetrical Y frame to add to the height of the model shape.<br> </blockquote> |

| Tolerances and limits | |
| --- | --- |
| Check results count | The expected number of results<ud> <li>None<br>No check.</li>  <li>Expected number<br>Number of results must be equal to Num. of results to find.</li>  <li>Less than<br>Number of results must be less then Num. of results to find.</li>  <li>Greater than<br>Number of results must be greater then Num. of results to find.</li> </ud>    | Num. of results to find | Number of results to be found. | | --- | --- | |
| Shape index | Enables or disables conformity limit condition.<blockquote> **Shape index limit**<br>Minimum acceptable shape index. (default = 1.0)<br> </blockquote> |
| Position offset | Enables or disables position tolerance.<blockquote> **Elliptical Region**<br>Use an elliptical region area instead of a rectangular one. Position XY tolerances are the semi-axes the ellipse or the semi-size of rectangle.<br>  **Position X tolerance**<br>Position tolerance in the X axes.(default = 10)<br>  **Position Y tolerance**<br>Position tolerance in the Y axes. (default = 10)<br> </blockquote> |
|
| Angle offset | Enables or disables orientation tolerance.<blockquote> **Angle+**<br>Tolerance for positive angles. (default = 360; min = 0; max = 360)<br>  **Angle-**<br>Tolerance for negative angles. (default = 360; min = 0; max = 360)<br> </blockquote> |
|
| Relative Contrast | Relative contrast is defined as the scale factor of the standard deviation of the runtime grey levels as compared to the standard deviation of the training time grey levels.<blockquote> **Tolerance-**<br>Lower limit for relative contrast.. (default = 0.00; min = 0.00; max = 1.00)<br>  **Tolerance+**<br>Upper limit for relative contrast. (default = 0.00; min = 0.00; max = FLT\_MAX)<br> </blockquote> |
|
| Relative Brightness | Relative brightness is defined as the scale factor of the mean of the runtime grey levels as compared to the mean of the training time grey levels.<blockquote> **Tolerance-**<br>Lower limit for relative brightness.. (default = 0.00; min = 0.00; max = 1.00)<br>  **Tolerance+**<br>Upper limit for relative brightness. (default = 0.00; min = 0.00; max = FLT\_MAX)<br> </blockquote> |
|
| Shear | Shear angle of the located model in the client coordinate system of the runtime image.<blockquote> **Tolerance-**<br>Lower limit for shear angle. (default = 0; min = -180; max = 180<br>  **Tolerance+**<br>Upper limit for shear angle. (default = 0; min = -180; max = 180)<br> </blockquote> |

| Analysis | |
| --- | --- |
| Max. number of results | Number of model instances to find. (default = 1) |
| Acceptance threshold | The acceptance level for the global searching score. Results with scores below this limit are not accepted. (default = 0.30) |
| Confusion | The confusion threshold is the score above which any match is guaranteed to be an instance of the model; all matches with scores greater than or equal to the confusion threshold are considered to be valid. The Search tool uses the confusion threshold to speed the search process. If you are searching for a single instance of the model in an image, as soon as Search tool finds an instance with a score above the confusion threshold, it stops searching and returns the location of the match. If CNLSearch does not find a match with a score above the confusion threshold, it locates all the matches with scores above the acceptance threshold and returns the location of the match with the highest score. (default = 1.0) |
| Angle | Enables or disables angle search range. (default = No)<blockquote> **Angle min**<br>Lower limit. (default = -180)<br>  **Angle max**<br>Upper limit. (default = 180)<br> </blockquote> |
| Scale | Enables or disables scale range. (default = No)<ud> <li>None</li> <li>Simmetric</li>  <li>Only X</li>  <li>Only Y</li><li>Shear</li> </ud>  <blockquote> **Min**<br>Lower limit in %. (default = 50)<br>  **Max**<br>Upper limit in %. (default = 200)<br> </blockquote> |
| Ignore polarity | You can specify whether to ignore the polarity of contours. A white square on black background will be found also if it becomes a black one on white background. |
| Pattern granularity | RSI Search uses large features first to do a pre-localization of the object and then refines the search using fine features. Granularity is expressed as the radius of interest, in pixels, within which features are detected.<ud> <li>Automatic (default)<br>The system perform, at train time, an estimate of the optimal settings for Fine and Coarse granularity.</li>  <li>Manual<br>You define fine and coarse granularity to use to train the pattern and to run.</li> </ud>  <blockquote> **Fine**<br>The smallest granularity used to detect features in the training image or shape description. (default = 1)<br>  **Coarse**<br>The largest granularity used to detect features. (default = 4)<br> </blockquote> |
| Operation Mode | This enumeration defines constants that specify when the template images are generated.<ud> <li>Generate templates<br>Templates are generated at training time,</li>  <li>Run-time models<br>Templates are generated at run time.</li> </ud> |
| Model compression | This enumeration defines constants that specify what type of compression to apply to the trained model. (default = None)<ud> <li>None<br>Do not compress the trained model.</li>  <li>Lossy<br>Compress the trained model using a lossy compression method. This method produces the fastest search, but may miss some model instances.</li>  <li>Lossyless<br>Compress the trained model using a lossless compression method. This method may result in a faster search than using eCompressionNone, but without the risk of failing to find some instances.</li> </ud> |
| Accepted overlap (%) | Percentage overlapping area needed to PatMax before it considers multiple overlapping instances as a single instance. (default = 0.00) |
| Angle overlap | Angle within which PatMax treats multiple overlapping instances as a single instance. (default = 360) |

### More

Click [here](../../../Windows/dialog_settings.md) to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| Processing time | Tool processing time in msec. |
| Position X | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset between the tool's specification X position and tool's result X position (specification reference system).<br> </blockquote> |
| Position Y | Y position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset Y**<br>Offset between the tool's specification Y position and tool's result Y position (specification reference system).<br> </blockquote> |
| Offset length | Distance between specification and result points. |
| Angle | Angle of the tool.<blockquote> **Angle offset**<br>Offset between the tool's specification orientation angle and tool's result orientation angle.<br> </blockquote> |
| Scale X | Scale value in the X axes. |
| Scale Y | Scale value in the Y axes. |
| Score | Match quality index. A value from 0 to 1 indicating the global level of conformity between the model and the pattern found. |
| Relative Contrast | Scale factor of the standard deviation of the runtime grey levels as compared to the standard deviation of the training time grey levels. |
| Relative Brightess | Scale factor of the mean of the runtime grey levels as compared to the mean of the training time grey levels. |
| Shear | Shear angle of the located model in the client coordinate system of the runtime image. |

Images
------

| Images | |
| --- | --- |
| Model | Image of the trained model . |
| Mask | Mask image to apply. White pixels are care pixels. Black pixels are don't care. |

Configuration
-------------

This tool is included into the library UvfCvl.
