# EXPERIMENT-3
## ANALYSIS OF MOS DIFFERENTIAL AMPLIFIER CIRCUIT
### Introduction to differential amplifier
To start with the understanding of the differential amplifier we first need to have an idea about the differential signal which is given as the input to the mos differential amplifier. We are familiar with a single ended signal which is measured between a node and ground whereas the differential signal is measured between 2 nodes. 
The differential mos amplifier configuration is the most widely used building block in the modern day IC design. Now the reason why these differential amplifier dominate modern day ICs is due to the following reasons:
1. When the signal is sent from one place to the another due to the external field and also due to the formation of parasitic capacitance the signal may develop some noise in them which when fed to the single ended amplifier may lead to amplification of the noise signal too which then might to lead to loss in the signal integrity. So in these case the differential input is feed to differential amp which removes the noise which is common in both the signals
2. These differential amplifier also suppresses the common mode signals like the dc offset, noise signal, power supply noise etc.

The MOS differential amplifier is formed using two identical common source mosfet amplifiers. These common source mosfets are identical is all sense that is they same device characteristics, same biasing and moreover they have same drain resistors. Therefore both amplifier will provide the same gain.The differential pair consist of two transistors M1 and M2(common source mos amplifiers), whose sources are joined together. If two transistor are connected to the different voltage input then there current across M1 and M2 are different due to gate voltage.If in case the voltage supply at gate terminal is same then the current through the M1 and M2 are same (Im1=Im2).This configuration is called Common Mode input voltage differential Amplifier.
![image](https://github.com/user-attachments/assets/34cb8670-b244-4816-8d69-b5afd5793ba9)

### Question:
Design and analyze the differential amplifier for the following specifications 
Vdd = 2.2V, P = 2.2mW, Vicm = 1.2V, Vocm = 1.25V, Vp = 0.4V
Perform DC anlysis, transient analysis, frequency response, and extract the parameters.

Now this experiment is done in three stages by changing the components connected at the common source 
1. Resistor
2. Current source
3. Mosfet

### Design 
Given                   
P = 2.2mW                       Therefore, Iss = 1mA
VI = 2.2mW                          Id1 = Id2 = Iss/2
I = 2.2/2.2                          Id1 = Id2 = 0.5mA
I = 1mA

Rd = (Vdd - Vocm)/Id1   Similarly, Vp = o.4, Iss = 1mA
Rd = 1.9kohm                       Rss = 0.4/1 = o.4kohm

Vds = Vd - Vs
      1.25 - 0.4
      0.28

The above are the obtained values for the provided design.


