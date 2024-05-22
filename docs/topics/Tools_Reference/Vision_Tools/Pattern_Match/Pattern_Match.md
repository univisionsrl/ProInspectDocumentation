Pattern Match
=============



Overview
--------


The purpose of Pattern Match tools is to find patterns in run-time images and return position, a score of likeliness. Searching is performed in a user defined region. All these tools have a model or more than one model to search in images.


How it works
------------


You first define a shape that includes the model you want to search in images. All regions outside the model shape will have don't care pixels, i.e. pixels that don't have weight on the matching process. Then you train the model (or more models) in the reference image. If the operation successes, you are ready to run the tool on run-time images.



