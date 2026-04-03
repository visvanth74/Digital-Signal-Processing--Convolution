# Digital-Signal-Processing--Convolution
## Aim:
                  To perform linear convolution using MAT LAB.
## Software Required:
MAT LAB R2012
## Algorithm:
Step 1: Open mat lab. Write the program.

Step 2: Read the first input sequence.

Step 3: Read the second impulse sequence.

Step 4: Plot the input sequences with x-label and y-label with suitable title. 

Step 5: Perform convolution for both the sequences using conv2() function.
  
Step 6: Plot the sequence with x-label and y-label with suitable title

Step 7: Terminate the program.

## PROGRAM: 
clear;
clc;
n=input('no of buses');
ele=input('no of elements');
for i=1:ele
    s=input('starting bus');
    e=input('ending bus');
    y(s,e)= input('element value');
    lca=input('Line charging admittance:');
    c=input(' checking 1 for imp 2 for admittance');
    if c==1
        y(s,e)=1/y(s,e);
    end
    y(e,s)=y(s,e);
    lc(s,e)=lca;
    lc(e,s)=lc(s,e);
    ybus=zeros(n,n);
end

for i=1:n
    for j=1:n
        if i==j
            for k=1:n
                ybus(i,j)=ybus(i,j)+y(i,k)+lc(i,k)/2;
            end
        else
            ybus(i,j)=-y(i,j);
        end
    end
end
ybus

## OUTPUT:


## RESULT:

