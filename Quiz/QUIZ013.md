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

![Screen Shot 2022-09-30 at 16 12 33](https://user-images.githubusercontent.com/111761417/193212703-06ae5b4f-d8a4-4a77-bd32-689bfa866919.png)

## FLOW DIAGRAM

![image](https://user-images.githubusercontent.com/111761417/194781924-0df0b927-0218-47a3-8d07-f225835a45ac.png)
