Calibration
===========

Overview
--------

Calibration is the procedure that allows you to establish a relationship between two coordinate spaces.

A calibration tool creates a calibration object that relate locations in image space to locations in physical space. Some of calibration tools are of type Grid-of-Dots Calibration in which a calibration plate is used. Other calibration tools create transform mapping user defined points.

The transformation object created by the calibration tool is used to convert back and forth between physical and image space.

![](../../../img/x_Graphics/Calibration/03000001.png)

Calibration tool

Usage
-----

There are several calibration tools that you can use in PROINSPECT:
- Automatic Check Board Calibration
- Automatic Grid Calibration
- Axis Calibration
- Find Point Calibration
- Grid Calibration
- Grid Calibration 2
- Point Calibration
- Raw Calibration
- Z Calibration

Definitions
-----------

| | Description |
| - | - |
| Calibration | A procedure to create a transform that establishes the relationship between points in one coordinate space and corresponding points in another coordinate space. |
| Calibration plate | A precision manufactured flat plate used to calibrate image acquisition systems. |
| Linear transform | A transform defined by a (2x2) matrix and a (2x1) vector. |
| Markers | Pair of rectangles in the calibration plate. Point defined by the intersection of the lines drawn through the two rectangles can be used as an anchor point for the physical coordinate system. |
| Nonlinear transform | A transform created from a set of data points. The transformation varies depending on the data point you transform. It is not consistent over a range of points as is the case of a linear transform. |
| Physical coordinates | The physical space coordinate system. For example, the coordinate system used to locate points on a calibration plate. |
| Pitch | The x and y distance between elements in a calibration plate. |
| Residual error | The difference between the actual grid point locations and the locations predicted by applying the calibrated transformation to the known grid spacing. |
| Transformation object | An object containing functions that map points in one coordinate system to another coordinate system. For example, a mapping between image space and client coordinate space. The transformation can be linear or nonlinear. |



