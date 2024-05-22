Color Match
===========


![](../../../../img/x_Graphics/Tools/UvfColorToolsStdMatch-0.png)


Overview
--------


The color match tool compares a region of color in a run-time image against a set of reference colors, and it generates a set of scores to indicate how closely the area of the run-time image matches each known color. The higher the comparison score, the greater the similarity. 


Settings
--------





| Options | |
| --- | --- |
| Enable | Enable or disable the tool. (default = Yes) |
| Geometry | Defines tool's region shape.<ud> <li>Circle<br>Circular shape.</li>  <li>General rectangle (default)<br>Rectangular shape.</li>  <li>Annulus<br>Annulus shape.</li>  <li>General polygon<br>General polygon shape.</li>  <li>Affine rectangle<br>Rectangular shape with rounded corners.</li> </ud> |
| Auto calibration | Automatically defines the reference color to match. (default = Yes) |

| Tolerances and limits | |
| --- | --- |
| Shape index | Minimum similarity for an acceptable result.<blockquote> **Shape index limit**<br>Minimum acceptable shape index. (default = 1.0)<br> </blockquote> |


### More


Click More... to access the More section description.


Results
-------


| Decision | Pass/Fail decision of a tool. |
| Score | A value ranging from 0 to 1 indicating the value of color distribution similarity. The highest is the score, the closer is the current color distribution to the one trained. |
| Processing time | Tool processing time in msec. |


Configuration
-------------


This tool is included into the library UvfColorToolsStd and UvfColorToolsCvl.



