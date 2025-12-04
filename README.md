# DSBSC-using-Python
## AIM:
To implement and analyze DSBSC using Python's NumPy and Matplotlib libraries.

## EQUIPMENTS REQUIRED
Software: Python with NumPy and Matplotlib libraries
Hardware: Personal Computer
## Algorithm:
Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
Generate Time Axis: Create a time vector for the signal duration.
Generate Message Signal: Define the message signal as a cosine wave.
Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
Generate DSBSC Signal: Apply the DSBSC formula to obtain the modulated signal.
Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.
## Program
```
import numpy as np
import matplotlib.pyplot as plt
Am=5.4
fm=457
Ac=10.8
fc=4570
fs=45700
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*np.pi*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*np.pi*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s1=(Ac+m)*np.cos(2*np.pi*fc*t)
s2=(Ac-m)*np.cos(2*np.pi*fc*t)
s=s1-s2
plt.subplot(3,1,3)
plt.plot(t,s)
```
Output Graph
<img width="696" height="516" alt="image" src="https://github.com/user-attachments/assets/2f3ed18b-ba93-4f9b-9a4c-e6945c2a9e7d" />

Tablular Column
![WhatsApp Image 2025-12-04 at 12 56 23_6f40cb5b](https://github.com/user-attachments/assets/4ec2ec7b-0ea8-4629-9a6d-765130756d58)



Result
Thus the DSB-SC-AM Modulation is generated using python.
