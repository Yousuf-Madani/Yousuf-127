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

Now first let us understand what is the need to replace the resistor which is present at source end by a current source: 
1. If in any case the common mode input has any minor changes in its value at the source it might vary the source terminal voltage because the current Id changes.
2. Which also might lead instability in biasing point.
3. By adding a current source we can imporve the common mode rejection ratio.

For the above circuit when resistor was present at the source terminal when we make some slight changes in the common mode input it causes changes in the operating voltages which is not diserable. In the below example I made slight changes in the dc offset of the input due to which the operating voltges changed drastically.

![image](https://github.com/user-attachments/assets/d0e64089-6a5f-4899-b70d-0c38e02ccb19)

Now let us start with the circuit 2 to deal with this problem that to make the source voltage independent of minor changes in the common mode input voltages. 

For the same circuit we just replace the resistor with current source and the value given to current source is nothing but value equivalent to Iss obtained during the designing that is equal to 1mA.

![image](https://github.com/user-attachments/assets/4d8d9895-26da-4f31-a190-63dddf1cbe45)

DC Analysis: 

We set the Vicm to desired value and fix the dc value of the current source as per the design so we obtain the following table of the operating point: 

![image](https://github.com/user-attachments/assets/705f8f99-1f5c-4b68-8ac2-7b65c665deab)

We obtain the desired values of operating point and withing the given power budget and also the current flowing through each mosfet is obtained as per the design.

Transient Analysis:

In the transient analysis we find the gain of the mos differential pair by observing the vout and vin graph. 

![image](https://github.com/user-attachments/assets/d8c356d5-5142-45be-a2af-fc2f02affb3a)

As in graph we obtain the output and input plots from which find the gain Av

        Gain = Av = Vout(p-p)/Vin(p-p)

                  = (1.4492-1.0508)/(1.2496-1.1503)

                  = 4.0120

As we can observe that the gain in the previous circuit was 1.4062 when resistor was used but now when the current source has been used the gain has increased significantly to 4.0120. This happens due to many reasons one of the reason is that

              we know that, Av = gm x Rout 

                               Rout increases the gain of the circuit also increases 

                                so in case of current source it has high output resistance which lead to increase in the overall gain.

AC analysis: 

In this we obtain the frequency response of the circuit and also observe the gain in dB

![image](https://github.com/user-attachments/assets/7f20bb24-39b7-4ba5-a0ae-d8dfcc40ec26)

As it can be seen in the graph the gain in dB is around 6.108dB

### Circuit 3: Connecting mosfet to the source terminal 

Now at the place of current source we replace it with the nmos which should have its drain current equal to the value of Iss which is the sum of both drain currents of mos M1 and M2. Now to obtain that desired current from mosfet we need to set the aspect ratio accordingly.

CIRCUIT: 

![image](https://github.com/user-attachments/assets/e6efc515-3601-410f-b5db-d71147a9e727)


DC Analysis:

Here as we have replaced the current source with the mosfet so now to make current through the mosfet M3 equal to 1mA we need to set aspect ratio of the mosfet so as to get the desired current and stable operating point. The obtained values of L and W are as follows

![image](https://github.com/user-attachments/assets/5c4856f0-e93e-4a7d-b1f8-1e90047e48fb)

By setting these values the obtained values by the dc analysis are: 

![image](https://github.com/user-attachments/assets/fbdfa2e3-b2d8-4979-a87d-ac35941071ef)

We have obatained a stable operating point.

Transient Analysis: 

![image](https://github.com/user-attachments/assets/6f74577d-15e7-41ca-a9e0-3fd529128325)

From the above graph the obtained gain is as follows: 

              Gain = Av = Vout(p-p)/Vin(p-p)

                   = (1.4492-1.0508)/(1.2496-1.1503)

                   = 4.0120

             Gain in dB = 20 x log x Av

                        = 20 x log x 4.0120

                        = 12.067dB

AC analysis: 

![image](https://github.com/user-attachments/assets/aec400b7-a2cf-4ad4-87ee-d0df5c23f4a7)

The above obtained Ac anlysis confirms that theoretically obtained value of gain in dB matches approximately to the practical value.

 The Gain in dB obtained is 12.12dB which is same as the gain in dB obtained in the above calculation that is 12.067.

 ### Inference: 

 In the above experiment we saw the 3 different configurations of differential mosfet's depending on which component is present at the tail of the differential mosfet. Each configuration have their own advantages and disadvantages. The 3 config are as follows Resistor, current source, and NMOS.

 1. When we use resistor in that case we saw that gain was low. And we also saw that if there is any small change in the common mode input the source voltage changed and also the current through the mosfet also changed so we can say that in the configuration where we connect resistor at the source terminal it will have a very low common mode rejection rate(CMRR).
 2. In case of the current source we saw that we obtained a drastically increased gain it is due to the reason that current source have a high output resistance than compared to the resistor configuration so we obtain a high gain in case of current source. We also saw that if there is a small change in the common mode input the source voltage remained the same which tells us that this configuration forces the drain currents of the mosfet to stay stable and hence the source voltage doesnt change which in turn says that it has a high common mode rejection rate(CMRR).
 3. Now when we use nmos at the source terminal it will provide increased bandwidth on basis of the resistance provided by the nmos, it also can provide high gain.
 



 










 


