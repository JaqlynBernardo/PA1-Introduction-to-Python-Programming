# PA1-Introduction-to-Python-Programming
This repository serves as a submission. This program was made and written in partial fulfillment of the requirements for Advanced Computer Programming and Algorithms (ECE2112).

## Description
This program solves three different given problems using some introductory Python programming essentials, namely: lists, strings, conditional statements, loops, and functions.

## Instructions
Write a Python script/code in the Jupyter Notebook to do the given problems.

### Problem #1: Alphabet Soup Problem
Create a function that takes a string and returns a string with its letters in alphabetical order.

**Solution**
```
def alphabet_soup(word):
    character = list(word)
    character.sort()
    result = ''.join(character)
    print(result)
```

First, the function was declared using the syntax:
```
def function_name(arguments/inputs)
```

The function was named "alphabet_soup" and the input variable was named "word." Inside the function, a variable, "character", was declared, which converts the variable, "word", into a list, which will make the individual letters into elements. Next, the ".sort()" syntax was used on the "character" variable to sort the elements. A "result" variable was declared, which contains a string, and using the ".join()" syntax, the sorted elements of the "character" list will be joined with the empty string. Lastly, the last statement in the function will print the result.

<br> **Testing**
```
alphabet_soup("hello")
alphabet_soup("hacker")
alphabet_soup("thequickbrownfoxjumpsoverthelazydog")
```
**Results**
```
ehllo
acehkr
abcdeeefghhijklmnoooopqrrsttuuvwxyz
```

### Problem #2: Emoticon Problem
Create a function that changes specific words into emoticons. Given a sentence
as a string, replace the words smile, grin, sad, and mad with their corresponding emoticon.
| Word | Emoticon |
| --- | --- |
| Smile | :) |
| Grin | :D |
| Sad | :(( |
| Mad | >:( |

**Solution**
```
def emotify(phrase):
    if "smile" in phrase:
        r = phrase.replace("smile", ":)")
    elif "grin" in phrase:
        r = phrase.replace("grin", ":D")
    elif "sad" in phrase:
        r = phrase.replace("sad", ":((")
    elif "mad" in phrase:
        r = phrase.replace("mad", ">:(")
    else: 
        pass
    print(r)
```

First, the function was declared using the syntax:
```
def function_name(arguments/inputs)
```
The function was named "emotify" and the input variable was named "phrase." Inside the function, there is a series of if and elif statements following the corresponding emoticon conversion shown earlier. Each statement follows this syntax:
```
# If statement
if <Word> in <input_variable>
    var = input_variable.replace("<Word>", "<Emoticon>")
# Elif statement
elif <Word> in <input variable>
    var = input_variable.replace("<Word>", "<Emoticon>")
```
Wherein:
* "var" is the variable used to store the replace syntax, in this case, the variable is "r".
* The input_variable is "phrase".
* <Word> refers to the words to replace.
* <Emoticon> refers to the emoticon that will replace the word.




<br> **Testing**
```
emotify("Make me smile")
emotify("I am mad")
emotify("Why are you sad?")
emotify("You made me grin")
```
**Results**
```
Make me :)
I am >:(
Why are you :((?
You made me :D
```



### Problem #3: Unpacking List Problem
Unpack the list writeyourcodehere into three variables, being first, middle, and last, with middle being everything in between the first and last element. Then print all three variables.

**Solution**
```
lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15] # reference list

# First
print("First:", lst[0])

# Middle
lst_num = len(lst) # number of elements in list
middle = [] # empty set
i = 1 # increment
while i < lst_num - 1:
    middle.append(lst[i])
    i += 1
print("Middle:", middle)

# Last
print("Last:", lst[-1])
```

**Results**
```
First: 1
Middle: [2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14]
Last: 15
```

## Author
Bernardo, Jaqlyn Trazy B.
* Section: 2ECE-C
* Student No.: 2024198347
