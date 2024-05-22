PatInspect
==========

![](../../../../img/x_Graphics/Tools/UvfUIGpmInspect-0.png)

Overview
--------

The purpose of PatInspect is to locate an object using the PatMax algorithm and to detect defects on its surface. PatInspect creates the template image of an object from a set of training images and then compares run-time images of the object against the template image trained statistically. A defect is any region that differs from model more than an expected tolerated variation given by the training images set. A defect can be a dark or bright spot on an object, an incorrectly shaped feature, or the absence of a shape. Basically, PatInspect aligns image, computes difference with threshold image, applies some morphology filtering, and runs blob analysis.

Settings
--------

| Options | |
| --- | --- |
| Enable | Enables or disables the tool. (default = Yes) |
| Search area | Selects the area where the tool searches for the model.<ud> <li>All image (default)<br>Search area is all the image.</li>  <li>Centered<br>Search area is positioned to the nominal position of the tool.</li>  <li>Free<br>Search area position is defined by the user.</li> </ud> If Search area is Centered the search area will be set as the minimum rectangle enclosing the model plus a surrounding frame:<blockquote> **Frame X (pixel)**<br>Frame width.<br>  **Frame Y (pixel)**<br>Frame height.<br> </blockquote> |
| Model | Defines tool model shape.<ud> <li>Circle<br>Circular shape.</li>  <li>General rectangle (default)<br>Rectangular shape.</li>  <li>Annulus<br>Annulus shape.</li>  <li>General polygon<br>General polygon shape.</li> </ud> |
| User origin | Allows to set the model origin in an arbitrary position, instead of the center of the model area. |

| Tolerances and limits | |
| --- | --- |
| Check results count | Enables or disables results count condition.<ud> <li>None<br>not enabled.</li>  <li>Less than<br>Decision positive if number of found items is less than the defined value.</li>  <li>Greater than<br>Decision positive if number of found items is greater than the defined value.</li>  <li>Expected number<br>Decision positive if number of found items is equal to the defined value.</li> </ud><blockquote> **Number of results to find**<br>User defined value for results count.<br> </blockquote> |
| Shape index | Conformity limit for acceptable result.<blockquote> **Shape index limit**<br>Minimum acceptable shape index. (default = 1.0)<br> </blockquote> |
| Position offset | Enables or disables position tolerance.<blockquote> **Elliptical region**<br>Instead of rectangular offset area a elliptical is used<br>  **Position X tolerance**<br>Position tolerance in the X axes. (default = 10)<br>  **Position Y tolerance**<br>Position tolerance in the Y axes. (default = 10)<br> </blockquote> |
| Angle offset | Enables or disables orientation tolerance.<blockquote> **Angle+**<br>Tolerance for positive angles. (default = 360; min = 0; max = 360)<br>  **Angle-**<br>Tolerance for negative angles. (default = 360; min = 0; max = 360)<br> </blockquote> |
| Min area | Area must be greater than this limit to be recognized as blob. (default = 0) |
| Blobs number | Enables or disables Blob number limit. <blockquote> **max. Blob number**<br>Maximum number of blobs to be found. (default = 0)<br>  **minor defects**<br>Includes minor defects to evaluation and therefore result.(default = No)<br> </blockquote> |
| Single Blob area | Enables or disables Single Blob area limit.<blockquote> **single blob area limit**<br>Maximum area for a single blob. (default = 100)<br>  **minor defects**<br>Includes minor defects to evaluation and therefore result.(default = No)<br> </blockquote> |
| Sum of all Blobs area | Enables or disables Sum of all Blobs area.<blockquote> **sum of all Blobs area limit**<br>Maximum value for the sum of the blobs' areas. (default = 500)<br>  **minor defects**<br>Includes minor defects to evaluation and therefore result.(default = No)<br> </blockquote> |
| Sum of all Blobs area (%) | Enables or disables Sum of all Blobs area as percentage of ROI.<blockquote> **All Blobs area limit**<br>Maximum value for the sum of the blobs' areas. (default = 0)<br>  **minor defects**<br>Includes minor defects to evaluation and therefore result.(default = No)<br> </blockquote> |

| Analysis | |
| --- | --- |
| Acceptance threshold | The acceptance level for the global matching score. Results with scores below this limit are not accepted. |
| Contrast threshold | Minimum contrast of boundaries used to locate the pattern. |
| Elasticity | It specifies the degree to which you will allow PatMax to tolerate deformations of the object boundaries. You specify the elasticity value in pixels. (default = 0.00) |
| Score using clutter | When this option is enabled, the system takes into account the clutter (presence of extra contours in the image that were not present in the model) in computing the global score. (default = Yes) |
| Angle | Enables or disables angle search range. (default = Yes)<blockquote> **Angle min**<br>Lower limit. (default = -30)<br>  **Angle max**<br>Upper limit. (default = 30)<br> </blockquote> |
| Scale | Enables or disables scale range. (default = No)<ud> <li>None<br>Not enabled.</li>  <li>Simmetric<br>Tolerates scale variations for X and Y directions.</li>  <li>Only X<br>Tolerates scale variations only for X direction.</li>  <li>Only Y<br>Tolerates scale variations only for Y direction.</li> </ud><blockquote> **Min**<br>Lower limit. (default =0)<br>  **Max**<br>Upper limit. (default = 0)<br> </blockquote> |
| Ignore polarity | Tool will ignore the polarity of the features to find in reference to the model. (default = No) |
| Pattern granularity | PatMax uses large features first to do a pre-localization of the object and then refines the search using fine features. Granularity is expressed as the radius of interest, in pixels, within which features are detected.<ud> <li>Automatic (default)<br>The system perform, at train time, an estimate of the optimal settings for Fine and Coarse granularity.</li>  <li>Manual<br>Fine and coarse granularity are used to train the pattern.</li> </ud><blockquote> **Fine**<br>The smallest granularity used to detect features in the training image or shape description. (default = 1)<br>  **Coarse**<br>The largest granularity used to detect features. (default = 4)<br> </blockquote> |
| Accepted overlap (%) | Percentage overlapping area needed to PatMax before it treats multiple overlapping instances as a single instance. |
| Angle overlap | Angle within which PatMax treats multiple overlapping instances as a single instance. |
| Intensity sensitivity | This parameter represents an index of the sensitivity of the tool to variations of brightness. The higher the value the smaller will be the intensity difference considered as a defect. (default = 25)<blockquote> **Proportional**<br>Scaling factor for the sensitivity function. (default = 13.80)<br>  **Constant**<br>Offset level for the sensitivity function. (default = 25.60)<br> </blockquote> |
| Dimension sensitivity | This parameter represents an index of the sensitivity of the tool to the area of defects. The higher the value the smaller will be the area of a region considered as a defect. (default = 25)<blockquote> **Area min. (pixel)**<br>Minimum area that can be considered as a defect. (default = 75)<br> </blockquote> |
| Sobel image | Enables or disables results count condition.<ud> <li>None<br>Do not use</li>  <li>Add image to samples<br>Apply sobel operation on mean image to enlarge template image on edges</li> </ud><blockquote> **Magnitude scaling factor**<br>The computed edge magnitude for each pixel is multiplied by magScale before being placed in the edge magnitude image.<br>  **Magnitude threshold**<br>Only sobel magnitude values greater than this value are taken into account (after having been multiplied by magScale).<br> </blockquote> |
| Use train image as sample | Includes the train image in the sampling. (default = No) |
| Use custom samples | Uses saved images for the sampling. (default = No)<blockquote> **Samples folder**<br>Specifies the folder containing sample images to use.<br> </blockquote> |

### More

Click More... to access the More section description.

Results
-------

| Results | |
| --- | --- |
| Decision | Pass/Fail decision of a tool, including multiple results if any. |
| Processing time | Tool processing time in msec. |
| Position X | X position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset X**<br>Offset from the trained tool position in the X axes.<br> </blockquote> |
| Position Y | Y position coordinates. The position is referred to the origin point of the tool.<blockquote> **Offset Y**<br>Offset from the trained tool position in the Y axes.<br> </blockquote> |
| Offset length | Distance from the trained tool position. |
| Angle | Angle of the tool.<blockquote> **Angle offset**<br>Angle offset from the trained tool angle position.<br> </blockquote> |
| Score | Match quality index. A value from 0 to 1 indicating the global level of conformity between the model and the pattern found. Refers only to the localization part of the tool. |
| Max blobs number | Found blobs count. |
| Total area (pixel) | Sum of the areas of all found blobs, in pixel. |
| Sum of all Blobs area (%) | Sum of the areas of all found blobs, in %. |
| Max. area (pixel) | Greatest area of all found blobs, in pixel. |
| Min. area (pixel) | Smallest area of all found blobs, in pixel. |
| Result | Select the index of the blob to show information about.<blockquote> **Area**<br>Area of the selected blob, in pixel.<br>  **Center X**<br>Position X of the center of mass of the selected blob.<br>  **Center Y**<br>Position Y of the center of mass of the selected blob.<br> </blockquote> |

Images
------

| Images | |
| --- | --- |
| Inspected | Runtime image |
| Threshold image | Threashold Image result of statistical training. Every pixel value of the image is the threshold of the difference between run-time image and template image. Sensitivity modifies this theshold. |
| Model features | Show features of the model |
| Difference | Difference image between runtime minus template and threshold image. |
| Model | Template image. |
| Sobel | Sobel image. |
| Mask | Mask image: care pixles are white; don't care pixels are black. |

Configuration
-------------

This tool is included into the library UvfCvl.
