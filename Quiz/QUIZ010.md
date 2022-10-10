# QUIZ010

## CODE
```.py
#Create a function that produces the power of ten from pico (10^-12), to tera (10^15) for a number provided as an input.
# [HL] User inputs a string with units Ex: 1 gram of salt
user_input = input("Enter number(units included: ")
separate = [int(s) for s in user_input.split() if s.isdigit()]
powers = []
final = []
Units = ["Tera", "Giga", "Mega", "Kilo", "Unit", "Milli", "Micro", "Nano", "Pico"]
msg = 20


def power(n):
    counter = 0
    for i in range(-12, 0, 3):
        temp = abs(i // 3)
        number = f"0.{(('000 ') * temp)}{str(n[0])} ".ljust(msg)
        powers.append(f"{number}{Units[counter]}{user_input[1:]}")
        counter += 1
    for i in range(0, 15, 3):
        temp = i//3
        number = f"{str(n[0])} {('000 '*temp)} ".ljust(msg)
        powers.append(f"{number}{Units[counter]}{user_input[1:]}")
        counter += 1

    return powers

print("\n".join(power(separate)))

```

## TEST
![Screen Shot 2022-10-10 at 7 41 41](https://user-images.githubusercontent.com/111761417/194782882-9d6cd170-d480-4407-aab3-0f7df25b91ae.png)

## FLOW DIAGRAM

![image](https://user-images.githubusercontent.com/111761417/194785635-795f31f3-ba17-456b-b71f-b86fc02e8880.png)
