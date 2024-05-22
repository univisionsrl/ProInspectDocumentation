OCV
===

![](../../../../img/x_Graphics/Tools/UvfIdToolsStdOcv-0.png)

Overview
--------

The OCV tool performs optical character verification (OCV), a process for verifying that each character in a text area is the expected character in the expected location.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enable or disable the tool. (default = Yes) |

| Tolerances and limits | |
| --- | --- |
| Value | If this value is not set, result always good. (default = Yes)<blockquote> **Specification**<br>Set line of characters to verify. This string will be used for train process too. (default = "ABC")<br> </blockquote> |
| Numbers | Enable or disable numbers. (default = Yes)<blockquote> **available numbers**<br>Type available numbers. (default = "0123456789")<br> </blockquote> |
| Uppercases | Enable or disable uppercase. (default = Yes)<blockquote> **available uppercases**<br>Type available uppercase characters. (default = "ABCDEFGHIJKLMNOPQRSTUVWXYZ")<br> </blockquote> |
| Lowercases | Enable or disable lowercases. (default = Yes)<blockquote> **available lowercases**<br>Type available lowercase characters. (default = "abcdefghijklmnopqrstuvwxyz")<br> </blockquote> |
| Other characters | Enable or disable other characters. (default = Yes)<blockquote> **other characters**<br>Type characters.<br> </blockquote> |
| Wildcards | Formatted string that specify if in the recognized text some characters have to assume a specific value. Sintax in BNF form is the following: <wild text>::={<position>:{<character>};} <position>::=[0-9]+ <character>::=[A-Za-z0-9]\ If <character> is empty means that the applied rule for the corresponding <position> is the same as the previous <position> one. |
| Shape index limit | Enable shape index limit. Matching score is evaluated for each character. The decision is taken by comparing the lowest score value of all accepted characters to this limit. (default = Yes)<blockquote> **shape index limit**<br>(default = 1.0)<br> </blockquote> |

| Analysis | |
| --- | --- |
| Font filename | Path of Font file containing the font to be used in verification process. |
| Font name | Font file usually contains different fonts. All available fonts will be listed. Select the desired one.<ud> <li>-Not selected-<br>No font is selected. (default)</li>  <li><available font#><br>Available font</li> </ud> |
| Edge polarity | Text polarity.<ud> <li>Dark to light<br>Dark text on light background. (default)</li>  <li>Light to dark<br>Light text on dark background</li> </ud> |
| Acceptance threshold | Sets the threshold used to locate character shapes in the run-time image. (default value = 0.6) |
| Contrast threshold | Gets the amount of contrast (in run-time image grey levels) that a result must have to be accepted. (default = 10.0) |
| Uncertainty X (pixel) | Sets the uncertainty of the starting pose in the x dimensions, in client coordinates. (default = 7.0) |
| Uncertainty Y (pixel) | Sets the uncertainty of the starting pose in the y dimensions, in client coordinates. (default = 7.0) |
| Angle | The search will be performed in the given angular range. Otherwise, it will use the single nominal value. (default = Yes)   | angle min. | Lower limit for angular range. (default = -5.0) | | --- | --- | | angle max. | Upper limit for angular range. (default = 5.0) | |
| Scale | The search will be performed for the given scale range. Otherwise, it will use the single nominal value.<ud> <li>None<br>No scale in applied. (default)</li>  <li>Symmetric<br>Uniform scale for X and Y.</li>  <li>Only X<br>Scale for X.</li>  <li>Only Y<br>Scale for Y.</li> </ud>    | min. | Lower limit for scale range. (default = 0.0) | | --- | --- | | max. | Upper limit for scale range. (default = 0.0) | |

### More

Click [here](../../../Windows/dialog_settings.md) to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool. |
| Processing time | Tool processing time in msec. |
| Read code | Display read code. Not matching characters are displayed as "\". |
| Score | Lowest score (matching) value for all recognized characters. Characters are "recognized" when the score value is greater then acceptance threshold. Not recognized characters do not change the score value. |

Configuration
-------------

This tool is included into the library UvfIdToolsStd and UvfIdToolsCvl.
