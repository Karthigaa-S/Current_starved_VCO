<h1 align="center"> Current starved VCO</h1>
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
<img src="images/Screenshot 2024-11-03 102856.png">

# SPECIFICATIONS

| Parameter           | Symbol     | Typical Value |
| ------------------- | ---------- | ------------- |
| Technology          | -          | 180 nm        |
| Supply voltage      | VDD        | 1.8 V         |
| Control voltage     | VCTRL      | 0.9 V         |
| Temperature         | T          | 300 K         |
| Output frequency    | FOUT       | 961 MHz       |
| Power consumption   | -          | 50 uW        |

# PRE LAYOUT SIMULATIONS 
## SHEMATIC
The current starved VCO designed using esim and the screenshot of the design is:

 <img src="images/Screenshot 2024-11-03 101120.png">

 ## SIMULATED WAVES
After extracting the netlist and performing transient analysis of VCO @ ` vctrl=0.9V `
<h1 align="center"> Voltage vs Time @ VCTRL=0.9V</h1>
<br>


<img src="images/Screenshot 2024-11-03 093043.png">

The output frequency was found to be, ` FOUT= 961MHz `
It is calculated by measuring the time interval between two troughs or the crests and taking the inverse of the value measured.

<h1 align="center"> Current vs Time @ VCTRL=0.9V</h1>
<br>

<img src="images/Screenshot 2024-11-03 093155.png">

The power can be calculated from the simulated current values.

# TOOLS USED FOR SIMULATIONS

## eSim
eSim is a free, open-source electronic design automation (EDA) tool for circuit design, simulation, analysis, and PCB design. It's an alternative to commercial software like OrCAD, Xpedition, and HSPICE.
Esim can be downloaded from the website:

https://esim.fossee.in/downloads

## Ngspice

Ngspice is a free, open-source circuit simulator for electronic and electric circuits. 
Ngspice can be downloaded  from the website:

http://ngspice.sourceforge.net/download.html

### RUNNING THE SIMULATION

- After intalling eSim and Ngspice the circuit is designed in eSim and then the netlist is generated. 
- The `Sky130A Tech ` file in `Layout_Files` folder in this repository is downloades and placed it in current working directory.
- The spice file is generated and named as `vco.cir.out` and then simulated in Ngspice.

# FUTURE WORK

- Further optimisation to achieve a high frequency range.
- More advanced bulk-driven techniques to reduce power consumption.
- Linearity can be increased further.

# ACKNOWLEDGEMENT

 Kunal Ghosh, Co-Founder of VLSI System Design (VSD) Corp. Pvt. Ltd.
# AUTHOR 

 :pencil: KARTHIGAA S (B.E. ELECTRONICS AND COMMUNICATION ENGINEERING), MADRAS INSTITUTE OF TECHNOLOGY, ANNA UNIVERSITY, CHENNAI, TAMILNADU.
