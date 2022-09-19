# QUIZ005

## CODE

![Screen Shot 2022-09-19 at 20 05 36](https://user-images.githubusercontent.com/111761417/191004218-740e2dd7-d68f-4708-a796-171c6b8a0989.png)

## QUESTION 
What is the intended purpose of this program?

The purpuse is to check if the number entered by the user is a perfect number or not.

## FLOW DIAGRAM IMPROVED

![image](https://user-images.githubusercontent.com/111761417/191009115-71cd4545-1ad7-447b-b101-15c04b6bcda8.png)

## CODE FOR FLOW DIAGRAM IMPROVED

```.py
num_1 = int(input("Please enter a number: "))

d_1 = num_1 % 10
num_2 = num_1 // 10
d_2 = num_2 % 10

output = "no perfect"

if num_1 != d_1 + d_2:
    output = "perfect"

print(f"The number {num_1} is {output}")
```
