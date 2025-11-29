# FM-using-Python

### Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

### Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
### Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



### Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

### Program

```python
import  numpy as np
import matplotlib.pyplot as plt
Am=6.4
fm=515
Ac=12.8
fc=5150
fs=51500
b=6.4
t=np.arange(0, 3/fm, 1/fs)

m = Am*np.cos(2*3.14*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)

c= Ac*np.cos(2*3.14*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)

s=Ac*np.cos(2*3.14*fc*t+b*np.sin(2*3.14*fm*t))
plt.subplot(3,1,3)
plt.plot(t,s)

```

### Output Waveform

<img width="699" height="417" alt="Screenshot 2025-11-09 224908" src="https://github.com/user-attachments/assets/32871f36-9bf7-46d5-bffe-bd0be654d1eb" />

### Tabular Column

![WhatsApp Image 2025-11-29 at 1 17 27 PM](https://github.com/user-attachments/assets/468dfeaa-038f-4404-b439-aa2e09e322eb)

### Calculation

![WhatsApp Image 2025-11-29 at 1 25 33 PM](https://github.com/user-attachments/assets/cb3cc771-ba7e-40df-920a-1738487f5028)

### Result

The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
