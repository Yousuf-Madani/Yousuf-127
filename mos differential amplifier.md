# EXPERIMENT-3
## ANALYSIS OF MOS DIFFERENTIAL AMPLIFIER CIRCUIT
### Introduction to differential amplifier
To start with the understanding of the differential amplifier we first need to have an idea about the differential signal which is given as the input to the mos differential amplifier. We are familiar with a single ended signal which is measured between a node and ground whereas the differential signal is measured between 2 nodes. 
The differential mos amplifier configuration is the most widely used building block in the modern day IC design. Now the reason why these differential amplifier dominate modern day ICs is due to the following reasons:
1. When the signal is sent from one place to the another due to the external field and also due to the formation of parasitic capacitance the signal may develop some noise in them which when fed to the single ended amplifier may lead to amplification of the noise signal too which then might to lead to loss in the signal integrity. So in these case the differential input is feed to differential amp which might remove the noise which is common in both the signals
2. These differential amplifier also suppresses the common mode signals like the dc offset, noise signal, power supply noise etc.
