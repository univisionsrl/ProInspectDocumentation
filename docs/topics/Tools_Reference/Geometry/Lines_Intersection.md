Lines Intersection
==================

![](../../../img/x_Graphics/Tools/UvfStdToolsLineIntersection-0.png)

Overview
--------


The Lines Intersection tool takes two lines as input and returns the intersection point and lines angle difference. The result position is the intersection point of the two lines. The result angle is the bisector of the angle of the two oriented lines.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |

| Tolerances and limits | |
| --- | --- |
| Position offset | Enables or disables position tolerance. Specification position is the trained one and it is defined as the intersection of nominal lines.<blockquote> **Elliptical region**<br>Search area has elliptical region instead of a rectangular one<br>  **Position X tolerance**<br>Position tolerance in the X axes. (default = 10)<br>  **Position Y tolerance**<br>Position tolerance in the Y axes. (default = 10)<br> </blockquote> |
| Angle offset | Enables or disables orientation tolerance.<blockquote> **Angle+**<br>Tolerance for positive angles. (default = 360; min = 0; max = 360)<br>  **Angle-**<br>Tolerance for negative angles. (default = 360; min = 0; max = 360)<br> </blockquote> |
| Angle between lines | Enables or disables angle span value condition.<blockquote> **Specification**<br>Expected angle value. (default = 90)<br>  **Tolerance+**<br>Positive tolerance of the measured angle. (default = 10)<br>  **Tolerance-**<br>Negative tolerance of the measured angle. (default = 10)<br> </blockquote> |
| Distances | Distances between the extrema of the segments that define lines and opposite line. (default = No)  <br><blockquote> **Specification** <br> Expected distance value. (default = 0) <br> **Tolerance+** <br> Positive tolerance of the measured angle. (default = 10) <br> **Tolerance-** <br> Negative tolerance of the measured angle. (default = 10) </blockquote> |

### More

Click More... to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| Processing time | Tool processing time in msec. |
| Position X | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset between the tool's specification X intersection position and tool's result X intersection position (specification reference system).<br> </blockquote> |
| Position Y | Y position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset Y**<br>Offset between the tool's specification Y intersection position and tool's result Y intersection position (specification reference system).<br> </blockquote> |
| Offset length | Distance from the trained tool position. |
| Angle | Angle of the tool.<blockquote> **Angle offset**<br>Angle offset from the trained tool angle position.<br> </blockquote> |
| Min. distance | Minimum distance between the extrema of the segments that define lines and the opposite line.<blockquote> **Difference with specification**<br>Difference between the specification value and the result value.<br> </blockquote> |
| Max. distance | Maximum distance between the extrema of the segments that define lines and the opposite line.<blockquote> **Difference with specification**<br>Difference between the specification value and the result value.<br> </blockquote> |
| Angle between lines | Angle between the specified lines.<blockquote> **Difference with specification**<br>Difference between the specification value and the result value.<br> </blockquote> |



