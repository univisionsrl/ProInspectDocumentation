Circle Fit
==========


![](../../../img/x_Graphics/Tools/UvfStdToolsCircleFit-0.png)


Overview
--------


The CircleFit tool is a Geometric tool. It lets you fit a circle to a set of points by minimizing the sum of the squares of the distances between all the points and the fit circle. The CircleFit tool generates as a result a circle. 


The result of the CircleFit tool is the center position of the circle. 


Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |

| Tolerances and limits | |
| --- | --- |
| Position offset | Enables or disables position tolerance. Specification position is the center of interpolated circle using specification contained tools' positions.<blockquote> **Elliptical region**<br>Use an elliptical region area instead of a rectangular one. Position XY tolerances are the semi-axes the ellipse or the semi-size of rectangle.<br>  **Position X tolerance**<br>Position tolerance in the X axes. (default = 10)<br>  **Position Y tolerance**<br>Position tolerance in the Y axes. (default = 10)<br> </blockquote> |
| Diameter | Enables or disables the diameter tolerance limits.<blockquote> **mode**<br>Criteria to compute diameter.            Interpolated      Diameter of best fit circle.          Worst      Diameter computed using the radius on the worst point.<br>  **specification**<br>Expected diameter value. (default = 100)<br>  **tolerance+**<br>Positive tolerance of the measured diameter. (default = 10)<br>  **tolerance-**<br>Negative tolerance of the measured diameter. (default = 10)<br> </blockquote> |
| Eccentricity | Enables or disables eccentricity tolerance condition. Eccentricity is defined as difference between maximum diameter and minimum diameter.<blockquote> **limit**<br>Max accepted difference accepted. (default = 0)<br> </blockquote> |
| Number of missing points | Enables or disables missing point condition.<blockquote> **Max. number of missing points**<br>The number of points that can be missing without a failure condition. (default = 0)<br> </blockquote> |
| Ignore points | The number of points to discard to have the best fit. The fitting algorithm ignores the points with the worst distance between the tool result point and the fit circle and recomputes the fit circle.<blockquote> **Residual limit for ignoring**<br>The minimum value to consider a point as a candidate for decimation. (default = 0)<br> </blockquote> |
| Best points | The number of points, with the best score, to use for fitting. |
| Positive worst error | Enables positive worst point error condition. If the point with the worst error has a residual bigger than the worst point error limit, the condition fails. Positive sign when the point lays outside the fit circle Worst point error limitMax accepted distance between any edge and the fitted line. (default = 0) |
| Negative worst error | Enables positive worst point error condition. If the point with the worst error has a residual bigger than the worst point error limit, the condition fails. Positive sign when the point lays inside the fit circle<blockquote> **Worst point error limit**<br>Max accepted distance between any edge and the fitted line. (default = 0)<br> </blockquote> |
| Mean error | Enables or disables mean error condition.<blockquote> **Error limit**<br>Max accepted mean error distance. (default = 0)<br> </blockquote> |
| Local errors | Enable or disable local error condition. Local errors are the errors of points relative to the errors of closest points. The residual error of each point is compared with neighbors (local) to evaluate if they are real defects. If this comparison is bigger than a threshold, the condition fails..<blockquote> **Positive local error**<br>Maximum accepted positive local error . (default = 0)<br>  **Negative local error**<br>Maximum accepted negative local error. (default = 0)<br>  **Filter for local errors**<br>Number of neighbor points used for comparison. (default = 2)<br>  **Filter latency**<br>Parameter that identifies neighbors: distance in pixels from current point to define neighbors for comparison. (default = 0)<br> </blockquote> |

### More

Click More... to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of the tool. |
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
| Number of missing points | Number of not found points. |



