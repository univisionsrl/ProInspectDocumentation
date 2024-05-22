Batch
=====

![](../../img/x_Graphics/Plugins/UvpPartIdBatchManage.png)

Overview
--------

You can save the production statistics, measurement, and inspection results, for a specific range of time using the batch options. When you open a batch all the production statistics are reset, updated during the production, and saved in a report file when the batch is closed.

Usage
-----

To start a batch, open the batch dialog by menu:

	Batch > Batch Manager

or with the batch manager button in the batch toolbar. 

	View > Toolbars > Batch

You can fill the field in the Batch Manager dialog .

#### Batch Manager


| | |
|-|-|
| Batch code | Name of the batch; it will be used as the batch report name |
| Operator | Name of the operator opening the batch (optional) |
| Parts | Number of batch parts |

You can:

- Open a batch with the Open button. The batch manager button in the batch toolbar displays the batch name when a batch is open.
- Modify the opened batch settings with the Modify button
- Close the opened batch with the Close button. Closing the batch saves the batch statistics data in a file with the batch code name.

If you close PROINSPECT when a batch is opened, the batch data is saved and reloaded when reopening PROINSPECT. 

You cannot use the same batch name across different recipes.

If you set the batch mode as automatic, the batch manager dialog is opened automatically when you open a recipe.

Open the System Options window and select the Batch panel ![](../../img/x_Graphics/OPC-UA/03000001.png).

#### General

| | |
|-|-|
| Save CSV | Save the batch statistics data in a file with the batch code name when the batch is closed (default = Yes) |
| Automatic | The batch manager dialog is opened automatically when opening a recipe (default = No) |

### Statistics Panels with Batch

The statistics panels show statistics data that is:

- Current statistics, if no batch is opened
- Current statistics or batch statistics, if a batch is opened.

### Reset Statistics

![](../../img/x_Graphics/Plugins/UvpPartIdStatisticsReset.png)

The command resets the current statistics. This will no reset the batch statistics.

### Batch Statistics

![](../../img/x_Graphics/Plugins/UvpPartIdBatchStats.png)

You can toggle between current statistics and batch statistics with the context menu command.

### Run Panel with Batch

When a batch is opened, the Run panel shows always the batch selected statistics data in the table and therefore are not reset with the Reset Statistics command.

### Batch Alarms

A device can set an alarm line when the batch reaches the number of parts set. 

Open the System Options window and select the Batch panel ![](../../img/x_Graphics/OPC-UA/03000001.png).

#### I/O

| | |
|-|-|
| Device | Select the device to use to set the alarm. (default = None) |
| Completion | Enables or disables the alarm. (default = Yes) |
| Line | The line to set where the alarm is set |
| Polarity | The polarity of the alarm (default = Active high) |

### Additional Operations

With the menu command

	Batch > Save Batch Data

you can save anytime the batch statistics data in a file.

Configuration
-------------

The statistics are available adding the UvpPartIdBatchUIS plugin in the registry Plugins key.

Refer to the UserInterface-UI PartIdBatch registry keys for configuration options.
