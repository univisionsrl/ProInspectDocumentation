Circle Finder
=============


![](../../../../img/x_Graphics/Tools/UvfUICircle-0.png)


Overview
--------


The Circle finder tool extracts a circular shape within an annular region. A number of Edge tools is automatically placed along radiuses centred on the centre of the annulus. Each Edge provides a result point and a circumference is computed as best fit on them. For reliable error evaluation the gap between the tools should be small. Therefore chose enough edge tools or points in the analysis section.


Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |

| Tolerances and limits | |
| --- | --- |
| Position offset | Enables or disables position tolerance. Specification position is the center of interpolated circle.<blockquote> **Elliptical Region**<br>Use an elliptical region area instead of a rectangular one. Position XY tolerances are the semi-axes the ellipse or the semi-size of rectangle.<br>  **Position X tolerance**<br>Position tolerance in the X axes. (default = 10)<br>  **Position Y tolerance**<br>Position tolerance in the Y axes. (default = 10)<br> </blockquote> |
| Diameter | Enables or disables the diameter value and tolerances to be used as pass/fail condition.<blockquote> **Diameter mode**<br>Criteria to compute diameter.            Interpolated      Diameter of best fit circle.          Worst      Diameter computed using the radius on the worst point.<br>  **Specification**<br>Expected diameter value. (default = 100)<br>  **Tolerance+**<br>Positive tolerance of the measured diameter. (default = 10)<br>  **Tolerance-**<br>Negative tolerance of the measured diameter. (default = 10)<br> </blockquote> |
| Eccentricity | Enables or disables eccentricity tolerance condition. Eccentricity is defined as difference between maximum diameter and minimum diameter.<blockquote> **limit**<br>Max accepted difference accepted. (default = 0)<br> </blockquote> |
| Number of missing points | Enables or disables missing point condition.<blockquote> **Max. number of missing points**<br>The number of points that can be missing without a failure condition. (default = 0)<br> </blockquote> |
| Ignore points | The number of points to discard to have the best fit. The fitting algorithm ignores the points with the worst distance between the tool result point and the fit circle. Then it recomputes the fit circle.<blockquote> **Residual limit for ignoring**<br>The minimum value to consider a point as a candidate for decimation. (default = 0)<br> </blockquote> |
|
| Best points | The number of points, with the best score, to use for fitting. |
| Positive worst error | Enables positive worst point error condition. If the point with the worst error has a residual bigger than the worst point error limit, the condition fails. Positive sign when the point lays outside the fit circle<blockquote> **Worst point error limit**<br>Max accepted distance between any edge and the fitted line. (default = 0)<br> </blockquote> |
| Negative worst error | Enables positive worst point error condition. If the point with the worst error has a residual bigger than the worst point error limit, the condition fails. Positive sign when the point lays inside the fit circle<blockquote> **Worst point error limit**<br>Max accepted distance between any edge and the fitted line. (default = 0)<br> </blockquote> |
|
| Mean error | Enables or disables mean error condition.<blockquote> **Error limit**<br>Max accepted mean error distance. (default = 0)<br> </blockquote> |
|
|
| Local errors | Enable or disable local error condition. Local errors are the errors of points relative to the errors of closest points. The residual error of each point is compared with neighbors (local) to evaluate if they are real defects. If this comparison is bigger than a threshold, the condition fails.<blockquote> **Positive local error**<br>Maximum accepted positive local error . (default = 0)<br>  **Negative local error**<br>Maximum accepted negative local error. (default = 0)<br> </blockquote> |





| Analysis | |
| --- | --- |
| Number of points | Number of edge tools to use. (default = 6) |
| Double edge | Enable or disable double edge searching. If set point used for interpolation will be the center of edge pair(default = No) |
| Contrast threshold | The contrast above which a transition is considered an edge (default = 20) |
| First edge polarity | The expected polarity of the edge. Only edges with the specified polarity are considered. <ud> <li>Dark to light<br>Transition from darker region to lighter one.</li>  <li>Light to dark<br>Transition from lighter region to darker one.</li>  <li>Don't care (default)<br>Any polarity.</li> </ud> |
| Filter size (pixel) | The filter width for edge extraction. (default = 2) |
| Contrast mode | The edge contrast is used to score single edges.<ud> <li>Disabled<br>No contrast criterion is used.</li>  <li>Stronger contrast (default)<br>Stronger edge pairs get higher scores.</li>  <li>Weaker contrast<br>Weaker edge pairs get higher scores.</li> </ud><blockquote> **Expected contrast**<br>Expected transition grey value that get higher score. (default = 255.00)<br> </blockquote> |
| Position mode | The edge position is used to score single edges.<ud> <li>Disabled (default)<br>No position criteria is used.</li>  <li>Centered position<br>The edge position closer to the center of the projection region gets higher scores.</li>  <li>Closer position<br>The edge position closer to the starting side of the projection region gets higher scores.</li>  <li>Farther position<br>The edge position further form the starting side of the projection region gets higher scores.</li> </ud> |
| Filter for local error (points) | Number of neighbor points used for comparison. (default = 2)<blockquote> **latency**<br>Parameter that identifies neighbors: distance in pixels from current point to define neighbors for comparison. (default = 0)<br>  **Overlap for local errors**<br>Overlap ends points for local errors investigation<br> </blockquote> |


### More


Click [here](../../../Windows/dialog_settings.md) to access the More section description.


Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| Processing time | Tool processing time in msec. |
| Position X | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset between the specification X position and result X position (specification reference system).<br> </blockquote> |
| Position Y | Y position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset Y**<br>Offset between the specification Y position and result Y position (specification reference system).<br> </blockquote> |
| Offset length | Distance between specification and result points. |
| Size | Measured diameter<blockquote> **Difference with specification**<br>Difference between the specification and result diameter.<br> </blockquote> |
| Max diameter | Diameter of the circle passing through the farthest point. |
| Min diameter | Diameter of the circle passing through the nearest point. |
| Eccentricity | Difference between Max diameter and min diameter. |
| Mean error | Mean distance between the results points and the fitted circle. |
| Positive worst error (point) | Worst positive distance between the results points and the fitted circle. The number between () indicates the point index the value refers to. |
| Number of missing points | Number of not found edges. |
| Position X | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset between the specification X position and result X position (specification reference system).<br> </blockquote> |
| Position Y | Y position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset Y**<br>Offset between the specification Y position and result Y position (specification reference system).<br> </blockquote> |
| Offset length | Distance between specification and result points. |


Configuration
-------------


This tool is included into the library UvfCvl.



