Settings
========


![](../../img/x_Graphics/Plugins/UvpSettingsSettings.png)


Overview
--------


This dialog can be accessed by menu


	View > Settings


Settings
--------


Settings dialog contains parameters for the selected object.


Parameters can be divided into some main categories.


### Options


Set how the tool is constructed (search area, model, ...).


An enable check allows you to logically exclude the tool from the recipe. Not enabled tools are not processed.


### Tolerances and Limits


Set constrains on measured values.


Algorithm specific parameters.


### More...


Mainly relates to how the object relates to others. All PROINSPECT items have the save more section parameters.





| More | |
| --- | --- |
| Tag | Generic tag for object identification. |
| Show | If unchecked, the object is showed for higher user levels only. |
| Conditionally hide | If checked, the object is hidden if its view has Hide tagged objects checked. |
| Adjust model | If checked, when the tool is in training mode, its shape can be fitted to the training image by making a run of the tool on the training image. |
| Description | Text field that user might use to give a brief tool description. |
| Comments | Text field that user might use to give a brief comments. |
| User Id | GUID field that user might use to identify the item. User can either edit this field or, by clicking on the button get a proposed GUID. |
| Invert result decision | If checked the inspection result is inverted: reject becomes good; good becomes reject. |
| Object sharing | Object can individually be stored on file (pvx) and the same file used to set parameters of another object.<blockquote> **Shared file**<br>Path of the shared pvx file.<br>  **Read only**<br>Object will not overwrite the shared file during saving action.<br> </blockquote> |
| Parameters sharing | Object parameters can be stored on file (xml) and the same file used to set parameters of another object.<blockquote> **Shared file**<br>Path of the shared xml file.<br>  **Read only**<br>Object will not overwrite the shared file during saving action.<br> </blockquote> |


#### Hide object


Want to share calibration objects over several recipes. We also have a separate calibration recipe where we do the calibration. In the type recipes, made to inspect the parts, it should not be possible to see the calibration object. So we use this option to hide the calibration objects in the type recipes. The calibration objects should only be visible in the calibration recipe. The calibration object will have its Hide object parameter set to true. The calibration view will have its Hide tagged objects parameter set to false and the part inspection view will have its Hide tagged objectsparameter set to true.



