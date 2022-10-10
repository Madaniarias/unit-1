# QUIZ016

## CODE
```.py
#Create a function that produces the output given the input shown
#out = blackBlowThree(given = "hello world")
#print(out)

def blackBlowThree(given:str)->str:
    output = ""
    #code comes here
    count = []
    for letter in given.lower():
        if  letter.isalpha():
            #check if letter already in count
            included = -1
            index = 0
            for item in count:
                if letter in item:
                    included = index
                index += 1
            if included == -1:
                count.append([letter,1])
            else:
                count[included][1] += 1
            output += str(count[included][1])
        else:
            output += letter

    return output

test1 = blackBlowThree("hello world")
print(test1)
```

## TEST

![Screen Shot 2022-10-07 at 11 40 40](https://user-images.githubusercontent.com/111761417/194456696-577c5b9f-6e27-452c-934b-bc011ac6f10e.png)

## FLOW DIAGRAM

![image](https://user-images.githubusercontent.com/111761417/194788227-0f8b28d0-c870-4bdb-b4f1-4a844761552d.png)
