Cycle Index
===========

![](../../../../img/x_Graphics/Tools/CTCycleIndexToolTool-0.png)

Overview
--------

CycleIndex is a simple tool that produces a code for current inspection. With default implementation it uses the View's conditioned run code acquired. This code is than transformed as a string code that is the own tool result.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |

| Tolerances and limits | |
| --- | --- |
| Value | Enables or disables check on current value (code) of the tool. (default = Yes)<blockquote> **Specification**<br>expected code<br>  **tolerance -**<br>negative tolerance. (default = 10)<br>  **tolerance +**<br>positive tolerance. (default = 10)<br> </blockquote> |

### More

Click [here](../../../Windows/dialog_settings.md) to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool. |
| Processing time | Tool processing time in msec. |
| Value | current value.<blockquote> **difference with specification**<br>Offset.<br> </blockquote> |

Configuration
-------------

This tool is included into the library CycleIndexTool
