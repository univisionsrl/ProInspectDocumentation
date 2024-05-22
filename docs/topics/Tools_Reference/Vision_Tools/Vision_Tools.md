Vision Tools
============



Overview
--------


Vision tools are usually stand alone tools (means not composite) that perform processing on the assigned image. 


A tool must always reside into one view. Usually the image they process is the one associated to the view they belong to.


How it works
------------


### Settings


A tool can be personalized setting some parameters. User usually specifies the shape of the ROI (region of interest) inside the image in which to perform the processing. Other parameters are tool specific.


Conditions on results acceptance can be specified , such as range of values ​​that can be taken from the results, number of results,...


### Train


Before using a tool it must be trained. The term Training refers to acquisition of parameters values by the tool. This operation may fail, in which case the tool cannot be run.


### Run


After a successful train operation, a tool can be run. Run means processing of the image with the algorithm provided by the tool and the given parameters values.


Run can result into the following values




| Good | Processing was successfully completed and the results satisfy the conditions set by the user. |
| --- | --- |
| Reject | Processing was unsuccessfully completed. |
| Out of tolerance | Processing was successfully completed but the results do not satisfy the conditions set by the user. |
| Not run | Processing has not occurred. |



