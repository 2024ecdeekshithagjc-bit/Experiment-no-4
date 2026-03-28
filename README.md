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
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/operating%20point%201.png?raw=true)

## Transient analysis:
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/Transient_analysis1.png?raw=true)

## AC analysis :
## a) first output waveform:
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/output%20waveform%201.png?raw=true)
## b)second output waveform:
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/output%20waveform%202.png?raw=true)
## DC sweep:
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/DC_sweep1.png?raw=true)

## Step 1: Total Current Calculation
P = (VDD - VSS) \ Itotal 2 × 10⁻³ = (0.9 - (-0.9)) \ Itotal

2 × 10⁻³ = 1.8 \ Itotal

Itotal = {2 × 10⁻³} \ {1.8} = 1.11 mA

So, tail current: I_{tail} = 1.11 mA

Each transistor carries:

I_D = {I_{tail}}{2} = 0.555 { mA}

To Check M3 is in saturation :
VDS3 = Vp -VSS VDS3 = -0.7V + 0.9V = 0.2V

VGS3 -Vth <= 0.2 VinCM-max = Vp + VGS1 VGS1 = 0.7V, Vth = 0.7V VinCM-max = 0V

Transconductance (gm)
 g_m = \frac{2I_D}{V_{OV}} 

 g_m = \frac{2 \times 0.555 \text{ mA}}{0.2} = 5.55 \text{ mS} 

## MOSFET Sizing (W/L)
Using:  I_D = \frac{1}{2} k_n \frac{W}{L} V_{OV}^2 

Assume:  k_n = 200 , \mu A/V^2 

0.555 \text{ mA} = \frac{1}{2} \cdot 200 \times 10^{-6} \cdot \frac{W}{L} \cdot (0.2)^2 

 0.555 \times 10^{-3} = 100 \times 10^{-6} \cdot \frac{W}{L} \cdot 0.04 

 0.555 \times 10^{-3} = 4 \times 10^{-6} \cdot \frac{W}{L} 

 \frac{W}{L} = \frac{0.555 \times 10^{-3}}{4 \times 10^{-6}} \approx 139 

## Step 5: Output Resistance
 r_o = \frac{1}{\lambda I_D} 

Assume: lambda = 0.02 , V^{-1} 

r_o = \frac{1}{0.02 \times 0.555 \times 10^{-3}} \approx 90 , k\Omega 

## Step 6: Voltage Gain
For differential amplifier: A_v = g_m \cdot r_o 

A_v = 5.55 \times 10^{-3} \cdot 90 \times 10^{3} \approx 500 

## final design summary:
The final design summary represents the key performance parameters of the circuit in a simplified form. The tail current of 1.11 mA is the total bias current flowing through the differential pair, which gets equally divided between the two transistors. As a result, each branch carries a drain current of approximately 0.555 mA. Based on this operating current, the transconductance (gm) is calculated to be 5.55 mS, which indicates how effectively the input voltage is converted into output current.

To achieve the desired performance, the transistor sizing is chosen such that the width-to-length (W/L) ratio is approximately 139. This relatively high ratio ensures sufficient current flow and improves gain. The output resistance of the circuit is around 90 kΩ, which plays a crucial role in determining the overall voltage gain.

Combining the transconductance and output resistance, the circuit achieves a high voltage gain of approximately 500. This indicates that even a small input signal can be significantly amplified at the output, making the design suitable for applications requiring strong signal amplification.

## Conclusion:
The differential amplifier design is functionally correct, with experimental results showing good agreement with theoretical calculations. Deviations are within acceptable engineering limits and are expected in practical implementations.

The designed MOS differential amplifier satisfies:

Low power constraint (≤ 2 mW)
Symmetric operation around 0 V
High gain (~500)

## second circuit:2b
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/circuit_2b.png?raw=true)
## DC operating point:
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/OP_2b.png?raw=true)
![Image description]()
![Image description]()
![Image description]()

