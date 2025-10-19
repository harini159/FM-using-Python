
# FM using Python


Aim:


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required:

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory:

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm:


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

PROCEDURE:

•	Refer Algorithms and write code for the experiment.
•	Open COLAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
Verify the generated waveform using Tabulation and Model Waveform


MODEL GRAPH:

<img width="512" height="365" alt="image" src="https://github.com/user-attachments/assets/acd787bd-5281-4f1b-802f-1aa39fac9189" />

Program:
```
import numpy as np
import matplotlib.pyplot as plt 
Ac = 3.21
fc = 2940
Am = 2.21
fm = 294
fs = 29400
B = 3.1
wc = 2 * np.pi * fc 
wm = 2 * np.pi * fm
t = np.arange(0, 2/fm, 1/fs)
Em = Am * np.cos(2 * np.pi * fm * t) 
plt.subplot(3, 1, 1)
plt.plot(t, Em)
Ec = Ac * np.cos(2 * np.pi * fc * t) 
plt.subplot(3, 1, 2)
plt.plot(t, Ec)
Efm = Ac * np.cos(wc * t + B * np.sin(wm * t)) 
plt.subplot(3, 1, 3)
plt.plot(t, Efm) 
plt.tight_layout() 
plt.show()
```


Output Waveform:

<img width="768" height="582" alt="image" src="https://github.com/user-attachments/assets/b523a22c-b3b2-47d3-becc-b6bfbb149113" />



Tabular Column:



Calculation:



Frequency Deviation Practical = 

Modulation Index Practical	= 

Modulation Index Theoretical	=




Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.


