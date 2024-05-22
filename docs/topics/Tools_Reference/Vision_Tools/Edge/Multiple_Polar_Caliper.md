Multiple Polar Caliper
======================

![](../../../../img/x_Graphics/Tools/UvfCTStdUnwrapGridCaliper-0.png)

Overview
--------

The tool applies several Caliper tools along a circular shape tangentially and returns min , max, average and standard deviation of their sizes. User defines the polar region and the first caliper region.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Geometry | Defines tool's region shape.<ud> <li>Polar grid<br>Circular shape.</li> </ud> |

| Tolerances and limits | |
| --- | --- |
| Num of sectors | Number of sectors: defines the number of caliper tools to use(default = 1) |
| Size | Enables or disables check on size of each caliper size. <blockquote> **Specification**<br>Nominal value. (default = 10)<br>  **Tolerance+**<br>Positive tolerance value. (default = 10)<br>  **Tolerance-**<br>Negative tolerance value. (default = 10)<br> </blockquote> |

| Analysis | |
| --- | --- |
| Contrast threshold | The contrast above which a transition is considered an edge. (default = 20) |
| First edge polarity | The expected polarity of the first edge. <ud> <li>Dark to light<br>Transition from darker region to lighter one.</li>  <li>Light to dark<br>Transition from lighter region to darker one.</li>  <li>Don't care (default)<br>Any polarity.</li> </ud> |
| Second edge polarity | The expected polarity of the second edge. <ud> <li>Dark to light<br>Transition from darker region to lighter one.</li>  <li>Light to dark<br>Transition from lighter region to darker one.</li>  <li>Don't care (default)<br>Any polarity.</li> </ud> |
| Filter size | The filter width for edge extraction. (default = 2) |
| Contrast mode | Contrast is used to score edges.<ud> <li>Disabled<br>No contrast criteria is used.</li>  <li>Stronger contrast (default)<br>Stronger couple of edges get higher scores.</li>  <li>Weaker contrast<br>Weaker couple of edges get higher scores.</li> </ud><blockquote> **Expected contrast**<br>Expected value of contrast: edges with contrast close to this value will get the highest score. (default = 255.00)<br> </blockquote> |
| Position mode | Position is used to score edges.<ud> <li>Disabled (default)<br>No position criteria is used.</li>  <li>Centered position<br>The center of edge pairs closer to the center of the projection region gets higher scores.</li>  <li>Closer position<br>The center of edge pairs closer to the starting side of the projection region gets higher scores.</li>  <li>Farther position<br>The center of edge pairs further form the starting side of the projection region gets higher scores.</li> </ud> |
| Size mode | Size (distance between the edge pair) is used to score edges.<ud> <li>Disabled (default)<br>No size mode criteria is used.</li>  <li>Expected size<br>Edge pair size closer to expected gets higher scores.</li>  <li>Smaller<br>Edge pair size smaller than expected one gets higher scores.</li>  <li>Larger<br>Edge pair size larger than expected one gets higher scores.</li> </ud><blockquote> **Expected size**<br>Expected edge pair size, in pixel. This value is used for scoring only. (default = 0.00)<br> </blockquote> |

### More

Click [here](../../../Windows/dialog_settings.md) to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool. |
| Processing time | Tool processing time in msec. |
| Num of passed | Number of calipers with good result. |
| Min E1 contrast (point) | Minimum contrast of the first edge found transitions. |
| Mean E1 contrast | Average contrast of the first edge found transitions. |
| Max E1 contrast (point) | Maximum contrast of the first edge found transitions. |
| Min E2 contrast (point) | Minimum contrast of the second edge found transitions |
| Mean E2 contrast | Average contrast of the second edge found transitions. |
| Max E2 contrast (point) | Maximum contrast of the second edge found transitions. |
| Min size (point) | Minimum measured size. |
| Mean size | Average measured size. |
| Max size (point) | Minimum measured size. |
| Std. Dev. size | Standard deviation of all measured sizes. |

Configuration
-------------

This tool is included into the library UvfCTStd and UvfCTCvl.
