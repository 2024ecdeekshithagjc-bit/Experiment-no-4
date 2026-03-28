# Experiment-no-4
OS Differential Amplifier Analysis
2a (First circuit )
## Aim
## Design and analyze a MOS differential amplifier for the following specifications:

VDD = 0.9 V
VSS = -0.9 V
Power (P) ≤ 2 mW
Input Common Mode Voltage (VinCM) = 0 V
Output Common Mode Voltage (VoCM) = 0 V
Threshold Voltage (Vp) = -0.7 V
## Introduction
A MOS Differential Amplifier is a fundamental building block in analog circuit design. It is widely used in operational amplifiers, comparators, and signal processing circuits.

The main function of a differential amplifier is to amplify the difference between two input signals while rejecting any signals that are common to both inputs (common-mode signals). This property is known as Common-Mode Rejection.

A typical MOS differential amplifier consists of:

Two matched MOSFETs (NMOS or PMOS)
A constant current source for biasing
Load elements (resistive or active loads)
Key Features
Amplifies differential input: Vout ∝ (Vin1 - Vin2)
High Common-Mode Rejection Ratio (CMRR)
Low power consumption (suitable for modern CMOS designs)
High gain and good linearity
## Circuit Diagram :
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/circuit%20diagram.png?raw=true)

## Design Considerations
Low Voltage Operation: With ±0.9 V supply, transistors must operate efficiently in limited headroom.
Power Constraint: Total current must be minimized to keep power ≤ 2 mW.
Symmetry: Ensures proper differential operation and zero output offset.
Biasing: Proper current source design is critical for stability.
Design Calculations for MOS Differential Amplifier

## Given Specifications
VDD = +0.9 V
VSS = -0.9 V
Maximum Power, P ≤ 2 mW
VinCM = 0 V
VoCM = 0 V
MOS Threshold Voltage, Vtp = -0.7 V
Differential Amplifier Calculation
Given:
 V_{DD} = 0.9,V 
 V_{SS} = -0.9,V 
Power P = 2mW 
 V_T = 0.36,V 
 V_{in,CM} = 0V, V_{out,CM} = 0V
## 1. Tail Current ( I_{SS} )
 P=(V_{DD} - V_{SS}) \cdot I_{SS} )

 2m = (0.9 - (-0.9)) \cdot I_{SS} 

 2*10^{-3} = 1.8 \cdot I_{SS} 

 I_{SS} = \frac{2 \times 10^{-3}}{1.8} = 1.11 \times 10^{-3} A = 1.11,mA 

## 2. Drain Currents
I_{D1} = I_{D2} = \frac{I_{SS}}{2} = 0.555,mA ]

## 3. Drain Resistance ( R_D )
 V_{out} = V_{DD} - I_D * R_D 

 0 = 0.9 - I_D* R_D 

R_D = \frac{0.9}{0.555 \times 10^{-3}} 

 R_D = 1636,\Omega \approx 1.636,k\Omega 

## 4. Region of Operation Check
 V_S = -0.7V\quad V_G = 0V 

 V_{OV} = V_{GS} - V_T = 0.34V 

V_{DS} = V_D - V_S = 0.7V 

V_{DS} > V_{OV} \Rightarrow 0.7 > 0.34 \quad \text

## 5. Width Calculation ( W )
 I_D = \frac{1}{2} \mu_n C_{ox} \frac{W}{L} (V_{OV})^2 

W = \frac{2 I_D L}{\mu_n C_{ox} (V_{OV})^2} 

 W = \frac{2 \times 0.555 \times 10^{-3} \times 360 \times 10^{-9}}{2.306 \times 10^{-4} \times (0.34)^2} 

 W \approx 14.88 \times 10^{-6} m = 14.88\mu m 

## 6. Input Common Mode Range (ICMR)
 V_{GS} \ge V_T 

 V_{GS} = V_{ICM} - V_S 

V_{ICM(min)} = V_S + V_T 

V_{ICM(min)} = -0.7 + 0.36 = -0.34,V 

## Final Results
 I_{SS} = 1.11,mA 
 I_D = 0.555,mA 
 R_D \approx 1.636,k\Omega 
 W \approx 14.88,\mu m 
 V_{ICM(min)} = -0.34,V 

## DC Operating Point :
![Image description]()


