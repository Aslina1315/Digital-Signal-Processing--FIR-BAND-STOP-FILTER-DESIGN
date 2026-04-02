# Digital-Signal-Processing--FIR-BAND-STOP-FILTER-DESIGN
## AIM:
To generate design of Band Stop FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the Band Stop filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
Wc1=input('enter the value of Wc1='); 
Wc2=input('enter the value of Wc2='); 
N=input('enter the value of N=');
alpha=(N-1)/2; 
eps=0.001;
%Band stop
n=0:1:N-1
hd=(sin(Wc1*(n-alpha+eps))+sin(pi*(n-alpha+eps))-sin(Wc2*(n-alpha+eps)))./(pi*(n-alpha+eps))
%Hamming Window Sequence
n=0:1:N-1;  
wh=1-(2*abs(n-((N-1)/2))/(N-1)) 
hn=hd.*wh 
% Plot the Band stop Filter with Hamming Window Technique
w=0:0.01:pi; 
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
```

## OUTPUT:
<img width="1919" height="795" alt="image" src="https://github.com/user-attachments/assets/b5f7d228-8538-4307-8028-428192f7ff5c" />

## RESULT:
![WhatsApp Image 2026-04-02 at 8 40 37 PM](https://github.com/user-attachments/assets/52f6eee9-3e22-4e58-b093-98bc7e965ae3)

