# Index
```table-of-contents
```

```python
import sys
import keyword
import operator
from datetime import datetime
import os
```
# 1.1Keywords
#keywords
**Keywords are the reserved words in python and can't be used as an identifier** 

```python
print(keyword.kwlist) # list all python keywords
```
['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']

```python
len(keyword.kwlist) # python contains 35 keywords
```
35

# 2.Identifiers
**An identifier us a given to entities like class, function, variables, etc. It helps to differentiate one entity from another.** #identifiers
#ERROR
```python
1var = 10 # Identifier can't start with a digit #ERROR 
val2@ = 35 # Identifier can't use special symbols #ERROR 
import = 125 # Keywords can't be used as identifiers #ERROR 
```

#CORRECT
```python
""" 
Correct way of defining an identifier
(Identifiers can be a combination of letters in lowercase (a to z) or Uppercase (A to z) or digit (0 to 9) )
"""
val2 = 10
val_ = 99
```

# 3.Comments in Python
**Comments can be used to explain the code for more readability** #comments
```python
# single line comments
val1 = 10
# Multiple
# line 
#comments 
val1 = 10
"""
Multiple
Line 
Commments
"""
val1 = 10
```

# 4.Statements
**Instructions that a Python interpreter can execute** #statements
```python
# single line statements
p1 = 10 + 20
p1

# single line statements
p2 = [ 'a', 'b', 'c']
p2

# Multiple line statements
p21 = 20 + 30 \
		+40 + 50 +\
		+70 +80
p21

# Multiple Line statements
p23 = ['a',
			'b',
			'c',
			'd'
			]
p23
```

# 5.Indentation
**Indentation refers to the spaces at the beginning of a code line. It is very important as Python uses indentation to indicate a block of code. if the indentation is not correct we will end up with *Indentation Error*  error**
#if
```python
p = 10
if p == 10:
	print('P is Equal to 10') #CORRECT correct indentation
```
#if
```python
# if indentation is skipped we will encounter "IndentationError: except an indented block"
p = 10
if p == 10:
print('P is equal to 10') #ERROR 
```

#for #loop
```python
for i in range(0,5):
	print(i) #CORRECT indentation
```
#for  #loop
```python
# if indentation is skipped we will encounter "IndentationError: expected an indented block"
for i in range(0,5):
print(i) #ERROR 
```
#less_readable
```python
for i in range(0,5): print(i) #CORRECT indentation but #less_readable 
```
#for #loop
```python
j = 20
for i in range(0,5):
	print(i) # inside the for loop
print(j) # outside the for loop
```

# 6.Docstring
**1. Docstring provide a convenient way of associating documentation with functions, classes, methods or modules.**
**2. They appear right after the definition of a function, methods, class, or module.**
#function
```python
def square(num): #function
	'''Square Function : This function will return the square of a number'''
	return num**2
square(2)
square.__doc__ # we can acess the Docstring using __doc__ method
```

# 7.Variables
**A Python variables is a reserved memory location to store values. A variables is created the moment you first assign a value to it**
```python
p = 30
''' 
id() function return the "Identity" of the object
Th identity of an object - Is an Integer
													- Guaranteed to be unique
													- Constant for this object during its lifetime.
'''
id(p)
hex(id(p)) # Memory address of the variable 
```
140735029552432
'0x7fff6d71a530'

```python
p = 20  # Creates an integer object with value 20 and assigns the variable p to point to that object.
q = 20  # Create new reference q which will point to value 20. p & q will be pointing to same memory location.
r = q  # variable r will also point to the same location where p & q are pointing/
p , type(p), hex(id(p)) # Variable P is pointing to memory location '0x7fff6d71a3f0' where value 20 is stored
q , type(q), hex(id(q))
r , type(r), hex(id(r))
```
(20, int, '0x7fff6d71a530')
(20, int, '0x7fff6d71a530')
(20, int, '0x7fff6d71a530')
![[Z.Attachments/variable.png]]

```python
p = 20
p = p + 10 # variable overwriting
print(p)
```

# 8.Variable Assignment
```python
intvar = 10 # Integer variable
floatvar = 2.57 # Float variable
strvar = "Python Language" # String variable
print(intvar)
print(floatvar)
print(strvar)
```

# 9. Multiple Assignments
```python
intvar, floatvar, strvar = 10,2.57, "Python Language" # Using commas to separate variables and their corresponding values.
print(intvar)
print(floatvar)
print(strvar)
```

```python
p1 = p2 = p3 = p4 = 44 # All variables pointing to same value
print(p1,p2,p3,p4)
```

# 10. Data Types
## Numeric
#Integer #data_type
```python
val1 = 10 # Integer data types
print(val1)
print(type(val1)) # type of object
print(sys.getsizeof(val1)) # size of integer object in bytes
print(val1, " is Integet?", isinstance(val1, int)) # val1 is an instance of int class
```
#Float #data_type 
```python
val2 = 92.78 # float data type
print(val2)
print(type(val2)) # type of object
print(sys.getsizeof(val2)) # size of float objects in bytes
print(val2, " is Float?", isinstance(val2, float)) # Val2 is an instance of float class
```
#complex #data_type 
```python
val3 = 25 + 10j # complex data type
print(val3)
print(type(val3)) # type of object
print(sys.getsizeof(val3)) # size of float object in bytes
print(val3, " is complex?", isinstance(val3, complex)) # val3 is an instance of complex class
```

```python
sys.getsizeof(int()) # size of integer object in bytes
sys.getsizeof(float()) # size of float object in bytes
sys.getsizeof(complex()) # size of comlex object in bytes
```

# 11.Boolean
**Boolean data type can have only two possible values True or False**
```python
bool1 = True
bool2 = False
print(type(bool1))
print(type(bool2))
isinstance(bool1, bool)
bool(0)
bool(1)
bool(None)
bool (False)
```

# 12.Strings
## String Creation 
#sting #data_type  
```python
str1 = "Hello Python"
print(str1)

mystr = 'Hello World' # Define string using single quotes
print(mystr)

mystr = "Hello World" # Define string using Double quotes
print(mystr)

mystr = '''Hello
						World''' # define string using triple quotes
print(mystr)
mystr = """Hello
						World"""
print(mystr)
```

```python
mystr = ('Happy '
					'Monday '
					'Everyone')
print(mystr)

mystr2 = 'woohoo '
mystr2 = mystr2*5
print(mystr2)

len(mystr2) # length of  string
```

## String Indexing
#indexing #string 
![[Z.Attachments/string.png]]
```python
str1 = "HELLO PYTHON"
print(str1)

str1[0] # First character in string "str1"
# H
str1[len(str1) - 1] # Last character in string using len function
# N
str1[-1] # Last charcter in string 
# N
str1[6] # french 7th element of the string
# P
str1[5]
# ' '
```

## String Slicing
#slicing #string 
```python
str1[0:5] # String slicing - Fetch all characters from 0 to 5 index location excluding the character at loc 5.
# 'HELLO'
str1[6:12] # String slicing - Retrieve all characters between 6 - 12 index loc excluding index loc 12.
# 'PYTHON'
str1[-4:] # Retrieve last four characters of the string
# 'THON'
str1[-6:] # Retrieve last six characters of the string
# 'PYTHON'
str1[:4] # Retrieve first four characters of the string
# 'HELL'
str1[:6] # Retrieve first six characters of the string
# 'HELLO '
```

## update and delete string
#update #delete #string
```python
str1
#Strings are immutable which means elements of a string cannot be changed once they have been assigned.
str1[0:5] = 'HOLAA' #ERROR 
del str1 #delete a string 
print(str1)
```

## String concatenation
```python
# String Concatenation
s1 = "Hello"
s2 = "Name"
s3 = s1 + s2
print(s3)

print(" ==============================================")
#string concatenation 
s1 = "Hello"
s2 = "Your Name"
s3 = s1 + " " + s2
print(s3)
```

## Iterating through a string
#iterating #string #enumerate #less_readable 
```python
mystr1 = "Hello Eveyone"
#iterating 
for i in mystr1:
	print(i)
print(" ==============================================")
for i in enumerate(mystr1):
	print(i)
print(" ==============================================")
list(enumerate(mystr1)) #enumerate method adds a counter to an iterable and returns it in a form of enumerate object. #less_readable 
```

## string Membership 
#string #membership
```python
#string #membership 
mystr1 = "Hello Everyone"
print ('Hello' in mystr1) # Check whether substring "Hello" is present in string "mysrt1"
print ('Everyone' in mystr1) # Check whether substring "Everyone" is present in string "mysrt1"
print ('Hi' in mystr1) # Check whether substring "Hi" is present in string "mysrt1"
```
## String Partitioning
#string #partioning
```python
""" 
The partition() method searches for a specified string and splits the string into a tuple containing three elements.
 - The first element contains the part before the argument string.
 - The second element contains the argument string.
 - The third element contains the part after the argument string.
"""
str5 = "Natural language processing with Python and R and Java"
L = str5.partition("and")
print(L)
```
#string #partioning 
```python
"""
The rpartition() method searches for the last occurance of the specified string and splits the string into a tuple containing three elements.
- The first element contains the part before the argument string
- The second elements contains the argument string
- The third elements contains the part after the argument string
"""
str5 = "Natural language processing with Python and R and Java"
L = str5.rpartition("and)
print(L)
```
#string #function #remove #white_space #strip 
```python
mystr2 = "     Hello Everyone     "
mystr2

mystr2.strip() #remve #white_space from begining and end
mystr2.rstrip() #remove all #white_space at the end of the string
mystr2.lstrip() #remove all #white_space at the begining of the string
```
#strip 
```python
mystr2 = "****************Hello Everyone**************All the Best ******"
print(mystr2)

mystr2.strip('*') #remove all '*' characters from begining and end of the string
mystr2
mystr2.rstrip('*') #remove all '*' characters at the end of the string
mystr2
mystr2.lstrip('*') #remove all '*' characters at the begining of the string
```
#string #lower #upper #replace  #return #upper_case #lower_case
```python
mystr2 = "      Hello Everyone      "
print(mystr2)
mystr2.lower() #return whole string in #lower_case 
mystr2.upper() #return whole string in #upper_case 
mystr2.replace("He" , "Ho") #replace substring "He" with "Ho"

```