Compute tool XML Configuration
==============================



Overview
--------


This window is accessed by pressing Config XML button in Compute settings window


Configuration
-------------


### Editor

| | |
| - | - |
|  | User can describe the features of compute tool through a XML language. |
| Computation Name | Define the user frendly name of this configuration. |
| Define | Starts the section for operands definitions. |
| Operand Name | Name of the Operand (position, measure, value, status) used in the computational script. This name is operand symbol ComputeTool uses in the script formula. |
| Result Name | Description of operand. This is the data source associated with its Operand name. Usually you get desired value by <Name of the tool in the recipe>.<one of the foolowing>   | Position.X.1 | Position X result of 1st position result of the named tool. (Position 1 in the case) | | --- | --- | | Position.Y.1 | Position Y result of 1st position result of the named tool. (Position 1 in the case) | | Position.A.1 | Angle result of 1st position result of the named tool. (Position 1 in the case) | | Measure.1 | Measure result of 1st result of the named tool. (Measure 1 in the case) | | Value.1 | Value result of 1st result of the named tool. (Value 1 in the case) | |
| ResultNum | Get as named operand 1st result of the i-th child of the named tool. |
| Results | Starts the section for Compute tool results definitions. Every result (General, Position, Value...) is the result of a computational script. Script may accept Operands (as described), values, mathematical functions. |
| General | Definition of result status General (pass == 0, reject != 0). This value is the result of the script execution. |
| PositionX, PositionY, PositionA | Definition of result position (X, Y, Angle) of the Compute tool. These values are the results of the scripts execution. |
| Measure | Definition of result Measure of the Compute tool. This value is the result of the script execution. |
| Value | Definition of result Value of the Compute tool. This value is the result of the script execution. |


### Import XML


Import a XML definition for this ComputTool from a stored file.


### Export XML


Export current XML definition of this ComputTool to a file.


### Verify XML


Verify correctness of Operands and Results. This action is neccessary to accept new ComputeTool definition.


Example

~~~
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<Computation Name="Hole">
<Define>
<Operand Name="PosX">
<ResultName>Locate Holes.PositionX</ResultName>
</Operand>
<Operand Name="PosY">
<ResultName>Locate Holes.PositionY</ResultName>
</Operand>
<Operand Name="PosA">
<ResultName>Locate Holes.PositionA</ResultName>
</Operand>
<Operand Name="Bot">
<ResultName>Bottom.Value.0</ResultName>
</Operand>
<Operand Name="Top">
<ResultName>Top.Value.0</ResultName>
</Operand>
</Define>
<Results>
<PositionX Name="Pos">PosX-200</PositionX>
<PositionY Name="Pos">PosY</PositionY>
<PositionA Name="Pos">PosA</PositionA>
<Value Name="Val0">(Top-Bot)\0.022</Value>
</Results>
</Computation>
~~~

where:


___Locate Holes___ is the name of tool in the recipe the Compute tool uses position x, y and angle. Compute X position result will have an offset of 200 from original result.


Compute tool value is the computed result from two operands (the first value of the result of the recipe tools ___Bot___ and ___Top___ and a simple value 0.02.



