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


