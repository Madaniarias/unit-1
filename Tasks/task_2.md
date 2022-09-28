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
#Example program for writting and reading file in python

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


#solve option 4: show all data
if option == 4:
    i = 0
    for line in ev_data:
        #strip removes the \n from the string
        line = line.strip()
        counter += 1
        print(f"{colors[2]} Log.No {i} {line}{end_code}")
    i += 1

#solve option 2: Total KWh used
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

#solve option 1: Average time per KWh
if option ==1:


print("Bye Bye".center(50,"#"))

```

## TEST

