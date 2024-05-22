Points Grid
===========

![](../../../img/x_Graphics/Tools/UvfStdToolsGridPoints-0.png)

Overview
--------

Points Grid is a tool that allows distributing contained tools in N user-defined positions. The user defines the N positions with X, Y and Angle, and the Points Grid tool executes the only instance of each contained tool in those positions.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Position mode | How the grid position is defined.    | Normal (default) | Position is the position of first contained tool. | | --- | --- | | Selective | Position components can be individually selected between the positions of the contained tools. | | X | Select tool to be used as X component.   | (Tools #n) | Use the selected tool's X component. | | --- | --- | | | Y | Select tool to be used as Y component.   | (Tools #n) | Use the selected tool's Y component. | | --- | --- | | | Angle | Select tool to be used as Angle component.   | (Tools #n) | Use the selected tool's Angle component. | | --- | --- | | |
| Local tuning | Tool expected position in an iteration is adjusted with the result found in the preceding point. It is a recursive pre-alignment(default = No) |

| Tolerances and limits | |
| --- | --- |
| Check results count | Enables or disables results count condition. Condition fails if number of good results don't agree with settings.   | None | Disabled | | --- | --- | | Expected number | The expected number of good results | | Less than | Less than number of good results | | Greater than | More than number of good results | | Number of results to find | Enter number of good results. (default = 1) | |

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
| Result | Result selection index, if there are multiple results. |
| Decision | Pass/Fail decision of a single result |
| Position X | Pass/Fail decision of a tool, including multiple results if any. |
| Position Y | Number of found results. |
| Offset length | Tool processing time in msec. |
| Angle | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset between the specification X position and result X position (specification reference system).<br> </blockquote> |


Configuration


This tool is included into the library UvfStdTools.



