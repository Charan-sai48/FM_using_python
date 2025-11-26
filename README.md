# FM_using_python

## Aim

To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries.

## Apparatus Required

Software: Python with NumPy and Matplotlib libraries<BR>
Hardware: Personal Computer
## Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. 


## Algorithm

Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.

Generate Time Axis: Create a time vector for the signal duration.

Generate Message Signal: Define the message signal as a cosine wave.

Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.

Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.

Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

## Program 
```import numpy as np
import matplotlib.pyplot as plt
Am = 5.8
fm = 507
Ac = 11.6
fc = 5070
fs = 507000
bt=4.75
t = np.arange(0, 3/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
efm = Ac * np.cos((2 * np.pi * fc * t) +  (bt * np.sin(2 * np.pi * fm * t)))
plt.subplot(3, 1, 3)
plt.plot(t, efm)
plt.tight_layout()
plt.show()
```
## Output

<img width="787" height="591" alt="image" src="https://github.com/user-attachments/assets/f3e4302b-3322-4560-977f-e20bb9681879" />


## Tabular column

![WhatsApp Image 2025-11-26 at 3 47 22 PM](https://github.com/user-attachments/assets/91e4dbad-bcf1-4334-b2e3-829471cc4398)


## calculation

<img width="452" height="786" alt="image" src="https://github.com/user-attachments/assets/4202f1a9-a5eb-4914-9954-62aacfb6b943" />


## Result

frequency modulation is executed using python
