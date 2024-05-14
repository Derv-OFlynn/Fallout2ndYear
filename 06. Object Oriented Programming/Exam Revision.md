3 hours

Section A - Python Do 2 out of 3
Section B - Java Do 2 out of 3

# <mark style="background: #AD21D9;">Classes</mark>

### <mark style="background:#AD21D9;">What is a class?</mark>

```Python

class Student(object):
	"""Simple student class"""

def __init__(self, first="", last="", id=0, grade=0):  # initializer
   self.first_name_str = first
   self.last_name_str = last
   self.id_int = id
   self.grade = grade

def __str__(self):
	return "{} {}, ID:{}".format(self.first_name_str, self.last_name_str, self.id_int)

def print_grade(self):
   return "Grade is: {}".format(self.grade)

student1 = Student("Lucas", "Rizzo", 1, 100)

print(student1.print_grade())
```


<mark style="background:#AD21D9;">Object Oriented Programming</mark> is a way to think about "objects" in a program (such as variables, functions, etc)

A program becomes less a list of instructions and more a set of objects and how they interact

### <mark style="background:#AD21D9;">Responding to "messages":</mark>

As a set of interacting objects, each object responds to "messages" sent to it

The interaction of objects via messages makes a high level description of what the program is doing

### <mark style="background:#AD21D9;">Everything in Python is an object:</mark>

As we said previously - everything in Python is an object

Thus Python embraces OOP at a fundamental level

### <mark style="background:#AD21D9;">Type vs Class:</mark>

There is a strong similarity between a type and a python class

<mark style="background:#AD21D9;">Types</mark> includes list, dict, str

They are suitable for representing different data

Respond to different messages regarding the manipulation of that data

Python is fundamentally an OOP language

When we call a constructor such as list or str, we are making a new object

Those objects have attributes and respond to methods

We can sort a list by calling the method `my_list.sort()`, change a string to lowercase with the method `my_str.lower()`

### <mark style="background:#AD21D9;">Encapsulation:</mark>

Hiding the details of the underlying data structures means that the changes can be made to the object, while the flow of messages (methods and their results) can stay the same

Thus the underlying implementation can change but its intended effect stay the same

This is known as <mark style="background:#AD21D9;">encapsulation</mark>

### <mark style="background:#AD21D9;">OOP principles:</mark>

<mark style="background:#AD21D9;">Encapsulation:</mark> hiding design details to make the program clearer and more easily modified later

<mark style="background:#AD21D9;">Modularity:</mark> the ability to make objects stand alone they can be reused

<mark style="background:#AD21D9;">Inheritance:</mark> create a new object by inheriting many object characteristics while creating or over-riding for this object

<mark style="background:#AD21D9;">Polymorphism:</mark> Allow one message to be sent to any object and have it respond appropriately based on the type of object it is (such as `count` and `len` functions

### <mark style="background:#AD21D9;">Classes vs Instances:</mark>

You define a class as a way to generate new instances of that class

Both the instances and the classes are themselves objects

The structure of an instance starts out the same, as dictated by the class

The instances respond to the messages defined as part of the class

### <mark style="background:#AD21D9;">Why a class?</mark>

We make classes because we need more complicated, user-defined data types to construct instances we can use

Each class has potentially two aspects:
- The <mark style="background:#AD21D9;">data </mark>that each instance might contain
- The <mark style="background:#AD21D9;">messages </mark>that each instance can respond


### <mark style="background:#AD21D9;">Our first class:</mark>

The standard way to name a class in Python is called <mark style="background:#AD21D9;">CamelCase</mark>:
- Each word of a class begins with a capital letter
- No underlines
- Makes recognising a class easier

![](https://i.imgur.com/CjWdZsP.png)

### <mark style="background:#AD21D9;">Constructor:</mark>

When a class is defined, a function is made with the <mark style="background:#AD21D9;">same name as the class</mark>

This function is called the <mark style="background:#AD21D9;">constructor</mark>. By calling it, you create an instance of the class

We can affect this creation, but by default Python can make an instance

### <mark style="background:#AD21D9;">dir() function:</mark>

The `dir` function lists all the attributes of a class

You can think of these as keys in a dictionary stored in the class

### <mark style="background:#AD21D9;">dot reference</mark>

We can refer to the attributes of an object by doing a dot reference of the form `obj.attribute`

The attribute can be a variable or a function

It is part of the object, either directly or by that object being part of a class

### <mark style="background:#AD21D9;">How to make an object-local value:</mark>

Once an object is made, the data is made the same way as in any other Python situation, by assignment

Any object can thus be augmented by adding a variable

### <mark style="background:#AD21D9;">Class Instance Relationship:</mark>

Because each instance has as its type that it was made from, an instance remembers its class

This is often called the<mark style="background:#AD21D9;"> instance-of</mark> relationship stored in the <mark style="background:#AD21D9;">__class__</mark> attribute of the instance

![](https://i.imgur.com/qiqsWke.png)


### <mark style="background:#AD21D9;">Object Scope Rule:</mark>

The first two rules in the object scope are:
1. First, look in the object itself
2. If the attribute is not found, look up to the class of the object and search for the attribute there

### <mark style="background:#AD21D9;">Methods:</mark>

A method and a function are closely related. They are both "small programs" that have  parameters, perform some operation and potentially return a value

The main difference is that methods are functions tied to a particular object

### <mark style="background:#AD21D9;">Difference in calling:</mark>

Functions are called by name anywhere in the program, methods are called in the context of an object:

```Python

function:
	do_something(param1)
method:
	obj.do_something(param1)
```

This means that the object that the method is called on is <mark style="background:#AD21D9;">always implicitly a parameter</mark>

### <mark style="background:#AD21D9;">Difference in definition:</mark>

Methods are defined <mark style="background:#AD21D9;">inside </mark>the suite of a class

Methods always bind the first parameter in the definition to the object that called it

This parameter can be named anything, but traditionally it is named self


```Python
class MyClass(object):
	def my_method(self, param1):
		suite
```


`self` is an important variable. In any method it is bound to the object that called the method

Through `self` we can access the instance that called the method

![](https://i.imgur.com/0gdzmHd.png)


### <mark style="background:#AD21D9;">Self is bound for us:</mark>

When a dot method call is made, the object that called the method is <mark style="background:#AD21D9;">automatically </mark>assigned to `self`

We can use `self` to remember, and therefore refer, to the calling object

To reference any part of the calling object, we must always precede it with `self`

The method can be written genetically, dealing with calling objects through self

### <mark style="background: #AD21D9;">Overloading:</mark>

### <mark style="background:#AD21D9;">Encapsulation in OOP:</mark>

<mark style="background:#AD21D9;">Encapsulation:</mark>  hides details of the implementation so that the program is easier to read and write  

<mark style="background:#AD21D9;">Modularity:</mark> make an object so that it can be reused in other contexts

These provide an interface (the methods) that are the approved way to deal with the <mark style="background:#AD21D9;">class</mark>

### <mark style="background:#AD21D9;">Private attributes/methods:</mark>

Many OOP languages allow you to make an attribute or method <mark style="background:#AD21D9;">private </mark>

Private means <mark style="background:#AD21D9;">not accessible</mark> by the <mark style="background:#AD21D9;">class user</mark>, only the <mark style="background:#AD21D9;">class developer</mark>

There are advantages to controlling who can access the instance values

<mark style="background:#AD21D9;">Example:</mark>

```Python

class NewClass(object):
	def __init__(self, attribute="default", name="Instance"):
		self.name = name
	    #The double underscore indicates privacy
		self.__attribute = attribute

	def __str__(self):
		return "{} has attributes {}".format(self.name, self.__attribute)
```


### <mark style="background:#AD21D9;">Access modifiers in Java:</mark>


<mark style="background:#AD21D9;">public:</mark> accessible anywhere by anybody

<mark style="background:#AD21D9;">private:</mark> accessible within the class only

<mark style="background:#AD21D9;">protected:</mark> accessible within the class or subclass

```Java
// Java class

public class Person 
{
	private String firstName;
	private String surname;

	public String getFirstName()
	{
		return firstName;
	}

. . .
}
```

### <mark style="background:#AD21D9;">Access modifiers in Python - public:</mark>

```Python

class Person:
	def __init__(self, n, age):
	  self.name = n
	  self.age = age

p = Person('Mary', 20)
print(p.name)  #Will print Mary
```


Note that the class variable (<mark style="background:#AD21D9;">name</mark>) and the parameter in the constructor (<mark style="background:#AD21D9;">n</mark>) doesn’t have to have the same name!

However, following the naming conventions, in practice they often do

### <mark style="background:#AD21D9;">Access modifiers in Python - Private:</mark>

<mark style="background:#AD21D9;">Private:</mark> use <mark style="background:#AD21D9;">double underscore</mark> as the start of the variable or method name

```Python

class Person:
	def __init__(self, name, age):
		self.__name = name
		self.age = age
	
p = Person('Mary',  20)

print(p.name)    
#^  Error!  AttributeError: 'Person' object has no attribute 'name'

print(p.__name)
#^  Error!   AttributeError: 'Person' object has no attribute '__name'

print(p._Person__name)  
#^  Returns 'Mary', but it is not a good practice. Other languages would not allow this.
```


What is the right way to access private attributes? Through public methods  

```Python

class Person:
	def __init__(self, name, age):
		self.__name = name
		self.age = age

def get_name(self):
	return self.__name

def set_name(self, name):
	self.__name = name

p = Person('Mary',  20)
print(p.get_name()) #← will print Mary
p.set_name('John') #← will update name
print(p.get_name()) #← will print John   
```

Get/set methods <mark style="background:#AD21D9;">hide </mark>the attributes of class from other classes.

No <mark style="background:#AD21D9;">accidental modification</mark> of the data happens.

### <mark style="background:#AD21D9;">Comments on privacy:</mark>

<mark style="background:#AD21D9;">Classes:</mark>

Use privacy only for attributes and methods that are completely internal to operation of object:
- Public attributes (variables, methods) are available to everyone (designer and programmer).
- Private attributes (variables, methods) are available only to the designer.

<mark style="background:#AD21D9;">Objects:</mark>
- Minimise direct reading of objects attributes
- Avoid directly altering objects attributes
- Never directly access objects private attributes or methods

### <mark style="background:#AD21D9;">Object-Oriented Programming - Operator Overloading:</mark>

<mark style="background:#AD21D9;">Another aspect:</mark>
- A new aspect we should consider in OOP is <mark style="background:#AD21D9;">consistency</mark>
- A new class should be consistent with the rules of the language.
- It should respond to standard messages, it should behave properly with typical functions (assuming the type allows that kind of call).


<mark style="background:#AD21D9;">Example - Rational Number class:</mark>

Consider a <mark style="background:#AD21D9;">Fraction number</mark> class.

It should respond to:
- construction
- printing
- arithmetic ops (+, -, *, /) 
- comparison ops (<, >, <=, >=)

```Python
r1 = Fraction(1,2)     #create the fraction 1/2

r2 = Fraction(3,2)     #create the fraction 3/2

r3 = Fraction(3)       #default denominator is 1,

# so really creating 3/1

r_sum = r1 + r2          #use "+" in a familiar way

print(r_sum)            # use " print " in a familiar way
4/2                  

if r1 == r2:     # use equality check "==" in a familiar way
	print('equal')
else:
	print('not equal')

not equal
print(r3 - r2)    # combine arithmetic and printing in a familiar way

3/2

```


Python can distinguish which <mark style="background:#AD21D9;">operator </mark>to use based on <mark style="background:#AD21D9;">types</mark>

Python provides more standard methods that represent the action of standard functions in the language. By defining them in our class, Python will call them in the "right way"

### <mark style="background:#AD21D9;">More on Type:</mark>

A class is essentially a new type

When we make an instance of a class, we have made an object of a particular type

For example:
- 1.36 is a float
- ` my_instance = MyClass()`  my_instance is of the type MyClass  

### <mark style="background:#AD21D9;">Introspection:</mark>

- Python does <mark style="background:#AD21D9;">not </mark>have a <mark style="background:#AD21D9;">type </mark>associated with any variable, since each variable is allowed to reference any object
	- Unlike C and Java, for example, (int i)

However, we can <mark style="background:#AD21D9;">query </mark>any <mark style="background:#AD21D9;">variable </mark>as to what <mark style="background:#AD21D9;">type </mark>it presently references

This is often called <mark style="background:#AD21D9;">introspection</mark>, that is, while the program is running we can determine the type a variable references

### <mark style="background:#AD21D9;">Python Introspection operations:</mark>

`type(variable)`: returns its type as an object

`isinstance(variable,type)`: returns a boolean indicating if the variable is of that type

<mark style="background:#AD21D9;">Example:</mark>

```Python

def special_sum(a, b):
""" Sum two ints or convert params to ints and add. return 0 if conversation fails."""

if type(a) == int and type(b) == int:
   result = a + b
else:
	try:
		result = int(a) + int(b)
	except ValueError:
		result = 0

return result
```

### <mark style="background:#AD21D9;">What does var1 + var2 mean?</mark>

So what does `var1 + var2` mean?

Answer: it <mark style="background:#AD21D9;">depends </mark>on the <mark style="background:#AD21D9;">type</mark>

The `+` operation has two operands. What are their types?

Python uses <mark style="background:#AD21D9;">introspection </mark>to find the type and then select the correct operator

What does var1+var2 do?
- with two <mark style="background:#AD21D9;">strings</mark>, we get concatenation
- with two <mark style="background:#AD21D9;">integers</mark>, we get addition
- with an <mark style="background:#AD21D9;">integer </mark>and a <mark style="background:#AD21D9;">string </mark>we get:

```Python

Traceback (most recent call last):File "<pyshell#9>", line 1, in <module> 1+'a'

TypeError: unsupported operand type(s) for +:   'int' and 'str'
```

### <mark style="background:#AD21D9;">Operator overloading:</mark>

The plus operator + is <mark style="background:#AD21D9;">overloaded</mark>

That means the operator can do/mean different things (have multiple/overloaded meanings) depending on the types involved

If python does not recognize the operation and that combination of types, you get an error

### <mark style="background:#AD21D9;">Python overload operations:</mark>

Python provides a set of operators that can be overloaded. You <mark style="background:#AD21D9;">can't overload all</mark> the operators, but you can overload many

Like all the special class operations, they use the two underlines before and after their name

They come in three general classes:
- <mark style="background:#AD21D9;">numeric type</mark> operations (+,-,<,>,print etc.)
- <mark style="background:#AD21D9;">container </mark>operations ([ ], iterate, len, etc.)
- <mark style="background:#AD21D9;">general </mark>operations (printing, construction)

![](https://i.imgur.com/UZqe1UW.png)


<mark style="background:#AD21D9;">Example:</mark>

```Python
class MyClass(object):
	def __init__(self, param1=0):
	""" Constructor. Sets attribute value to param 1, default is 0"""
	print("in constructor")
	self.value = param1

	def __str__(self):
		""" Convert value attribute to string"""
		print("in str")
		return "Val is: {}".format(str(self.value))

	def __add__(self, param2):
		""" Perform addition with param2, a MyClass instance. Return a new MyClass instance with sum as a value attribute"""

		print("in add")
		result = self.value + param2.value 
		return MyClass(result)
```

### <mark style="background:#AD21D9;">How does v1 + v2 map to __add__?</mark>

```Python

v1 + v2
#is turned, by Python, into
v1.__add__(v2)
```

These are exactly equivalent expressions. It means that the first variable calls the `__add__` method with the second variable passed as an argument

v1 is bound to `self`, v2 bound to `param2`

### <mark style="background:#AD21D9;">Calling __str__:</mark>

When does the `__str__` method get called? Whenever a string representation of the instance is required:
- <mark style="background:#AD21D9;">Directly</mark>, by saying  `str(my_instance)`
- <mark style="background:#AD21D9;">Indirectly</mark>, calling `print(my_instance)`

### <mark style="background:#AD21D9;">Simple Rational Number class:</mark>

A <mark style="background:#AD21D9;">Rational </mark>is represented by two integers: the <mark style="background:#AD21D9;">numerator </mark>and the <mark style="background:#AD21D9;">denominator</mark>

We can apply many of the numeric operators to Rational

<mark style="background:#AD21D9;">Example - Fraction class:</mark>

```Python

class Fraction(object):
""" Fraction with numerator and denominator. Denominator parameter defaults to 1"""



def __init__(self, numer, denom=1):
   print('in constructor')
   self.numer = numer
   self.denom = denom

def __str__(self):
	""" String representation for printing """
	print('in str')
	return str(self.numer) + '/' + str(self.denom)
```


### <mark style="background:#AD21D9;">The __init__ method:</mark>

Each instance gets an attribute `numer` and `denom` to represent the numerator and denominator of that instance's values  

```Python
def __init__(self, numer, denom=1):
	print('in constructor')
	self.numer = numer
	self.denom = denom
```

### <mark style="background:#AD21D9;">Rational number - Addition:</mark>

Remember how we add fractions:
- if the denominator is the same, add the numerators
- if not, find a new common denominator that each denominator divides without remainder.
- modify the numerators and add

<mark style="background:#AD21D9;">__add__:</mark>

```Python

def __add__(self, param):
	""" Add two Rationals . Allows int as a parameter"""
	print('in add')
	
	if type(param) == int:  # convert ints to Rationals
		param = Fraction(param)
	
	if type(param) == Fraction:
		# find a common denominator
		# ps: the optimal algorithm would find the lowest common denominator
		
		common_denominator = self.denom * param.denom
		numerator_sum = (common_denominator * self.numer / self.denom) + (
		common_denominator * param.numer / param.denom)
		return Fraction(int(numerator_sum), common_denominator)
	
	else:
		print('wrong type')  # problem : some type we cannot handle
		raise (TypeError)
```

<mark style="background:#AD21D9;">__sub__:</mark>

```Python
def __sub__(self, param):
	""" Subtract two Rationals """
	
	print('in sub')
	# subtraction is the same but with '−' instead of '+'
	# ps: the optimal algorithm would find the lowest common
	# denominator
	
	common_denominator = self.denom * param.denom
	numerator_diff = (common_denominator * self.numer / self.denom) - (common_denominator * param.numer / param.denom)

	return Fraction(int(numerator_diff), common_denominator)
```

<mark style="background:#AD21D9;">__eq__:</mark>


```Python
def __eq__(self, param):
	""" Compare two Rationals for equality, return Boolean """
	
	print('in eq')
	return abs((self.numer / self.denom) - (param.numer / param.denom)) < 0.0001

		```


<mark style="background:#AD21D9;">Example:</mark>

```Python

one_half = Fraction(1, 2)
two_fifths = Fraction(2, 5)

sum_Fraction = one_half + two_fifths
print(sum_Fraction) # 9/10

two = Fraction(2)
print(two - one_half) # 3/2

five_tenths = Fraction(5, 10)

if one_half == five_tenths:
	print("equal")

multiplication = one_half * two_fifths
print(multiplication) # 2/10
```

### <mark style="background:#AD21D9;">Summary:</mark>

Overloading operators: A+B maps to `A.__add__(B)`

which maps to `__add__(self, param)` by mapping A to self and mapping B to param

Expanded class organization:

```Python

class ClassName(object):
	def __init__ (self,param):
		self.value == param
		
	def __add__(self,param):
		the_sum = self.value + param.value
		return ClassName(the_sum)
		
	def __radd__(self,f):
		return self.__add__(f)
		
	def __str__(self):
		return str(self.value)
```


# <mark style="background: #AD21D9;">Strings:</mark>


### <mark style="background:#AD21D9;">Strings</mark> 

A string is a sequence of characters. In python they are enclosed between ' ' or " ". 

<mark style="background:#AD21D9;">Non-printable characters:</mark> 
These can be inserted directly in the string, preceded by a backslash
- newline ``\n``
- tab ``\t``


<mark style="background:#AD21D9;">Inserting an apostrophe:</mark> 

```Python
#mix up the quotes:
a = "knight's"

#use the escape character:
b = 'knight\'s'  
``` 

### <mark style="background:#AD21D9;">The Index:</mark> 

Because the elements of a string are a sequence, we can associate each element with an index, a location in the sequence:

positive values count up form left, beginning with the index 0 negative values count down from the right, starting with -1

![](https://i.imgur.com/dvAjkwJ.png)
 

### <mark style="background:#AD21D9;">Accessing an element:</mark> 

Each particular element of the string is accessed by the index of the element surrounded by square brackets
- hello_str = "Hello World"
- print(hello_str[1]) ⇒ prints e
- print(hello_str[-1] ⇒ prints d
- print(hello_str[11] ⇒ ERROR


### <mark style="background:#AD21D9;">String Slicing:</mark> 

<mark style="background:#AD21D9;">Slicing</mark> is the ability to select a subsequence of the overall sequence (where the sequence can be a string, list, etc)

Uses the syntax `[start:finish]` where:
- `start`  is the index of where we start the subsequence
- `finish` is the index of <mark style="background:#AD21D9;"> _one after_ </mark> the end of the subsequence

If either `start` or `finish` are not provided (empty), it defaults to the beginning of the sequence for `start` and the end of the sequence for `finish` 

![](https://i.imgur.com/VLpwAf3.png)

### <mark style="background:#AD21D9;">Extended Slicing:</mark> 

We can also list three arguments:

```Python
[start: finish: step]
```

Defaults are:
- `start` is index 0
- `finish` is length of the string (index after last)
- `step` is 1

![](https://i.imgur.com/gfZXnMI.png)
 

How to make a copy of a string:

```Python
my_str = "Hello World"
new_str = my_str[:] 
```

Python interprets a negative step as going backwards. For example, to reverse a string

```Python
my_str= "hello world"
reverse_str = my_str[::-1]  
```

The output will be "dlrow olleh"
 
### <mark style="background:#AD21D9;">String Operations:</mark> 

<mark style="background:#AD21D9;">Sequences are Iterable:</mark> 
- A for-loop iterates through each element of a sequence in order
- For a string, this means character by character

<mark style="background:#AD21D9;">For loop:</mark>

```Python
my_str = "abc"

for char in my_str:
print(char) 
```

The loop prints each character in a string in order and ends when it reaches the end of the string 

<mark style="background:#AD21D9;">Basic String Operations:</mark> 

| Name        | Operation | Example                                  |
| ----------- | --------- | ---------------------------------------- |
| Length      | len()     | ![](https://i.imgur.com/2S2R1Xe.png)<br> |
| Concatenate | +         | ![](https://i.imgur.com/pBDYht9.png)<br> |
| Repeat      | *         | ![](https://i.imgur.com/hQC96uM.png)<br> |

Both + and * on strings create a new string, they do not modify the arguments

Order of operation:
- Important for concatenation
- Irrelevant for repetition

The types of operands required:
- For concatenation you need two strings
- For repetition you need a string and an int
  
### <mark style="background:#AD21D9;">The type() function:</mark> 

You can check the type of the value associated with a variable using type() 

```Python
x = "Hello World"
type(x) 
#output is <type 'str'> 
```

### <mark style="background:#AD21D9;">String representation:</mark> 

Every character in python is mapped to an integer

UTF-8, a subset of unicode, is such a mapping

`ord()`  takes a character and returns its UTF-8 int value

`chr()` take an int and returns the UTF-8 character
 
### <mark style="background:#AD21D9;">Membership Operator:</mark> 

We can use the `in` operator to check if a string exists in another string (substring). It returns `True` or`False` 

```Python
my_str = 'aabbccdd'

'a' in my_str   ⇒ True
'abb' in my_str ⇒ True
'x' in my_str   ⇒ False
```

### <mark style="background:#AD21D9;">Strings are Immutable:</mark> 

Strings are <mark style="background:#AD21D9;">immutable</mark>, meaning you cannot change it when it has been created

```Python
a_str = 'spam'
a_str[1] = 'l' 🡪 ERROR
```

You can make another string using the original one (copy, slice, etc)

```Python
new_str = a_str[:1] + 'l' + a_str[2:]
a_str   🡪 'spam'
new_str 🡪 'slam'
```
  
### <mark style="background:#AD21D9;">String methods and functions:</mark> 

<mark style="background:#AD21D9;">Functions:</mark> 
- A <mark style="background:#AD21D9;">function</mark> is a piece of code that performs some operation. Its details are hidden, only its interface is provided.
- A function takes some number of inputs (arguments) and returns a value based on the arguments and the functions operations.
- Example:

```Python
s = "Hello"
print(len(s))
#output is 5 
```


<mark style="background:#AD21D9;">Methods:</mark> 

A <mark style="background:#AD21D9;">method</mark> is similar to a function, only it is applied in the context of a particular object. Methods are tied to the type of the object calling it. Each object has different methods.

This is indicated by the <mark style="background:#AD21D9;">dot notation</mark> 

```Python
my_str = "Python Rules!"
my_str.upper()
print(my_str)
#output is "PYTHON RULES!"
```

The upper() method was called in the context of my_str, indicated by the dot between them

Find() method:

```Python
my_str = "hello"
my_str.find('l')

#returns 2 
```

### <mark style="background:#AD21D9;">Python String methods:</mark> 

 ![](https://i.imgur.com/oYjF8dt.png)
 
### <mark style="background:#AD21D9;">Chaining methods:</mark> 

Methods can be chained together.
- Perform the first operation, yielding an object
- Use the yielded object for the next method

```Python
my_str = 'Python Rules!'
my_str.upper() ⇒  'PYTHON RULES!'

my_str.upper().find('O')
#returns 1 
```

### <mark style="background:#AD21D9;">Optional Arguments:</mark> 

Some methods have optional arguments:

If the user doesn't provide one of these, as default is assumed

For example, `find()` has a default second argument of 0, the index at which the search begins

```Python
a_str = 'He had the bat'
a_str.find('t')   ⇒ 7    # 1st 't', start at 0
a_str.find('t',8) ⇒ 13   # 2nd 't'
```


### <mark style="background:#AD21D9;">Nesting methods:</mark> 

You can nest some methods, meaning you can use the result of one method as an argument for another

```Python
a_str.find('t', a_str.find('t')+1)
#finds the location of the second t 
```

### <mark style="background:#AD21D9;">Enumerate function:</mark> 

The enumerate function adds a counter to each element of an iterable object, and returns an enumerate object

```Python
s = "hello"
enumerate(s) -> (0,'h'), (1,'e'), (2,'l'), (3,'l'), (4, 'o')

#Syntax:
for i, ch in enumerate(s):
print(i, ' ', ch)
```

Can use it to iterate through both the index and the element simultaneously, doing dual assignment

```Python
river = "Mississippi"
target = input("Input a target to find:")

for index,letter in enumerate(river):
if letter <mark style="background:#AD21D9;"> target:
print("letter found at index", index)
break
else:
print("letter", target, "not found in river", river)

```

### <mark style="background:#AD21D9;">Split function:</mark> 

The split function will take a string and break it into multiple new string parts depending on the argument character

If no argument is provided, by default the split is on any whitespace character

You can assign the pieces with multiple assignments if you know how many pieces are yielded

Example: re-order a name

```Python
name = "John Marwood Cheese"
first, middle, last = name.split()
transformed = last + "," + first + " " + middle
print(transformed) 
```
 
### <mark style="background:#AD21D9;">String Formatting:</mark> 

<mark style="background: #AD21D9;">Better Printing:</mark>
So far, we have just used the default of the print function

Python provides us with a way more complex and powerful ways to format and output strings

<mark style="background: #AD21D9;">Example:</mark>
```Python
print("Name: {}, Surname:{}".format("John","Smith"))

#prints Name: John, Surname: Smith
```

### <mark style="background: #AD21D9;">Format Method:</mark>

<mark style="background: #AD21D9;">format</mark> is a method that creates a new string where certain elements of the string are re-organized i.e., formatted

The elements to be re-organized are the curly bracket elements in the string

Formatting can be quite complex, for full range of options refer to the documentation

### <mark style="background: #AD21D9;">Mapping args to {}:</mark>

The string is modified so that the {} elements in the string are replaced by the format method arguments

They replacement is in order: first {} is replaced by the first argument, second {} by the second argument and so forth.

<mark style="background: #AD21D9;">Example:</mark>
![](https://i.imgur.com/5tJtwZk.png)

### <mark style="background: #AD21D9;">Format string:</mark>

The content of the curly bracket elements are the format string, descriptors of how to organise that particular substitution.

Types are the kind of thing to substitute, numbers indicate total spaces.

![](https://i.imgur.com/tlecNy5.png)

### <mark style="background: #AD21D9;">Each format string:</mark>

Each bracket looks like 

``{:align width .precision type}``

- <mark style="background: #AD21D9;">align</mark> is optional
- <mark style="background: #AD21D9;">width</mark> is how many spaces (default just enough)
- <mark style="background: #AD21D9;">.precision</mark> is for floating point rounding (default no rounding)
- <mark style="background: #AD21D9;">type</mark> is the expected type (error if the arg is the wrong type)

<mark style="background: #AD21D9;">Example:
</mark>![](https://i.imgur.com/GWCTLQU.png)

<mark style="background: #AD21D9;">Nice Table Example:</mark>
![](https://i.imgur.com/XY96TZH.png)

### <mark style="background: #AD21D9;">Floating Point Precision:</mark>

We can round floating point to specific number of decimal places

```Python
#Terminal Example

>>> import math
>>> print(math.pi)
3.141592653589793
>>> print("Pi is {:.4f}".format(math.pi))
Pi is 3.1416
>>> print("Pi is {:.8f}".format(math.pi))
Pi is 3.14159265
>>> print("Pi is {:8.4f}".format(math.pi))
Pi is   3.1416
>>> print("Pi is {:8.2f}".format(math.pi))
Pi is     3.14
>>>
```

### <mark style="background: #AD21D9;">Arg:</mark>

To override the {}-to-argument matching we have seen, you can indicate the argument you want in the bracket

```Python
>>> print("{0} is {2} and {0} is {1}".format("Bill", 25, "tall"))

Bill is tall and Bill is 25
```

### <mark style="background: #AD21D9;">fill, =</mark> 

Besides alignment, you can fill empty spaces with a fill character:
- 0= fill with 0s
- += fill with +

```Python
>>> print ("{1:+=10d} | {0:0=10d}".format(22,35))
>>> ++++++++35 | 0000000022
```

### <mark style="background: #AD21D9;">sign:</mark>

`+` means a sign for both positive and negative numbers

``-`` means a sign for only negative numbers

space means space for positive, minus for negative

### <mark style="background: #AD21D9;">Example:</mark>

args are before the : and format after

```Python
>>> print("{0:.>12s} | {1:0=+10,d} | {2:->5d}".format("abc", 35, 22))

.........abc | +0,000,035 | ---22
```

- 0🡪 first (count from 0) arg of format, abc
- 1🡪 second (count from 0) arg of format, 35
- 2🡪 third (count from 0) arg of format, 22
- :🡪 separator
- 0= 🡪 fill with 0's
- . 🡪 fill with .'s
- `-` 🡪 fill with -'s
- +🡪 plus or minus sign
- Xd🡪 occupy X spaces (left justify) decimal
- X,d🡪 occupy X spaces (left justify) decimal, put comma every three digits 
- Xs 🡪 occupy X spaces (left justify) string
- > 🡪 right alignment

### <mark style="background: #AD21D9;">Example - Printing a table:</mark>

For example, consider making a table of polygon sides, total interior degrees, the degrees of each interior angle, and the degrees for each exterior angle.

```Python
>>> for n in range(3, 11):

print("{:4}-sides:{:6}{:10.2f}{:10.2f}".format(n,180*(n-2),180*(n-2)/n,360/n))
```

   3-sides:     180      60.00   120.00
   4-sides:     360      90.00     90.00
   5-sides:     540    108.00     72.00
   6-sides:     720    120.00     60.00
   7-sides:     900    128.57     51.43
   8-sides:   1080    135.00     45.00
   9-sides:   1260    140.00     40.00
 10-sides:   1440    144.00     36.00

### <mark style="background: #AD21D9;">F-Strings:</mark>

Python version 3.6 introduced formatted string literals, simply called “f-strings.”  
  
They are called f-strings because you need to prefix a string with the letter 'f' to create an fstring

```Python
>>> name = "Eric"
>>> age = 74
>>> f"Hello, {name}. You are {age}."
'Hello, Eric. You are 74.'
```

### <mark style="background: #AD21D9;">Modifiers:</mark>

Like the .format() method, f-strings support extensive modifiers that control the final appearance of the output string.  

The modifiers are the same for f-strings and .format()

```Python
>>> n = 123
>>> '{:=+8}'.format(n)
'+    123'
>>> f'{n:=+8}'
'+    123'

>>> s = 'foo'
>>> '{0:*^8}'.format(s)
'**foo***'
>>> f'{s:*^8}'
'**foo***'

```

### <mark style="background: #AD21D9;">Modifiers:</mark>

Modifiers in summary:

```Python
:fill align sign # 0 width sep .precision type
```

![](https://i.imgur.com/8XfbQll.png)

### <mark style="background: #AD21D9;">When to use f-string and .format():</mark>

Overall f-strings are easier to read, faster, and more modern than ``.format()``

For most cases f-strings will be considered better

``.format()`` allows a single variable to be placed in multiple parts of a same string. It has a bit more flexibility when handling long and complex strings

### <mark style="background: #AD21D9;">String Summary:</mark>

Strings are immutable.

Strings are sequences.

Strings have many methods.

Standard operations:
- length function: len(s)
- membership: in

### <mark style="background: #AD21D9;">Slicing Summary:</mark>

Given: s = 'Mississippi'
- Indexing starts at 0: s[0] is 'M'.
- Negative indices work backward from the end: s[-1] is 'i'.
- Slicing selects a subset up to but not including the final index: s[3:6] is 'sis'.
- Slicing default start is the beginning, so s[:4] is 'Miss'.
- Slicing default end is the end, so s[7:] is 'ippi'.
- Using both defaults makes a copy: s[:].
- Slicing’s optional third argument indicates step: s[:6:2] is 'Msi'.
- The idiom to reverse a string: s[::-1] is 'ippississiM'

# <mark style="background: #AD21D9;">Dictionaries</mark>

### <mark style="background:#AD21D9;">More Data Structures:</mark>

Last time we looked at lists and tuples data structures and what it can be used for

We will now examine a more advanced data structure <mark style="background:#AD21D9;">Dictionary</mark>

n particular, the dictionary is an important and very useful part of Python, as well as generally usually useful to solve many problems

### <mark style="background:#AD21D9;">What is a dictionary?</mark>

In data structure terms, a <mark style="background:#AD21D9;">dictionary</mark> is better termed an <mark style="background:#AD21D9;">associative array</mark>, <mark style="background:#AD21D9;">associative list</mark> or a <mark style="background:#AD21D9;">map</mark>.

You can think if it as a list of pairs, where the first element of the pair, the <mark style="background:#AD21D9;">key</mark>, is used to retrieve the second element, the <mark style="background:#AD21D9;">value</mark>.

Thus we <mark style="background:#AD21D9;">map a key to a value</mark>

### <mark style="background:#AD21D9;">Key-value pairs:</mark>

The key acts as an index to find the associated value

Just like in a dictionary, you look up a word by its spelling to find the associated definition

A dictionary can be searched to locate the value associated with a key

### <mark style="background:#AD21D9;">Create a Python Dictionary:</mark>

Use the { } marker to create a dictionary

Use the : marker to indicate key:value pairs

Separate elements by comma

```Python

contacts= {'bill': '353-1234', 'rich': '269-1234', 'jane': '352-1234'}

print(contacts)

{'jane': '352-1234',
'bill': '353-1234',
'rich': '369-1234'}
```


### <mark style="background:#AD21D9;">Example: Dictionary</mark>

![](https://i.imgur.com/Eorobed.png)


### <mark style="background:#AD21D9;">Keys and Values:</mark>


Key must be <mark style="background:#AD21D9;">immutable</mark>
- strings, integers, tuples are fine
- lists are NOT

Value can be anything

Keys can not be repeated in the dictionary

### <mark style="background:#AD21D9;">Collections, but not a sequence:</mark>

Dictionaries are collections but they are not sequences (such as lists, strings or tuples)
- there is <mark style="background:#AD21D9;">no order</mark> to the elements of a dictionary
- in fact, the order (for example, when printed) might change as elements are added or deleted

So, how to access dictionary elements?

### <mark style="background:#AD21D9;">Dictionary: Access Elements:</mark>

Access requires [ ], but the key is the index!  

```Python

my_dict={}
#an empty dictionary

my_dict['bill']=25
#added the pair 'bill':25

print(my_dict['bill'])
#prints 25
```



### <mark style="background:#AD21D9;">Dictionaries are mutable:</mark>

Like lists, dictionaries are a <mark style="background:#AD21D9;">mutable </mark>data structure

You can change the object via various operations, such as index assignment


```Python
my_dict = {'bill':3, 'rich':10}
print(my_dict['bill']) # prints 3

my_dict['bill'] = 100
print(my_dict['bill']) # prints 100
```

### <mark style="background:#AD21D9;">Dictionary: Operations</mark>

Like other data structures we've seen so far, with dictionaries we can use the following:

```Python
len(my_dict)
#number of key:value pairs in the dictionary

key in my_dict
#boolean; checks if key is a key  in the dictionary

for key in my_dict:
#iterates through the keys of a dictionary

```

### <mark style="background:#AD21D9;">Dictionary: Methods</mark>

Some of the methods:

```Python

my_dict.clear() #empty the dictionary
my_dict.update(yourDict) #for each key in yourDict, updates my_dict with that key/value pair

my_dict.copy() #shallow copy
my_dict = copy.deepcopy(dict) #deep copy from copy library (import copy)

my_dict.pop(key) #remove key, return value
```

### <mark style="background:#AD21D9;">Dictionary content models:</mark>

```Python
my_dict.items() # all the key/value pairs
my_dict.keys() #all the keys
my_dict.values() #all the values
```


These return what is called a dictionary view:
- dynamically updated with changes
- iterable

### <mark style="background:#AD21D9;">Views are iterable:</mark>

```Python
for key in my_dict:
	print(key)
#prints all the keys

for key,value in my_dict.items():
	print(key,value)
#prints all the key/value pairs

for value in my_dict.values():
	print(value)
#prints all the values
```

### <mark style="background:#AD21D9;">Passing mutables:</mark>

Because we are passing a mutable data structure, a dictionary, we do not have to return the dictionary when the function ends

If all we do is update the dictionary (change the object) then the argument will be associated with the changed object.

### <mark style="background:#AD21D9;">Dictionary summary:</mark>

Dictionaries are unordered collections specified by curly braces: {}.

Each dictionary item is a key-value pair (specified with a colon).

Key must be immutable.
`Example: {'a':5, 6:[1,2], (3,4):'abc'}  `

Assignment: D[2] = `'xyz'` creates entry 2: `'xyz'`

The get method returns the value or the specified default: my_dict.get(value, default)

Iterating through a dictionary D:

```Python
for k in D: # iterate by key
for k,v in D.items()# iterate by key,value pairs
for v in D.values(): # iterate by value
for k in D.keys(): # iterate by key
```

### <mark style="background:#AD21D9;">Class-Instance relations:</mark>

Remember the <mark style="background:#AD21D9;">relationship </mark>between a class and its instances:

A class can have many instances, each made initially from the <mark style="background:#AD21D9;">constructor </mark>of the class

The <mark style="background:#AD21D9;">methods </mark>an instance can call are initially <mark style="background:#AD21D9;">shared </mark>by all instances of a class


### <mark style="background:#AD21D9;">Class-Class relations:</mark>

Classes can also have a <mark style="background:#AD21D9;">separate relationship</mark> with other classes

The relationships forms a <mark style="background:#AD21D9;">hierarchy </mark>


<mark style="background:#AD21D9;">Computer science "trees"</mark>

![](https://i.imgur.com/mXCaNum.png)

### <mark style="background:#AD21D9;">Classes related by a hierarchy:</mark>

When we create a class, which itself is another object, we can state <mark style="background:#AD21D9;">how </mark>it is <mark style="background:#AD21D9;">related </mark>to other <mark style="background:#AD21D9;">classes</mark>

The relationship we can indicate is the class that is <mark style="background:#AD21D9;">'above'</mark> it in the hierarchy

### <mark style="background:#AD21D9;">Class statement:</mark>

![](https://i.imgur.com/ucdQxhG.png)


The top class in Python is called <mark style="background:#AD21D9;">object</mark>:
- It is predefined by Python, always exists
- Use object when you have no superclass


### <mark style="background:#AD21D9;">Simple class hierarchy:</mark>

![](https://i.imgur.com/PAwFJea.png)


### <mark style="background:#AD21D9;">is-a: super and sub class:</mark>

The class hierarchy imposes an <mark style="background:#AD21D9;">is-a</mark> relationship between classes

MyChildClass <mark style="background:#AD21D9;">is-a</mark> MyClass

MyClass <mark style="background:#AD21D9;">is-a</mark> object

object has as a <mark style="background:#AD21D9;">subclass</mark> MyClass

MyChildClass has as a <mark style="background:#AD21D9;">superclass</mark> MyClass


### <mark style="background:#AD21D9;">Inheritance:</mark>

Different kinds of objects have certain things in <mark style="background:#AD21D9;">common</mark>:
- <mark style="background:#AD21D9;">Example</mark>: trucks, cars, motorbikes are all motorised vehicles
- <mark style="background:#AD21D9;">States:</mark> current speed, current gear, cc value…
- <mark style="background:#AD21D9;">Behaviours</mark>: drive, stop, change gear. Some are executed slightly differently, depending on vehicle -> <mark style="background:#AD21D9;">method overwriting</mark>


OOP allows classes to inherit certain traits, aka common states and behaviours, and implement their own versions if required.  

### <mark style="background:#AD21D9;">Using Inheritance:</mark>

If a new class is created as part of an existing class hierarchy, then the new class can reuse existing code from the hierarchy, specializing only those aspects or attributes that are unique to the new class.

It emphasizes a need that OOP often fills: group development.

Developers need to work together to create software, and OOP is a tool to help in that regard.

<mark style="background:#AD21D9;">Example:</mark>

Physicists have developed the Standard Model.  

It is a description of all the fundamental pieces from which matter is constructed and three of the fundamental forces of nature (gravity not yet being incorporated)

It describes particles by a number of attributes, including mass, spin, charge, and name. They also have intrinsic attributes, such as location (in three dimensional space) and velocity (direction of movement in three-dimensional space).

This classification of particles is perfect for a class hierarchy.

![](https://i.imgur.com/u2oVeg5.png)



```Python
class Particle(object):
	def __init__(self,
				name='',
				position=(0.0, 0.0, 0.0),
				velocity=(0.0, 0.0, 0.0),
				spin=0.0):

		self.position = position
		self.velocity = velocity
		self.name = name
		self.spin = spin

	def __str__(self):
		print('in particle str')
		pos_str = '({}:{}:{})'.format(self.position[0],
		self.position[1],
		self.position[2])
	
	vel_str = '({}:{}:{})'.format(self.velocity[0],
	
	self.velocity[1],
	
	self.velocity[2])

	result_str = "{} at {} with velocity {} and spin {}".format(self.name, pos_str, vel_str, self.spin)
	return result_str

class MassParticle(Particle):

	def __init__(self,
				name='',
				position=(0.0, 0.0, 0.0),
				velocity=(0.0, 0.0, 0.0),
				spin=0.0, 
				mass=0.0):

		Particle.__init__(self, name, position, velocity, spin)
		self.mass = mass

def __str__(self):
	print('in mass str')
	result_str = Particle.__str__(self)
	result_str = result_str + ' and mass {}'.format(self.mass)
	return result_str

class ChargedParticle(MassParticle):
	def __init__(self,
				name='',
				position=(0.0, 0.0, 0.0),
				velocity=(0.0, 0.0, 0.0),
				spin=0.0,
				mass=0.0,
				charge=0.0):

		MassParticle.__init__(self, name, position, velocity, spin, mass)
		self.charge = charge

	def __str__(self):
		print('in charged str')
		result_str = MassParticle.__str__(self)
		result_str = result_str + ' and charge {}'.format(self.charge)
	return result_str
```

### <mark style="background:#AD21D9;">Bound methods:</mark>

Normal methods are called <mark style="background:#AD21D9;">bound methods</mark>. Bound methods have an instance in front of the method call and automatically pass self

```Python
my_inst = MyClass()

my_inst.method(arg1,arg2)
#my_inst is an instance, so the method is bound
```

### <mark style="background:#AD21D9;">Unbound methods:</mark>

It is also possible to call a method <mark style="background:#AD21D9;">without Python binding</mark> `self`. In that case, the user has to do it.

Unbound methods are <mark style="background:#AD21D9;">called</mark> as part of the <mark style="background:#AD21D9;">class</mark> but `self` is passed by the user

```Python
my_inst = MyClass()
MyClass.method(my_inst, arg2, arg3)

#self is passed explicitly (my_inst ) here!
```

<mark style="background:#AD21D9;">Why unbound methods?</mark>
- Consider an example. We want to specialise a new class as a subclass of list.
	```Python
	class MyClass(list):
	```
- But we want to make sure that we get our new class instances initialized the way they are supposed to, by calling `__init__` of the super class
- If we don't explicitly say so, our class may inherit stuff from the super class, but we must make sure we call it in the proper context. For example, our `__init__` would be:  

We explicitly call the <mark style="background:#AD21D9;">super class constructor</mark> using an unbound method

Then, <mark style="background:#AD21D9;">after</mark> it <mark style="background:#AD21D9;">completes</mark> we can do anything special for our new class

We <mark style="background:#AD21D9;">specialise</mark> the <mark style="background:#AD21D9;">new class</mark> but <mark style="background:#AD21D9;">inherit</mark> most of the work from the <mark style="background:#AD21D9;">super</mark>.

### <mark style="background:#AD21D9;">Method Overwriting:</mark>

Ability of a class to change the implementation of a method that is provided by one of its ancestors

A very important concept in OOP

![](https://i.imgur.com/RX3fmBY.png)


<mark style="background:#AD21D9;">It gives us a way to organise code:</mark>
- <mark style="background:#AD21D9;">Specialisation:</mark> A subclass can inherit code from its superclass, but modify anything that is particular to that subclass
- <mark style="background:#AD21D9;">Override:</mark> change a behavior to be specific to a subclass
- <mark style="background:#AD21D9;">Reuse-code:</mark> Use code from other classes (without rewriting) to get behaviour in our class.

### <mark style="background:#AD21D9;">Expanded class organisation example:</mark>

```Python

class ClassName(object):
	def __init__ (self, param):
		self.value = param

	def __str__ (self):
		return “some string”

class ChildClass(ClassName):
	def __init__ (self,param):
		ClassName.__init__(self,param)

	def __str__ (self):
		return “some other string”

	def method(self, param):
		#do something
```