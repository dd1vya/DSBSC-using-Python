# DSBSC USING PYTHON

### Aim:
To implement and analyze Double Sideband Suppressed Carrier (DSB-SC) modulation using Python's NumPy and Matplotlib libraries.

### Apparatus Required:
Software: Python with NumPy and Matplotlib libraries
Hardware: Personal Computer

### Theory:
Double Sideband Suppressed Carrier (DSB-SC) modulation is a type of amplitude modulation where the carrier signal is suppressed, and only the sidebands containing the information are transmitted.

### Program:
```
import numpy as np
import matplotlib.pyplot as plt

am = 6.7
fm = 564
ac = 13.4
fc = 5640
fs = 56400
t = np.arange(0, 2/fm, 1/fs)

m = am * np.cos(2 * np.pi * fm * t)
plt.subplot(3,1,1)
plt.plot(t, m)

c = ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3,1,2)
plt.plot(t, c)

s1 = (ac + m) * np.cos(2 * np.pi * fc * t)
s2 = (ac - m) * np.cos(2 * np.pi * fc * t)
s = s1 - s2

plt.subplot(3,1,3)
plt.plot(t, s)
plt.title("DSB-SC")

plt.tight_layout()
plt.show()
```

### Output Waveform:
<img width="630" height="469" alt="image" src="https://github.com/user-attachments/assets/2c30b256-ff36-49cf-b71e-8cf7f946e4cc" />



### Tabular Column:
![WhatsApp Image 2025-10-24 at 19 36 35_900f1511](https://github.com/user-attachments/assets/031f2bc8-9218-4494-9018-9b6dc941085f)


### Algorithm:
Initialize Parameters:
Set the values for carrier frequency, message frequency, sampling frequency, and amplitude levels.
Generate Time Axis:
Create a time vector for the desired duration of the signal.
Generate Message Signal:
Create the message signal using a cosine function.
Generate Carrier Signal:
Create the carrier signal using a cosine function.
Perform Modulation:
Multiply the message and carrier signals to obtain the DSB-SC modulated signal.
Plot the Signals:
Use Matplotlib to display the message signal, carrier signal, and DSB-SC signal.

### Result:
The message, carrier, and DSB-SC modulated signals are successfully generated and displayed using Python.
Thus, DSB-SC modulation is implemented using NumPy and Matplotlib.
