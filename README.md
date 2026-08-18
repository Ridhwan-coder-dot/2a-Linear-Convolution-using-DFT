EXPT 2a: LINEAR CONVOLUTION-USING-DFT
AIM
To perform and verify linear convolution operation of two given sequences using SCILAB.

APPARATUS REQUIRED
PC installed with SCILAB

PROGRAM:
LINEAR CONVOLUTION

clc;
clear;
x = [1 1 1 1];
h = [1 2 3 4];
m = length(x);
n = length(h);
a=0:1:m-1;
b=0:1:n-1;
subplot(3,1,1);
plot2d3(a,x);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Input Signal X');
subplot(3,1,2);
plot2d3(b,h);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Impulse Signal h');
for i = 1: n+m-1
conv_sum = 0;
for j = 1:i
if (((i-j+1) <= n)&(j <=m))
conv_sum = conv_sum + x(j)*h(i-j+1);
end;
y(i) = conv_sum;
end;
end;
disp(y,'Convolution Sum using Direct Formula Method = ')
subplot(3,1,3);
plot2d3(y)
title('Graphical Representation of output Signal y');




### CALCULATIONS:

<img width="899" height="1599" alt="WhatsApp Image 2026-08-18 at 09 27 23" src="https://github.com/user-attachments/assets/827354db-c7e0-4c51-8faf-44fcef02ab8f" />


<img width="899" height="1599" alt="WhatsApp Image 2026-08-18 at 09 27 29" src="https://github.com/user-attachments/assets/6011913b-9193-4996-86fc-3ef52ce8afd6" />

### SAMPLE OUTPUT:
<img width="1600" height="896" alt="WhatsApp Image 2026-08-08 at 08 58 09" src="https://github.com/user-attachments/assets/013032f2-b8d7-4ce9-a360-12bd3dec1b5a" />





RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
