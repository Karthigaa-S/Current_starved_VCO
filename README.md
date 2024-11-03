<h1 align="center"> Current_starved_VCO</h1>
This repository presents the design of an analog IP - VCO

It is a Current Starved Voltage Controlled Oscillator targerting 180nm tech for PLL based applications.
</br>
</br>
<img src="https://github.com/Karthigaa-S/Current_starved_VCO/blob/main/images/Linearized-current-starved-Voltage-Controlled-Oscillator.png">
# INTRODUCTION
A Voltage-Controlled Oscillator (VCO) is an electronic oscillator whose oscillation frequency is controlled by an input voltage. As the input control voltage changes, the output frequency varies proportionally, making VCOs essential in applications where frequency tuning is needed. VCOs are widely used in communication systems, such as phase-locked loops (PLLs), frequency synthesizers, and modulation circuits.
This Voltage-Controlled Oscillator (VCO) design is a hybrid current-starved ring oscillator with bulk-driven techniques for efficient low-power operation. The VCO circuit features three main stages:

Bias Stage: Controls the current fed into the oscillator stages based on the control voltage (V_ctrl), allowing frequency tuning.

Ring Oscillator Stages: Consist of a series of inverters that generate oscillations. The current-starved configuration, combined with bulk-driven transistors, minimizes power consumption while maintaining stable frequency output.

Buffer Inverters: These inverters drive the output, ensuring a clean signal at the Ring_Out node.

This structure allows for low-power, tunable frequency output, suitable for applications in low-power communication circuits.
# BLOCK DIAGRAM
