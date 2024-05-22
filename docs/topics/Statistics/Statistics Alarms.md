Statistics Alarms
=================

![](../../img/x_Graphics/Plugins/UvpPartIdAlarm.png)

Overview
--------

You can send alarms to an external device when the reject percentage value of a process reaches an alarm limit. The alarm limit applies to all the processes running. When any process reaches the alarm limit, the alarm is set.

Usage
-----

To set statistics alarms, open the Alarm dialog


	Tools > Recipe Options > Alarms

In the general section, there are limit values for the alarms.

| General | |
| --- | --- |
| Limit for too many rejects (%) | Reject percentage to activate the alarm (default = 3%) |
| Min. number of samples | Minimum number of parts when the limit for too many rejects is valid |

| I/O | |
| --- | --- |
| Device | Select the device to use to set the alarm. (default = None) |
| Alarm for too many reject | Enables or disables the alarm. (default = Yes) |
| Line | The line to set where the alarm is set |

Additional Device Operations
----------------------------

The same device I/O section can be used to:

- Reset the statistics: when the enable statistic reset line is set, the statistics are reset
- Disable the statistics update: when the enable update line is on, the statistics are updated

| I/O | |
| --- | --- |
| Enable statistic reset | Enables or disables the statistic reset. (default = No) |
| Line | The line to read to check if the statistic reset is set. |
| Enable update | Enables or disables the statistic update. (default = No) |
| Line | The line to read to check if the statistic reset is set |

Configuration
-------------

The alarm statistics options are available adding the UvpPartIdUIS plugin in the registry Plugins key.

The alarm statistics settings are saved in the ProInspect.cfg file.


