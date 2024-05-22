Geometry
========

![](../../img/x_Graphics/Plugins/UvpSettingsShape.png)

Overview
--------

Almost all the tools in PROINSPECT have a shape model to define the region of interest (ROI). The shape used to define these ROI can be driven with the tracker tool or directly specifying the features of the shape. All the value settings of this dialog are expressed in image units. There are only some tools that permits a setting in calibrated units. To access the dialog, select in the selector panel the desired tool, then show the Geometry Settings by the menu:

	View > Geometry.

The Tools, that have a model to look for, can provide the #Model geometry settings section.

Origin geometry settings
------------------------

The Tools that have an origin (usually expressed by a Cartesian axes shape) can provide this section.

### Origin

|  | Description |
| --- | --- |
| Name | Displays the name of the origin this section refers to. |
| Origin X | X coordinate of the origin. |
| Origin Y | Y coordinate of the origin. |
| Angle | Angle in degree of the origin. |
| Width | Length of the X axis. |
| Height | Length of the Y axis. |

Region geometry settings
------------------------

All Tools that implement an image processing can provide this section. The parameters listed in this section vary depending on the shape .

### Rectangle

|  | Description |
| --- | --- |
| Name | Displays the name of the shape this section refers to. |
| Upper left X | X coordinate of the upper left corner of rectangle. |
| Upper left Y | Y coordinate of the upper left corner of rectangle. |
| Width | Width of rectangle. |
| Height | Height of rectangle. |

### General Rectangle

|  | Description |
| --- | --- |
| Name | Displays the name of the shape this section refers to. |
| Calibrated data | Use the input data as calibrated units instead of image units. |
| Center X | X coordinate of the center of rectangle. |
| Center Y | Y coordinate of the center of rectangle. |
| Width | Width of rectangle. |
| Height | Height of rectangle. |
| Rotation | Orientation around the center of the rectangle. |

### Circle

|  | Description |
| --- | --- |
| Name | Displays the name of the shape this section refers to. |
| Calibrated data | Use the input data as calibrated units instead of image units. |
| Diameter | Diameter of the circle. |
| Center X | X coordinate of the center of circle. |
| Center Y | Y coordinate of the center of circle. |

### Annulus

|  | Description |
| --- | --- |
| Name | Displays the name of the shape this section refers to. |
| Center X | X coordinate of the center of circle. |
| Center Y | Y coordinate of the center of circle. |
| Inner radius | Internal radius. |
| Outer radius | External radius. |

### Annulus Section

|  | Description |
| --- | --- |
| Name | Displays the name of the shape this section refers to. |
| Center X | X coordinate of the center of circle. |
| Center Y | Y coordinate of the center of circle. |
| Inner radius | Internal radius |
| Outer radius | External radius |
| Start angle | Start angle of polar section. |
| End angle | End angle of polar section. If (end – start) equals 360 a full range is adopted. |

### General Polygon

|  | Description |
| --- | --- |
| Name | Displays the name of the shape this section refers to. |
| Edit mode | Selects the tracker Edit mode.   <ud><li> Vertex <br> The tracker shows handles at the vertices polygon shape. </li><li> New vertices <br> The tracker shows handles at the center of each side of the polygon and permits to fork it adding new vertices. </li><li> Rounding <br> The tracker shoes a circular handle at the vertices and in the middle of the polygon shape and permits to round a vertex or arch a side. </li><li> Delete vertex <br> The tracker deletes the selected vertex of the current shape. </li></ud>|
 Drag mode | Selects the tracker Drag mode.<br><ud><li> Translate <br> When dragged on a side the tracker translates. </li><li>Rotate <br> When dragged on a side the tracker rotates around its center. </li><li> Scale <br> When dragged on a side the tracker scale its sizes. </li></ud>|
| Origin X | X coordinate of the first vertex of the shape. |
| Origin Y | Y coordinate of the first vertex of the shape. |

### Thick Cross

|  | Description |
| --- | --- |
| Name | Displays the name of the shape this section refers to. |
| Calibrated data | Use the input data as calibrated units instead of image units. |
| Center X | X coordinate of the center of Cross. |
| Center Y | Y coordinate of the center of Cross. |
| Rotation | Orientation around the center of the Cross. |
| Thickness | Thickness of the body of the Cross. |
| Arm length | Length of each arm of the Cross. |

### CAD

|  | Description |
| --- | --- |
| Name | Displays the name of the shape this section refers to. |
| Origin X | X coordinate of the first vertex of the shape. |
| Origin Y | Y coordinate of the first vertex of the shape. |
| Angle | Orientation around the center of the bounding box rectangle of the CAD shape. |
| Width | Width of the boundign box rectangle of the CAD shape. |
| Height | Height of the boundign box rectangle of the CAD shape. |

### Circle Finder

It is a circle with several rectangle aligned on its circumference.

|  | Description |
| --- | --- |
| Name | Displays the name of the shape this section refers to. |
| Diameter | Diameter of the circle. |
| Center X | X coordinate of the center of circle. |
| Center Y | Y coordinate of the center of circle. |
| Start angle | Starting angle of first rectangle (deg). |
| Angle span | Angle range of all rectangles. |
| Width | Width of each rectangle. |
| Height | Height of each rectangle. |
| Arrange position mode | Position of each rectangle.   <br><ud><li>  Automatic <br> Each rectangle is spaced by an automatically computed angular step. </li><li>  Free <br> You can locate each rectangle at a desired angle. </li><li> Enable edge selection <br> Enables/disables selection of the single rectangle for manual setting by the tracker. </li></ud>|

### Line Finder

It is a line segment with several rectangle aligned on its perimeter.

|  | Description |
| --- | --- |
| Name | Displays the name of the shape this section refers to. |
| Diameter | Diameter of the circle. |
| X point 1 | X coordinate of the first point of segment. |
| Y point 1 | Y coordinate of the first point of segment. |
| X point 2 | X coordinate of the second point of segment. |
| Y point 2 | Y coordinate of the second point of segment. |
| First offset (%) | Percentage of the half-length of the segment to offset the first rectangle. |
| Second offset (%) | Percentage of the half-length of the segment to offset the last rectangle. |
| Mirrored by center | Offset are calculated starting from middle point of segment. |
| Width | Width of each rectangle. |
| Height | Height of each rectangle. |
| Arrange position mode | Position of each rectangle.   <br><ud><li> Automatic <br> Each rectangle is spaced by an automatically computed step. </li><li> Free <br> You can locate each rectangle at a desired position on the perimeter. </li><li> Enable edge selection <br> Enables/disables selection of the single rectangle for manual setting by the tracker. </li></ud>|

### Polar Grid

It is a Grid with sectors on a circular polar shape.

|  | Description |
| --- | --- |
| Name | Displays the name of the shape this section refers to. |
| Center X | X coordinate of the center of circle. |
| Center Y | Y coordinate of the center of circle. |
| Inner radius | Internal radius. |
| Outer radius | External radius. |
| Start angle | Start angle of polar section. |
| End angle | End angle of polar section. If (end – start) equal 360 a full range is adopted. |
| Angular search tol (deg) | How many degrees to enlarge internal sector (it is used for the width of the shape of internal tools). |
| Radial search tol (pixels) | How many pixels enlarge the internal sector. (it is used for height of the shape of internal tools). |

### Set of points

|  | Description |
| --- | --- |
| Name | Displays the name of the shape this section refers to. |
| Origin X | X coordinate of the point. |
| Origin Y | Y coordinate of the point. |
| Angle | Orientation of the point. |
| Options | TODO |
| Axes size | Size of the Axis identifying the point. |

### Grid

|  | Description |
| --- | --- |
| Name | Displays the name of the shape this section refers to. |
| Origin X | X coordinate of the center of the grid. |
| Origin Y | Y coordinate of the center of the grid. |
| Width | Width of the grid. |
| Height | Height of the grid |
| Rows | Number of rows of the grid. |
| Columns | Number of columns of the grid. |
| Gap X | Frame size of each cell in row direction of the grid. |
| Gap Y | Frame size of each cell in column direction of the grid. |

### Masks

Several tools provide use of masks to modify the inspection porpoise. When a mask is added to the tool a proper section is displayed in the Geometry setting dialog. In particular, there are the items to define the relationship between the mask and a run-time pre-alignment. The Mask’s shape is a General polygon: so this section shows also its settings as well.

|  | Description |
| --- | --- |
| Name | Displays the name of the mask this section refers to. |
| Fixed position | Tells the tool to not pre-align this mask. The mask is fixed in position as in train-time: it doesn’t follow tool’s pre-alignment. |
| Use fixture | Enables/disables the pre-alignment of this fixture with a proper external tool (different from shape owner’s tool). You have to select the external tool from the provided list.  <br><ud><li> <Fixture tool\> <br> Name of the external tool to use as pre-alignment fixture. </li></ud> |
| …TODO | General polygon items. |



