# dsbsc-modulation

EX NO: 2 DSB-SC- MODULATION

AIM:

To write a program to perform DSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

EQUIPMENTS REQUIRED

• Computer with i3 Processor • SCI LAB

Note: Keep all the switch faults in off position

Algorithm:

Define Parameters: • Fs: Sampling frequency. • T: Duration of the signal. • Fc: Carrier frequency. • Fm: Frequency of the message signal. • Amplitude: Maximum amplitude of the message signal.
Generate Signals: • Message Signal: A sinusoidal signal that will be modulated. • Carrier Signal: A high-frequency sinusoidal signal used for modulation.
DSBSC Modulation: • Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
DSBSC Demodulation: • Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components). • Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
Visualization: Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation. PROCEDURE
• Refer Algorithms and write code for the experiment. • Open SCILAB in System • Type your code in New Editor • Save the file

• Execute the code • If any Error, correct it in code and execute again • Verify the generated waveform using Tabulation and Model Waveform

Program
```
Am=6.55;
fm=1318;
Ac=9.8;
fc=13180;
fs=131800;
t=0:1/fs:2/fm;
em=Am*cos(2*3.14*fm*t);
subplot(3,1,1);
plot(t,em);
ec=Ac*cos(2*3.14*fc*t);
subplot(3,1,2);
plot(t,ec);
eam1=(Ac+em).*cos(2*3.14*fc*t);
eam2=(Ac-em).*cos(2*3.14*fc*t);
edsbsc=(eam1-eam2);
subplot(3,1,3);
plot(t,edsbsc);
```
Output Graph
<img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/dd8ca003-a4de-4890-abd2-b508236f1ab1" />


Tablular Column
<img width="1280" height="791" alt="image" src="https://github.com/user-attachments/assets/d7715796-20fe-4e9d-b2d5-930dc90f77d3" />


Result

Thus the DSB-SC-Modulation is generated
