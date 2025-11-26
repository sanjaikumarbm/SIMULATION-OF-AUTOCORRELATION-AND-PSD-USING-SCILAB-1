# SIMULATION-OF-AUTOCORRELATION-AND-PSD-USING-SCILAB-1

# AIM

Write a program for Autocorrelation and PSD of signals in SCILAB and verify Wiener-Khinchin relation. 


# EQUIPMENTS Needed:

.Computer with i3 Processor 

.SCI LAB


# THEORY:

The Wiener-Khinchin theorem states that the power spectral density of a wide sense stationary random process is the 
Fourier transform of the corresponding autocorrelation function.

# Algorithm:

 1.Load or Define the Signal: Input your time-domain signal. 

 2.Compute Autocorrelation: Calculate the autocorrelation function of the signal.

3.Compute Power Spectral Density (PSD): Estimate the PSD of the signal, either directly using a method like
Welch’s periodogram or by using the Fourier transform of the autocorrelation.

4.Plot Results: Visualize the autocorrelation function and PSD. 

# PROCEDURE:


Refer Algorithms and write code for the experiment. 

Open SCILAB in System 

Type your code in New Editor 

Save the file 

Execute the code 

If any Error, correct it in code and execute again 

Verify the generated waveform using Tabulation and Model Waveform 

# PROGRAM:
```
clc;
clear all;
close;

t = 0:0.01:%pi*2;
x = sin(2*t);

// Plot original signal
subplot(3,2,1);
plot(t, x);
title('Original Signal');

// Autocorrelation
au = xcorr(x, x);
subplot(3,2,2);
plot(au);
title('Autocorrelation');

// FFT of autocorrelation
v = fft(au);
subplot(3,2,3);
plot(abs(v));
title('FFT of Autocorrelation');

// FFT of original signal
fw = fft(x);
subplot(3,2,4);
plot(abs(fw));
title('FFT of Original Signal');

// Power spectrum
fw2 = (abs(fw)).^2;
subplot(3,2,5);
plot(fw2);
title('Power Spectrum');
```

# OUTPUT:
<img width="1920" height="1080" alt="Screenshot 2025-11-11 112243" src="https://github.com/user-attachments/assets/9a6a2cfa-fa80-457c-a0c9-ff495323d975" />


# RESULT:
Thus, the Autocorrelation and PSD are executed in Scilab and output is verified.
