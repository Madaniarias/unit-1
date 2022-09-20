# QUIZ004

## CODE

![Screen Shot 2022-09-19 at 20 02 06](https://user-images.githubusercontent.com/111761417/191172261-7c935240-1aa0-4743-9941-bb05c98588f1.png)

## QUESTION 
What is the intended purpose of this program?

The purpuse is to check if the number entered by the user is a perfect number or not.

## FLOW DIAGRAM IMPROVED

![image](https://user-images.githubusercontent.com/111761417/191173792-6d472d56-d564-45f4-aeef-ad84324fe01a.png)

## CODE FOR FLOW DIAGRAM IMPROVED

```.py
number_user = int(input("Please enter a number: "))

module = number_user % 10
division_1 = number_user // 10
division_2 = division_1 % 10

output = "no perfect"

if number_user != module + division_2:
    output = "perfect"

print(f"The number {number_user} is {output}")
```
## TEST FOR CODE IMPROVED

![Screen Shot 2022-09-20 at 14 03 36](https://user-images.githubusercontent.com/111761417/191171892-c93771f5-2db2-45ae-b8f5-e14f1216d288.png)
