# \# Analog Temperature Sensing Prototype



## Project Overview

This project is an \*\*Analog Temperature Sensing Breakout Board\*\* designed for Battery Management Systems (BMS). It utilizes an NTC Thermistor in a voltage divider topology to convert thermal changes into measurable analog voltage signals.



!\[3D PCB View](images/pcb\_3d.png)

!\[3D PCB View](images/pcb\_3d\_2.png)



## Technical Specifications

\- \*\*Input Voltage (VCC):\*\* 5V DC (typical)

\- \*\*Top Resistor (R1):\*\* 10kΩ Fixed (0805 SMD)

\- \*\*Bottom Resistor (TH1):\*\* 10kΩ NTC Thermistor (0805 SMD)

\- \*\*Output:\*\* Analog Voltage (Vout) via 2.54mm Header



!\[Schematic Diagram](images/schematic.png)



## Design \& Layout

The PCB was designed using \*\*LibrePCB\*\*. The layout is optimized for a small form factor while maintaining clear signal paths between the power source and the microcontroller interface.



## Simulation \& Verification

To verify the circuit's accuracy, I performed an \*\*Operating Point (.op)\*\* analysis using \*\*Ngspice\*\*. This step ensures the hardware logic matches the mathematical model before manufacturing.



!\[Ngspice Simulation Results](images/simulation\_result.png)



## Mathematical Model

The output voltage is calculated using the Voltage Divider formula:

$$V\_{out} = V\_{in} \\times \\frac{R\_{NTC}}{R\_1 + R\_{NTC}}$$



## Simulation Results (Ngspice)

\- \*\*Scenario 1 (Room Temp @ 25°C):\*\* $R\_{NTC} = 10k\\Omega \\rightarrow V\_{out} = 2.5V$

\- \*\*Scenario 2 (High Temp):\*\* $R\_{NTC} = 5k\\Omega \\rightarrow V\_{out} = 1.66V$



## Tools Used

\- \*\*LibrePCB:\*\* Schematic Capture \& PCB Layout

\- \*\*Ngspice:\*\* Circuit Simulation \& Verification

\- \*\*GitHub:\*\* Documentation and Version Control

