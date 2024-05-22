Compute
=======


![](../../../../img/x_Graphics/Tools/UvfStdToolsCompute-0.png)


Overview
--------


Compute tool is an utility tools that permits to manage results from other tools. You can implement yourself the behaviour of the tool editing a script: this script tells the Compute tools which data collect and how to use them. The Compute tool can have a position (defined by the script), a measure (defined by the script) and a value (defined by the script).


Settings
--------





| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |





| Tolerances and limits | |
| --- | --- |
| Position offset | Enables or disables position tolerance limits. Specification position is defined by the script.<blockquote> **Elliptical Region**<br>Use an elliptical region area instead of a rectangular one. Position XY tolerances are the semi-axes the ellipse or the semi-size of rectangle.<br>  **Position X tolerance**<br>Position tolerance in the X axes. (default = 10)<br>  **Position Y tolerance**<br>Position tolerance in the Y axes. (default = 10)<br> </blockquote> |
| Angle offset | Enables or disables orientation tolerance limits. Specification orientation is defined by the script. <blockquote> **Angle+**<br>Tolerance for positive angles. (default = 360; min = 0; max = 360)<br>  **Angle-**<br>Tolerance for negative angles. (default = 360; min = 0; max = 360)<br> </blockquote> |
| Size | Enables or disables the size tolerance limit. Sizeis defined by the script.<blockquote> **Specification**<br>Expected size value. (default = 100)<br>  **Tolerance+**<br>Positive tolerance. (default = 10)<br>  **Tolerance-**<br>Negative tolerance. (default = 10)<br> </blockquote> |
| Value | Enable or disable a value tolerance limit. Value is defined by the script.<blockquote> **Specification**<br>Specification value. (default = 0)<br>  **Tolerance+**<br>Upper tolerance accepted. (default = 0)<br>  **Tolerance-**<br>Down tolerance accepted. (default = 0)<br> </blockquote> |





| Analysis | |
| --- | --- |
| Config XML | Press this button to show Compute tool XML Configuration dialog. |


### More


Click [here](../../../Windows/dialog_settings.md) to access the More section description.


Results
-------






| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| Processing time | Tool processing time in msec. |
| Position X | Distance between specification and result points. |
| Position Y | Distance between the edge pairs.<blockquote> **Difference with specification**<br>Difference between the size specified in the Tolerances and limits settings and this measured size.<br> </blockquote> |
| Offset length | Distance between specification and result points. |
| Angle | Angle of the tool.<blockquote> **Angle offset**<br>Offset between the tool's specification orientation angle and tool's result orientation angle.<br> </blockquote> |
| Size | Size result.<blockquote> **Difference with specification**<br>Difference between the size specified in the Tolerances and limits settings and this measured size.<br> </blockquote> |
| Value | Value result.<blockquote> **Difference with specification**<br>offset from specification value.<br> </blockquote> |


Configuration
-------------


This tool is included into the library UvfStdTools.



