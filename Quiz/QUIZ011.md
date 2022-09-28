# QUIZ011

## CODE
```.py
#Create a function that shows the days of your birthday's month for the year 2022
end_color = "\33[0m"
bold_purple = "\33[1;35m"
def bestmonth (month:int)->str:
    out = " "
    week_days = ["Sa","Su","Mo","Tu","We","Th","Fr"]
    for d in range(1,32):
        days = f"{week_days[d%7]} {d} \n"
        out += days
    return out

#using the function
print(f"{bold_purple}The days of the best month, October, for the year 2022 are the following: {end_color}")
month = 31
test1 = bestmonth(month)
print (test1)
```

## TEST

![Screen Shot 2022-09-29 at 1 06 12](https://user-images.githubusercontent.com/111761417/192830119-2cd168f4-ae10-44ce-972f-2bc144332a71.png)

## FLOW DIAGRAM

![image](https://user-images.githubusercontent.com/111761417/192832985-9e892326-ec12-4a26-8227-96fb7542848e.png)

