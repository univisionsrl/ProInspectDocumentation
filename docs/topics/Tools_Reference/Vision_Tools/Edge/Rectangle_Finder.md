Rectangle Finder
================

![](../../../../img/x_Graphics/Tools/UvfUIRect-0.png)

Overview
--------

The Rectangle finder tool lets you fit a set of points to a rectangle. It is the container of four Line Finder tools, one for each rectangle side. Found each line, the Rectangle tool computes the four vertexes, the center (as intersection of diagonals), width and height, and side parallelism/ orthogonality.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |

| Tolerances and limits | |
| --- | --- |
| Position offset | Enables or disables position tolerance. Specification position is the center of rectangle (intersection of diagonals).<blockquote> **Elliptical region**<br>Use an elliptical region area instead of a rectangular one. Position XY tolerances are the semi-axes the ellipse or the semi-size of rectangle.<br>  **Position X tolerance**<br>Position tolerance in the X axes. (default = 10)<br>  **Position Y tolerance**<br>Position tolerance in the Y axes. (default = 10)<br> </blockquote> |
| Angle offset | Enables or disables orientation tolerance limits. <blockquote> **Angle+**<br>Tolerance for positive angles. (default = 360; min = 0; max = 360)<br>  **Angle-**<br>Tolerance for negative angles. (default = 360; min = 0; max = 360)<br> </blockquote> |
| Height | Enables or disables the height tolerance limits.<blockquote> **Specification**<br>Expected height. (default = 0.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 0.00)<br>  **Tolerance-**<br>Negative tolerance. (default = 0.00)<br> </blockquote> |
| Width | Enables or disables the width tolerance limits.<blockquote> **Specification**<br>Expected width. (default = 0.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 0.00)<br>  **Tolerance-**<br>Negative tolerance. (default = 0.00)<br> </blockquote> |
| Diagonal | Enables or disables the diagonal tolerance limits.<blockquote> **Specification**<br>Expected diagonal length. (default = 0.00)<br>  **Tolerance+**<br>Positive tolerance. (default = 0.00)<br>  **Tolerance-**<br>Negative tolerance. (default = 0.00)<br> </blockquote> |
| Orthogonality | Enables or disables the orthogonality tolerance limits.<blockquote> **Tolerance+**<br>Positive tolerance. (default = 0.00)<br>  **Tolerance-**<br>Negative tolerance. (default = 0.00)<br> </blockquote> |

| Single Side | |
| --- | --- |
| Side | Each side of the rectangle is a LineFinder tool. Each LineFinder has its own settings: both tolerance limits and analysis. The selection of the side shows the desired LineFinder's setting <ud> <li>Top<br>Top side selected.</li>  <li>Right<br>Right side selected.</li>  <li>Bottom<br>Bottom side selected.</li>  <li>Left<br>Left side selected.</li> </ud> |

### Tolerances and Limits

For Tolerances and Limits please reference to selected single side. See Tolerances and limits.

### Analysis

For Analysis please reference to selected single side. See Analysis.

### More

Click [here](../../../Windows/dialog_settings.md) to access the More section description.

Results
-------

### Tool general results

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| Processing time | Tool processing time in msec. |
| Position X | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset between the tool's specification X position and tool's result X position (specification reference system).<br> </blockquote> |
| Position Y | Y position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset Y**<br>Offset between the tool's specification Y position and tool's result Y position (specification reference system).<br> </blockquote> |
| Offset length | Distance from the trained tool position. |
| Angle | Angle of the tool. Angle of the fit rectangle is the nominal angle + the angle of transformation that fits specification vertexes to result ones.<blockquote> **Angle offset**<br>Angle offset from the specification an result angle.<br> </blockquote> |
| Width AB | Size of AB side of the rectangle. ABCD are the result vertexes: A is left-top, B is right-top, C is right-bottom, D is left-bottom.<blockquote> **Difference with specification**<br>Difference between results and specification.<br> </blockquote> |
| Width BC | Size of BC side of the rectangle. ABCD are the result vertexes: A is left-top, B is right-top, C is right-bottom, D is left-bottom.<blockquote> **Difference with specification**<br>Difference between results and specification.<br> </blockquote> |
| Height BC | Size of BC side of the rectangle. ABCD are the result vertexes: A is left-top, B is right-top, C is right-bottom, D is left-bottom.<blockquote> **Difference with specification**<br>Difference between results and specification.<br> </blockquote> |
| Width CD | Size of CD side of the rectangle. ABCD are the result vertexes: A is left-top, B is right-top, C is right-bottom, D is left-bottom.<blockquote> **Difference with specification**<br>Difference between results and specification.<br> </blockquote> |
| Height DA | Size of CD side of the rectangle. ABCD are the result vertexes: A is left-top, B is right-top, C is right-bottom, D is left-bottom.<blockquote> **Difference with specification**<br>Difference between results and specification.<br> </blockquote> |
| Diagonal AC | Size of AC diagonal of the rectangle<blockquote> **Difference with specification**<br>Difference between results and specification.<br> </blockquote> |
| Diagonal BD | Size of BD diagonal of the rectangle. ABCD are the result vertexes: A is left-top, B is right-top, C is right-bottom, D is left-bottom.<blockquote> **Difference with specification**<br>Difference between results and specification.<br> </blockquote> |
| Angle DA^AB | Angle between DA and AB sides of the rectangle<blockquote> **Difference with specification**<br>Difference between results and specification.<br> </blockquote> |
| Angle AB^BC | Angle between AB and BC sides of the rectangle<blockquote> **Difference with specification**<br>Difference between results and specification.<br> </blockquote> |
| Angle BC^CD | Angle between BC and CD sides of the rectangle. ABCD are the result vertexes: A is left-top, B is right-top, C is right-bottom, D is left-bottom.<blockquote> **Difference with specification**<br>Difference between results and specification.<br> </blockquote> |
| Angle CD^DA | Angle between CD and DA sides of the rectangle. ABCD are the result vertexes: A is left-top, B is right-top, C is right-bottom, D is left-bottom.<blockquote> **Difference with specification**<br>Difference between results and specification.<br> </blockquote> |

### Single Side results

Reference to selected single side results. See Line Finder Results.

Configuration
-------------

This tool is included into the library UvfCvl.
