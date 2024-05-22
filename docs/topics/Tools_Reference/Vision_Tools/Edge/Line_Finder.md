Line Finder
===========

![](../../../../img/x_Graphics/Tools/UvfUILine-0.png)

Overview
--------

The Line finder tool lets you extract a line using a set of multiple Edge tools placed perpendicularly along a line. Each Edge tool returns a point and a line is interpolated as best fit on all points found. The result of the Line tool is the center position and the orientation of the line.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |

| Tolerances and limits | |
| --- | --- |
| Position offset | Enables or disables position tolerance. Specification position is the center segment laying on the interpolated line.<blockquote> **Elliptical Region**<br>Use an elliptical region area instead of a rectangular one. Position XY tolerances are the semi-axes the ellipse or the semi-size of rectangle.<br>  **Position X tolerance**<br>Position tolerance in the X axes. (default = 10)<br>  **Position Y tolerance**<br>Position tolerance in the Y axes. (default = 10)<br> </blockquote> |
| Angle offset | Enables or disables orientation tolerance.<blockquote> **Angle+**<br>Tolerance for positive angles. (default = 360; min = 0; max = 360)<br>  **Angle-**<br>Tolerance for negative angles. (default = 360; min = 0; max = 360)<br> </blockquote> |
| Number of missing points | Enables or disables missing point condition.<blockquote> **Max. number of missing points**<br>The number of points that can be missing without a failure condition. (default = 0)<br> </blockquote> |
| Ignore points | The number of points to discard to have the best fit. The fitting algorithm ignores the points with the worst distance between the tool result point and the fit line. Then it recomputes the fit line.<blockquote> **Residual limit for ignoring**<br>The minimum value to consider a point as a candidate for decimation. (default = 0)<br> </blockquote> |
| Best points | The number of points, with the best score, to use for fitting. |
| Positive worst error | Enables positive worst point error condition. If the point with the worst error has a residual bigger than the worst point error limit, the condition fails. Positive sign when the normal to the line passing from this point generates with the oriented line an angle of +90°. Worst point error limitMax accepted distance between any edge and the fitted line. (default = 0) |
| Negative worst error | Enables negative worst point error condition. If the point with the worst error has a residual bigger than the worst point error limit, the condition fails. Negative sign when the normal to the line passing from this point generates the oriented line an angle of -90°.<blockquote> **Worst point error limit**<br>Max accepted distance between any edge and the fitted line. (default = 0)<br> </blockquote> |
| Mean error | Enables or disables mean error condition.<blockquote> **Error limit**<br>Max accepted mean error distance. (default = 0)<br> </blockquote> |
| Local errors | Enable or disable local error condition. Local errors are the errors of points relative to the errors of closest points. The residual error of each point is compared with neighbors (local) to evaluate if they are real defects. If this comparison is bigger than a threshold, the condition fails.<blockquote> **Positive local error**<br>Max accepted positive peak of the error derivative. (default = 0)<br>  **Negative local error**<br>Max accepted negative peak of the error derivative. (default = 0)<br> </blockquote> |
|

| Analysis | |
| --- | --- |
| Number of points | Number of edge tools to use. (default = 4) |
| Double edge | Enable or disable double edge searching. If set point used for interpolation will be the center of edge pair(default = No) |
| Contrast threshold | The contrast above which a transition is considered an edge.  (default = 20) |
| First edge polarity | The expected polarity of the edge. Only edges with the specified polarity are considered. <ud> <li>Dark to light<br>Transition from darker region to lighter one.</li>  <li>Light to dark<br>Transition from lighter region to darker one.</li>  <li>Don't care (default)<br>Any polarity.</li> </ud> |
| Filter size (pixel) | The filter width for edge extraction. (default = 4) |
| Contrast mode | The edge contrast is used to score single edges.<ud> <li>Disabled<br>No contrast criterion is used.</li>  <li>Stronger contrast (default)<br>Stronger edge pairs get higher scores.</li>  <li>Weaker contrast<br>Weaker edge pairs get higher scores.</li> </ud><blockquote> **Expected contrast**<br>Expected transition grey value that get higher score. (default = 255.00)<br> </blockquote> |
| Position mode | The edge position is used to score single edges.<ud> <li>Disabled (default)<br>No position criteria is used.</li>  <li>Centered position<br>The edge position closer to the center of the projection region gets higher scores.</li>  <li>Closer position<br>The edge position closer to the starting side of the projection region gets higher scores.</li>  <li>Farther position<br>The edge position further form the starting side of the projection region gets higher scores.</li> </ud> |
| Line position mode | Criterion for fitted line positioning.<ud> <li>Centered (default)<br>The line is positioned minimizing the fitting errors.</li>  <li>Worst negative<br>The line is positioned at the worst negative point.</li>  <li>Worst positive<br>The line is positioned at the worst positive point.</li> </ud> |
| Filter for local errors (points) | Filter width<blockquote> **Filter latency (points)**<br>Shift of the values of the filter from its center. (default = 255.00)<br> </blockquote> |


### More


Click [here](../../../Windows/dialog_settings.md) to access the More section description.


Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| Processing time | Tool processing time in msec. |
| Position X | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset between the tool's specification X position and tool's result X position (specification reference system).<br> </blockquote> |
| Position Y | Y position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset Y**<br>Offset between the tool's specification Y position and tool's result Y position (specification reference system). .<br> </blockquote> |
| Offset length | Distance from the trained tool position. |
| Angle | Angle of the tool.<blockquote> **Angle offset**<br>Angle offset from the trained tool angle position.<br> </blockquote> |
| Min. edge contrast (point) | Edge minimum value. The number between () indicates the point index the value refers to. |
| Max. edge contrast (point) | Edge maximum value. The number between () indicates the point index the value refers to. |
| Mean error | Mean distance between the edges and the fitted line. |
| Worst error+ (point) | Worst positive distance between the edges and the fitted line. The number between () indicates the point index the value refers to. |
| Worst error- (point) | Worst negative distance between the edges and the fitted line. The number between () indicates the point index the value refers to. |
| Max local error+ (point) | Maximum positive local error. The number between () indicates the point index the value refers to. |
| Max local error- (point) | Maximum negative local error. The number between () indicates the point index the value refers to. |
| Number of missing points | Number of not found edges. |


Configuration
-------------


This tool is included into the library UvfCvl.



