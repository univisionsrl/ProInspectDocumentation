Image Warp
==========

![](../../../../img/x_Graphics/Tools/UvfUIImageUnwrapTool-0.png)

Overview
---------------------

The Image Warp tool produces, as result, a warped image from multiple camera views and stitches them so that it can be used as reference image for other Groups or tools. Warping is given by a specific calibration that gives the transformation settings.

Settings
----------------

| Options | |
| --- | --- |
| Enable | Enables or disables the Image. (default = Yes) |
| Geometry | Shape that defines region to unwrap. |
| Inherit golden image | if enabled, the Input reference image for this Image tool is inherited by golden image: when View changes reference image, automatically the input image is updated and, in train, its result image. (default = No) |
| All image | Enables or disables region of interest for Image tool |


| Analysis | |
| --- | --- |
| Overlapping (deg) | defines how many pixels of image (width) to copy at the end of warped image. |
| Warping type | Warping algorithm<ud> <li>None<br>No warping</li>  <li>Cylindrical<br>Cylindrical calibration</li>  <li>Calibration2<br>Calibration of type 2</li> </ud> |
| Pre-Scale | Enables or disables the scale provided by selected fixturing tool. |
| Save pre-processing images | Save intermediate runtime image result. |


### More


Click [here](../../../Windows/dialog_settings.md) to access the More section description.


Images
------

| | |
| --- | --- |
| Reference image | Input reference image. |
| Preprocessing | Image processed result. |

