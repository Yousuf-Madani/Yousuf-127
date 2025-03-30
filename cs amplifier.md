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

# Design-2

![Screenshot (14)](https://github.com/user-attachments/assets/77363cad-47dd-46c5-aaed-4c98c9a6b92a)


Aim : To find DC operating point find gain using transient analysis and AC analysis.

Components:
Mosfets M1 and M2 DC power supply.

Procedure:
1. Make the circuit connections as show abovce.
2. Connect dc power supply to the gate terminal.
3. Connect the source terminal to the ground.
4. Set the input voltage by obtaining Vtc curve and Vdd to 1.8 V.
5. Using the Formula for Power
   P=vi
   We will get the Values of Id
   Id= 27uA
   We have to get the output current Id for the given circuits by adjusting the values of L & W of both the MOSFETS by 
   adjusting the value of width and length of the mosfet we will get the current Id.
   As length is given 180nm by adjusting we will get width=0.61um this value of width and length is for both the mosfet

 1.DC Analysis:
 To perform the DC analysis we have to select the {DC op pnt} in the edit simulation command and run the simulation
 the figure below is the values obtained from the DC analysis.

 ![Screenshot (10)](https://github.com/user-attachments/assets/08c5ad4b-102c-4dd5-b716-61159345edc1)

 2. Transient Analysis:
    To perform transient analysis we have to select the transient analysis in the edit simulation
   and give the stop time as 5ms and run the simulation.
   The below shown graph is obtained.

![image](https://github.com/user-attachments/assets/7d031fb9-f0c7-439e-8d66-d0b843c6b10e)

3. AC analysis:
   We enter the values to get the ac analysis as shown below.

   ![image](https://github.com/user-attachments/assets/f195c4b8-8f05-40e5-9512-1a5b792679c1)

RESULTS:

  1.DC analysis
  
  
  The calculated drain current Id aligns with the expected value based on power and voltage  where the value of Id = 27um 
  By fine-tuning the channel dimensions  of both MOSFETs  the desired current was achieved L=180nm and W=0.61um for both mosfets
  The circuit operates correctly within the selected DC parameters 

  
  2.Transient Analysis:

  The transient response graph confirms that the circuit transitions smoothly over time.
  The circuit responds effectively to input variations, indicating stable operation.

  
  3.AC Analysis:

  The AC response graph confirms that the circuit maintains stability over the tested frequency range.
  The circuit functions as expected under AC conditions.


  INFERENCE:
  The experiment validates that by choosing the correct mosfet dimensiions the drain current can be effectively regulated.
  The voltage transfer characteristics  helped to select the correct operating voltage  for saturation.
  M1  has a stronger influence on ID, meaning its width significantly affects the output current  Increase in width increases Id  and vice-versa.
  M2 has a smaller influence on ID  meaning changes in its width result in only minor changes  in Id. Increase in width increases ID by small 
  value and vice-versa.


