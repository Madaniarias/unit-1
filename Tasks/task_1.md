# TASK 1: COMPUTATIONAL THINKING

## Research

Question 1: What is the most powerful computer? Glad you asked. Watch this video about Sierra Computer. Describe below points that surprised you the most.

R/. After watching the video titled "The new supercomputer behind the US nuclear arsenal" about the Sierra Computer, the following points surprised me the most:

Question 2: Supercomputers are currently used to investigate solutions to real life problems from cancer research, Ai, economics, or brain simulation. Military uses are also one major force behind the development of these machines. Analyze the benefits and possible drawbacks of developing supercomputers in our modern world? Should we do it?
-

Question 3: Identify the most advanced computer in your Country (What, specs, location, uses). 


## Programming task

Save your program in a file called task1.md. In a school there are 2400 students and each student uses one locker. Each locker has a unique number from 1 to 2400. The lockers are to be painted in four colors: red, white, yellow and blue, in order of locker numbers, as shown in the following table.link

The pattern of colors continues in this manner. For example, locker number 15 will be painted yellow.

Task 1: Create a program and the flow diagram that shows the colors of all the lockers from 1 to 2400.

**Code**

```.py
locker = int(input("Indicate the number of lockers: "))
i = 0
locker_color = ["red", "white", "yellow", "blue"]
locker_number = 1
while i <= locker and locker_number <= locker:
        print(f"Locker number {locker_number} {locker_color[i%4]}")
        i = i + 1
        locker_number = locker_number + 1
```
**Flow diagram**

![image](https://user-images.githubusercontent.com/111761417/189787590-e5f9991d-3c8c-44b3-b70a-a68f1fabd2a6.png)

Task 2: Using the program above, create another program that allows the user to enter a number and the program outputs the color that should be used in the locker.



[HL] Task 3: Create a program that receives a color from the user, validates the input,  and outputs the numbers of the lockers of the color provided. Use at least 10 different functions for Manipulating Strings (Learning Log Item 19)

[HL] Task 4: Given a list of names of students in the format lastname, firstname, create a program that assigns an email address and a locker to each student and saves the results in a file in the format lastname, firstname, email, locker 

