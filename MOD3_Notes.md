
#Running your Python Code
to run your scripts, type in "py" in the command prompt. It creates a python environment and a >>> will be a prompt for you to type your code
you can also run it in a "python terminal" by right clicking but this will not work well when trying to reference other files in the same directory
you can also type "python" and then type your python file (.py) extension to run your code

#Data Types
Integers. they are used to perform mathematical equations. Positive or negative whole numbers. Limit 32k in 16 bits. Limit 2,147,483,647 in 32 bits.
Booleans. they can only have one of two values: true or false
Float or Float point numbers. numbers with decimals
String. you know this. it's what you're typing now
Tuple. are like lists except they can not be changed
Lists. are lists. editable. also similar to arrays

#Codes
type () ... will return the data type of what is in the parenthesis
    examples: int, float, tuple, str, bool
print() ... will print whatever you call or index
    you can call a vairable without print if wanted
    in either case, you can display part of your list by direct listing (01,2,3) or from last, or second to last by using negatives (-1,-2,-3)
List[] ... declares a list or array
    you can use "slicing" to pull certain things
    example list[start:end] will display your whole list beginning to end
    another example would be to call a range. for example counties[0:2]
    If you omit the first part of the range, it will assume and begin at zero ... counties[:2]...conversely, omitting the end also goes to the end of the list
.append() ... adds to your list manually
    your list name goes first before " . "
    counties.append("El Paso")
.insert(index, obj) ... adds item and where to add
    counties.insert(2, "El Paso")
.remove() ... removes objects from your list
     it will return and tell you what is removed
.pop() will remove items in your list based on position, not by object name (1,2,3 or -1, -2 etc)
{key:value} or dict() works like a dictionary. you set definitions to key-value pairs. enter your list or name of dictionary first followed by dict()
    objects can be any type such as integers, floating decimal points, strings, booleans, etc.
    Keys must be immutable objects like integers, floating-point decimals, or strings.
len() will return the length of your list, arrary, or dictionary
    example: len(counties_dict)
items() displays items in a dictionary (not lists)
    example: counties_dict.items()
dict_keys ... returns all the keys in a dictionanary
dict_values ... returns are the values in a dictionary
get() returns the value of a key
    example: counties_dict.get("Denver")
int(input()) 
    example: my_votes = int(input("How many votes did you get in the election?"))
    total_votes = int(input("What is the total votes in the election?"))
    percentage_votes = (my_votes / total_votes) * 100
    print("I recieved" + str(percentage_votes) + "% of the total votes.")
if () == : ...
    example if len(counties) > 2:
    booleans: >  >=  < <= == !=
    != means not equal to
    == is equal to


#Notes
Equal sign is used in multiple ways. One "=" assigns values. "==" is how you produce a result of an if statement or conditional
When typing integers greater than 999 do not use a comma it gets confused
Always start out with declaring your variables, see "=" notes above
When declaring variables, do not uses spaces, use underscores. First character can not be a number
There are keywords used in Python, so you want to avoid using these words for declaring variables:
    false, def, if, raise, none, del, import, return, true elif, in try, and, else, is while, as, except, lambda, with, assert, finally, nonlocal, yield, break, for, not, class, from, or, continue, global, pass
    You can type help("keywords") in the command prompt to get this list



Arithmetic Operators
    "+" adds two numbers, I.E.  X+Y
    " - " subracts two numbers
    " * " multiplies two numbers, I.E.  x*y
    " / " Divides two numbers
    " % " known as the modulus. can use in place of " / " it will divide two numbers and return the remainder, I.E. x % y 
    " // " this is called floor division, it will divide the two numbers and return an integer (decimal number)
    " ** " Raises a number to a power. I.E.  x**y is x to the power y









