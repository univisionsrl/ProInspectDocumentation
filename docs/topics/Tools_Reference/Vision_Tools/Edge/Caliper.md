
Caliper
=======


![](../../../../img/x_Graphics/Tools/UvfUICaliper-0.png)


Overview
--------

Caliper tool uses the same techniques described for the Edge tool applied to edge pairs. It locates pair of edges instead of a single edge and reports as additional result the distance between them.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |

| Tolerances and limits | |
| --- | --- |
| Check results count | The expected number of results<ud> <li>None<br>No check.</li>  <li>Expected number<br>Number of results must be equal to Num. of results to find.</li>  <li>Less than<br>Number of results must be less then Num. of results to find.</li>  <li>Greater than<br>Number of results must be greater then Num. of results to find.</li> </ud>    | Num. of results to find | Number of expected edge pair results. | | --- | --- | |
| Position offset | Enables or disables position tolerance limits. Specification position is the center of the Projection region in the reference image .<blockquote> **Elliptical Region**<br>Use an elliptical region area instead of a rectangular one. Position XY tolerances are the semi-axes the ellipse or the semi-size of rectangle.<br>  **Position X tolerance**<br>Position tolerance in the X axes. (default = 10)<br>  **Position Y tolerance**<br>Position tolerance in the Y axes. (default = 10)<br> </blockquote> |
| Size | Enables or disables the size tolerance limit. Sizeis the distance between edge pair.<blockquote> **Specification**<br>Expected size value. (default = 100)<br>  **Tolerance+**<br>Positive tolerance. (default = 10)<br>  **Tolerance-**<br>Negative tolerance. (default = 10)<br> </blockquote> |
| Size (md) | Enable this condition for minor defects evaluation.(default = No)<blockquote> **Tolerance+ (%)**<br>Positive tolerance. (default = 10)<br>  **Tolerance- (%)**<br>Negative tolerance. (default = 10)<br> </blockquote> |

| Analysis | |
| --- | --- |
| Max number of results | Number of result to find. |
| Contrast threshold | The contrast above which a transition is considered an edge. (default = 20) |
| First edge polarity | The expected polarity of the first edge. <ud> <li>Dark to light<br>Transition from darker region to lighter one.</li>  <li>Light to dark<br>Transition from lighter region to darker one.</li>  <li>Don't care (default)<br>Any polarity.</li> </ud> |
| Second edge polarity | The expected polarity of the second edge. <ud> <li>Dark to light<br>Transition from darker region to lighter one.</li>  <li>Light to dark<br>Transition from lighter region to darker one.</li>  <li>Don't care (default)<br>Any polarity.</li> </ud> |
| Filter size | The filter width for edge extraction. (default = 2) |
| Contrast mode | Contrast is used to score edges.<ud> <li>Disabled<br>No contrast criteria is used.</li>  <li>Stronger contrast (default)<br>Stronger couple of edges get higher scores.</li>  <li>Weaker contrast<br>Weaker couple of edges get higher scores.</li> </ud>  <blockquote> **Expected contrast**<br>Expected value of contrast: edges with contrast close to this value will get the highest score. (default = 255.00)<br> </blockquote> |
| Position mode | Position is used to score edges.<ud> <li>Disabled (default)<br>No position criteria is used.</li>  <li>Centered position<br>The center of edge pairs closer to the center of the projection region gets higher scores.</li>  <li>Closer position<br>The center of edge pairs closer to the starting side of the projection region gets higher scores.</li>  <li>Farther position<br>The center of edge pairs further form the starting side of the projection region gets higher scores.</li> </ud> |
| Size mode | Size (distance between the edge pair) is used to score edges.<ud> <li>Disabled (default)<br>No size mode criteria is used.</li>  <li>Expected size<br>Edge pair size closer to expected gets higher scores.</li>  <li>Smaller<br>Edge pair size smaller than expected one gets higher scores.</li>  <li>Larger<br>Edge pair size larger than expected one gets higher scores.</li> </ud>  <blockquote> **Expected size**<br>Expected edge pair size, in pixel. This value is used for scoring only. (default = 0.00)<br> </blockquote> |


### More


Click [here](../../../Windows/dialog_settings.md) to access the More section description.


Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| Processing time | Tool processing time in msec. |
| First edge contrast | Contrast of the found first edge. |
| Second edge contrast | Contrast of the found second edge. |
| Position X | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset between the tool's specification X position and tool's result X position (specification reference system).<br> </blockquote> |
| Position Y | Y position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset Y**<br>Offset between the tool's specification Y position and tool's result Y position (specification reference system).<br> </blockquote> |
| Offset length | Distance between specification and result points. |
| Size | Distance between the edge pairs.<blockquote> **Difference with specification**<br>Difference between the size specified in the Tolerances and limits settings and this measured size.<br> </blockquote> |
| Score | Score of edge result. |


Configuration
-------------

This tool is included into the library UvfCvl.



