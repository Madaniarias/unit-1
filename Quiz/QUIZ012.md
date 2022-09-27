# QUIZ012

## CODE

```.py
#Create a function that receives integer 2<N<10, and returns the multiplication for the number up to 9
number = int(input("Introduce a number between 1-9: "))
color_red = "\33[0;31m"
end_code = "\033[00m"
def operations(number:int)->str:
    multiply = ""
    if number > 1 and number < 10:
        for multiplier in range (2,10):
            multiply += f"{color_red}{number}X{multiplier}={number * multiplier}{end_code}\n"
    else:
        multiply = "Error. Try again"

    return multiply

test = operations(number)
print(test)
```
## TEST

![Screen Shot 2022-09-27 at 9 17 50](https://user-images.githubusercontent.com/111761417/192403068-83761568-6dc5-4404-8334-379f1d15af2a.png)

## FLOW DIAGRAM


