# Arty-XADC <!-- Replace this line with the project name -->
Created for Vivado 2016.4

This simple XADC Demo project demonstrates a simple usage of Arty A7-35's XADC pin capability. The behavior is as follows:
  * The 8 User LEDs increment from top right to left then bottom left to right as the voltage difference on the selected XADC pins gets larger.
  * The four switches select which channel to read from.
  
In order to open the project in Vivado, follow the [Using Digilent Github Demo Projects Tutorial](https://reference.digilentinc.com/learn/programmable-logic/tutorials/github-demos/start). This is an HDL design project, and as such does not support Vivado SDK. Select the tutorial options appropriate for a Vivado-only design. The circuit to be measured does not need to be connected to the Arty A7 before it is programmed.

For this demo, A0-A5 are single ended analog pins while A6-A7, A8-A9, and A10-A11 are differential ports. Measured voltages should only be in the range of 0-1 Volt.

An XADC channel can be selected by changing the positions of the user switches as shown in the table below.

Channel | SW3  | SW2  | SW1  | SW0 
------- | ---- | ---- | ---- | ----
A0      | Down | Down | Down | Down
A1      | Down | Down | Down | Up  
A2      | Down | Down | Up   | Down
A3      | Down | Down | Up   | Up  
A4      | Down | Up   | Down | Down
A5      | Down | Up   | Down | Up  
A6-A7   | Down | Up   | Up   | Down
A8-A9   | Down | Up   | Up   | Up  
A10-A11 | Up   | Down | Down | Down

The LEDs turn on from right to left then wrap around the bottom as the input voltage of the selected channel increases. 