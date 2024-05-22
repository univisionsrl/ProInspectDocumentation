SCTSConnector
=============

![](../../../../img/x_Graphics/Tools/CTSuperConnectorTool-0.png)

Overview
--------

Super Connector (SCTSConnector) tool is a container of Connector tools. It calculates the transform that fits the contained Connectors to their specification positions. The result is the Super Connector is the point resulting from the application of the found fit transform to its tool reference point.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Super Connector ref. point X | Reference point X. (default = 0.00) |
| Super Connector ref. point Y | Reference point Y. (default = 0.00) |
| Super Connector angle | Reference angle. (default = 0.00) |

| Connector | |
| --- | --- |
| Connector | Connector selection to set their position parameters.<ud> <li>(Connector #n)<br> </li> </ud> |
| Position | Choose how to consider the connector position.<ud> <li>Absolute<br>Use absolute connector position. (default)</li>  <li>Relative<br>Use offset relative to Super Connector reference point.</li> </ud> |
| Offset X | Relative offset X. (default = 0.00) |
| Offset Y | Relative offset Y. (default = 0.00) |
| Offset Angle | Relative Angle. (default = 0.00) |

| Tolerances and limits | |
| --- | --- |
| Position offset | Enables or disables position tolerance.<blockquote> **Elliptical region**<br>Search area has elliptical region instead of a rectangular one.<br>  **Position X tolerance**<br>Position tolerance in the X axes. (default = 10)<br>  **Position Y tolerance**<br>Position tolerance in the Y axes. (default = 10)<br> </blockquote> |
| Angle offset | Enables or disables orientation tolerance.<blockquote> **Angle+**<br>Tolerance for positive angles. (default = 360; min = 0; max = 360)<br>  **Angle-**<br>Tolerance for negative angles. (default = 360; min = 0; max = 360)<br> </blockquote> |
| Ignore points | Enables or disables missing point condition. Points with a larger distance than the limit below are ignored.<blockquote> **Residual limit for ignoring**<br>How many point can be missing without set fail condition. (default = 0)<br> </blockquote> |
| Best points | The fitting algorithm use only the points with best score. |
| Positive worst error | Enables positive worst point error condition; worst point is the one with the largest distance from the fitted points.<blockquote> **Worst point error limit**<br>Max accepted distance between any point and the fitted point. (default = 0)<br> </blockquote> |
| Mean error | Enables or disables mean error condition.<blockquote> **Error limit**<br>Max accepted mean error distance. (default = 0)<br> </blockquote> |
|


### More


Click [here](../../../Windows/dialog_settings.md) to access the More section description.


Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| Processing time | Tool processing time in msec. |
| Position X | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset from the trained tool position in the X axes.<br> </blockquote> |
| Position Y | Y position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset Y**<br>Offset from the trained tool position in the Y axes.<br> </blockquote> |
| Offset length | Distance from the trained tool position. |
| Angle | Angle of the tool.<blockquote> **Angle offset**<br>Angle offset from the trained tool angle position.<br> </blockquote> |
| Mean error | Mean distance between the points and the fitted points. |
| Worst error+ (point) | Worst positive distance between the points and the fitted points. The number between () indicates the point index the value refers to. |


Configuration
-------------


This tool is included into the library SuperConnector.



