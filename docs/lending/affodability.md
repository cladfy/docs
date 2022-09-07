---
sidebar_position: 1
---


# Daily disposable amount

This is amount that a client can set aside to repay a loan on a daily basis. It is calculated from the last 3 months


## What is a disposable amount

Computed from the total amount in from at most the last 3 months.


```
let T = Total money in from the last 90 days
let L = Largest money in from all the transactions
let A = Disposable amount from T


if L is in the transactions cmputed in T

    Then:
        if (L/T)*100 > 45%
            Then
                T-L
        else:

Finally

A = (T/length of T)*25%
```

