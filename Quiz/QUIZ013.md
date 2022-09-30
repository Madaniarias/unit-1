# QUIZ013

## CODE
```.py
def mystery(A:int,B:int)->str:
    if A < 10 and B < 10:
        multiplier = B + 1
        total = multiplier * A - B
    elif A > 10 and B > 10:
        difference = abs(A-B)
        total = (A*B)-difference
    else:
        total = (A*B)-B

    return total

out = mystery(A=2, B=6)
print(out)
```

## TEST



## FLOW DIAGRAM
