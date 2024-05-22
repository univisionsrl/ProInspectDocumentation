Arithmetic
==========

![](../../../img/x_Graphics/Tools/UvfStdToolsArithmetic-0.png)

Overview
--------

Arithmetic tool performs arithmetical operations on tools results. Its execution consists in getting position, size, value results of each contained tool and computing its result applying selected arithmetical operation. Available tolerances for Arithmetic tool depend on available result type of contained tools.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |

| Tolerances and limits | |
| --- | --- |
| Position offset | Enables or disables position tolerance limits. Specification position is the trained one and it is defined as middle point between the two tool points.<blockquote> **Elliptical Region**<br>Use an elliptical region area instead of a rectangular one. Position XY tolerances are the semi-axes the ellipse or the semi-size of rectangle.<br>  **Position X tolerance**<br>Position tolerance in the X axes. (default = 10)<br>  **Position Y tolerance**<br>Position tolerance in the Y axes. (default = 10)<br> </blockquote> |
| Angle offset | Enables or disables orientation tolerance limits. Specification orientation is the trained one and it is defined as the orientation of the segment between the two points. <blockquote> **Angle+**<br>Tolerance for positive angles. (default = 360; min = 0; max = 360)<br>  **Angle-**<br>Tolerance for negative angles. (default = 360; min = 0; max = 360)<br> </blockquote> |
| Size | Enables or disables the distance tolerance limits.<blockquote> **Specification**<br>Expected size value. (default = 100)<br>  **Tolerance+**<br>Positive tolerance of the measured size. (default = 10)<br>  **Tolerance-**<br>Negative tolerance of the measured size. (default = 10)<br> </blockquote> |
| Value | Enables or disables the value tolerance limit.<blockquote> **Specification**<br>Expected value. (default = 100)<br>  **Tolerance+**<br>Positive tolerance of the measured value. (default = 10)<br>  **Tolerance-**<br>Negative tolerance of the measured value. (default = 10)<br> </blockquote> |

| Analysis | |
| --- | --- |
| Operation | Operation to be applied.<ud> <li>Sum (default)<br>Sum of all included tool's results.</li>  <li>Subtract<br>Subtracts results' values of second, third,... tools to the first tool's values' result.</li>  <li>Minimum<br>Minimum result values.</li>  <li>Maximum<br>Minimum result values.</li>  <li>Average<br>Average values.</li>  <li>Multiply<br>Multiply values</li>  <li>Range<br>Range between values.</li> </ud> |

### More

Click [here](../../Windows/dialog_settings.md) to access the More section description.

Results
-------
|  | Description |
| --- | --- |
| Decision | Pass/Fail decision of the tool. |
| Processing time | Tool processing time in msec. |
| Position X | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset between the specification X position and result X position (specification reference system).<br> </blockquote> |
| Position Y | Y position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset Y**<br>Offset between the specification Y position and result Y position (specification reference system).<br> </blockquote> |
| Offset length | Distance between specification and result points. |
| Angle | Angle of the tool.<blockquote> **Angle offset**<br>Angle offset from the trained tool angle position.<br> </blockquote> |
| Size | Size.<blockquote> **Difference with specification**<br>Difference between result and specification size.<br> </blockquote> |
| Value | Result of the arithmetic operations.<blockquote> **Difference with specification**<br>Difference between result and specification value.<br> </blockquote> |

Configuration

This tool is included into the library UvfStdTools.



