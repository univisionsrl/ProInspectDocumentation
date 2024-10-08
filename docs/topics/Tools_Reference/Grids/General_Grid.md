General Grid
============

![](../../../img/x_Graphics/Tools/UvfStdToolsGridGeneral-0.png)


Overview
--------

Grid is a tool that automatically executes contained user-selected tools and positions them alongside the perimeter of an arbitrary shape. Every contained tool is run at the same position and orientation relative to the position of starting point of the shape. The perimeter is divided into n-points (number of regions): these points are the reference points of each reiteration.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Position mode | How the grid position is defined. <br><blockquote> **Normal** (default) <br> Position is the position of first contained tool. <br> **Selective** <br> Position components can be individually selected between the positions of the contained tools. <br> **X**  Select tool to be used as X component.   <br> <ud><li> (Tools #n) <br> Use the selected tool's X component. </ud></li> **Y** <br> Select tool to be used as Y component.   <br> <ud><li> (Tools #n) <br> Use the selected tool's Y component. </ud></li>**Angle** <br> Select tool to be used as Angle component.   <br> <ud><li> (Tools #n) <br> Use the selected tool's Angle component. </ud></li></blockquote>
| Local tuning | Tool expected position in an iteration is adjusted with the result found in the preceding cell. It is a recursive pre-alignment(default = No) |
| Geometry | Defines tool's region shape.<ud> <li>Circle<br>Circular shape.</li>  <li>General rectangle (default)<br>Rectangular shape.</li>  <li>Annulus<br>Annulus shape.</li>  <li>General polygon<br>General polygon shape.</li>  <li>LineSeg<br>Segment shape.</li>  <li>Ellipse arc<br>Ellipse arc shape.</li> </ud> |

| Tolerances and limits | |
| --- | --- |
| Check results count | Enables or disables results count condition. Condition fails if number of good results don't agree with settings.  <br><blockquote> **None** <br> Disabled <br> **Expected number** <br> The expected number of good results <br> **Less than** <br> Less than number of good results <br> **Greater than** <br> More than number of good results <br> **Number of results to find** <br> Enter number of good results. (default = 1) <blockquote> |

| Analysis | |
| --- | --- |
| Points | Number iterative regions. (default = 1) |

### More

Click More... to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| Results count | Number of found results. |
| Processing time | Tool processing time in msec. |
| Position X | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset between the specification X position and result X position (specification reference system).<br> </blockquote> |
| Position Y | Y position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset Y**<br>Offset between the specification Y position and result Y position (specification reference system).<br> </blockquote> |
| Offset length | Distance between specification and result points. |
| Angle | Angle of the tool.<blockquote> **Angle offset**<br>Angle offset from the trained tool angle position.<br> </blockquote> |


Configuration


This tool is included into the library UvfStdTools.



