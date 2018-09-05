Arty A7-35T XADC Demo
==============
  
Description
--------------
This project is a Vivado demo using the Arty A7-35T analog-to-digital converter ciruitry,switches and LEDs, written in Verilog. When programmed onto the board, voltage levels between 0 and 1 Volt are read off of the JXADC header. The 6 User LEDs increment from top right to left then bottom right to left as the voltage difference on the selected XADC pins gets larger. A0-A5 are single ended analog pins while A6-A7, A8-A9, and A10-A11 are differential ports. Each XADC channel can be selected depending on the switches position as shown in the following table.  See the Arty A7-35T's [Reference Manual](https://reference.digilentinc.com/reference/programmable-logic/arty-a7/reference-manual) for more information about how the Artix 7 FPGA's XADC is connected to header JXADC.

| Channel Pin/s  | SW3    | SW2   | SW1   | SW0   |
| -------------- | -------| ------| ------| ------| 
| A0             | Down   | Down  | Down  | Down  |
| A1             | Down   | Down  | Down  | Up    |
| A2             | Down   | Down  | Up    | Down  |
| A3             | Down   | Down  | Up    | Up    |
| A4             | Down   | Up    | Down  | Down  |
| A5             | Down   | Up    | Down  | Up    |
| A6-A7          | Down   | Up    | Up    | Down  |
| A8-A9          | Down   | Up    | Up    | Up    |
| A10-A11        | Up     | Down  | Down  | Down  |
| V_P-V_N        | Up     | Down  | Down  | Up    |
  
Requirements
--------------
* **Arty A7-35T**: To purchase a Arty A7-35T, see the [Digilent Store](https://store.digilentinc.com/arty-a7-artix-7-fpga-development-board-for-makers-and-hobbyists/)
* **Vivado 2018.2 Installation**: To set up Vivado, see the [Installing Vivado and Digilent Board Files Tutorial](https://reference.digilentinc.com/vivado/installing-vivado/start).
* **MicroUSB Cable**
* **Wires and a Circuit to Measure**

Demo Setup
--------------
1. Download and extract the most recent release ZIP archive from this repository's [Releases Page](https://github.com/Digilent/Arty-A7-35-XADC/releases).
2. Open the project in Vivado 2018.2 by double clicking on the included XPR file found at "\<archive extracted location\>/vivado_proj/Arty-A7-35-XADC.xpr".
3. In the Flow Navigator panel on the left side of the Vivado window, click **Open Hardware Manager**.
4. Plug the Arty A7-35T into the computer using a MicroUSB cable.
5. In the green bar at the top of the window, click **Open target**. Select "Auto connect" from the drop down menu.
6. In the green bar at the top of the window, click **Program device**.
7. In the Program Device Wizard, enter "\<archive extracted location\>vivado_proj/Arty-A7-35-XADC.runs/impl_1/XADCdemo.bit" into the "Bitstream file" field. Then click **Program**.
8. The demo will now be programmed onto the Arty A7-35T. See the Introduction section of this README for a description of how this demo works.

Next Steps
--------------
This demo can be used as a basis for other projects, either by adding sources included in the demo's release to those projects, or by modifying the sources in the release project.

Check out the Arty A7-35T's [Resource Center](https://reference.digilentinc.com/reference/programmable-logic/arty-a7/start) to find more documentation, demos, and tutorials.

For technical support or questions, please post on the [Digilent Forum](https://forum.digilentinc.com).

Additional Notes
--------------
For more information on how this project is version controlled, refer to the [Digilent Vivado Scripts Repository](https://github.com/digilent/digilent-vivado-scripts)

