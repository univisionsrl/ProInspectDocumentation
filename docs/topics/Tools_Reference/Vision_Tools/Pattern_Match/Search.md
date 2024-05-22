Search
======

![](../../../../img/x_Graphics/Tools/UvfUISearch-0.png)

Overview
--------

The purpose of Search is to locate and measure the quality of one (or more) previously trained model.

The search operation measures how a part in an image matches a previously trained model of that part. The pattern to be searched is the distribution of its grey levels. Search locates the part finding the area of the image most similar to the trained model.

The score indicates how close a match exists between the trained image and the image whose location was returned. Scores ranges from 0.0, indicating no similarity between the model and the feature, to 1.0, indicating a perfect match. Trained image and inspected one should not be rotated to each other and of same scale.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Search area | Select the area where search for a model.<ud> <li>All Image (default)<br>Search area agrees with overall image area.</li>  <li>Centered<br>Search area is the model area enlarged by a symmetrical frame.</li>  <li>Free<br>Search area is defined by the user.</li> </ud><blockquote> **Frame X**<br>Frame width. (default = 20)<br>  **Frame Y**<br>Frame height. (default = 20)<br> </blockquote> |
| Model | Defines tool's model shape.<ud> <li>Circle<br>Circular shape.</li>  <li>General rectangle (default)<br>Rectangular shape.</li>  <li>Annulus<br>Annulus shape.</li>  <li>General polygon<br>General polygon shape.</li>  <li>CAD (Closed ROI)<br>Closed shape imported from a CAD file.</li> </ud> |
| CAD file | CAD file name. |
| Layer name | Lists the layer names defined in the selected CAD file.<blockquote> **Connection tolerance**<br>Distance between close segment points to be considered as connected.. (default = 0)<br>  **Normalize XY weight**<br>If checked weight is distributed for 50% to X features and for 50% to Y features. If unchecked all features have the same weight. (default = No)<br> </blockquote> |
| User calibration | If checked user defines parameters for CAD shapes calibration. Otherwise tool calibration is used.<blockquote> **Axes X rotation**<br>Rotation in the X axes to be applied to the CAD shape. (default = 0; min = -360; max = 360)<br>  **Axes Y rotation**<br>Rotation in the Y axes to be applied to the CAD shape. (default = 0; min = -360; max = 360)<br>  **Scale X**<br>Scale variation in the X axes to be applied to the CAD shape. You express scale value as a multiplier value. (default = 1)<br>  **Scale Y**<br>Scale variation in the Y axes to be applied to the CAD shape. You express scale value as a multiplier value. (default = 1)<br> </blockquote> |
| User origin | Allows to set the model origin in an arbitrary position, instead of the center of the model area. |
| Synthetic model | Model is created using a synthetic image shapes instead of using the reference image.<blockquote> **Model polarity**<br>Polarity of the shapes represented in the synthetic model<br> </blockquote><ud> <li>White on black background (default)<br>White foreground (pixels within the shape) on black background.</li>  <li>Black on white background<br>Black foreground (pixels within the shape) on white background.</li> </ud>  <blockquote> **Model frame X (pixel)**<br>symmetrical X frame to add to the width of the model shape.<br>  **Model frame Y (pixel)**<br>symmetrical Y frame to add to the height of the model shape.<br> </blockquote> |

| Tolerances and limits | |
| --- | --- |
| Check results count | The expected number of results<ud> <li>None<br>No check.</li>  <li>Expected number<br>Number of results must be equal to Num. of results to find.</li>  <li>Less than<br>Number of results must be less then Num. of results to find.</li>  <li>Greater than<br>Number of results must be greater then Num. of results to find.</li> </ud>    | Num. of results to find | Number of results to be found. | | --- | --- | |
| Shape index | Conformity limit for acceptable result.<blockquote> **Shape index limit**<br>Minimum acceptable shape index. (default = 1.0)<br> </blockquote> |
| Position offset | Enables or disables position tolerance.<blockquote> **Elliptical Region**<br>Use an elliptical region area instead of a rectangular one. Position XY tolerances are the semi-axes the ellipse or the semi-size of rectangle.<br>  **Position X tolerance**<br>Position tolerance in the X axes. (default = 10)<br>  **Position Y tolerance**<br>Position tolerance in the Y axes. (default = 10)<br> </blockquote> |
| Contrast ratio | Enables or disables contrast ratio condition.<blockquote> **Tolerance -**<br>Negative tolerance.<br>  **Tolerance +**<br>Positive tolerance.<br> </blockquote> |

| Analysis | |
| --- | --- |
| Max. number of results | Number of model instances to find. (default = 1) |
| Multimodel | This button shows [Multimodel](../Pattern_Match/Multimodel.md) parameters settings. |
| Acceptance threshold | The acceptance level for the global searching score. Results with scores below this limit are not accepted. (default = 0.30) |
| Confusion | The confusion threshold is the score above which any match is guaranteed to be an instance of the model; all matches with scores greater than or equal to the confusion threshold are considered to be valid. The Search tool uses the confusion threshold to speed the search process. If you are searching for a single instance of the model in an image, as soon as Search tool finds an instance with a score above the confusion threshold, it stops searching and returns the location of the match. If CNLSearch does not find a match with a score above the confusion threshold, it locates all the matches with scores above the acceptance threshold and returns the location of the match with the highest score. (default = 1.0) |

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
| Score | A value from 0 to 1 indicating the global level of conformity between the model and the pattern found. |
| Contrast ratio | A measure of the contrast of the pattern in relation to the model. 1.0 indicates a contrast equal to the trained pattern. Higher or lower values indicate higher or lower contrast. |

Images
------

| Images | |
| --- | --- |
| Model | Image of the trained model . |
| Mask | Mask image to apply. White pixels are care pixels. Black pixels are don't care. |

Configuration
-------------

This tool is included into the library UvfCvl.
