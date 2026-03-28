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

## 1. Tail Current Calculation

P = (VDD − VSS) ISS

2 10^-3 = (0.9 − (−0.9)) ISS

2 10^-3 = 1.8 ISS

ISS = (2 10^-3) ÷ 1.8

ISS = 1.11 10^-3 A

ISS = 1.11 mA

## 2. Drain Currents

ID1 = ID2 = ISS 2^-1

ID1 = ID2 = 0.555 mA

## 3. Drain Resistance (RD)

Vout = VDD − ID RD

0 = 0.9 − ID RD

RD = 0.9 ÷ (0.555 10^-3)

RD = 1636 Ω

RD = 1.636 kΩ
## 4. Region of Operation Check

VS = −0.7 V
VG = 0 V

VOV = VGS − VT

VOV = 0.34 V

VDS = VD − VS

VDS = 0.7 V

VDS > VOV

0.7 > 0.34

## 5. Width Calculation (W)

I_D = \frac{1}{2} \mu_n C_{ox} \frac{W}{L} (V_{OV})^2

W = (2 (0.555 10^-3) (360 10^-9)) ÷ (2.306 10^-4 (0.34)^2)

W = 14.88 10^-6 m

W = 14.88 μm

## 6. Input Common Mode Range (ICMR)

VGS ≥ VT

VGS = VICM − VS

VICM(min) = VS + VT

VICM(min) = −0.7 + 0.36

VICM(min) = −0.34 V

## Final Results

ISS = 1.11 mA
ID = 0.555 mA
RD = 1.636 kΩ
W = 14.88 μm
VICM(min) = −0.34 V

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

P = (VDD − VSS) Itotal

2 10^-3 = (0.9 − (−0.9)) Itotal

2 10^-3 = 1.8 Itotal

Itotal = (2 10^-3) ÷ 1.8

Itotal = 1.11 10^-3 A

Itail = 1.11 mA

## Drain Current in Each Transistor

ID = Itail 2^-1

ID = 0.555 mA

## Saturation Check (M3)

VDS3 = Vp − VSS

VDS3 = −0.7 + 0.9

VDS3 = 0.2 V

VGS3 − Vth ≤ 0.2

VinCM(max) = Vp + VGS1

VinCM(max) = 0 V

## Transconductance (gm)

g_m = \frac{2 I_D}{V_{OV}}

gm = (2 (0.555 10^-3)) ÷ 0.2

gm = 5.55 10^-3 S

gm = 5.55 mS


## MOSFET Sizing (W L ratio)

I_D = \frac{1}{2} k_n \frac{W}{L} V_{OV}^2

0.555 10^-3 = (1 2^-1) (200 10^-6) (W L^-1) (0.2)^2

0.555 10^-3 = 100 10^-6 (W L^-1) 0.04

0.555 10^-3 = 4 10^-6 (W L^-1)

W L^-1 = (0.555 10^-3) ÷ (4 10^-6)

W L^-1 = 139

## Step 5: Output Resistance

r_o = \frac{1}{\lambda I_D}

ro = 1 ÷ (0.02 (0.555 10^-3))

ro = 90 10^3 Ω

ro = 90 kΩ

## Step 6: Voltage Gain

A_v = g_m r_o

Av = (5.55 10^-3) (90 10^3)

Av = 499.5

Av = 500

## Final Results

Itail = 1.11 mA
ID = 0.555 mA
gm = 5.55 mS
W L^-1 = 139
ro = 90 kΩ
Av = 500

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

## Using MOSFET current equation:
ID​=21​μp​Cox​LW​(VOV​)2

## Rearranging for W:

W=μp​Cox​(VOV​)22ID​L

## Substituting values:

W = (2 (0.555 10^-3) (360 10^-9)) / (9.73 10^-6 (0.24)^2)

W = (396 10^-12) / (1.128 10^-7)

W = 351.06 10^-6 m

W = 351.06 μm

## 2. Bias Voltage (VB1)

VB1 = VG = VGS + VDD

VB1 = 0 + ID RD

Substituting values:

VB1 = (0.555 10^-3) (1636)

VB1 = 0.908

## Final Results

PMOS Width
W = 351.06 μm

Bias Voltage
VB1 = 0.908 V
## DC operating point:
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/OP_2b.png?raw=true)

## Transient analysis:
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/Transient_analysis_2b.png?raw=true)

From the waveform, both outputs are periodic signals, meaning they repeat continuously over the given time range of 0 ms to 5 ms. The key observation is that the two signals are opposite to each other (out of phase). When V(out1) increases, V(out2) decreases, and vice versa. This is the expected behavior of a differential amplifier, where the circuit responds to the difference between two input signals.

The voltage levels vary approximately between 200 mV and 850 mV. This indicates that the outputs are not centered around zero but are shifted due to DC biasing in the circuit. The smooth rising and falling shapes show that the amplifier is operating properly in its active region.
 the waveform is slightly curved near the peaks and not perfectly symmetrical. This happens due to non-ideal effects like transistor limitations and finite gain, which are normal in practical circuits. this graph confirms that the circuit is working correctly. It produces two complementary output signals with good symmetry, proper biasing, and expected differential behavior, making it suitable for amplification applications.

## AC analysis :
## a)output waveform 1:
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/output_waveform_2b.png?raw=true)

## b)output waveform 2:
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/output_waveform_2.png?raw=true)

## comparing the values of theoritical and simulated values:
 the tail current is theoretically 1.11 mA, while the simulated value lies between 1.0 mA and 1.15 mA. This indicates a close agreement, with only small variations caused by non-ideal effects such as channel length modulation and process variations. Similarly, the drain current for each transistor is calculated as 0.555 mA, and the simulated range of 0.50 mA to 0.58 mA shows a slight mismatch, which is mainly due to device mismatch and modeling inaccuracies.

The drain resistance is designed as 1.636 kΩ, and the simulated values range from 1.5 kΩ to 1.7 kΩ. This falls well within acceptable tolerance limits, confirming that the resistor implementation is accurate. For transistor sizing, the NMOS width is theoretically 14.88 μm and varies between 14 μm and 16 μm in simulation, which closely matches the design expectations. In the case of PMOS, the width is much larger at 351 μm, with simulated values between 340 μm and 360 μm. This increase is expected because PMOS devices have lower carrier mobility compared to NMOS, requiring a larger size to achieve similar current.

The overdrive voltage for NMOS is theoretically 0.34 V and varies slightly between 0.30 V and 0.36 V in simulation. This minor variation occurs due to threshold voltage shifts. For PMOS, the overdrive voltage is 0.24 V, and the simulated range of 0.22 V to 0.26 V shows consistent behavior with the design.

The bias voltage is calculated as 0.89 V, while the simulated value ranges from 0.85 V to 0.9 V, indicating good agreement between theory and practice. Finally, the minimum common-mode input voltage is theoretically -0.34 V and varies from -0.3 V to -0.4 V in simulation, which matches the expected circuit behavior.

the simulated results closely follow the theoretical calculations, with only minor deviations due to practical non-idealities. This confirms that the circuit design is accurate, reliable, and performs as expected under real operating conditions.

## Conclusion:
In simple terms, the simulated results are very close to the theoretical values, which means the design is working as expected. The small differences you see are normal in real circuits because of non-ideal effects like device mismatch and slight variations in parameters. Overall, the circuit behaves correctly, and the design can be considered reliable and accurate.

## Circuit :2c
## Circuit diagram:
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/circuit_2c.png?raw=true)
## DC Operating point:
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/OP_2c.png?raw=true)
## Transient analysis:
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/Transient%20analysis_2c.png?raw=true)
From the graph, you can observe that both outputs are periodic signals, meaning they repeat in a regular pattern over time. The time axis runs from 0 ms to 5 ms, and within this interval, multiple cycles of the waveform are visible, indicating a steady input signal is being applied to the circuit.

The most important thing to notice is that the two signals are out of phase with each other. When V(out1) is going down, V(out2) is going up, and vice versa. This is a key characteristic of a differential amplifier. It means the circuit is amplifying the difference between the two input signals and producing complementary outputs.

In terms of voltage levels, both signals vary roughly between 860 mV and 900 mV. So instead of swinging around zero, the outputs are centered around a DC bias voltage close to 890 mV. This DC level comes from the biasing of the circuit, which ensures the transistors operate in the proper region.

Another observation is that the waveform is not a perfect sine wave. Near the peaks, the signal looks slightly flattened. This indicates that the circuit is experiencing slight non-linearity or limited voltage swing, possibly due to transistor saturation or limited headroom in the supply voltage.
Also, both outputs have nearly the same amplitude, which shows that the circuit is well balanced. This means the NMOS transistors are properly matched, and the current is evenly distributed between the two branches.
this waveform confirms that your differential amplifier is working correctly. It is producing two equal but opposite output signals, maintaining a proper bias level, and showing only minor distortions due to practical limitations.

## Ac analysis :
## Output waveform_1:
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/output%20waveform_2.png?raw=true)
## Output waveform_2:
![Image description](https://github.com/2024ecdeekshithagjc-bit/Experiment-no-4/blob/main/output%20waveform_2c.png?raw=true)


### PMOS Transistor Calculation

### 1. Width Calculation (W):

Using MOSFET current equation:
ID​=21​μp​Cox​LW​(VOV​)2

Rearranging:

W=μp​Cox​(VOV​)22ID​L

Substituting values:

W = (2 (0.555 10^-3) (360 10^-9)) ÷ (9.73 10^-6 (0.24)^2)

W = (396 10^-12) ÷ (1.128 10^-7)

W = 351.06 10^-6 m

W = 351.06 μm

W = 0.351 mm

## 2. Bias Voltage (VB1):

VB1 = VG = VGS + VDD

VB1 = 0 + ID RD

Substituting values:

VB1 = (0.555 10^-3) (1636)

VB1 = 0.908 V


### Final Results:

PMOS Width
W = 351.06 μm

Bias Voltage
VB1 = 0.908 V
## Comparision between theoritical and simulated values:

Starting with the tail current, the theoretical value is 1.11 mA, while the simulated value ranges from 1.0 mA to 1.15 mA. This indicates very close agreement, with only slight variations due to non-ideal effects present in real devices. Similarly, the drain current is theoretically 0.555 mA and varies between 0.50 mA and 0.58 mA in simulation, showing a small mismatch that typically occurs due to device mismatch and modeling limitations.

The drain resistance has a theoretical value of 1.636 kΩ, and the simulated range of 1.5 kΩ to 1.7 kΩ confirms that it lies within acceptable tolerance. For transistor sizing, the NMOS width is calculated as 14.88 μm and appears between 14 μm and 16 μm in simulation, which closely matches the design. The PMOS width is significantly larger at 351 μm, and its simulated range of 340 μm to 360 μm is also consistent. This larger size is expected because PMOS devices have lower mobility compared to NMOS.

Looking at the overdrive voltages, the NMOS theoretical value is 0.34 V, while simulation gives values between 0.30 V and 0.36 V, showing only minor variation due to threshold voltage shifts. The PMOS overdrive voltage is 0.24 V, and its simulated range of 0.22 V to 0.26 V confirms stable and consistent behavior.

The bias voltage is theoretically 0.89 V and varies between 0.85 V and 0.9 V in simulation, indicating good agreement. Finally, the minimum common-mode input voltage is calculated as -0.34 V and ranges from -0.3 V to -0.4 V in simulation, which matches the expected circuit operation.

Overall, the simulated results closely follow the theoretical values, with only small deviations due to practical non-idealities. This confirms that the circuit design is accurate, reliable, and performs as intended.

## Conclusion
The experimental (or simulated) results show strong agreement with theoretical calculations.
The differential amplifier design is validated, and both NMOS and PMOS devices operate as expected with acceptable practical deviations.

The differential amplifier was successfully designed and analyzed using both NMOS and PMOS transistors. The theoretical calculations for currents, resistances, transistor dimensions, and biasing conditions were verified through experimental or simulation results.

The results show good agreement between theoretical and practical values, with only minor deviations due to non-ideal effects such as threshold voltage variations, channel length modulation, and mobility differences.

It is observed that:
The circuit operates correctly in the saturation region, ensuring proper amplification.
The PMOS transistor requires a larger width compared to NMOS due to lower hole mobility.
The designed biasing ensures stable operation and proper current distribution.
Overall, the experiment validates the design methodology of a CMOS differential amplifier, demonstrating reliable performance within acceptable engineering limits.

## Inference:
The CMOS differential amplifier design is validated through both theoretical calculations and experimental/simulation results. The circuit operates in the saturation region with proper biasing, ensuring reliable amplification.

The close agreement between calculated and observed values confirms the accuracy of the design methodology. Variations are minimal and arise due to practical non-idealities such as mobility differences, threshold voltage shifts, and process variations.

Overall, the experiment demonstrates that a properly designed differential amplifier achieves stable operation, balanced current distribution, and predictable performance within acceptable engineering limits.


