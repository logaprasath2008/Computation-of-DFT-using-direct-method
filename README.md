# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT DIRECT METHOD

```
clc;
clear;
clf;

xn = [1,2,3,4,4,3,2,1];

N = length(xn);
n = 0:N-1;
j = %i;

Xk = zeros(1, N);

// Direct DFT calculation
for k = 0:N-1
    for r = 0:N-1
        Xk(k+1) = Xk(k+1) + ...
            xn(r+1)*exp(-j*2*%pi*k*r/N);
    end
end

disp("DFT output:");
disp(Xk);

K = 0:N-1;
magnitude = abs(Xk);
phase = atan(imag(Xk), real(Xk));

subplot(3,1,1);
plot2d3(n, xn);
xtitle("Input Sequence", "n", "x(n)");

subplot(3,1,2);
plot2d3(K, magnitude);
xtitle("Magnitude Spectrum", "k", "|X(k)|");

subplot(3,1,3);
plot2d3(K, phase);
xtitle("Phase Spectrum", "k", "Phase (radians)")
```


### CALCULATIONS:

<img width="1280" height="1254" alt="WhatsApp Image 2026-11-10 at 2 02 44 PM" src="https://github.com/user-attachments/assets/f50b2535-4fc8-4d54-9fbd-65a6bba794c7" />

<img width="771" height="1280" alt="WhatsApp Image 2026-11-10 at 2 02 44 PM (1)" src="https://github.com/user-attachments/assets/d81e38d2-bd39-4e00-9c70-f7760a6d928a" />

<img width="773" height="1280" alt="WhatsApp Image 2026-11-10 at 2 02 44 PM (2)" src="https://github.com/user-attachments/assets/5b800879-c5ad-472c-a9fb-77c23919add1" />

<img width="801" height="1280" alt="WhatsApp Image 2026-11-10 at 2 02 44 PM (3)" src="https://github.com/user-attachments/assets/e09cc764-3e08-43d6-845c-a41aad313f07" />




### SAMPLE OUTPUT:

<img width="1599" height="1513" alt="WhatsApp Image 2026-11-10 at 11 00 31 AM" src="https://github.com/user-attachments/assets/49076880-2c3a-4326-9703-fa497b455957" />


## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

