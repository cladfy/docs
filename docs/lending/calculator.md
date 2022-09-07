---
sidebar_position: 2
---

# Loan ability calculator

This tool is used to compute a lendable amount calculated from a client transactions.


## What is lendable amount 

This is the esimated loan size that a client can affored to borrow and repay

## Lendable amount 

Lendable amount is calculated using the following formula


$$
AMOUNT = P * I * T 
$$

Where

$$
P = Principal
$$

Principal is given by six month total money in less loans

We compute the principal by 

$$
I = Interest
$$

This is set by a business for a specific loan product as a percentage

$$
T = Time
$$

Which is the periods in months for a given loan product set by a business


```
let M = Total money in from the last 6 months
let L = Largest money in from all the transactions
let A = Lendable amount from T


if L is in the transactions computed in T

    Then:
        if (L/M)*100 > 30%
            Then
               P = (M-L)/4
else:
    P = (M)/4 


Finally:

A = ( 
        ( (P/length of M)*(T) )
        /
        ( ((I/100)/12) * T) +1) 
    )


round(
    ((affordable_limit_calculated/len(last_months_paidIn))*int(duration))
    /
    ((((float(interestRate)/100)/12)*int(duration))+1)
    
    )
```