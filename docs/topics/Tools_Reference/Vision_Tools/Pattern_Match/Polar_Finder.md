Polar Finder
============

![](../../../../img/x_Graphics/Tools/UvfCTStdUnwrapFinder-0.png)

Overview
--------

Polar Finder lets you search inside an annulus region. A tool must be associated to the Polar Finder and it will be executed in the region defined by the annulus. For example, it is possible to associate a PatMax, Search or Caliper tool and get the result of the tool applied to a region obtained unwrapping the annulus. Polar Finder unwrap the image region within the polar shape and run contained tool into this unwrapped image. It returns, in particular, the angle where the contained tool finds its own model or edge.


Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Geometry | Defines tool region shape.<ud> <li>Polar grid<br>Annulus shape.</li> </ud> |

| Tolerances and limits | |
| --- | --- |
| Overlapping (degree) | Defines an overlapping region made of pixels taken from the beginning and the end of the unwrapped image. (default = 0) |
| Scale X | X scale factor for scaling the unwrapped image. (default = 1.00) |
| Scale Y | Y scale factor for scaling the unwrapped image. (default = 1.00) |
| Angle offset | Enables or disables orientation tolerance. (default = No)<blockquote> **Angle+**<br>Tolerance for positive angles. (default = 360; min = 0; max = 360)<br>  **Angle-**<br>Tolerance for negative angles. (default = 360; min = 0; max = 360)<br> </blockquote> |

### More

Click [here](../../../Windows/dialog_settings.md) to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| Processing time | Tool processing time in msec. |
| Position X | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset between the tool's specification X position and tool's result X position (specification reference system).<br> </blockquote> |
| Position Y | Y position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset Y**<br>Offset between the tool's specification Y position and tool's result Y position (specification reference system).<br> </blockquote> |
| Offset length | Distance between specification and result points. |
| Angle | Angle where the contained tool finds its result.<blockquote> **Angle offset**<br>Angle offset from the trained tool angle position.<br> </blockquote> |

Images
------

| Images | |
| --- | --- |
| Model | unwrapped image of the polar shape reference image region. |
| Mask | run-time unwrapped image. |

Configuration
-------------

This tool is included into the library UvfCTStd and UvfCTCvl.
