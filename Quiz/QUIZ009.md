# QUIZ009

## CODE

```.py
#Create a function that receives as input a string and returns the string ciphered with a shift 13.

def stringciphered (shift:int, user)->str:
    out = ""
    for character in user:
        ord_1 = ord(character)
        if ord_1==32:
            ord_2=32
        else:
            ord_2=ord_1+shift
        if ord_2>122:
            ord_2-=26
        out += chr(ord_2)
    return out



user = input("Introduce the word/sentence you would like to cipher: ")
user = user.lower()
shift = int(input("Introduce the desired shift for your word/sentence: "))
shift = shift%26

test = stringciphered(shift, user)
print(test)
    
```

## TEST

![Screen Shot 2022-09-29 at 1 36 54](https://user-images.githubusercontent.com/111761417/192838073-70113686-3310-43f2-b36f-a22f18db83e0.png)

## FLOW DIAGRAM

![image](https://user-images.githubusercontent.com/111761417/194784508-40b13766-06d4-4d57-a973-4d3592c5edad.png)

