# Design and analyze current mirror circuit as active load in cs amplifier circuit

Before starting with the experiment we need to know what is necessity of replacing the resistive load with current mirror circuit as active load.
So let us perform the experiment with resistive load and analyze the circuit and then perform experiment on the current mirror circuit as active load.

The following experiment analyzes a Common-Source (CS) amplifier with a resistive load using LTspice simulation. The objective is to study its voltage gain, frequency response, output resistace, and power consumption. The results help in understanding the limitations of a resistive load and serve as a foundation for exploring active load alternatives.

![image](https://github.com/user-attachments/assets/7dd91e86-358a-40ac-a6a2-1e94630185b3)

![image](https://github.com/user-attachments/assets/9481e4c4-6fff-4598-97c3-5f6adeb95395)

Above is the design of the cs amplifier with a resitive load and also the width and length is also shown in the above image now let us see the dc analysis of the above circuit.

![image](https://github.com/user-attachments/assets/581a5caf-c6cb-4c04-8348-c40d8bd755be)

As it can be seen that the current through the mos is 1mA and it is in saturation.

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

