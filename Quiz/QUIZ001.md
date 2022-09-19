# QUIZ001

## CODE

```.py
user = input("Enter a word/s: ")
words = user.split(' ')
count = 0
while count < len(words):
        if len(words[count]) > 2:
          print(f"{words[count][0]}{str(len(words[count])-2)}{words[count][-1]}")
          count = count + 1
        else:
          print(words[count])
          count = count + 1
         
```

## TEST

![Screen Shot 2022-09-19 at 21 29 08](https://user-images.githubusercontent.com/111761417/191017395-20f04306-ee95-466f-9b14-2255f8789590.png)


## PICTURE

![QUIZ001](https://user-images.githubusercontent.com/111761417/190468188-ae7f84ea-2b2c-4b91-aed2-fda1e86ea682.jpg)
