Online Setup
============


![](../../img/x_Graphics/Plugins/UvpMainAppMode.png)

When PROINSPECT is in Setup mode, you can do actions as acquire images, change the recipe definition, change tool parameters, Train the recipe, define how to communicate with external devices.  When PROINSPECT is in #Run mode there are a limited number of possible actions. These actions have an immediate effect on the running inspections: for example, changing a tool parameter, where possible, applies immediately to the next inspections.


Instead, you can use the Online Setup mode to do changes safely, test, and apply to the recipe when validated, without stopping the inspection cycle.


Usage
-----


The Online Setup mode is available only when PROINSPECT is in #Run mode. To enter Online Setup mode, select in the Selection panel the view you want to edit and press the Setup button . The Selection panel will show now only the selected view. This is a partial recipe copy to work with, without affecting the running inspection.


Some panels will continue to show data of the running inspections and others will show data of your changes. Here is some example:





| Panel name | Behaviour |
| --- | --- |
| Statistics | Run time data |
| Image history | Run time images |
| Main display | Setup image |
| Report | Setup results |
| Results | Setup results |


In this mode, you can do most of the operations you can do when PROINSPECT is in Online Setup mode. You cannot acquire images but you can load images from files or select them from the image history panel.


In this mode you can do all these operations without affecting the running inspection:


 - Train the tools
 - Change tools parameters
 - Test the recipe with different images
 - Do the tool statistic sampling
 - Validate the changes with the validation tool


When finished, you can apply the changes to the recipe pressing again the Setup button or you can discard the changes using the Setup-Undo Changes button.


Optionally you can edit the entire recipe un-checking the menu option Setup-Selected View.


Configuration
-------------


The Online Setup mode is available setting the ApplicationSetupMode in the registry Options\Process key.


Refer to the Options-PartId and UserInterface- UI PartId registry keys for configuration options.



