XML
===

![](../../../../img/x_Graphics/Tools/UvfStdToolsXml-0.png)

Overview
--------

XML tool is a container of tools that can be exported on a XML file. Settings of all contained tools are exported to the XML file. XML tool can be exported by menu:


	File > Import and Export > Export XML tool


The xml file resulting from the Export XML tool operation can be imported into another XML tool by menu:

	File > Import and Export > Import XML tool


The operation of importing a previously exported xml file will result in initializing the XML tool with all the tools saved in the xml file.

When there are tools with a valid SearchId , the tool searches for the tools positions. Then compares the found positions to the expected positions, as defined in the nominal search position, and calculates the mean and worst errors.

The tool position is defined as the origin (0, 0) mapped with the transformation that best fits the found to the expected positions.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| XML file | Insert file name to initialize the tool with a XML file. |

| Tolerances and limits | |
| --- | --- |
| Mean error | Enables or disables tolerance check on mean error for tool fixture.<blockquote> **Error limit**<br>Max accepted mean error distance. (default = 0)<br> </blockquote> |
| Worst error | Enables or disables tolerance check on worst error for fixture tool. Worst point is the one with the largest distance from the fitted point. <blockquote> **Worst point error limit**<br>Max accepted distance between any point and the fitted point. (default = 0)<br> </blockquote> |

### More

Click [here](../../../Windows/dialog_settings.md) to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool. |
| Processing time | Tool processing time in msec. |
| Position X | X position coordinates. The position is referred to the origin point of the tool. |
| Position Y | Y position coordinates. The position is referred to the origin point of the tool. |
| Offset length | Distance from the trained tool position. |
| Angle | Angle of the tool. |



