# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB-
__AIM:__

To write a program for mean, variance and cross correlation in SCILAB and verify the output. 

__EQUIPMENTS NEEDED:__

.Computer with i3 Processor 

.SCI LAB 

__ALGORITHM:__

1. Define the Function: Specify the function you want to simulate. For example, 
f(x)=sin⁡(x)f(x)=sin(x) or any other function. 
2. Generate Sample Points: Decide on the range and the number of sample points. Generate 
these sample points within the desired range. 
3. Evaluate the Function: Compute the function values at each of these sample points. 
4. Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the 
mean and variance of the computed function values. 
5. Display Results: Output the computed mean variance and Cross Correlation 

__PROCEDURE:__ 

1.Refer Algorithms and write code for the experiment. 

2.Open SCILAB in System 

3.Type your code in New Editor 

4.Save the file 

5.Execute the code If any Error, correct it in code and execute again 
  
6.Verify the generated results

__PROGRAM:__
```asm
clear;
clc;
clear;
function z = f(x)
    z = 3*(1 - x)^2
endfunction
a = 0;
b = 1;
EX = intg(a, b, f)
function z = c(y)
    z = 3*(1 - y)^2
endfunction
EY = intg(a, b, c)
function z = g(x)
    z = (x^2)*3*(1 - x)^2
endfunction
EX2 = intg(a, b, g)
function z = h(y)
    z = (y^2)*3*(1 - y)^2
endfunction
EY2 = intg(a, b, h)
vX2 = EX2 - (EX)^2
vY2 = EY2 - (EY)^2
disp(EX, "Mean of X =")
disp(EY, "Mean of Y =")
disp(vX2, "Variance of X =")
disp(vY2, "Variance of Y =")
x = input("Type in the reference sequence = ")
y = input("Type in the second sequence = ")
n1 = max(size(y)) - 1
r = corr(x, y, n1)
plot2d3('gnn', r)
```
__OUTPUT GRAPH:__
<img width="740" height="685" alt="image" src="https://github.com/user-attachments/assets/93682841-4b0d-4dcf-a235-df15c9314199" />
Type in the reference sequence = [1 2 3 4 5 6 7 8]

Type in the second sequence = [2 4 6 8 10 11 12 13]
![WhatsApp Image 2025-11-22 at 17 24 05_0f3c6c2e](https://github.com/user-attachments/assets/7d717cf8-29fc-4dae-807d-27735a36f0ac)
![WhatsApp Image 2025-11-22 at 17 24 07_7c085017](https://github.com/user-attachments/assets/5c3f87b4-9589-4565-ab7b-d7a5a7de4349)
![WhatsApp Image 2025-11-22 at 17 24 09_b1565082](https://github.com/user-attachments/assets/2d948758-fdb9-4cb4-b985-7b792a003be1)
![WhatsApp Image 2025-11-22 at 17 24 12_52e431bd](https://github.com/user-attachments/assets/a57ab271-2fbe-4097-84f3-16ad7564a7a9)
__RESULT:__
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.

