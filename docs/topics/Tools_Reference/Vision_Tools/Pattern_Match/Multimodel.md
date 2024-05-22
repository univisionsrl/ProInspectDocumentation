Multimodel
==========



Overview
--------


This dialog is accessed by [Search](Search.htm) and [PatMax](PatMax.htm) settings dialog Analysis > Multi model > Edit model.


Multimodel
----------


### Consoles


Search and PatMax tools can have different models to work to, and the tool result is done by the model that gives the best result.


Multimodel dialog has two image consoles:


- Image console Shows the image the model is extracted from.
- Models console Shows all defined models. Current model can be selected in this console.


The first time this dialog is entered, the default model is shown in both consoles. If other models will be added, their search area and model area will be displayed in the image console, whereas the model image will be displayed in the models console.


Each console has a text field in its lower part that displays the coordinate of the mouse pointer when the mouse enters the console area.


### Reference image


Reference image is the image the model is extracted from.


- Reference image name This text field shows the path of the image the currently selected model is extracted from. Each model has its own reference image.
- Load ref. Displays an Open File dialog to select the current model's reference image. This button is active when the current model is in Edit mode.
- Cur. image Selects the current image as the current model's reference image. Always enabled.


### Edit


Edit commands are to modify, add and delete models.


- Edit Pressing this button current model can be edited. In the Image console its search area and model area can be modified. Its reference image can be changed. To exit edit mode and confirm changes press this button again.
- Add mode A new model is created.
- Delete model Currently selected model is removed.
- Cancel Exits the edit mode skipping changes.
- Lock User can to change current model search area and/or model position leaving the model's image unchanged


### Archive


Model can be archived and used to initialize other models.


- Load Shows an Open file dialog to select a .mod file that will initializes current model.
- Save Open a Save file dialog to save the current model to a .mod file.



