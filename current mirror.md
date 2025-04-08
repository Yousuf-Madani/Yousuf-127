# Design and analyze current mirror circuit as active load in cs amplifier circuit

Before starting with the experiment we need to know what is necessity of replacing the resistive load with current mirror circuit as active load.
So let us perform the experiment with resistive load and analyze the circuit and then perform experiment on the current mirror circuit as active load.

The following experiment analyzes a Common-Source (CS) amplifier with a resistive load using LTspice simulation. The objective is to study its voltage gain, frequency response, output resistace, and power consumption. The results help in understanding the limitations of a resistive load and serve as a foundation for exploring active load alternatives.

![image](https://github.com/user-attachments/assets/7dd91e86-358a-40ac-a6a2-1e94630185b3)

![image](https://github.com/user-attachments/assets/9481e4c4-6fff-4598-97c3-5f6adeb95395)

Above is the design of the cs amplifier with a resitive load and also the width and length is also shown in the above image now let us see the dc analysis of the above circuit.

![image](https://github.com/user-attachments/assets/581a5caf-c6cb-4c04-8348-c40d8bd755be)

As it can be seen that the current through the mos is 1mA and it is in saturation.
Now let us also setup the cs amplifier with current mirror resistive load which also has 1ma current flowing through it.

![image](https://github.com/user-attachments/assets/24e4e964-73ae-4d4d-879e-9bdc58bae98f)

As we can see that the cs amplifier is set perfectly to operating point as it can be seen in the dc analysis.

## COMPARISION PARAMETERS
### GAIN
Now first let us see the gain of the cs amplifier through the transient analysis which would later help us to compare it with circuit with current mirror as load. 

![image](https://github.com/user-attachments/assets/82ea214b-d0d5-46db-9f39-e4e744a4de32)

Now by observing the above waveform of input and output voltages we can calculate the gain as

  Av = Voutp-p/Vinp-p
     = (1.255-0.283)/(0.649-0.55)
     = 0.972/0.099
     = 9.81V/V

Therefore the obtained gain is 9.81v/v of the cs amplifier with resister as the load.

Calculating the gain of cs amplifier with a current mirror circuit as load by transient analysis:

![image](https://github.com/user-attachments/assets/01da6faf-b531-4dd6-b7ad-3517fbb3481e)

  Av = Voutp-p/Vinp-p
     = (1.679-0.098)/(0.649-0.55)
     = 1.581/0.101
     = 15.65V/V

By the above obtained results we can conclude that using current mirror circuit as load can provide a high gain even we have the same amount of current is flowing through the load.
The above obtained high gain is due to the reason of having a high output resistance in case of current mirror circuit. So next let us compare the output resistace of both the circuits.

### Output resistance

Circuit 1:
   Rout = Rd
   that is 1kohm.

Circuit 2:
   Rout = 1/λId
        = 1/1.011891x10^-6
        =988.24kohm

As we can clearly see from the obtained result that the output resistance in case of current mirror circuit is 1000 times greater than the output resistance in case of resistive load.

There are many more comparision parameters which can be used for comparision but for now keeping the above parameters in mind it becomes clear to use current mirror as load in the cs amplifier circuit.

## Design Question:

Design a current mirror circuit which has a gain of AV = -10V/V, power supply of Vdd = 1.8V, and power of P <= 1mW. Find reference current (Iref), output current (Id), and total current (Itotal). Perform DC and AC analysis for mirror ratio 1:1, 1:2. Vary length from 180nm -> 500nm -> 1µm and do the analysis.

Below shown is the calculation to find out the total current wrt to the given power rating.
![WhatsApp Image 2025-04-05 at 08 29 45_f99a642b](https://github.com/user-attachments/assets/f89d2022-10fd-4cb4-b4ff-318aad0f2f5d)

Designing the circuit as per the above calculation:

![image](https://github.com/user-attachments/assets/a87fd3da-fc32-442f-859b-022c5389d3dd)

DC analysis:

![image](https://github.com/user-attachments/assets/1cbf452d-b0a0-43b1-9897-cf181561b41c)

As it can be clearly seen that by the analysis of the gate drain and source voltages all the mosfet are in saturation and the current is being perfectly mirrored after setting the w/l of the nmos where L = 180nm and W = 18.053u.

Transient analysis:

![image](https://github.com/user-attachments/assets/a2bd5c4b-d431-487b-a298-c200543e3580)

The above shown waveform is the output waveform the circuit, the input given is having a dc offset of 0.6V with a amplitude of 10m whereas the output voltage is 1.40V.

AC analysis:

![image](https://github.com/user-attachments/assets/abfe00f8-6e2a-4f6a-b391-56300ad1021b)

The gain in dB obtained is 29.881dB
29.881 - 3 = 26.881dB
58.833Mhz is the High frequency.
Therefore the bandwidth of the circuit is fH - fL = 58.833Mhz - 0 = 58.833Mhz.

### Now performing the circuit analysis when the ratio is 1:2

Initially W = 70u
Now for the ratio 1:2 the new value of W is 140u.
As total current is 0.55mA, it is divided into 3 parts, where 1/3 of current is its reference current Iref and remaining is the output current Id.
i.e 0.55m / 3 = 0.183mA.
Hence, Iref = 0.183mA and Id = 0.3667mA

DC Analysis:

![image](https://github.com/user-attachments/assets/8f040228-c318-4111-93a1-68573af84f8a)

The current is set as per the above calculation and all voltages are prefectly set such all the three mos are in saturation.

Transient Analysis:

![image](https://github.com/user-attachments/assets/4f2dd08b-3d98-4dbc-a756-25c74e470300)

The output swing for both output waveform is the same only there is small dc shift in above case.

AC Analysis:

![image](https://github.com/user-attachments/assets/8507bd8d-f4ba-4d11-abb1-630d73ffbb66)

There is no much difference in the gain of the 1:1 and 1:2 ratio they are nearly the same.














