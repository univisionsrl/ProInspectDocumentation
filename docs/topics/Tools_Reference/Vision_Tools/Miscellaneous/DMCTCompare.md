DMCTCompare
===========

![](../../../../img/x_Graphics/Tools/CTDMCTCompare-0.png)

Overview
--------

The DMCTCompare tool allows to reference one (1) Data Matrix tool and several text (OCV or the future OCR) tools. In the settings it allows to specify a format string which combines single characters of the results of the text tools, given constant characters and wildcards into one string which must match the result of the Data matrix tool.

Formatted string bust be constructed with has the following rules (BNF):

~~~
<format string>::={<component>}
<component>::=<tool>|<tool characters>|<wildcard>|<alphanumeric>
<tool>::='%',<tool position>,'%'
<tool position>::=<number>
<number>::=digit, { digit }
<digit>::="0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"
<tool characters>::='%',<tool position>,':',{<character position>},'%'
<character position>::=<number>, ','
<wildcard>::='?'
<alphanumeric>::=?all visible characters?
~~~

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |

| Tolerances and limits | |
| --- | --- |
| Value | Enables or disables value.<blockquote> **Specification**<br>Formatted string.<br> </blockquote> |

### More

Click [here](../../../Windows/dialog_settings.md) to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool. |
| Processing time | Tool processing time in milliseconds. |
| Data Matrix code | Mata matrix read code. |
| Compare Code | Result code |
| Components | Select code component.<blockquote> **Code**<br>Component code.<br> </blockquote> |

Configuration

This tool is included into the library DMCTCompare.

