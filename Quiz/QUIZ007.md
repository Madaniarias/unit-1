# QUIZ007

## CODE
```.py
#Create a program that creates 10 random passwords with digits and letters of length 20
#HL Ask the user for the length and if symbols should be included. Print answer in RED

import random
end_code = "\033[00m"
color_red = "\33[0;31m"

length = input("Input the length you would like your password to have: ")
while not length.isdigit():
    length = input(f"{red} For this program to work, you need to input a number. Try again{end_code}")
length = int(length)

user_symbol = str(input("Input 'yes' if you would like your password to inlcude symbols. Input 'no' if you rather not have any symbols in your password: "))
while not user_symbol in ["yes", "no"]:
    user_symbol= str(input(f"{red} For this program to work, you need to input 'yes' or 'no'. Try again{end_code}"))

for n in range(10):
    password = ""
    for i in range(length):
        number = random.randint(48,122)
        if user_symbol == "no":
            while 65>number>57 or 97>number>90:
                number = random.randint(48,122)

        character = chr(number)
        password = password + character

    print(f"The password number {n+1} will be{color_red} {password} {end_code}")

print("Thank you for using the random password generator program.")
```

## TEST

![Screen Shot 2022-09-27 at 1 39 10](https://user-images.githubusercontent.com/111761417/192333179-24427b25-4c12-4206-a2ea-a143a5de388f.png)

## FLOW DIAGRAM

