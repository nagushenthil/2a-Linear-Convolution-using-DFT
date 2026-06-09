## EXPT 2a: LINEAR CONVOLUTION-USING-DFT
## AIM
To perform and verify linear convolution operation of two given sequences using SCILAB.

## APPARATUS REQUIRED
PC installed with SCILAB

## PROGRAM:
LINEAR CONVOLUTION
```c
clc;
clear;
x = [1 1 1 1];
h = [0 4 2 1];
m = length(x);
n = length(h);
a = 0:m-1;
b = 0:n-1;
subplot(3,1,1);
plot2d3(a, x);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Input Signal X');
subplot(3,1,2);
plot2d3(b, h);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Impulse Signal h');
y = zeros(1, m+n-1);
for i = 1:(m+n-1)
conv_sum = 0;
for j = 1:i
if ((j <= m) & ((i-j+1) <= n))
conv_sum = conv_sum + x(j) * h(i-j+1);
end
end
y(i) = conv_sum;
end
disp(y, 'Convolution Sum using Direct Formula Method = ');
subplot(3,1,3);
t = 0:(m+n-2);
plot2d3(t, y);
xlabel('Time');
ylabel('Amplitude');
title('Graphical Representation of Output Signal y');
```

### CALCULATIONS:
<img width="903" height="1600" alt="b51b8c46-1b6b-4766-a884-beda28cd08f7" src="https://github.com/user-attachments/assets/3c157bc0-744a-49b7-b153-1f71e2e630c7" />


### SAMPLE OUTPUT:

<img width="1920" height="1200" alt="Screenshot 2026-05-25 124242" src="https://github.com/user-attachments/assets/09e2d0ee-b04a-4b26-9994-7c5528157010" />


## RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
