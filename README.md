# Experiment 1

AIM: Analysis of CS amplifier

SPECIFICATIONS: Length = 180 nm, tsmc, VDD = 1.8 V, Power budget = 50 uW.

# DESIGN-1:

![Screenshot (9)](https://github.com/user-attachments/assets/d9fb1059-eb89-4171-b208-372857a43756)

PROCEDURE: 
1. Make the circuit connections as shown above.
2. After making the connection connect a dc voltage source that is VDD = 1.8V.
3. Resistance of the resistor is given as 1k.
4. The length of the nmos is 180nm as given.
5. As the power budget is 50uW we vary the width of the nmos to get the desired drain current.
6. The width is set to 1.08um.

DC ANALYSIS:

In the dc analysis we are finding the dc operating point of the nmos. Which is done by selecting DC op pnt option in the simulate section of lt spice.

![Screenshot (16)](https://github.com/user-attachments/assets/cb8e8e85-7385-488f-a05d-0e46ebfabebe)

TRANSIENT ANALYSIS:

The transient analysis is done to understand and analyze how the circuit responds to changes in input signals over time. Now to perform the transient analysis the stop time is set to 5ms and after running the simulation we obtained the below output

![Screenshot (17)](https://github.com/user-attachments/assets/79c9d7e9-4ae1-47f4-a1d3-11d86f6daa4e)

AC ANALYSIS:

To proceed with ac analysis we enter the following values as shown below

![Screenshot (18)](https://github.com/user-attachments/assets/2a7568da-01cc-4732-a839-ccd2bd1b1143)

After running the analysis we obtain the below output waveform 

![Screenshot (19)](https://github.com/user-attachments/assets/f931d569-7bab-4ca5-baa3-9154f485cdff)

Result:
Dc analysis:
 1. The required current is obtained on the basis of given power and voltage values that is ID= 2.70824e-05.
 2. We were able to obtain the above drain current by adjusting the width to 1.08um.
 3. The circuit behaves in the desired manner as expected by selecting appropriate value of width.

Transient analysis:
 1. The response obtained is smooth, with no expected delays or distortions.

AC analysis: 
 1. The ac response of the circuit confirms that the circuit remains stable at different frequencies.

Inference:

From the above experiment we conclude that by choosing the right values of width and length we can design the desired circuit with desired current flowing through it. We also observed that by increasing the value of width the drain current also increases and decreasing the width of the nmos the drain current also decreases.

