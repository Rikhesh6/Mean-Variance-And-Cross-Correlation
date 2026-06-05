# Mean-Variance-And-Cross-Correlation:

## Aim: 

To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## EQUIPMENTS Needed:

• Computer with i3 Processor • SCI LAB

## Algorithm:

Define the Function:
Specify the function you want to simulate.
For example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
Generate Sample Points:
Decide on the range and the number of sample points.
Generate these sample points within the desired range.
Evaluate the Function: Compute the function values at each of these sample points.
Compute Mean, Variance and Cross Correlation:
Use Scilab's functions to calculate the mean and variance of the computed function values.
Display Results:
Output the computed mean variance and Cross Correlation PROCEDURE 
• Refer Algorithms and write code for the experiment. 
• Open SCILAB in System • 
Type your code in New Editor:
• Save the file
• Execute the code 
• If any Error, correct it in code and execute again 
• Verify the generated results.

## Code:
```
clear; 
clc; 
clear;
function X=f(x),
    z= 4*(1+x)^2,
    X=x*z
endfunction
a=0;
b=1;
EX=intg(a,b,f);
function Y=c(y),
    z=4*(1+y)^2,
    Y=y*z
endfunction
EY=intg(a,b,c);
disp("i) Mean of X=",EX)
disp("  Mean of Y=",EY)

function X=g(x),
    z=4*(1+x)^2,
    X=x^2*z
endfunction 
a=0;
b=1;
EX2=intg(a,b,g); 
function Y=h(y)
    z=4*(1+y)^2,
    Y=y^2*z
endfunction 
EY2=intg(a,b,h);
vX2=EX2-(EX)^2;
vY2=EY2-(EY)^2;
disp(vX2,"ii) Variance of X"); 
disp(vY2,"   Variance of Y");

x= input("type in the reference sequence="); 
y= input("type in the second sequence="); 
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);


```
## Output:

<img width="1918" height="1110" alt="image" src="https://github.com/user-attachments/assets/505ddfb1-b28b-48a5-8f66-4ef9b26696ec" />


## Calculation:
<img width="887" height="756" alt="image" src="https://github.com/user-attachments/assets/70fdbf8e-8c69-48d2-a06d-80b0908b91f1" />
<img width="679" height="1111" alt="image" src="https://github.com/user-attachments/assets/2c05f101-f8e3-49fc-a458-ba5fff920fab" />





i) Mean of X = 5.6666667 ;Mean of Y = 5.6666667

ii) Variance of X = -27.977778; Variance of Y = -27.977778

Cross Correlation: Type in the reference sequence = [1 2 3 4 5 6 7 8]

Type in the second sequence = [2 1 3 5 6 3 5 9]

## Result:

Thus the mean , variance and cross correlation are executed in Scilab and output is verified
