Polar Grid
==========

![](../../../img/x_Graphics/Tools/UvfStdToolsGridPolar-0.png)

Overview
--------

Polar Grid is a tool that automatically executes contained user-selected tools and positions them alongside the perimeter of an polar region. Every contained tool is run at the same position and orientation relative to the position of starting point of the shape. The polar region is divided into n-sectors (number of regions): the centers of these points are the reference points of each reiteration.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Position mode | How the grid position is defined.    <br><blockquote> **Normal** (default) <br> Position is the position of first contained tool. <br> **Selective** <br> Position components can be individually selected between the positions of the contained tools. <br> **X** <br> Select tool to be used as X component. <ud><li>  (Tools #n) <br> Use the selected tool's X component. </li></ud> **Y** <br> Select tool to be used as Y component. <br> <ud><li> (Tools #n) <br> Use the selected tool's Y component.</li></ud> **Angle** <br> Select tool to be used as Angle component. <ud><li> (Tools #n) <br> Use the selected tool's Angle component. </li> </ud>|
| Local tuning | Tool expected position in an iteration is adjusted with the result found in the preceding point. It is a recursive pre-alignment(default = No) |

| Tolerances and limits | |
| --- | --- |
| Check results count | Enables or disables results count condition. Condition fails if number of good results don't agree with settings.  <ud><li> None <br> Disabled </li><li> Expected number <br> The expected number of good results </li><li> Less than <br> Less than number of good results </li><li> Greater than <br> More than number of good results </li><li> Number of results to find <br> Enter number of good results. (default = 1) </li></ud>

| Analysis | |
| --- | --- |
| Sectors | Number sectors the polar region is split to.(default = 1) |

### More

Click More... to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| Results count | Number of found results. |
| Processing time | Tool processing time in msec. |
| Result | Result selection index, if there are multiple results. |
| Decision | Pass/Fail decision of a single result |
| Position X | Pass/Fail decision of a tool, including multiple results if any. |
| Position Y | Number of found results. |
| Offset length | Tool processing time in msec. |
| Angle | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset between the specification X position and result X position (specification reference system).<br> </blockquote> |


Configuration


This tool is included into the library UvfStdTools.



