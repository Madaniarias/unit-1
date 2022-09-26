# QUIZ008

## CODE

```.py
#A hotel has 10 floors and 10 rooms on each floor. Write a program that prints the names of all rooms in the following format:
#[HL]  Use a function receive the room number (1-100) and prints the Room floor location and number
output = []
counter = 1
color_red = "\33[0;31m"
end_code = "\033[00m"
print(f"{color_red}In this hotel we have the following rooms located in their respective floors: {end_code}")
for floor in range(10):
    for room in range(10):
        print(f"{counter}-Room {floor+1}F{room+1:02}")
        output.append(f"{floor+1}F{room+1:02}")
        counter += 1

user_room_number = input("Introduce your room number:")
print(f"Your room number is {output[int(user_room_number)-1]}")

```
## TEST

![Screen Shot 2022-09-27 at 2 14 30](https://user-images.githubusercontent.com/111761417/192339659-857bf2ef-9014-4081-92c4-3c13564dd5bd.png)
![Screen Shot 2022-09-27 at 2 16 34](https://user-images.githubusercontent.com/111761417/192339911-c2d03af0-885e-4f9e-b08e-f53ee154832b.png)

## FLOW DIAGRAM

