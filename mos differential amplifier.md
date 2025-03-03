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

P = 2.2mW

VI = 2.2mW

I = 2.2/2.2                          

I = 1mA

Therefore, Iss = 1mA

Id1 = Id2 = Iss/2

Id1 = Id2 = 0.5mA

Rd = (Vdd - Vocm)/Id1  

Rd = 1.9kohm                      

Similarly, Vp = o.4, Iss = 1mA

Rss = (Vdd-Vocm)/Id1

Rss = o.4kohm

Vds = Vd - Vs

Vds = 1.25 - 0.4
    
Vds = 0.85V

The above are the obtained values for the provided design.

## Circuit1 : The common source terminal is connected to the resistor

In the following circuit we have given same input to both the mosfet which is nothing but the common mode input. The resistor connected at the drain end is nothing but the load to obtain in output. And at the source terminal both the source have been connected together which it turn connected to resistor Rss in which current Iss which is the summ of Id1 and Id2 flows.

CIRCUIT: 

![Screenshot (24)](https://github.com/user-attachments/assets/7b1252d2-5886-4144-aeeb-536c1f3376ae)

DC Analysis: 

In the dc analysis we find out the dc operating point also known as the q point by varying the aspect ratio of the mosfet. Here in the differential pair it becomes necessary to keep the aspect ratio that is ratio of the width and lenght to be same. The aim is to get the precise value of Vocm by altering the value of the aspect ratio of the two mosfets. 

The obtained values of aspect ratio are L = 180nm and W = 6.41246um

![image](https://github.com/user-attachments/assets/4f5dd7a6-7cbc-4dab-bd8b-5f479a00d7ff)

By setting the values of L and W we were able to obtain the perfect operating point.

From the above we can observe that: 
1. The drain currents in both mosfets are the same that is 0.5mA
2. For the same input the output is also same that is equal to 1.25V
3. Now as the output is same if we take the difference it is equal to 0, so we can conclude that differential amplifier is effectively rejecting the common mode voltage.

Transient Analysis:

In the transient analysis we apply a time varying signal by giving it some initial dc offset value to ensure that the mos remains in operateing region. The obtained ouput for the trnsient analysis is as follows

![image](https://github.com/user-attachments/assets/99afe131-a23b-4112-a020-3aa24df03f32)

Now in the above graph we have obtained the graph between output and input. From which we can calculate the voltage gain of the circuit from the following formula that is , 

                    Gain = Av = Vout(p-p)/Vin(p-p)

                    Av = (1.3219 - 1.1788)/(1.2488 - 1.1508)

                    Av = 1.4602

We have obtained the gain now to obtain the gain in dB we know that 

                   gain in dB = 20logAv

                              = 20log(1.4602)

                              = 3.288

The above obtained gain in dB should be approximately equal to ac anlyisis gain in dB. 

AC Analysis: 

In the ac analysis we obtain the frequency response of the circuit and we will not be able to see the low frequency region in graph due to the absence of bypass or coupling capcitor. The obtained graph is as follows: 

![image](https://github.com/user-attachments/assets/c389b08c-af90-4ef5-a9a9-a3aa9a66077f)

As we can see that the above calculated theory value of gain in dB matches the practical value that is 3.288.

### Circuit2: Common source terminal connected to current source

Now first 



 


