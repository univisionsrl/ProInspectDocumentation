Blob
====



Overview
--------


The simplest kinds of images that can be used for machine vision are simple two-dimensional shapes or blobs. Blob analysis is the detection and analysis of two-dimensional shapes within images.


Blob analysis can provide your application with information about the number, location, shape, and orientation of blobs within an image.


Since blob analysis is fundamentally an analysis process of the shape of a closed object, before blob analysis can be performed on an image, the image must be segmented into those pixels that make up the blob being analyzed, and those pixels that are part of the background.


How it works
------------


### Hard threshold


The simplest technique for segmenting an image is to pick a threshold pixel value. All pixels with grey-scale values below the threshold are assigned as object pixels, while all pixels with values above the threshold are assigned as background pixels. This technique is called binary thresholding or hard thresholding.


Object pixels are assigned a value of 1 while background pixels are assigned a value of 0.


### Soft threshold


Pixels with values above the threshold range are assigned weights of 0 (background), pixels with values below the threshold range are assigned weights of 1 (object), and pixels with values within the threshold range are assigned weights between 0 and 1, typically in a linear manner.


### Pre-Processing


Blob tools can be performed also on an processed images: a filter is applied to the blob's image roi before blob analysis.



