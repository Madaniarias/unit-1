# TASK 2

Complete the program for the EV calculator.

## Create charging_log.cvs to store the data

date, charge, duration

12.9.22, 8.878Kwh, 12:32:36

15.9.22, 3.533Kwh, 5:02:23

17.9.22, 6.828Kwh, 9:41:46

18.9.22, 5.425Kwh, 7:43:35

![Screen Shot 2022-09-29 at 2 03 42](https://user-images.githubusercontent.com/111761417/192844834-1a8c5efd-fd2e-4640-911a-a9f4175925bb.png)

## CODE
```.py
#Example program for writing and reading file in python

from my_library import validate_int_input

colors =  ["\033[0;30m", "\033[0;31m", "\033[0;32m", "\033[0;34m"]
end_code = "\033[00m"

intro_msg = f"[colors[2] Welcome to EV calculator{end_code}"
print (intro_msg.center(50, "-"))

#""" lets you print multiple lines in one
menu = """1. Average time per KWh
2. Total KWh used
3. Total charge time
4. Show all data
"""

print("Options".center(50))
print(menu)

option = validate_int_input("Please enter an option [1-4]:　")
while option > 4 or option < 1:
    option = validate_int_input(f"{option} is incorrect. Please enter an option [1-4]: ")

#this is how to read a file
# r: read
#w:write
#a:append
with open ("charging_log.cvs", "r") as file:
    ev_data = file.readlines()

#OPTION 1: Average time per KHw
if option == 1:
    n = 0
    total_energy = 0
    time = 0
    for line in ev_data:
        if n > 0:
            values = line.split(',')
            date = values[0]
            charge = values[1]
            time_split = values[2].split(':')
            time += (int(time_split[0]) * 3600 + int(time_split[1]) * 60 + int(time_split[2]))
            total_energy += float(charge[0:5])
            time_average = int(time / total_energy)
        n += 1
    print(f"{colors[1]} The average time per KWh is {time_average} seconds.{end_code}")


#OPTION 2: Total KWh used
if option == 2:
    i = 0
    total_energy = 0.0
    for line in ev_data:
        if i>0: #this skips the first line
            values = line.split(",")
            charge = values[1]
            charge_cleaned = charge[:5] #without the unit
            charge_float = float(charge_cleaned)
            total_energy += charge_float
        i += 1

    print(f"{colors[1]} Total energy used so far {total_energy} KWh {end_code}")

#OPTION 3: Total charge time
if option ==3:
    total = 0
    n = 0
    for line in ev_data:
        if n > 0:
            all_data = line.split(",")
            full_time = all_data[2]
            full_time = full_time.split(":")
            full_time = int(full_time[0]) * 60 + int(full_time[1])
            total += full_time
        n += 1
    print(f"{colors[1]}The total charge time is {total // 60} hours with {total % 60} minutes{end_code}")

#OPTION 4: show all data
if option == 4:
    i = 0
    counter = 0
    for line in ev_data:
        #strip removes the \n from the string
        line = line.strip()
        counter += 1
        print(f"{colors[2]} Log.No {i} {line}{end_code}")
    i += 1

print("Bye Bye".center(50,"#"))

```

## TESTS
![Screen Shot 2022-10-10 at 8 10 41](https://user-images.githubusercontent.com/111761417/194783907-ed362f20-e201-4ce4-aaa1-36c1f50aa5cd.png)
![Screen Shot 2022-10-10 at 8 10 48](https://user-images.githubusercontent.com/111761417/194783915-413bc406-b79a-4d94-855a-31cc2b2b609f.png)
![Screen Shot 2022-10-10 at 8 10 56](https://user-images.githubusercontent.com/111761417/194783918-e4318c86-58da-4ccb-b85b-a5f7524b9e22.png)
![Screen Shot 2022-10-10 at 8 11 17](https://user-images.githubusercontent.com/111761417/194783921-033616b2-7133-4adc-94c7-6b9076124e72.png)





