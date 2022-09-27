# QUIZ 005

## CODE

```.py

user = int(input("Enter a number:　"))
number = ''
sum = 0
counter = 1
for i in range(1,user):
    if user % i == 0:
        number += str(i)
        number += ','
        sum = sum + counter 
        counter += 1

output = "FALSE"
if user == sum:
        output= "TRUE"

print(f"The divisors for the number {user} are {number}{output}")

```
## TEST

![Screen Shot 2022-09-19 at 23 41 08](https://user-images.githubusercontent.com/111761417/191044558-cc87d6d7-ade8-4ae4-a8fd-a7236e8bc765.png)


## FLOW DIAGRAM

![image](https://user-images.githubusercontent.com/111761417/192585146-8fb13269-0900-463e-a8ed-5f3a25263bfc.png)

