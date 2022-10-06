# QUIZ015

## CODE
```.py
#There are N closed doors in a school and N students present. The first student opens each door.
# The second student flips (open-close) every second door. The third student flips every third door, and so on.
#SL Create a function that shows the doors after 5 students
#HL Create a function that shows the doors open after N students.

def open_doors (N:int)->str:
    doors = []
    for n in range (N):
        doors.append(False)

    for d in range (1,N+1):
        for stu in range (1,N+1):
            if d%stu == 0:
                doors[d-1] = not doors[d-1]

    counter = doors.count(True)
    return counter

number_students = int(input("Enter the number of students: "))
out = open_doors(N=number_students)
print(f"The number of doors open for {number_students} students is {out}.")
```

## TEST

![Screen Shot 2022-10-06 at 14 03 40](https://user-images.githubusercontent.com/111761417/194218618-9c1a9144-7116-4b93-9ef4-cf19cf395336.png)


## FLOW DIAGRAM
