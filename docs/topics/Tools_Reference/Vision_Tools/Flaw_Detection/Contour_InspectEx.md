Contour Inspect Ex
==================


![](../../../../img/x_Graphics/Tools/UvfCTStdContourInspect2-0.png)


Overview
--------


Contour Inspect Ex Tool is a different optimized and accurate implementation of Contour Inspect tool. The shape of the tool defines a contour where Contour Inspect Ex extracts a set of boundary points and computes the distance between each point and the and the expected shape. Boundary points are extracted by several Edge tools that, differently from ContourInspect tool, work on a rectified image of the perimeter of shape.


Settings
--------





| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Geometry | Defines tool's model shape.<ud> <li>Circle<br>Circular shape.</li>  <li>General rectangle (default)<br>Rectangular shape.</li>  <li>Annulus<br>Annulus shape.</li>  <li>General polygon<br>General polygon shape.</li>  <li>Line seg<br>Line segment.</li>  <li>CAD (Closed ROI)<br>Closed shape imported from a CAD file.</li>  <li>Ellipse arc<br>Ellipses arc.</li> </ud> |
| CAD file | CAD file name. |
| Layer name | Lists the layer names defined in the selected CAD file.<blockquote> **Connection tolerance**<br>Distance between close segment points to be considered as connected.. (default = 0)<br> </blockquote> |
| User calibration | If checked user defines parameters for CAD shapes calibration. Otherwise tool calibration is used.<blockquote> **Axes X rotation**<br>Rotation in the X axes to be applied to the CAD shape. (default = 0; min = -360; max = 360)<br>  **Axes Y rotation**<br>Rotation in the Y axes to be applied to the CAD shape. (default = 0; min = -360; max = 360)<br>  **Scale X**<br>Scale variation in the X axes to be applied to the CAD shape. You express scale value as a multiplier value. (default = 1)<br>  **Scale Y**<br>Scale variation in the Y axes to be applied to the CAD shape. You express scale value as a multiplier value. (default = 1)<br> </blockquote> |

| Tolerances and limits | |
| --- | --- |
| Position offset | Enables or disables position tolerance limits. Specification position is the center of the reference shape in the reference image. Reference shape is the shape originated by nominal shape and the laid on reference points.<blockquote> **Elliptical Region**<br>Use an elliptical region area instead of a rectangular one. Position XY tolerances are the semi-axes the ellipse or the semi-size of rectangle.<br>  **Position X tolerance**<br>Position tolerance in the X axes. (default = 10)<br>  **Position Y tolerance**<br>Position tolerance in the Y axes. (default = 10)<br> </blockquote> |
| Angle offset | Enables or disables orientation offset check. (default = No)<blockquote> **Angle+**<br>Tolerance for positive angles. (default = 360.00)<br>  **Angle-**<br>Tolerance for negative angles. (default = 360.00)<br> </blockquote> |
| Worst intrusion depth | Enables or disables worst intrusion depth check. It is the point more distant from the contour and internal to the inspected object.(default = Yes)<blockquote> **worst point error limit**<br>Maximum error accepted. (default = 0.00)<br> </blockquote> |
| Worst protrusion depth | Enables or disables worst protrusion depth check. It is the point more distant from the contour and external to the inspected object. (default = No)<blockquote> **worst point error limit**<br>Maximum error accepted. (default = 0.00)<br> </blockquote> |
| Intrusion defect length | Enables or disables intrusion defect length check. It is the length of the shape contour that is distant to the reference shape internal to the object more than Intrusion min. depth(default = Yes)<blockquote> **Limit**<br>Maximum length accepted. (default = 0.00)<br> </blockquote> |
| Sum of intrusion lengths | Enables or disables sum of intrusion length check. (default = No)<blockquote> **Limit**<br>Maximum error accepted. (default = 0.00)<br> </blockquote> |
| Intrusion area | Enables or disables intrusion area check. Intrusion area is the area subtended between single intrusion defect and reference shape. (default = Yes)<blockquote> **Limit**<br>Maximum error accepted. (default = 0.00)<br> </blockquote> |
| Sum of intrusion areas | Enables or disables sum of intrusion areas check. (default = No)<blockquote> **Limit**<br>Maximum error accepted. (default = 0.00)<br> </blockquote> |
| Protrusion defect length | Enables or disables protrusion defect length check. It is the length of the shape contour that is distant to the reference shape external to the object more than Protrusion min. depth(default = Yes)<blockquote> **Limit**<br>Maximum length accepted. (default = 0.00)<br> </blockquote> |
| Sum of protrusion lengths | Enables or disables sum of protrusion length check. (default = No)<blockquote> **Limit**<br>Maximum error accepted. (default = 0.00)<br> </blockquote> |
| Protrusion area | Enables or disables protrusion area check. Protrusion area is the area subtended between single protrusion defect and reference shape. (default = Yes)<blockquote> **Limit**<br>Maximum error accepted. (default = 0.00)<br> </blockquote> |
| Sum of protrusion areas | Enables or disables sum of protrusion areas check. (default = No)<blockquote> **Limit**<br>Maximum error accepted. (default = 0.00)<br> </blockquote> |
| Number of missing points | Enables or disables maximum number of not found points. (default = Yes)<blockquote> **Max number of missing points**<br>Maximum number. (default = 0)<br> </blockquote> |

| Classification | |
| --- | --- |
| Short intrusion length | Classification of intrusion lengths. An intrusion length is short if longer than intrusion defect length limit and shorter than this value. (default = 0) |
| Short protrusion length | Classification of protrusion lengths. A protrusion length is short if longer than protrusion defect length limit and shorter than this value. (default = 0) |
| Small intrusion area | Classification of intrusion areas. An intrusion area is small if bigger than intrusion area limit and smaller than this value. (default = 0) |
| Small protrusion area | Classification of protrusion areas. A protrusion area is small if bigger than protrusion area limit and smaller than this value. (default = 0) |
| Small intrusion depth | Classification of intrusion depth. An intrusion depth is small if bigger than intrusion min. depth and smaller than this value. (default = 0) |
| Small protrusion depth | Classification of protrusion depth. A protrusion depth is small if bigger than protrusion min. depth and smaller than this value. (default = 0) |

| Analysis | |
| --- | --- |
| Error polarity | Select polarity of error respect to the reference shape of the inspected object.<ud> <li>Only positive<br>Outside.</li>  <li>Only negative<br>Inside.</li>  <li>Don't care (default)<br>Inside or outside.</li> </ud> |
| Intrusion min. depth | Maximum error accepted inside inspected object. |
| Protrusion min. depth | Maximum error accepted outside inspected object. |
| Inspection mode | Select how the reference shape is calculated. It is the contour algorithm refers to decide if a border point accepted or is a defect. <ud> <li>Ideal shape<br>Geometric shape. It is the specification shape mapped by alignment transformation.</li>  <li>LS fitted shape<br>Fitting shape. It is the result of fitting operation of reference points versus specification shape model.</li>  <li>Spline fitted shape (default)<br>A spline. It is the result of the interpolation of reference points on the best spline.</li> </ud> |
| Num. reference points | Number of points used to calculate the reference shape. (default = 15.00) |
| Num. of points to get average | Number of points to be used in average calculation. (default = 10.00) |
| Ignore points | The number of points to discard to have the best fit. The fitting algorithm ignores the points with the worst distance to the fitted contour. (default = 0)<blockquote> **Residual limit for ignoring**<br>Ignore points for fitting whose residual goes beyond this value. (default = 0)<br> </blockquote> |
| Best points | The number of points, with the best score, to use for fitting. (default = 0.0) |
| Pitch | Distance between Edge tools. (default = 10.00) |
| Edge search width (pixel) | Edge tools width. (default = 20.00) |
| Contrast threshold | The contrast, in gray levels, above which a transition is considered an edge. (default = 5.00) |
| First edge polarity | The expected polarity of the edge. Only edges with the specified polarity are considered. <ud> <li>Dark to light<br>Transition from darker region to lighter one.</li>  <li>Light to dark<br>Transition from lighter region to darker one.</li>  <li>Don't care (default)<br>Any polarity.</li> </ud> |
| Filter size | The filter width for edge extraction. (default = 2) |
| Contrast mode | The edge contrast is used to score single edges.<ud> <li>Disabled<br>No contrast criterion is used.</li>  <li>Stronger contrast (default)<br>Stronger edge pairs get higher scores.</li>  <li>Weaker contrast<br>Weaker edge pairs get higher scores.</li> </ud><blockquote> **Expected contrast**<br>Expected transition grey value that get higher score. (default = 255.00)<br> </blockquote> |
| Position mode | The edge position is used to score single edges.<ud> <li>Disabled (default)<br>No position criteria is used.</li>  <li>Centered position<br>The edge position closer to the center of the projection region gets higher scores.</li>  <li>Closer position<br>The edge position closer to the starting side of the projection region gets higher scores.</li>  <li>Farther position<br>The edge position further form the starting side of the projection region gets higher scores.</li> </ud> |
| Check background | This value checks if a not found edge tool result is due to an obstruction of the border (eg. transfer belts). If the point is not found and the ROI of this edge tool is the expected background, then this point is missing and valuated, otherwise algorithm assumes this region is obstructed and ignore the result.(default = Yes)<blockquote> **Dark background**<br>Background is dark on foreground is brighter or conversely. (default = No)<br>  **Background color limit**<br>Gray value that defines background limit. (default = 128)<br> </blockquote> |

### More

Click More... to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool. |
| Processing time | Tool processing time in msec. |
| Position X | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset between the tool's specification X position and tool's result X position (specification reference system).<br> </blockquote> |
| Position Y | Y position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset Y**<br>Offset between the tool's specification Y position and tool's result Y position (specification reference system). .<br> </blockquote> |
| Offset length | Distance from the trained tool position. |
| Angle | Angle of the tool.<blockquote> **Angle offset**<br>Angle offset from the trained tool angle position.<br> </blockquote> |
| Min contrast | Minimum founded contrast level. |
| Worst intrusion depth | Worst error between the contour point and the result reference shape inside inspected object. |
| Worst protrusion depth | Worst error between the contour point and the result reference shape outside inspected object. |
| Number of intrusions | Number of segment of contour classified as intrusions. |
| Min intrusion length | Minimum length of intrusions. |
| Max intrusion length | Maximum length of intrusions. |
| Sum of intrusions length | Sum of lengths of all intrusion segments. |
| Number of protrusion | Number of segment of contour classified as protrusions. |
| Min protrusion length | Minimum length of protrusions. |
| Max protrusion length | Maximum length of protrusions. |
| Sum of protrusions length | Sum of lengths of all protrusion segments. |
| Number of all intrusion areas | Number of all areas subtended inside the inspected object. |
| Min intrusion area | Minimum area of intrusions. |
| Max intrusion area | Maximum area of intrusions. |
| Sum of intrusions areas | Sum of areas of all intrusions. |
| Number of all protrusion areas | Number of all areas subtended outside the inspected object. |
| Min protrusion area | Minimum area of protrusions. |
| Max protrusion area | Maximum area of protrusions. |
| Sum of protrusions area | Sum of areas of all protrusions. |
| Number of missing points | Number of points not found. |
| Number of points | Number of used Edge tools. |

Configuration
-------------

This tool is included into the library UvfCTStd and UvfCTCvl.

