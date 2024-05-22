View
====

![](../../../../img/x_Graphics/Tools/UvfUIView-0.png)

Overview
--------

The View object is the container of all inspection items that use an image. It is responsible for the acquisition settings and all other processing operations as a global result, output, statistic, image reports, cycle run-time behavior. Every recipe must have at least a View object that defines acquisition, image processing sequence, run cycle mode, input-output interface, statistics report, etc. Several features depend on the View object.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Save golden image | Enables or disables saving of reference image into recipe (default = Yes) |
| Save measurements calibration image | Enables or disables saving of measurements calibration image into recipe. (default = No) |

| Camera | |
| --- | --- |
| Acquisition module | Acquiring device associated with this view. Every View must have a valid acquisition module to permit run-time processing. |
| Folder | Folder path containing images for the File virtual acquisition module. Acquisition acts returning a valid picture from a file in the selected folder. |
| Channel | The physical channel on the selected module. |
| Description | Description name of module. It needs to match the module name used in the configurazione file. |
| Contrast | Camera contrast. (default = 0.51; min = 0.00; max = 1.00) |
| Brightness | Camera brightness. (default = 0.51; min = 0.00; max = 1.00) |
| Exposure | Exposure time in ms. |
| Trigger | Sets the trigger mode.<ud> <li>None (default)<br>No trigger is required to start the acquisition.</li>  <li>Fast<br>Acquisition is driven by a hardware signal to the module.</li>  <li>Normal<br>Acquisition is driven by PROINSPECT watching the input line of the selected device.</li>  <li>Manual<br>Acquisition is driven manually by user.</li>  <li>Fast Software<br>Acquisition is driven by PROINSPECT internally on custom events.</li> </ud><blockquote> **Device**<br>Available devices for normal input trigger.<br>  **Normal trigger line**<br>Input device line to watch. (default = 1)<br>  **Manual trigger mode**<br>Keystroke <space> (default)      Trigger is fired by pressing <space> keyboard bar.(default)          Elapsed time      Periodically cycle time. Trigger is fired after interval elapsed time<br>  **Interval**<br>Periodic elapsed time. (default = 500)<br>  **Number of acquisition**<br>Number of cycles to do before stopping. Zero equals to infinite. (default = 0)<br> </blockquote> |
| Trigger polarity | Polarity of acquisition trigger .<ud> <li>Rising edge (default)<br>Acquisition starts on the rising edge of the trigger signal.</li>  <li>Falling edge<br>Acquisition starts on the falling edge of the trigger signal.</li> </ud> |
| Strobe | Enables or disables the strobe output. (default = Yes)<blockquote> **Strobe polarity**<br>Polarity of output strobe signal.<br>  **Strobe duration**<br>Strobe duration in ms.<br>  **Strobe lines**<br>Active strobe lines.<br> </blockquote> |
| Light control device | Device selection for output acquisition actions: when acquisition get armed PROINSPECT sets the light control lines to selected polarity status; when acquisition is completed PROINSPECT sets reversal polarity status.<blockquote> **Light control lines**<br>Output lines of device used in acquisition.<br>  **Light control polarity**<br>Active status of the light control lines.<br> </blockquote> |
| Number of lines | Number of lines to acquire. This parameter is meaningful for line scan cameras. (default = 1024) |
| Line exposure | Single line exposure time in ms. This parameter is meaningful for line scan cameras. (default = 0.20) |
| Line period | Line period in ms, if line trigger is disabled. This parameter is meaningful for line scan cameras. (default = 1.00) |
| Line trigger | Enables line trigger mode. This parameter is meaningful for line scan cameras. (default = Yes) |
| Encoder rate | Ratio between camera line triggers and encoder triggers. This parameter is meaningful for line scan cameras. (default = 1.00) |
| White balance red | Gain of red channel with respect to green. This parameter is meaningful for color cameras. (default = 0.50) |
| White balance blue | Gain of blue channel with respect to green. This parameter is meaningful for color cameras.  (default = 0.50) |

| More | |
| --- | --- |
| Tag | Generic label for object custom identification. |
| Show | Enables or disables visibility of the View object into the Selection for users not administrator |
| Description | Text field to give a brief tool description. |
| Comments | Text field to give a brief comments. |
| User Id | Unique GUID of this item. You can either edit it by clicking on the button. |
| Conditioned-Run Device | Input device to limit execution of groups of the view. PROINSPECT watches the selected lines of this device to create conditions that enable the execution of the internal groups.<blockquote> **Lines for Conditioned-Run**<br>Lines to watch<br>  **Conditioned-Run polarity**<br>polarity of input lines.            Active high (default)                 Active low       <br>  **Conditioned-Run mode**<br>I/O device code      Internal groups are executed only if their Conditioned-Run code equals the read status of selected input lines.          Incremental      Conditioned-Run code is automatically incremented. Value is reset on input line active status.<br> </blockquote> |
| Selectively hide objects | Enables or disables visibility of all view's objects set as conditionally hide for users not administrator. |
| Invert result decision | Invert inspection result: View result return fails it all owned items are pass and vice-versa. |
| Object sharing | Enable or disable saving of the configuration of the View in a separate binary files that can be shared over several recipes.<blockquote> **Shared file**<br>Path of the file (pvx extension)<br>  **Read only**<br>Enables or disables overwriting of the shared file during recipe saving.<br> </blockquote> |
| Parameters sharing | Enable or disable saving of the settings of the View in a separate files that can be shared over several recipes.<blockquote> **Shared file**<br>Path of the file (xml extension)<br>  **Read only**<br>Enables or disables overwriting of the shared file during recipe saving.<br> </blockquote> |

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail for all the tools in the view. If all tools will pass, the view will pass. A single tool fail will cause the view to fail. |
| Part Id | Inspection identification. |



