# QUIZ002

```.py
#Give 2 numbers, A and B, Output TRUE if one of them is 20 or if their sum is 20.

number_A = int(input("Enter a number "))
number_B = int(input("Enter a number "))
print (f"You entered {number_A} and {number_B}")
output = "FALSE"

if number_A == 20 or number_B == 20 or number_A + number_B == 20:
        output = "TRUE"

print (f"The answe to the quiz 002 is {output}")
```
