# MEAN-AND-VARIANCE

## AIM:

To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## EQUIPMENTS Needed:

1.Computer with i3 Processor 2.SCI LAB

## Algorithm:

1.Define the Function: Specify the function you want to simulate. For example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function. 2.Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range. 3.Evaluate the Function: Compute the function values at each of these sample points. 4.Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values. 5.Display Results: Output the computed mean variance and Cross Correlation

## PROCEDURE:
1.Refer Algorithms and write code for the experiment. 2.Open SCILAB in System 3.Type your code in New Editor 4.Save the file 5.Execute the code 6.If any Error, correct it in code and execute again 7.Verify the generated results

## PROGRAM
```
clear;
clc;
function fx = pdfx(u)
    z = 6*(1-u)^2;
    fx = u*z;
endfunction
a = 0;
b = 1;
EX = intg(a, b, pdfx);
function fy = pdfy(v)
    z = 9*(1-v)^2;
    fy = v*z;
endfunction
EY = intg(a, b, pdfy);

disp("1)Mean of X =");
disp(EX);

disp("2)Mean of Y =");
disp(EY);

function p = f1(u)
    q = 5*(1+u)^2;
    p = u^2 * q;
endfunction

a = 0;
b = 1;

EX2 = intg(a, b, f1);

function r = f2(v)
    s = 10*(1+v)^2;
    r = v^2 * s;
endfunction

EY2 = intg(a, b, f2);

vX2 = EX2 - (EX)^2;
vY2 = EY2 - (EY)^2;

disp("3) Variance of X =");
disp(vX2);

disp("4)Variance of Y =");
disp(vY2);

x= input("type in the reference sequence=");
y= input("type in the second sequence=");
S1=max(size(y))-1;
S2=max(size(x))-1;
r=corr(x,y,S1);
plot2d3('gnn',r);

```

## OUTPUT GRAPH:

<img width="745" height="532" alt="Screenshot 2025-11-04 161624" src="https://github.com/user-attachments/assets/8a97c042-235c-4268-a3bf-32cc3d6fa362" />

## OUTPUT:

<img width="518" height="457" alt="Screenshot 2025-11-04 161657" src="https://github.com/user-attachments/assets/956e8a27-363e-4f01-a12d-34ac9d3a2841" />


## TABULATION:


## CALCULATION:

## RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.


