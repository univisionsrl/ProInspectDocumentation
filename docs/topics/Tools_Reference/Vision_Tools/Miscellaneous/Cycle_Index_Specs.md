Cycle Index specs
=================

![](../../../../img/x_Graphics/Tools/CTCycleIndexSpecs-0.png)

Overview
--------

CycleIndex Specs is a simple tool that produces a code for current inspection and adapts specific nominal values and tolerances to check. With the default implementation, it uses the View's conditioned run code acquired, transforms this code into an index, load from a file the specification and tolerance values for this index, and uses these new settings for current inspection. Inspection consists in running specification checking of the results of an external tool CycleIndexSpecs tool accepts as a link.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |

| Tolerances and limits | |
| --- | --- |
| Index | Enables or disables check on current index (code) of the inspection. (default = Yes)<blockquote> **Specification**<br>expected code<br>  **tolerance -**<br>negative tolerance. (default = 10)<br>  **tolerance +**<br>positive tolerance. (default = 10)<br> </blockquote> |
| Spcifications | Enables or disables check on linked tool specification. Specification and tolerances reported are current index's values. (default = Yes)<blockquote> **Specification**<br>value at current index read from external file.<br>  **tolerance -**<br>negative tolerance at current index read from external file. (default = 10)<br>  **tolerance +**<br>positive tolerance at current index read from external file. (default = 10)<br> </blockquote> |

| Analysis | |
| --- | --- |
| Specification file | Path of external file containing specifications and tolerances for each index. The file as the following format: ;index spec tol- tol+ example: 1 1.1 1.2 1.3 2 2.1 2.2 2.3 |
| Result Id | It is the index of result of the linked tool. As tools can have several measurements or values into a single inspection result, this parameter select proper one. If the linked tool is a toolMeasure, the result iddrives the measure results. if the linked tool is a toolValue, the result Id drives the value results. |
| Test index | the index to use for manual testing of recipe. |
| View specifications | command to display external file with the index specifications. |

### More

Click [here](../../../Windows/dialog_settings.md) to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool. |
| Processing time | Tool processing time in msec. |
| Index | current index. |
| Specification | result value checked. |

Configuration
-------------

This tool is included into the library CycleIndexSpecs.

