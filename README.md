# 2.-Design-implement-and-simulatioin-of-Integrator-and-Differentiator
**AIM:**
To design , implement and simulate  an integrator and differentiator circuits

**APPARATUS  and SOFTWARE REQUIRED:**
S.No	Name of the Apparatus	Range	Quantity
1.	Signal Generator	3 MHz	1
2.	DSO	30 MHz	1
3.	Dual RPS	(0 – 30) V	1
4.	Op-Amp	µA741	1
5.	Bread Board		1
6.	Resistors	1K,10K,100K,	2
7.	Capacitors	0.1µF,0.01µF	1
8.	Connecting wires and probes	As required	
9.  LT SPICE software

**THEORY:**

**INTEGRATOR**
A circuit in which the output voltage waveform is the integral of the input voltage waveform is the integrator. Such a circuit is obtained by using a basic inverting amplifier configuration if the feedback resistor Rf is replaced by a capacitor Cf . The expression for the output voltage is given as,
Vo = - (1/Rf C1 ) ∫ Vi dt

Here the negative sign indicates that the output voltage is 180 0 out of phase with the input signal. Normally between fa and fb the circuit acts as an integrator. Generally, the value of fa < fb . The input signal will be integrated properly if the Time period T of the signal is larger than or equal to Rf Cf . That is,
T ≥ Rf Cf

The integrator is most commonly used in analog computers and ADC and signal-wave shaping circuits.

**DESIGN:**
 
To obtain the output of an Integrator circuit with component values R1Cf = 0.1ms , Rf = 10 R1 and Cf = 0.01 µF and also if 1 V peak square wave at 1000Hz is applied as input.
We know the frequency at which the gain is 0 dB, fb = 1 / (2π R1 Cf) Therefore fb = 	 Since fb = 10 fa , and also the gain limiting frequency fa = 1 / (2π Rf Cf)
We get , R1 =	and hence Rf = 	

**DIFFEERENTIATOR:**

The differentiator circuit performs the mathematical operation of differentiation; that is, the output waveform is the derivative of the input waveform. The differentiator may be constructed from a basic inverting amplifier if an input resistor R1 is replaced by a capacitor C1 . The expression for the output voltage is given as,
Vo = - Rf C1 ( dVi /dt )

Here the negative sign indicates that the output voltage is 180 0 out of phase with the input signal. A resistor Rcomp = Rf is normally connected to the non-inverting input terminal of the op-amp to compensate for the input bias current. A workable differentiator can be designed by implementing the following steps:
1.	Select fa equal to the highest frequency of the input signal to be differentiated. Then, assuming a value of C1 < 1 µF, calculate the value of Rf.
2.	Choose fb = 20 fa and calculate the values of R1 and Cf so that R1C1 = Rf Cf.

The differentiator is most commonly used in wave shaping circuits to detect high frequency components in an input signal and also as a rate–of–change detector in FM modulators.
 
**DESIGN (DIFFERENTIATOR):**

Design an op-amp differentiator that will differentiate an input signal with fmax = 100HZ Select fa = fmax = 100 HZ = 1 / 2πRFC1
Let C1 = 0.1μF
Then RF = 1 / 2π(102)(10-7)
= 15.9KΩ
Now choose fb = 10fa = 1 / 2πR1C1 Therefore, R1 = 1 / 2π(103)(10-7)
= 1.59KΩ Since RFCF = R1C1
We get, CF = (1.59*103*10-7) / 15.9*103
= 0.01μF


**PROCEDURE:**
1.	Connections are given as per the circuit diagram
2. + Vcc and - Vcc supply is given to the power supply terminal of the Op-Amp IC.
3.	By adjusting the amplitude and frequency knobs of the function generator, appropriate input voltage is applied to the inverting input terminal of the Op- Amp.
4.	The output voltage is obtained in the CRO and the input and output voltage waveforms are plotted in a graph sheet.

 
**INTEGRATOR:**
  **CIRCUIT DIAGRAM**
<img width="1600" height="945" alt="image" src="https://github.com/user-attachments/assets/6155cc62-edc7-4667-8019-b43b85f58133" />


  **MODEL GRAPH:**
<img width="1600" height="857" alt="image" src="https://github.com/user-attachments/assets/7e614461-38b5-4928-aa10-2d84c17ffdea" />
<img width="1600" height="1067" alt="image" src="https://github.com/user-attachments/assets/89c59778-848a-4965-a6bd-849febc2f174" />


  **TABULATION:**
 <img width="1600" height="664" alt="image" src="https://github.com/user-attachments/assets/b7febf44-094f-4bed-803b-e59607cbbd82" />


**MODEL CALCULATION:**
<img width="1600" height="1409" alt="WhatsApp Image 2026-09-13 at 8 25 49 PM" src="https://github.com/user-attachments/assets/3030dddd-4239-4cd4-9f89-2538e5d26aad" />

**DIFFERENTIATOR:**
  **CIRCUIT DIAGRAM**
<img width="1359" height="1600" alt="image" src="https://github.com/user-attachments/assets/b387e885-3e33-4f8e-b62d-fa187ccb96f0" />


  **MODEL GRAPH:**
<img width="1600" height="669" alt="image" src="https://github.com/user-attachments/assets/6c2dcb0d-e653-402b-a31e-bd79d765466d" />


  **TABULATION:**
<img width="1600" height="1113" alt="image" src="https://github.com/user-attachments/assets/13fd0124-d5fb-43d1-b2b3-6694dd3d4dc3" />

 

**LT-SPICE Tool:PROCEDURE:**
•	Double click on LT-Spice icon.
•	New schematic window open.
•	Pick and paste the required component from the library and draw the circuit diagram .
•	Complete the connection.
•	Save the file by giving file name.
•	Click on the run option ->click advanced open ->select Ac analysis->enter the amplitude time delay stop time value.
•	Click on the run option ->simulation window opens->place the probe ->output graph is obtained.
 
  **LT SPICE**
  **CIRCUIT and Waveform**
  <img width="1600" height="850" alt="image" src="https://github.com/user-attachments/assets/eb07bbcd-3349-4396-99e4-aab40033e836" />
<img width="1600" height="850" alt="image" src="https://github.com/user-attachments/assets/efaf9e02-9079-491c-9760-8b851ef59b7b" />
<img width="1600" height="850" alt="image" src="https://github.com/user-attachments/assets/9b94ab66-a1dc-4b80-8cea-cad8297dd0b4" />
<img width="1600" height="850" alt="image" src="https://github.com/user-attachments/assets/833346d5-3174-4b4a-896b-05515c5c6756" />




**RESULT:**
Thus the Integrator and Differentiator are designed and simulated performance was successfully tested using op-amp IC 741 and LT SPICE.
