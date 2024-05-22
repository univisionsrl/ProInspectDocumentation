Point Fit
=========

![](../../../img/x_Graphics/Tools/UvfStdToolsPointFit-0.png)

Overview
--------

The Point Fit lets you compute a transformation that fits the resulting position of the contained tools to their specification position. The resulting position is the reference point mapped with the result transformation. Tools that specifies positions to be fitted can be either their nominal positions or user specified positions or custom defined id positions. The point fit reference point can be the center of mass of contained points or a user-defined position.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |

| Tolerances and limits | |
| --- | --- |
| Position offset | Enables or disables position tolerance. Specification position relays on theReference point mode selected.<blockquote> **Elliptical region**<br>se an elliptical region area instead of a rectangular one. Position XY tolerances are the semi-axes the ellipse or the semi-size of rectangle<br>  **Position X tolerance**<br>Position tolerance in the X axes. (default = 10)<br>  **Position Y tolerance**<br>Position tolerance in the Y axes. (default = 10)<br> </blockquote> |
| Angle offset | Enables or disables angle tolerance limits. <blockquote> **Angle+**<br>Tolerance for positive angles. (default = 360; min = 0; max = 360)<br>  **Angle-**<br>Tolerance for negative angles. (default = 360; min = 0; max = 360)<br> </blockquote> |
| Number of missing points | Enables or disables missing point condition.<blockquote> **Max. number of missing points**<br>The number of points that can be missing without a failure condition. (default = 0)<br> </blockquote> |
| Ignore points | The number of points to discard to have the best fit. The fitting algorithm ignores the points with the worst distance between the tool result point and the ideal expected point (nominal point mapped by the fit transformation) and recomputes the transformation<blockquote> **Residual limit for ignoring**<br>The minimum value to consider a point as a candidate for decimation. (default = 0)<br> </blockquote> |
| Best points | The number of points, with the best score, to use for fitting. |
| Worst error | Enables or disables worst point error condition. The worst point is the one with the largest distance from the expected ideal point.<blockquote> **Worst point error limit**<br>Max accepted distance between any point and the ideal point. (default = 0)<br> </blockquote> |
| Mean error | Enables or disables the mean error condition.<blockquote> **Error limit**<br>Max accepted mean error distance. (default = 0)<br> </blockquote> |

| Analysis | |
| --- | --- |
| Points to fit | Select the points to fit. (default = Yes)<blockquote> **Tool position**<br>Resulting tools' positions are fitted to their nominal position. (default)<br>  **User points**<br>Resulting tools' positions are fitted to the user defined positions.<br>  **Tool Search Id point**<br>Resulting tools' positions are fitted to their Search id positions (if configured).<br> </blockquote> |
| Reference point | Reference point mode to use as tool position.<blockquote> **Center of mass**<br>Center of mass of all contained tools' points. (default)<br>  **Origin**<br>Reference system origin.<br>  **(Tools #n)**<br>One of the contained tool's position.<br> </blockquote> |
| Point selection | Select point to see its specification point. Points values are editable if Points to fit mode is User points.<blockquote> **(Tools #n)**<br>Tool.<br> </blockquote><blockquote> **X Point**<br>Specification point X coordinate. (default = 0.00)<br>  **Y Point**<br>Specification point Y coordinate. (default = 0.00)<br>  **Angle**<br>Specification point Angle. (default = 0.00)<br> </blockquote> |

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
| Angle | Angle of the transformation that maps specification points to result points.<blockquote> **Angle offset**<br>Angle offset between specification and result angle.<br> </blockquote> |
| Mean error | Mean residual. |
| Worst error (point) | Worst distance between result points and ideal points. The number between () indicates the point index the value refers to. |
| Number of missing points | Number of not found points. |

