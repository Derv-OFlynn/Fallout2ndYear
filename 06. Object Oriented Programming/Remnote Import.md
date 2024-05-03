
- <mark style="background:#AD21D9;">Mutables, Tuples</mark> 
    - <mark style="background:#AD21D9;">Assignment:</mark> 
        - 
        - Assignment takes an object from the RHS and associates it with a variable on the LHS
        - When you assign one variable to another, you <mark style="background:#AD21D9;">^share the association</mark>^ with the same object
        - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FC2NZhMvxMBPMFmkoD_yazumxyr2-gMivTDSKXwfYnxv79Fmkk2a_Nze9AciAPfw5dMHMdgJfdiobE9PJl_qLXOXgAdaFezBufM_Ilx08M0zKh9IhbhucGNbsM9DKUJ6l.png)
        - 
    - <mark style="background:#AD21D9;">Immutable objects:</mark> 
        - 
        - For immutable objects, object sharing is not a problem since the object cannot be changed
        - Any changes that occur generate a <mark style="background:#AD21D9;">^new</mark>^ object
        - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FHE0mLtoX07Xukqo4QbOONvirBeAPkDVMWTGKxXCOBX7obdwQWLJsWnTBvoWkxSW7sM_TsInWDn2qiT9VZH0zPqWIOjywbza_AKnviz1XXsj0EnIxXbENOFL2Gw1gGBF6.png) 
        - 
    - <mark style="background:#AD21D9;">Mutability:</mark> 
        - 
        - If two variables associate with the same object then they <mark style="background:#AD21D9;">^both reflect</mark>^ any change to that object
        - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FrH5XUgEA_o8XvRmnjfL3tHQckyKKZA9E6rJ-H1Pn4ml4Z-ZdcoTDFM_XxUxuvHCMHAxWiguOrwV5ARnHW67JeZAf1dcEUb4Xlfzd4x01W2ph2MwW1BahGjRkzJTcsFvf.png) 
        - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FrbYI3VjZwzz3YXYctRrcyl2kW8TBwkfWB2fS_1XmwotTHThkCYsgNzj_ZvQEdv3uPkB3OvV3UN9zf-QBHOmOwxCKjaFtiEOfTwgdf2dREzWgcDrnldZh8bdKydL0n-uo.png) 
        - 
        - 
    - <mark style="background:#AD21D9;">Copying:</mark> 
        - If we copy, does this solve the problem? It depends
        - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FiyfUf5YLS2KVcl8GoTHiX70k_2JblqAc_lsI0tO4sVdQoqItCbKmSJZ9ajhhexe-WuGm6oTR46ppv8zzVn-Zn2ggEHKK_MFP0q45tb5DgCeAyoQm0iOYPETjvqq_cYN_.png) 
        - 
        - 
        - What actually gets copied is the <mark style="background:#AD21D9;">^top level reference</mark>^. If the list has nested lists or uses other associations, the association gets copied. This is called a <mark style="background:#AD21D9;">^shallow copy</mark>^ 
        - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FqAQwEDQgouc7mwJfFkL9enXHXWrMAjVix2sz73JtXGksRPZPcZGM_Yt8kTX-rzaSxDK42PJos0LvSKowuUVQoj3xDdKfjDhdRBgSnhYc-fR2jJaZqMm8FmcD96IiSB8O.png) 
        - 
        - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FbunJGw1fC9usG6ZiCk4HY8q2pjTqYf0xJG8oR_JEjL4ihiWveZGTh5e1dikf6u_vjuBfeZo7wk-KwtdyTb2uzx8Q_jb15G5TQJ6FZoJeTNP_d0mj2rJ73vMWQPU2XGFb.png) 
        - 
        - <mark style="background:#AD21D9;">Shallow vs. Deep copies:</mark> 
            - 
            - Regular copy, the `[:]` approach, only copies the top level reference. If you want a full copy you can use deepcopy
            - .
                ```Python
                a_list = [1,2,3]
b_list = [5,6,7]
a_list.append(b_list)
a_list -> [1,2,3,[5,6,7]]

import copy 
c_list = copy.deepcopy(a_list)

b_list[0] = 1000

a_list -> [1,2,3, [1000, 6, 7]]
c_list -> [1,2,3, [5,6,7]] 
                ```
            - 
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2F-e0-1Je9Thu0jazDL8Sxmss1OW25D1RU0FoDVadg8hNdcPMv1KmEUj85bdOsX0mPucICNQ0jNpR9FmAsdf0zcXgIBSwuTXuxilZldKhUxN6Ry8W_SCVtTul2BLuUMXmQ.png) 
            - 
            - 
        - 
        - 
    - <mark style="background:#AD21D9;">List Comprehension:</mark> 
        - 
        - The use of lists in python is a major part of its power
        - Lists are very useful and can be used to accomplish many tasks
        - Therefore, python provides great support to make common list tasks easier
        - <mark style="background:#AD21D9;">^Comprehension</mark>^ refers to constructing a new collection by performing some operation on the elements of another collection
        - .
            ```Python
            expression for-clause condition
            ```
        - 
        - <mark style="background:#AD21D9;">Constructing lists using comprehension:</mark> 
            - 
            - .
                ```Python
                [n for n in range(1, 5)]
                ```
            - 
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FYRPlb1oy90i7DlGfmyTQFN4ToGCxWVa1jG1XRzkU2-jHTfIc6jtpWWF-8Vx0BXoV_8R2L9qWQZ9QtgZ4ak3M_ntzrb-xGCWHUJe3m-xRyZJdr4ZkALn4wnoap5NZyIOM.png) 
            - 
            - .
                ```Python
                [n**2 for n in range(1,6)]
                ```
            - this returns [1,4,9,16,25]
            - Note that we can only change the values we are iterating over, in this case `n` 
            - 
        - <mark style="background:#AD21D9;">Multiple collects:</mark> 
            - 
            - .
                ```Python
                [x + y for x in range(1,4) for y in range(1,4)]

# This is the same as:

my_list = []
for x in range(1,4):
    for y in range(1,4):
        my_list.append(x + y)
        
-> [2,3,4,3,4,5,4,5,6] 
                ```
            - 
        - <mark style="background:#AD21D9;">Modifying what gets collected:</mark> 
            - 
            - .
                ```Python
                [c for c in "Hi There Mom" if c.isupper()] 
                ```
            - 
            - The if part of the comprehensive controls of which the iterated values is collected at the end
            - Only those values which make the if part true will be collected
            - ⇒ ["H", "T", "M"]
            - 
            - .
                ```Python
                [i for i in range(1,7) if i%2<mark style="background:#AD21D9;">0]
-> [2,4,6] 
                ```
            - 
        - 
    - <mark style="background:#AD21D9;">Tuples:</mark> 
        - 
        - <mark style="background:#AD21D9;">^Tuples</mark>^ are <mark style="background:#AD21D9;">^immutable</mark>^ sequences
        - They are printed with (,) and similarly to lists, can have various lengths
        - .
            ```Python
            >>> 10,12    # Python creates a tuple
(10, 12)
>>> tup = 2,3    # Assigning a tuple to a variable
>>> tup
(2, 3)
>>> (1)     # not a tuple, a grouping
1
>>> (1,)    # comma makes it a tuple
(1,)
>>> x,y = "a",3.14159    # multiple assignments
>>> x
'a'
>>> y
3.14159
>>> x,y    # create a tuple
('a', 3.14159)
>>> 
            ```
        - 
    - <mark style="background:#AD21D9;">Why do we need tuples?</mark> 
        - 
        - The real question is, why have an immutable list as a separate type?
        - An immutable list give you a data structure with some integrity
        - You know you cannot accidentally change one
        - 
    - <mark style="background:#AD21D9;">Lists and Tuples:</mark> 
        - 
        - Everything that works with a list also works with a tuple <mark style="background:#AD21D9;">^except</mark>^ methods that <mark style="background:#AD21D9;">^modify </mark>^the tuple
        - Indexing, slicing, len and print all work as expected
        - <mark style="background:#AD21D9;">None of the mutable methods</mark> work:
            - `append` 
            - `extend`
            - `del` 
            - 
        - 
    - <mark style="background:#AD21D9;">Commas make a tuple:</mark> 
        - 
        - For tuples you can think of a comma as the operator that makes a tuple, where the () simple acts as a grouping:
        - 
        - .
            ```Python
            myTuple = 1,2 #creates (1,2)
myTuple = (1,) #creates (1)
myTuple = (1) #creates 1, not (1)
myTuple = 1, #creates (1) 
            ```
        - 
    - <mark style="background:#AD21D9;">Data Structures in General:</mark> 
        - 
        - <mark style="background:#AD21D9;">Organisation of data:</mark> 
            - 
            - Data Structures focus on the organisation of data and the operations we can perform on the data
            - Different data structures will be suitable for solving different problems
            - We have seen strings, lists and tuples so far
            - 
        - <mark style="background:#AD21D9;">Data structures: Efficiency:</mark> 
            - 
            - Efficient with respect to an <mark style="background:#AD21D9;">^algorithm</mark>^ 
            - Efficient with respect to the amount of <mark style="background:#AD21D9;">^memory</mark>^ space used
            - Efficient with respect to the <mark style="background:#AD21D9;">^time</mark>^ it takes to perform some operations
            - 
        - <mark style="background:#AD21D9;">Other Data Structures:</mark> 
            - 
            - <mark style="background:#AD21D9;">^Queue:</mark>^ a sequence of data elements that "stand in a line", in which the data can only be removed from the front of the line and new elements can only be added to the back of the line
                - <mark style="background:#AD21D9;">^Operations:</mark>^ check to see if the queue is empty, add to the back and remove from the front
                - 
            - <mark style="background:#AD21D9;">^Dictionary:</mark>^ a data structure is one in which we can look up a key and access some value 
                - <mark style="background:#AD21D9;">^Operations:</mark>^ look up a value associated with the key, add key value pairs, remove key-value pairs, etc
                - 
            - <mark style="background:#AD21D9;">^Set:</mark>^ collection of unordered elements allows us to access and modify individual elements
                - <mark style="background:#AD21D9;">^Operations:</mark>^ insertion, removal, union, intersection
                - 
            - <mark style="background:#AD21D9;">^Matrix: </mark>^of numbers is a common mathematical data structure.
                - <mark style="background:#AD21D9;">^Operations:</mark>^ multiplication, find determinant, invert, transpose
                - 
            - Some of these are built-in for python e.g. a dictionary and a set
            - 
        - 
    - <mark style="background:#AD21D9;">Summary:</mark> 
        - 
        - Lists are mutable
        - Tuples are immutable
        - Lists and tuples are sequences
        - Lists allow assignment, tuples do not
        - <mark style="background:#AD21D9;">Standard operations:</mark> 
            - length function `len(L)` 
            - membership `in` 
            - max and min: `max(L)` and `min(L)` 
            - 
        - Tuples work the same with indexing and slicing
    - 
    - 
    - 
    - 
    - 
    - 
    - 
- <mark style="background:#AD21D9;">Dictionaries</mark> 
    - <mark style="background:#AD21D9;">More Data Structures:</mark> 
        - 
        - Last time we looked at lists and tuples data structures and what it can be used for
        - We will now examine a more advanced data structure <mark style="background:#AD21D9;">^Dictionary</mark>^ 
        - In particular, the dictionary is an important and very useful part of Python, as well as generally usually useful to solve many problems
        - 
    - <mark style="background:#AD21D9;">What is a dictionary?</mark> 
        - 
        - In data structure terms, a <mark style="background:#AD21D9;">^dictionary </mark>^is better termed an <mark style="background:#AD21D9;">^associative array</mark>^, <mark style="background:#AD21D9;">^associative list</mark>^ or a <mark style="background:#AD21D9;">^map</mark>^.
        - You can think if it as a list of pairs, where the first element of the pair, the <mark style="background:#AD21D9;">^key</mark>^, is used to retrieve the second element, the <mark style="background:#AD21D9;">^value</mark>^.
        - Thus we <mark style="background:#AD21D9;">^map a key to a value</mark>^ 
        - 
    - <mark style="background:#AD21D9;">Key-value pairs:</mark> 
        - 
        - The key acts as an index to find the associated value
        - Just like in a dictionary, you look up a word by its spelling to find the associated definition
        - A dictionary can be searched to locate the value associated with a key
        - 
    - <mark style="background:#AD21D9;">Create a Python Dictionary:</mark> 
        - 
        - Use the { } marker to create a dictionary
        - Use the : marker to indicate key:value pairs
        - Separate elements by comma
        - 
        - .
            ```Python
            contacts= {'bill': '353-1234', 'rich': '269-1234', 'jane': '352-1234'}
print(contacts)

{'jane': '352-1234',
'bill': '353-1234',
'rich': '369-1234'}
            ```
        - 
        - <mark style="background:#AD21D9;">Example: Dictionary</mark> 
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2F6CuS1640hiXHt5rKoKKQylWj6XkYtjpc2tmYqr5aT98JD2eFgWiLMHICTK9n0NA2wTgMPq0jSWUtyQFdzHqGNZnC1K-HDsjSxRHVtWt9Zv-9PK3H0AvZU0pBumpNR1N-.png) 
            - 
        - 
    - <mark style="background:#AD21D9;">Keys and Values:</mark> 
        - 
        - Key must be <mark style="background:#AD21D9;">^immutable</mark>^ 
            - strings, integers, tuples are fine
            - lists are NOT
            - 
        - Value can be anything
        - Keys can not be repeated in the dictionary
        - 
    - <mark style="background:#AD21D9;">Collections, but not a sequence:</mark> 
        - 
        - Dictionaries are collections but they are not sequences (such as lists, strings or tuples)
            - there is <mark style="background:#AD21D9;">^no order</mark>^ to the elements of a dictionary
            - in fact, the order (for example, when printed) might change as elements are added or deleted
        - So, how to access dictionary elements?
        - 
    - <mark style="background:#AD21D9;">Dictionary: Access Elements:</mark> 
        - 
        - Access requires [ ], but the key is the index!  
        - .
            ```Python
            my_dict={}
#an empty dictionary 

my_dict['bill']=25
#added the pair 'bill':25

print(my_dict['bill'])
#prints 25
            ```
        - 
    - <mark style="background:#AD21D9;">Dictionaries are mutable:</mark> 
        - 
        - Like lists, dictionaries are a <mark style="background:#AD21D9;">^mutable </mark>^data structure
        - You can change the object via various operations, such as index assignment
        - 
        - .
            ```Python
            my_dict = {'bill':3, 'rich':10}
print(my_dict['bill']) # prints 3

my_dict['bill'] = 100
print(my_dict['bill']) # prints 100
            ```
    - 
    - <mark style="background:#AD21D9;">Dictionary: Operations</mark> 
        - 
        - Like other data structures we've seen so far, with dictionaries we can use the following:
        - .
            ```Python
            len(my_dict)
#number of key:value pairs in the dictionary

key in my_dict
#boolean; checks if key is a key  in the dictionary

for key in my_dict:
#iterates through the keys of a dictionary
            ```
        - 
    - <mark style="background:#AD21D9;">Dictionary: Methods</mark>
        - 
        - Some of the methods:
        - .
            ```Python
            my_dict.clear() #empty the dictionary
my_dict.update(yourDict) #for each key in yourDict, updates my_dict with that key/value pair
my_dict.copy() #shallow copy
my_dict = copy.deepcopy(dict) #deep copy from copy library (import copy)
my_dict.pop(key) #remove key, return value
            ```
        - 
    - <mark style="background:#AD21D9;">Dictionary content models:</mark> 
        - 
        - .
            ```Python
            my_dict.items() # all the key/value pairs
my_dict.keys() #all the keys
my_dict.values() #all the values
            ```
        - 
        - These return what is called a dictionary view:
            - dynamically updated with changes
            - iterable
            - 
        - 
    - <mark style="background:#AD21D9;">Views are iterable:</mark> 
        - 
        - .
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
        - 
    - <mark style="background:#AD21D9;">Passing mutables:</mark> 
        - 
        - Because we are passing a mutable data structure, a dictionary, we do not have to return the dictionary when the function ends
        - If all we do is update the dictionary (change the object) then the argument will be associated with the changed object.
        - 
    - <mark style="background:#AD21D9;">Dictionary summary:</mark> 
        - 
        - Dictionaries are unordered collections specified by curly braces: {}. 
        - Each dictionary item is a key-value pair (specified with a colon).
        - Key must be immutable.
            - `Example: {'a':5, 6:[1,2], (3,4):'abc'}  ` 
            - 
        - Assignment: D[2] = `'xyz'` creates entry 2: `'xyz'` 
        - The get method returns the value or the specified default: my_dict.get(value, default)
 
        - Iterating through a dictionary D:
            - .
                ```Python
                for k in D: # iterate by key
for k,v in D.items()# iterate by key,value pairs
for v in D.values(): # iterate by value
for k in D.keys(): # iterate by key 
                ```
        - 
- <mark style="background:#AD21D9;">Sets</mark> 
    - In mathematics, a <mark style="background:#AD21D9;">^set</mark>^ is a collection of objects, potentially of many different types
    - In a set, <mark style="background:#AD21D9;">^no two elements are identica</mark>^l. A set consists of elements, each of which is unique compared to other elements
    - There<mark style="background:#AD21D9;">^ is no order</mark>^ to the elements of a set
    - A set with no elements is the <mark style="background:#AD21D9;">^empty set</mark>^ 
    - 
    - <mark style="background:#AD21D9;">Creating a set:</mark> 
        - 
        - Sets can be created in one of two ways:
            - 
            - <mark style="background:#AD21D9;">^Constructor:</mark>^ `set(iterable)` where the argument is iterable
            - .
                ```Python
                my_set = set('abc')
my_set -> {'a', 'b', 'c'} 
                ```
            - 
            - <mark style="background:#AD21D9;">^Shortcut:</mark>^ {}, curly brackets to distinguish them from dicts
            - .
                ```Python
                my_set = {'a', 'b', 'c'}
                ```
            - 
        - 
    - <mark style="background:#AD21D9;">Diverse elements:</mark> 
        - 
        - A set can consist of a mixture of different types of elements:
        - .
            ```Python
            my_set = {'a', 1, True}
            ```
        - 
    - <mark style="background:#AD21D9;">No duplicates:</mark> 
        - 
        - Duplicates are automatically removed:
        - .
            ```Python
            my_set = set("aabbccdd")
print(my_set)

-> {'a', 'b', 'c', 'd'} 
            ```
        - 
    - <mark style="background:#AD21D9;">Sets: Common operators:</mark> 
        - 
        - Most data structures respond to these:
        - .
            ```Python
            # number of elements in a set
len(my_set)

#boolean indicating whether elements are in the set
element in my_set

#iterate through elements in my_set 
for element in my_set 
            ```
        - 
    - <mark style="background:#AD21D9;">Set operators:</mark> 
        - 
        - The set data structure provides some special operators that correspond to the operators you learned in maths
        - These are various combinations of set contents
        - These operations have both a method name and a shortcut binary operator
        - 
        - <mark style="background:#AD21D9;">Method: intersection (& operator):</mark> 
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2Ffn0EbDb7NG-Ncg3pu9ot_xCp2rnuiYERLiqLYffCe8whOTpph0uSY9c6oVkA1CiVr64XWs-bXyNwRLq4_Ni_nZbAVYO-ThL8T5QUa9-u-Kz3MlV1CKZzQjMEfcJ4tGbI.png) 
            - 
        - <mark style="background:#AD21D9;">Method: difference (- operator):</mark> 
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2Fgu1Soj4a0DZnIFBfhUycdVoHfU2BxK8TIFhuMbx622SVuKZIw_ivFUEvrzEvW8vmjuKAXQbnPW-Up9gISAZTasRL5XmBiZV91CVkyz3PbkNcvZkzIAaIPuhmGCVDLvZ5.png) 
            - 
        - <mark style="background:#AD21D9;">Method: union ( | operator):</mark> 
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FrTmbGIs0a40BFrSLKkqIVYvamye2x1lCXsFgZnuD-y3l14Ffbs_ZdnSWNoiTWuLXVp38HzPMF5O9pznP8RC-Hn7f4a6biLTjIjKOctTA4vNqqHaRRQ_E8uVqnHWth_R7.png) 
            - 
        - <mark style="background:#AD21D9;">Method: symmetric_difference ( ^ operator)</mark> 
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FTQGOBUaAG7ps8Rqa9XO-B6rtOcbU6mStucNxaKphp_zSf8Z8mZ0VK_F-k6CQBbEXKLmc_Rwhdehq_pfflh9AoPoZcaqrsag4ADpiI3jb23ECTkIZjwKQxE5bTpQGSyD1.png) 
            - 
        - <mark style="background:#AD21D9;">Method: issubset ( ⇐ operator) and issuperset ( >= operator)</mark> 
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2Fumyf9ByyghnizuGEuU_4vMmpYnFZa-qeqCdsX_DLeQBA0uu-oQtQJwq_SbsILGZi8qiE3ANA9lB2YIJoJhE3T6c03AorCBdg-pnVhJ49pEpUSWsXAikcIPiYhHqqFnvN.png) 
            - 
        - 
    - <mark style="background:#AD21D9;">Other Set Methods:</mark> 
        - .
            ```Python
            #adds to the set, no effect if item is in set already
my_set.add("g")

#empties the set
my_set.clear()

#remove throws an error if "g" isn't there, discard does not
my_set.remove("g")
my_set.discard("g")

#returns a shallow copy of my_set
my_set.copy() 
            ```
    - 
    - 
- <mark style="background:#AD21D9;">More on Functions</mark> 
    - <mark style="background:#AD21D9;">Defining scope:</mark> 
        - 
        - <mark style="background:#AD21D9;">^Scope: </mark>^Refers to the understanding, for any variable, what its assocated value is
        - <mark style="background:#AD21D9;">^Problem:</mark>^ multiple namespaces might be involved (when a function is executed, it creates its own namespace)
        - 
    - <mark style="background:#AD21D9;">Namespace:</mark> 
        - 
        - A <mark style="background:#AD21D9;">^namespace</mark>^ is the table that contains the association of a name with a value
        - 
        - <mark style="background:#AD21D9;">Find the namespace:</mark> 
            - 
            - For Python, there are potentially multiple namespaces that could be used to determine the object associated with a variable
            - Remember, namespace is an association of name and objects
            - We will begin by looking at functions
            - 
        - <mark style="background:#AD21D9;">A function's namespace:</mark> 
            - 
            - Each function maintains a namespace for names defined <mark style="background:#AD21D9;">^locally within the function</mark>^ 
            - Locally means one of two things
                - A name assigned within the function
                - An argument received by invocation of the function
                - 
            - 
        - 
    - <mark style="background:#AD21D9;">Passing:</mark> 
        - 
        - <mark style="background:#AD21D9;">Passing an argument to a parameter:</mark> 
            - 
            - For each argument in the function invocation, the argument's associated object is passed to the corresponding parameter in the function
            - 
        - <mark style="background:#AD21D9;">Passing immutable objects:</mark>
            - 
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2Fu2Gfnz0_-IFc7FsEOeeTBgsUr5RTasvip94o5DPDOWpPsMSceVZNQNT8oCOQobWhV7sY4qxGpLbGm-hFZE_BvpIvZ4-lbHdA50U5LOpyCSkHuu5UptiTqGpT0sMWc3p3.png) 
            - 
        - <mark style="background:#AD21D9;">What does "passing" mean?</mark> 
            - 
            - The diagram should make it clear that the parameter name is local to the function namespace
            - Passing means that the argument and the parameter share an association with the same object
            - So "passing" means <mark style="background:#AD21D9;">^"sharing"</mark>^ in Python
            - 
        - <mark style="background:#AD21D9;">Assignment changes association:</mark>
            - 
            - If a parameter is assigned to a <mark style="background:#AD21D9;">^new value</mark>^, then (just like any other assignment) a <mark style="background:#AD21D9;">^new association</mark>^ is created
            - This assignment <mark style="background:#AD21D9;">^does not affect</mark>^ the <mark style="background:#AD21D9;">^object </mark>^associated with the argument, as a new association was made with the parameter
            - 
            - 
        - <mark style="background:#AD21D9;">Passing immutable objects:</mark> 
            - 
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FFwtGCb55weuyK0bFzv_tDKoQesLd3rS4J59w1Cllr0rXQ-p5ToFF0XNpHSSSlwQ2EGzGe37eHRmktlqmfuh5X4TYvJ-ZYFFIPTuAiwD3uF-Xsy3WQSg4bCNvBNzgPTTS.png) 
            - 
        - <mark style="background:#AD21D9;">Sharing mutables:</mark>
            - 
            - When passing mutable data structures, it is possible that if the shared object is directly modified, both the parameter and the argument reflect the change
            - Note that the operation must be <mark style="background:#AD21D9;">^a mutable change</mark>^, a change of the object. An <mark style="background:#AD21D9;">^assignment</mark>^ is <mark style="background:#AD21D9;">^not</mark>^ such a change
            - 
        - <mark style="background:#AD21D9;">Passing mutable objects:</mark>
            - 
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FnZZGXP84vSKPazvp6q0nPnj5u7DGEKQ8-Fl1q7wKDwOdX0qD7Hxr0QGke6cbbIABaK_I0fO_fkZ4r_AXCDU3_myeRl-ysQmnKhHGtfOreuLp2ywJTCgpul19_V18jtea.png) 
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2F-oCkcttNeUWBrpMnpKZdm1l1RyQFBPmLiSDB5Ja6HJx3QDT5m7U4TznpqWyyWDwBnNZo9SQF2onV0W4TwUSY0vju-bMRIotWu023vfxU3lqqeidY9oVNlkQSlOcfXtMM.png) 
            - 
        - <mark style="background:#AD21D9;">Assignment to a local variable:</mark> 
            - 
            - Assignment creates a <mark style="background:#AD21D9;">^local variable</mark>^ 
            - Changes to a local variable affects only the local context, even if it is a parameter and mutable
            - If a variable is assigned locally, cannot reference it before this assignment, even if it exists in main as well
            - .
                ```Python
                def my_fun():
    print (a)
    a = 20
    print (a)
        
a = 10
my_fun() 
                ```
            - 
        - <mark style="background:#AD21D9;">Default and Named parameters</mark>
            - 
            - .
                ```Python
                def box(height = 10, width = 10, depth = 10, colour = "blue"):
    print(height, width, length)
                ```
            - 
            - The parameter assignment means two things:
                - If the caller does not provide a value, the default is the parameter assigned value
                - You can get around the order of parameters by using thr name
                - 
            - If you call the function with no parameters, it will just print the values assigned in the function definition (<mark style="background:#AD21D9;">^the defaults</mark>^) 
            - .
                ```Python
                #Named parameter:

def box(height = 10, width = 10, length = 10):
    print(height, width, length)

#prints 25 10 25
box(length = 25, height = 25)

#prints 15 15 15
box(15, 15, 15) 
                ```
            - 
            - .
                ```Python
                def my_fun(a,b):
    print(a,b)
   
#prints 1 2
my_fun(1,2)

#prints 2 1
my_fun(b = 1, a = 2) 
                ```
            - 
        - <mark style="background:#AD21D9;">Default args and mutables:</mark> 
            - 
            - One of the the problems with default arguments occurs with mutables. This is because:
                - The <mark style="background:#AD21D9;">^default value is created once</mark>^ when the function is defined and stored in the function namespace
                - A mutable can change that value of that default
                - 
            - .
                ```Python
                def fn1 (arg1=[], arg2=27):
arg1.append(arg2)
    return arg1


my_list = [1,2,3]

# [1, 2, 3, 27]
print(fn1(my_list)) 
    
# [27]
print(fn1()) 

# !!! [27, 27]             
print(fn1())               
                ```
            - 
        - 
    - <mark style="background:#AD21D9;">Functions as Objects and Docstrings:</mark>
        - 
        - Functions are objects, just like anything else in Python. As such, they have attributes and methods
        - There is a special set of properties which names start and end with a <mark style="background:#AD21D9;">^double underscore</mark>^, they have a special meaning
        - .
            ```Python
            _ _name_ _ : function name
_ _str_ _  : string function
_ _dict_ _ : function namespace
_ _doc_ _ : docstring

            ```
        - 
    - <mark style="background:#AD21D9;">Function annotations:</mark> 
        - 
        - You can associate strings of information, ignored by Python, with a parameter
        - To be used by the reader or user, the colon ":" indicates the parameter annotation, the "⇒" annotation is associated with the return value stored in dictionary "name_fn._annotations__ "
        - .
            ```Python
            def my_func (param1 : int, param2 : float) -> None :
   print('Result is:', param1 + param2)

>>> my_func(1, 2.0)

Result is: 3.0

>>> my_func(1, 2)

Result is: 3

>>> my_func('a', 'b')

Result is: ab

>>> my_func.__annotations__
{'return': None, 'param2': <class 'float'>, 'param1': <class 'int'>}

            ```
        - 
        - <mark style="background:#AD21D9;">Docstring:</mark>
            - 
            - If the item after the def is a string, then that string is specially stored as the <mark style="background:#AD21D9;">^docstring </mark>^of the function
            - This string describes the function and is what is shown if you do a help on a function
            - Usually triple quoted since it is multi-lined
            - Every object can have a docstring, it is stored as an attribute of the function
            - 
        - <mark style="background:#AD21D9;">Arbitrary arguments:</mark>
            - 
            - It is also possible to pass an arbitrary  number of arguments to a function
            - The function simply collects all the arguments into a tuple to be processed by the function
            - Tuple parameter is preceded by *
            - .
                ```Python
                def aFunc(fixedParam,*tupleParam):
   print("fixed =",fixedParam)
   print("tuple =",tupleParam)

#prints	fixed=1 tuple=(2,3,4)
aFunc(1,2,3,4)

#prints	fixed=1	tuple=()				
aFunc(1)

#prints fixed=4 tuple=()
aFunc(fixedParam=4)

                ```
            - 
        - 
    - <mark style="background:#AD21D9;">Summary:</mark> 
        - 
        - <mark style="background:#AD21D9;">^Scope </mark>^is the set of program statements over which an object exists
        - <mark style="background:#AD21D9;">^Passing multiple objects</mark>^ allows a function to change values in the calling program
        - <mark style="background:#AD21D9;">^Default parameters</mark>^ are specified with assignment (=), e.g. `param = value` 
        - <mark style="background:#AD21D9;">^Don't use a mutable</mark>^ object as a <mark style="background:#AD21D9;">^default parameter</mark>^ value
        - Optionally, parameters can be specified in an invocation using the <mark style="background:#AD21D9;">^name of the parameter</mark>^, e.g. fun(param = 4)
        - <mark style="background:#AD21D9;">^Docstrings </mark>^describe a function's purpose and appear in the line after the function header
        - <mark style="background:#AD21D9;">^Arbitrary number of arguments</mark>^ can be defined by a tuple parameter preceded by *
        - 
    - 
    - 
    - 
    - 
    - 
    - 
    - 
    - 
    - 
    - 
    - 
- <mark style="background:#AD21D9;">Classes</mark> 
    - <mark style="background:#AD21D9;">What is a class?</mark> 
        - 
        - .
            ```Python
            class Student(object):
   """Simple student class"""

   def __init__(self, first="", last="", id=0, grade=0):  # initializer
       self.first_name_str = first
       self.last_name_str = last
       self.id_int = id
       self.grade = grade

   def __str__(self):
       return "{} {}, ID: {}".format(self.first_name_str, self.last_name_str, self.id_int)

   def print_grade(self):
       return "Grade is: {}".format(self.grade)


student1 = Student("Lucas", "Rizzo", 1, 100)
print(student1.print_grade())
            ```
        - 
        - <mark style="background:#AD21D9;">^Object Oriented Programming</mark>^ is a way to think about "objects" in a program (such as variables, functions, etc)
        - A program becomes less a list of instructions and more a set of objects and how they interact
        - 
    - <mark style="background:#AD21D9;">Responding to "messages":</mark> 
        - 
        - As a set of interacting objects, each object responds to "messages" sent to it
        - The interaction of objects via messages makes a high level description of what the program is doing
        - 
    - <mark style="background:#AD21D9;">Everything in Python is an object:</mark> 
        - 
        - As we said previously - everything in Python is an object
        - Thus Python embraces OOP at a fundamental level
        - 
    - <mark style="background:#AD21D9;">Type vs Class:</mark> 
        - 
        - There is a strong similarity between a type and a python class
        - <mark style="background:#AD21D9;">^Types </mark>^includes list, dict, str
        - They are suitable for representing different data
        - Respond to different messages regarding the manipulation of that data
        - Python is fundamentally an OOP language
        - When we call a constructor such as list or str, we are making a new object
        - Those objects have attributes and respond to methods
        - We can sort a list by calling the method `my_list.sort()`, change a string to lowercase with the method `my_str.lower()` 
        - 
    - <mark style="background:#AD21D9;">Encapsulation:</mark> 
        - 
        - Hiding the details of the underlying data structures means that the changes can be made to the object, while the flow of messages (methods and their results) can stay the same
        - Thus the underlying implementation can change but its intended effect stay the same
        - This is known as <mark style="background:#AD21D9;">^encapsulation</mark>^ 
        - 
    - <mark style="background:#AD21D9;">OOP principles:</mark> 
        - 
        - <mark style="background:#AD21D9;">^Encapsulation:</mark>^ hiding design details to make the program clearer and more easily modified later
        - <mark style="background:#AD21D9;">^Modularity:</mark>^ the ability to make objects stand alone they can be reused 
        - <mark style="background:#AD21D9;">^Inheritance:</mark>^ create a new object by inheriting many object characteristics while creating or over-riding for this object
        - <mark style="background:#AD21D9;">^Polymorphism:</mark>^ Allow one message to be sent to any object and have it respond appropriately based on the type of object it is (such as `count` and `len` functions
        - 
    - <mark style="background:#AD21D9;">Classes vs Instances:</mark> 
        - 
        - You define a class as a way to generate new instances of that class
        - Both the instances and the classes are themselves objects
        - The structure of an instance starts out the same, as dictated by the class
        - The instances respond to the messages defined as part of the class
        - 
    - <mark style="background:#AD21D9;">Why a class?</mark> 
        - 
        - We make classes because we need more complicated, user-defined data types to construct instances we can use
        - Each class has potentially two aspects:
            - The <mark style="background:#AD21D9;">^data </mark>^that each instance might contain
            - The <mark style="background:#AD21D9;">^messages </mark>^that each instance can respond
            - 
        - 
    - <mark style="background:#AD21D9;">Our first class:</mark> 
        - 
        - The standard way to name a class in Python is called <mark style="background:#AD21D9;">^CamelCase</mark>^:
            - Each word of a class begins with a capital letter
            - No underlines
            - Makes recognising a class easier
            - 
        - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FaeZRppzC5yg0yxcRsT5I6GfRFDKsSLOnEC9BWjbmxUbHppmY-dT5eVVoVbUYoqy4stZQmB8hsJGuydzNDieZy7bSqhg-RSlNf71N96IJqtWHvqCwleWet2r3McC1PEoL.png) 
        - 
    - <mark style="background:#AD21D9;">Constructor:</mark> 
        - 
        - When a class is defined, a function is made with the <mark style="background:#AD21D9;">^same name as the class</mark>^ 
        - This function is called the <mark style="background:#AD21D9;">^constructor</mark>^. By calling it, you create an instance of the class
        - We can affect this creation, but by default Python can make an instance
        - 
    - <mark style="background:#AD21D9;">dir() function:</mark> 
        - 
        - The `dir` function lists all the attributes of a class
        - You can think of these as keys in a dictionary stored in the class
        - 
    - <mark style="background:#AD21D9;">dot reference</mark> 
        - 
        - We can refer to the attributes of an object by doing a dot reference of the form `obj.attribute` 
        - The attribute can be a variable or a function
        - It is part of the object, either directly or by that object being part of a class
        - 
    - <mark style="background:#AD21D9;">How to make an object-local value:</mark> 
        - 
        - Once an object is made, the data is made the same way as in any other Python situation, by assignment
        - Any object can thus be augmented by adding a variable
        - 
    - <mark style="background:#AD21D9;">Class Instance Relationship:</mark> 
        - 
        - Because each instance has as its type that it was made from, an instance remembers its class
        - This is often called the<mark style="background:#AD21D9;">^ instance-of</mark>^ relationship stored in the <mark style="background:#AD21D9;">^__class__</mark>^ attribute of the instance
        - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2Fb6hMwiETJzEJFIwbCNLvjXrpQ63EuIZvl_jv0IquDoOOn6mH-EHWrAz8Ji9MLlBhZluTVCUzKCYsBrL0PAmRLyVQ0qov2l-WNTvQmHPodHZOd7ah5-bQiE3sCcyyukB8.png)
        - 
        - <mark style="background:#AD21D9;">Object Scope Rule:</mark>
            - The first two rules in the object scope are:
                1. First, look in the object itself
                2. If the attribute is not found, look up to the class of the object and search for the attribute there
                - 
            - 
        - 
    - <mark style="background:#AD21D9;">Methods:</mark> 
        - 
        - A method and a function are closely related. They are both "small programs" that have  parameters, perform some operation and potentially return a value
        - The main difference is that methods are functions tied to a particular object
        - 
        - <mark style="background:#AD21D9;">Difference in calling:</mark>
            - Functions are called by name anywhere in the program, methods are called in the context of an object:
            - 
            - .
                ```Python
                function:
    do_something(param1)
method:
    obj.do_something(param1)
                ```
            - 
            - This means that the object that the method is called on is <mark style="background:#AD21D9;">^always implicitly a parameter</mark>^ 
            - 
        - <mark style="background:#AD21D9;">Difference in definition:</mark>
            - 
            - Methods are defined <mark style="background:#AD21D9;">^inside </mark>^the suite of a class
            - Methods always bind the first parameter in the definition to the object that called it
            - This parameter can be named anything, but traditionally it is named self
            - .
                ```Python
                class MyClass(object):
    def my_method(self, param1):
        suite 
                ```
            - 
            - `self` is an important variable. In any method it is bound to the object that called the method
            - Through `self` we can access the instance that called the method
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FHFOQWUowtp3T-_On8LgA4rbnm_PDEUB982pU4dgpLQjqdRgpHekCDY6bbv8ui-KB-FZ0oICxg5XGah_cstuuyGWk1pTusGm6tJH5PC628uRR78TCOEvTbUq6eeBUJnfT.png) 
            - 
        - <mark style="background:#AD21D9;">Self is bound for us:</mark> 
            - 
            - When a dot method call is made, the object that called the method is <mark style="background:#AD21D9;">^automatically </mark>^assigned to `self` 
            - We can use `self` to remember, and therefore refer, to the calling object
            - To reference any part of the calling object, we must always precede it with `self` 
            - The method can be written genetically, dealing with calling objects through self
    - 
    - 
    - 
    - 
    - 
- <mark style="background:#AD21D9;">Writing a class</mark> 
    - <mark style="background:#AD21D9;">Python Standard Methods:</mark> 
        - 
        - Python provides a number of standard methods which, if the class designer provides, can be used in a normal "Python" way
        - Many of these have the double underlines in the front and back of their names
        - By using these methods, we "fit in" to the normal Python flow
        - 
    - <mark style="background:#AD21D9;">Standard Method: Constructor</mark> 
        - 
        - Constructor is called when an instance is made, and provides the class designer the opportunity to set up the instance with variables, by assignment
        - 
        - <mark style="background:#AD21D9;">Calling a constructor:</mark>
            - 
            - A constructor class is called by using the name of the class as a function call
            - 
            - .
                ```Python
                student_inst = Student()
                ```
            - 
            - Creates a new instance using the constructor from class `Student` 
            - 
        - <mark style="background:#AD21D9;">Defining the constructor:</mark>
            - 
            - One of the special method names in a class is the constructor name __init__ 
            - By assigning the values in the constructor, every instance will start out with the same 
            - You can also pass arguments to a constructor through its init method
            - Example:
                - .
                    ```Python
                    def __init__ (self, first='', last='', id=0):
      self.first_name_str = first
      self.last_name_str = last
      self.id_int = id

                    ```
            - 
            - `self` is bound to the default instance as it is being made
            - If we want to add an attribute to that instance, we modify the attribute with self
                - .
                    ```Python
                    s1 = Student()
print(s1.last_name_str)
>>>

s2 = Student(last='Python', first='Monty')
print(s1.last_name_str)
                    ```
            - 
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FTffGUai2Y5lH8gtCxoTkGB05_247ixVoCWUBntpjgPM67xLIICUg88wNkX6epxsiMln2-N8xjjJZSGmOvWQqETVYVoQ0XMYDEOxvE_l7lqnkQmp4IUQVbHOK_EzSm7yJ.png) 
            - 
        - <mark style="background:#AD21D9;">Default constructor:</mark>
            - 
            - If you don't provide a constructor, then only the default constructor is provided
            - The default constructor does system stuff to create the instance, nothing more
            - You cannot pass arguments to the default constructor
            - 
        - 
    - <mark style="background:#AD21D9;">Every class should have __init__</mark>
        - 
        - By providing the constructor, we ensure that every instance, at least at the point of construction, is created with the same contents
        - This gives us some control over each instance
        - 
    - <mark style="background:#AD21D9;">__str__, printing:</mark> 
        - 
        - .
            ```Python
            def __str__(self):
   return "{} {}, ID: {}".format(self.first_name_str, self.last_name_str, self.id_int)
            ```
        - 
        - When `print(my_inst)` is called, it is assumed, by Python, to be a call to “convert the instance to a string”, which is the <mark style="background:#AD21D9;">^__str__</mark>^ method 
        - In the method, `my_inst` is bound to `self`, and printing then occurs using that instance.
        - `__str__` <mark style="background:#AD21D9;">^must return a string</mark>^!
        - 
    - <mark style="background:#AD21D9;">Summary:</mark> 
        - 
        - Make sure your class does the right thing. A class should behave in a way similar to a Python Programmer e.g. the ability to call the print function on it.
        - <mark style="background:#AD21D9;">^OOP </mark>^helps <mark style="background:#AD21D9;">^software engineering</mark>^ 
        - <mark style="background:#AD21D9;">^Software Engineering</mark>^ is the discipline of <mark style="background:#AD21D9;">^managing </mark>^code to ensure its <mark style="background:#AD21D9;">^long-term</mark>^ use
        - 
        - <mark style="background:#AD21D9;">OOP:</mark> 
            - Takes existing code and modifies it
            - Makes the overall code simpler, easier to understand
            - Doesn't change the functionality, only the form
            - 
        - <mark style="background:#AD21D9;">Encapsulation means:</mark>
            - Understanding the details of the underlying class structure should not be necessary to utilise an instance of a class
            - Hide details of the implementation so that the program is easier to read and write
            - 
        - <mark style="background:#AD21D9;">^Modularity:</mark>^ makes an object reusable in other other contexts, providing an interface (the methods) that are the approved way to deal with the class
        - Creating a new class creates a new type
        - A class is to its instance as a cookie cutter is to a cookie
        - Classes have attributes and methods that act on those attributes
        - Attributes are usually created within the `__init__` method
        - The identifier `self` refers to the current instance
        - The first parameter of methods is self
        - 
        - <mark style="background:#AD21D9;">Class structure:</mark> 
            - 
            - .
                ```Python
                Class structure 

class ClassName(object):
   def __init__(self, param1=4):
       self.att = param1 # create attribute.

   def __str__(self):
       return "some string"

   def some_method(self,param):
       # do something
                ```
    - 
    - 
    - 
    - 
    - 
    - 
    - 
    - 
    - 
- <mark style="background:#AD21D9;">Inheritance</mark> 
    - <mark style="background:#AD21D9;">Class-Instance relations:</mark> 
        - 
        - Remember the <mark style="background:#AD21D9;">^relationship </mark>^between a class and its instances:
            - A class can have many instances, each made initially from the <mark style="background:#AD21D9;">^constructor </mark>^of the class
            - The <mark style="background:#AD21D9;">^methods </mark>^an instance can call are initially <mark style="background:#AD21D9;">^shared </mark>^by all instances of a class
            - 
        - 
    - <mark style="background:#AD21D9;">Class-Class relations:</mark> 
        - 
        - Classes can also have a <mark style="background:#AD21D9;">^separate relationship</mark>^ with other classes
        - The relationships forms a <mark style="background:#AD21D9;">^hierarchy </mark>^ 
        - 
        - <mark style="background:#AD21D9;">Computer science "trees"</mark> 
        - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FfPK9YRRgSIZB9kGyVAWxu6kfyrNkPMnAiblvmgZc365xXRfQa8VrY31AGUX5uJVhMHflA5wQHAALAfwJ7iY3Ba3ZqJMG7b8D2Q2szlNOnmU6ZAm9ZMCNNcvKf5Vog-fe.png) 
        - 
        - <mark style="background:#AD21D9;">Classes related by a hierarchy:</mark> 
            - 
            - When we create a class, which itself is another object, we can state <mark style="background:#AD21D9;">^how </mark>^it is <mark style="background:#AD21D9;">^related </mark>^to other <mark style="background:#AD21D9;">^classes</mark>^ 
            - The relationship we can indicate is the class that is <mark style="background:#AD21D9;">^'above'</mark>^ it in the hierarchy
            - 
        - <mark style="background:#AD21D9;">Class statement:</mark> 
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FSsFosLzJscZ9XLWVkfrlhuOkbtqQ_FCdWkXSoee0Xn7EHMfxGfbRNwB8Sc_gB5izlTidcGKRo97MNK2xbfOHxa7xYPe-Nqezj20IZVXEG2M4DquavJpl7CXrTjenHYCm.png) 
            - The top class in Python is called <mark style="background:#AD21D9;">^object</mark>^:
                - It is predefined by Python, always exists
                - Use object when you have no superclass
                - 
            - 
        - <mark style="background:#AD21D9;">Simple class hierarchy:</mark> 
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2F-fk-KnfoPqCsnSrj0rrjZsP-QzqFdZwQnv6Im7f3bignEisJNDAtxMIWU_sZO3gnkdvg7lmUwLTspqxrGtc8Jg4BdBuCpXA4Up-f3uQP7Appq8kcZvmSJ6h-wqN-34kC.png) 
            - 
        - <mark style="background:#AD21D9;">is-a: super and sub class:</mark> 
            - 
            - The class hierarchy imposes an <mark style="background:#AD21D9;">^is-a</mark>^ relationship between classes

                - MyChildClass <mark style="background:#AD21D9;">^is-a</mark>^ MyClass
                - MyClass <mark style="background:#AD21D9;">^is-a</mark>^ object
                - object has as a <mark style="background:#AD21D9;">^subclass</mark>^** **MyClass
                - MyChildClass has as a <mark style="background:#AD21D9;">^superclass</mark>^** **MyClass
                - 
            - 
        - 
    - <mark style="background:#AD21D9;">Inheritance:</mark> 
        - 
        - Different kinds of objects have certain things in <mark style="background:#AD21D9;">^common</mark>^:
            - <mark style="background:#AD21D9;">^Example</mark>^: trucks, cars, motorbikes are all motorised vehicles
            - <mark style="background:#AD21D9;">^States</mark>^: current speed, current gear, cc value…
            - <mark style="background:#AD21D9;">^Behaviours</mark>^: drive, stop, change gear. Some are executed slightly differently, depending on vehicle -> <mark style="background:#AD21D9;">^method overwriting</mark>^
            - 
        - OOP allows classes to inherit certain traits, aka common states and behaviours, and implement their own versions if required.  
        - 
    - <mark style="background:#AD21D9;">Using Inheritance:</mark> 
        - 
        - If a new class is created as part of an existing class hierarchy, then the new class can reuse existing code from the hierarchy, specializing only those aspects or attributes that are unique to the new class.
        - It emphasizes a need that OOP often fills: group development.
        - Developers need to work together to create software, and OOP is a tool to help in that regard.
        - 
        - <mark style="background:#AD21D9;">Example:</mark> 
            - 
            - Physicists have developed the Standard Model.  
            - It is a description of all the fundamental pieces from which matter is constructed and three of the fundamental forces of nature (gravity not yet being incorporated)
            - It describes particles by a number of attributes, including mass, spin, charge, and name. They also have intrinsic attributes, such as location (in three dimensional space) and velocity (direction of movement in three-dimensional space).
            - This classification of particles is perfect for a class hierarchy.
            - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FCfXCmE3AZtuJCHniVuiWknaLMoh8ayK1_nc_b_xDRE5ID8ihWfXofj97mBVHU3OQcOs_2JII4dhMFyWo8vTiSHHYUaByvgEh9GKJX1DE8k4xTipkWwEL-qPScl8S51VT.png) 
            - 
            - .
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
                spin=0.0, mass=0.0):
      
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
            - 
        - 
    - <mark style="background:#AD21D9;">Bound methods:</mark> 
        - 
        - Normal methods are called <mark style="background:#AD21D9;">^bound methods</mark>^. Bound methods have an instance in front of the method call and automatically pass self
        - .
            ```Python
            my_inst = MyClass()
my_inst.method(arg1,arg2)

#my_inst is an instance, so the method is bound
            ```
        - 
    - <mark style="background:#AD21D9;">Unbound methods:</mark> 
        - 
        - It is also possible to call a method <mark style="background:#AD21D9;">^without Python binding </mark>^`self`. In that case, the user has to do it.
        - Unbound methods are <mark style="background:#AD21D9;">^called </mark>^as part of the <mark style="background:#AD21D9;">^class </mark>^but `self` is passed by the user
        - 
        - .
            ```Python
            my_inst = MyClass()
MyClass.method(my_inst, arg2, arg3)

#self is passed explicitly (my_inst ) here!
            ```
        - 
        - <mark style="background:#AD21D9;">Why unbound methods?</mark> 
            - 
            - Consider an example. We want to specialise a new class as a subclass of list. 
                - 
                - .
                    ```Python
                    class MyClass(list):
                    ```
                - 
            - But we want to make sure that we get our new class instances initialized the way they are supposed to, by calling `__init__` of the super class
            - If we don't explicitly say so, our class may inherit stuff from the super class, but we must make sure we call it in the proper context. For example, our `__init__` would be:  
            - 
        - We explicitly call the <mark style="background:#AD21D9;">^super class constructor</mark>^ using an unbound method
        - Then, <mark style="background:#AD21D9;">^after </mark>^it <mark style="background:#AD21D9;">^completes </mark>^we can do anything special for our new class
        - We <mark style="background:#AD21D9;">^specialise </mark>^the <mark style="background:#AD21D9;">^new class</mark>^ but <mark style="background:#AD21D9;">^inherit </mark>^most of the work from the <mark style="background:#AD21D9;">^super</mark>^. 
        - 
    - <mark style="background:#AD21D9;">Method Overwriting:</mark> 
        - 
        - Ability of a class to change the implementation of a method that is provided by one of its ancestors
        - A very important concept in OOP
        - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FGPGRXheVp-NykIk5vMayfiPwpephpQ27tQgg3X4fv7Ew2Qm6hzzoOgppWdS_JXA4W9GA8mcocZieMMj_57ip-vFP0w8wf1yCp8hLejipjSbUbl-B6H03mofIUQUeUoeS.png) 
        - 
        - <mark style="background:#AD21D9;">It gives us a way to organise code:</mark> 
            - 
            - <mark style="background:#AD21D9;">^Specialisation:</mark>^ A subclass can inherit code from its superclass, but modify anything that is particular to that subclass
            - <mark style="background:#AD21D9;">^Override:</mark>^ change a behavior to be specific to a subclass
            - <mark style="background:#AD21D9;">^Reuse-code:</mark>^ Use code from other classes (without rewriting) to get behavior in our class.
            - 
        - 
    - <mark style="background:#AD21D9;">Expanded class organisation example:</mark> 
        - 
        - .
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
    - 
    - 
    - 
    - 
    - 
    - 
    - 
    - 
    - 
- <mark style="background:#AD21D9;">Aggregation and Composition</mark> 
    - <mark style="background:#AD21D9;">Composition:</mark> 
        - 
        - Composition is a concept that models a <mark style="background:#AD21D9;">^has-a</mark>^ relationship.
        - It enables creating complex types by combining objects of other types.
        - Composition enables the reuse of code without having to inherit.
        - 
        - <mark style="background:#AD21D9;">Example:</mark> 
            - .
                ```Python
                class Horse(object):

   def __init__(self, age=0, breed="", tail_length = 0, tail_braid=False):
       self.age = age
       self.breed = breed
       self.tail = Tail(tail_length, tail_braid)

   def __str__(self):
       return "Horse age is {}. The breed is {}. {}".format(str(self.age), self.breed, str(self.tail))
       
class Tail(object):

   def __init__(self, tail_length = 0, tail_braid=False):
       self.tail_length = tail_length
       self.tail_braid = tail_braid

   def __str__(self):
       return_str = "The tail is " + str(self.tail_length) + "m long. "

       if self.tail_braid:
           return_str += "It has a braid."
       else:
           return_str += "It does not have a braid."

       return return_str

appaloosa = Horse(5, "appaloosa", 0.8)
falabella = Horse(3, "falabella", 1.2, True)

print(appaloosa)
print(falabella)

#Output
#Horse age is 5. The breed is appaloosa. The tail #is 0.8m long. It does not have a braid.
#Horse age is 3. The breed is falabella. The tail #is 1.2m long. It has a braid.
 
                ```
            - 
        - 
    - <mark style="background:#AD21D9;">Aggregation:</mark> 
        - 
        - <mark style="background:#AD21D9;">^Aggregation </mark>^is a weak form of composition.
        - The difference is that both objects are independent of each other.
        - .
            ```Python
            class Horse(object):

   def __init__(self, age=0, breed="", tail):
       self.age = age
       self.breed = breed
       self.tail = tail

   def __str__(self):
       return "Horse age is {}. The breed is {}. {}".format(str(self.age), self.breed, str(self.tail))
            ```
        - 
        - The `Tail` class is still the same
        - .
            ```Python
            class Tail(object):

   def __init__(self, tail_length = 0, tail_braid=False):
       self.tail_length = tail_length
       self.tail_braid = tail_braid

   def __str__(self):
       return_str = "The tail is " + str(self.tail_length) + "m long. "

       if self.tail_braid:
           return_str += "It has a braid."
       else:
           return_str += "It does not have a braid."

       return return_str
            ```
        -  
        - But the Tail instances are now created in the main, and passed to the Horse constructor. The output is the same   
        - .
            ```Python
            tail_appaloosa = Tail(0.8)
tail_falabella = Tail(1.2, True)

appaloosa = Horse(5, "appaloosa", 0.8)
falabella = Horse(3, "falabella", 1.2, True)

print(appaloosa)
print(falabella)
            ```
        - 
    - <mark style="background:#AD21D9;">Composition vs. Aggregation:</mark> 
        - 
        - Which one was better? Depends on the problem. 
        - When using composition, if you delete the horse you also delete the tail.
        - When using aggregation, if you delete the horse, the tail continues to exist.
        - In this case it is probably better to delete the tail with the horse.
    - 
    - 
- <mark style="background:#AD21D9;">Private vs Public Overloading</mark> 
    - <mark style="background:#AD21D9;">Encapsulation in OOP:</mark> 
        - 
        - <mark style="background:#AD21D9;">^Encapsulation:</mark>^  hides details of the implementation so that the program is easier to read and write  
        - <mark style="background:#AD21D9;">^Modularity:</mark>^ make an object so that it can be reused in other contexts
        - These provide an interface (the methods) that are the approved way to deal with the <mark style="background:#AD21D9;">^class</mark>^ 
        - 
    - <mark style="background:#AD21D9;">Private attributes/methods:</mark> 
        - 
        - Many OOP languages allow you to make an attribute or method <mark style="background:#AD21D9;">^private </mark>^ 
        - Private means <mark style="background:#AD21D9;">^not accessible</mark>^ by the<mark style="background:#AD21D9;">^ class user</mark>^, only the <mark style="background:#AD21D9;">^class developer</mark>^ 
        - There are advantages to controlling who can access the instance values
        - 
        - <mark style="background:#AD21D9;">Example:</mark> 
            - .
                ```Python
                class NewClass(object):
   def __init__(self, attribute="default", name="Instance"):
       self.name = name
       #The double underscore indicates privacy
       self.__attribute = attribute

   def __str__(self):
       return "{} has attributes {}".format(self.name, self.__attribute)


                ```
            - 
        - 
    - <mark style="background:#AD21D9;">Access modifiers in Java:</mark> 
        - 
        - <mark style="background:#AD21D9;">^public:</mark>^** **accessible anywhere by anybody
        - <mark style="background:#AD21D9;">^private:</mark>^ accessible within the class only
        - <mark style="background:#AD21D9;">^protected:</mark>^** **accessible within the class or subclass
        - .
            ```Python
            // Java class

public class Person {

   private String firstName;
   private String surname;

   public String getFirstName(){
         return firstName;
    }

. . .
}

            ```
        - 
    - <mark style="background:#AD21D9;">Access modifiers in Python - public:</mark> 
        - 
        - .
            ```Python
            class Person:
     def __init__(self, n, age):
          self.name = n
          self.age = age
          
p = Person('Mary', 20)
print(p.name)  #Will print Mary
            ```
        - 
        - Note that the class variable (<mark style="background:#AD21D9;">^name</mark>^) and the parameter in the constructor (<mark style="background:#AD21D9;">^n</mark>^) doesn’t have to have the same name!
        - However, following the naming conventions, in practice they often do
        - 
    - <mark style="background:#AD21D9;">Access modifiers in Python - Private:</mark> 
        - 
        - <mark style="background:#AD21D9;">^Private:</mark>^ use <mark style="background:#AD21D9;">^double underscore</mark>^ as the start of the variable or method name 
        - 
        - .
            ```Python
            class Person:
     def __init__(self, name, age):
          self.__name = name
          self.age = age
          
p = Person('Mary',  20)
print(p.name)     
#^  Error!  AttributeError: 'Person' object has no attribute 'name'
print(p.__name) 
#^  Error!   AttributeError: 'Person' object has no attribute '__name'
print(p._Person__name)  
#^  Returns 'Mary', but it is not a good practice. Other languages would not allow this.
 
            ```
        - 
        - What is the right way to access private attributes? Through public methods  
        - .
            ```Python
            class Person:
    def __init__(self, name, age):
         self.__name = name
         self.age = age

    def get_name(self):
         return self.__name 

    def set_name(self, name):
        self.__name = name
        
p = Person('Mary',  20)

print(p.get_name()) #← will print Mary

p.set_name('John') #← will update name

print(p.get_name()) #← will print John        
            ```
        - 
        - Get/set methods <mark style="background:#AD21D9;">^hide </mark>^the attributes of class from other classes.
        - No <mark style="background:#AD21D9;">^accidental modification</mark>^ of the data happens.
        - 
    - <mark style="background:#AD21D9;">Comments on privacy:</mark> 
        - 
        - <mark style="background:#AD21D9;">Classes:</mark> 
            - Use privacy only for attributes and methods that are completely internal to operation of object
                - Public attributes (variables, methods) are available to everyone (designer and programmer).
                - Private attributes (variables, methods) are available only to the designer.
        - <mark style="background:#AD21D9;">Objects:</mark> 
            - Minimize direct reading of objects attributes
            - Avoid directly altering objects attributes
            - Never directly access objects private attributes or methods
            - 
        - 
    - <mark style="background:#AD21D9;">Object-Oriented Programming - Operator Overloading:</mark>
        - 
        - <mark style="background:#AD21D9;">Another aspect:</mark> 
            - A new aspect we should consider in OOP is <mark style="background:#AD21D9;">^consistency</mark>^ 
            - A new class should be consistent with the rules of the language.
            - It should respond to standard messages, it should behave properly with typical functions (assuming the type allows that kind of call).
            - 
        - <mark style="background:#AD21D9;">Example - Rational Number class:</mark> 
            - 
            - Consider a <mark style="background:#AD21D9;">^Fraction number</mark>^** **class. 
            - It should respond to:
                - construction
                - printing
                - arithmetic ops (+, -, *, /)
                - comparison ops (<, >, <=, >=)
                - 
            - .
                ```Python
                r1 = Fraction(1,2)     # create the fraction 1/2
r2 = Fraction(3,2)     # create the fraction 3/2
r3 = Fraction(3)       # default denominator is 1, 
# so really creating 3/1

r_sum = r1 + r2          # use "+" in a familiar 
 								  # way

print(r_sum)              # use " print " in a 
4/2								# familiar way

if r1 <mark style="background:#AD21D9;"> r2:     # use equality check "</mark>" in a 
   # familiar way
  print('equal')
else:
  print('not equal')

not equal

print(r3 - r2)    # combine arithmetic and printing
                  # in a familiar way

3/2
 
                ```
            - 
            - Python can distinguish which <mark style="background:#AD21D9;">^operator </mark>^to use based on <mark style="background:#AD21D9;">^types</mark>^ 
            - Python provides more standard methods that represent the action of standard functions in the language. By defining them in our class, Python will call them in the "right way"
            - 
        - 
    - <mark style="background:#AD21D9;">More on Type:</mark> 
        - 
        - A class is essentially a new type
        - When we make an instance of a class, we have made an object of a particular type
        - For example:
            - 1.36 is a float
            - ` my_instance = MyClass()`  my_instance is of the type MyClass  
            - 
        - 
    - <mark style="background:#AD21D9;">Introspection:</mark> 
        - 
        - Python does <mark style="background:#AD21D9;">^not </mark>^have a <mark style="background:#AD21D9;">^type </mark>^associated with any variable, since each variable is allowed to reference any object
            - Unlike C and Java, for example, (int i)
            - 
        - However, we can <mark style="background:#AD21D9;">^query </mark>^any <mark style="background:#AD21D9;">^variable </mark>^as to what <mark style="background:#AD21D9;">^type </mark>^it presently references
        - This is often called <mark style="background:#AD21D9;">^introspection</mark>^, that is, while the program is running we can determine the type a variable references
        - 
    - <mark style="background:#AD21D9;">Python Introspection operations:</mark> 
        - 
        - `type(variable)`: returns its type as an object
        - `isinstance(variable,type)`: returns a boolean indicating if the variable is of that type
        - <mark style="background:#AD21D9;">Example:</mark> 
        - .
            ```Python
            def special_sum(a, b):
   """ Sum two ints or convert params to ints
       and add. return 0 if conversation fails."""
   if type(a) <mark style="background:#AD21D9;"> int and type(b) </mark> int:
       result = a + b
   else:
       try:
           result = int(a) + int(b)
       except ValueError:
           result = 0

   return result
            ```
        - 
    - <mark style="background:#AD21D9;">What does var1 + var2 mean?</mark> 
        - 
        - So what does `var1 + var2` mean?
        - Answer: it <mark style="background:#AD21D9;">^depends </mark>^on the <mark style="background:#AD21D9;">^type</mark>^ 
        - The `+` operation has two operands. What are their types?
        - Python uses <mark style="background:#AD21D9;">^introspection </mark>^to find the type and then select the correct operator
        - What does var1+var2 do?
            - with two <mark style="background:#AD21D9;">^strings</mark>^, we get concatenation
            - with two <mark style="background:#AD21D9;">^integers</mark>^, we get addition
            - with an <mark style="background:#AD21D9;">^integer </mark>^and a <mark style="background:#AD21D9;">^string </mark>^we get:
            - .
                ```Python
                Traceback (most recent call last):File "<pyshell#9>", line 1, in <module> 1+'a'
TypeError: unsupported operand type(s) for +: 	'int' and 'str'
                ```
            - 
        - 
    - <mark style="background:#AD21D9;">Operator overloading:</mark> 
        - 
        - The plus operator + is <mark style="background:#AD21D9;">^overloaded</mark>^ 
        - That means the operator can do/mean different things (have multiple/overloaded meanings) depending on the types involved
        - If python does not recognize the operation and that combination of types, you get an error
        - 
    - <mark style="background:#AD21D9;">Python overload operations:</mark> 
        - 
        - Python provides a set of operators that can be overloaded. You <mark style="background:#AD21D9;">^can't overload all</mark>^ the operators, but you can overload many
        - Like all the special class operations, they use the two underlines before and after their name
        - They come in three general classes:
            - <mark style="background:#AD21D9;">^numeric type</mark>^ operations (+,-,<,>,print etc.)
            - <mark style="background:#AD21D9;">^container </mark>^operations ([ ], iterate, len, etc.)
            - <mark style="background:#AD21D9;">^general </mark>^operations (printing, construction)
            - 
        - ![](local://C%3A%2FUsers%2Fdervl%2Fremnote%2Fremnote-644bbf51117a5271f76257fc%2Ffiles%2FneKTJbQKcXa_rmWS_fWZobnw27ZIRBkBHgW1NnDrBUxoh8kEjPPbJIb_AkUppAN__ZxW6_WVv6fK1XnAN41SQamwTJPhi-Qv0r2goEPG7IstyYDBLE8oJTXA5wBxf7a_.png) 
        - 
        - <mark style="background:#AD21D9;">Example:</mark> 
        - .
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
       """ Perform addition with param2, a MyClass instance.
           Return a new MyClass instance with sum as a value attribute"""
       print("in add")
       result = self.value + param2.value
       return MyClass(result)
            ```
        - 
    - <mark style="background:#AD21D9;">How does v1 + v2 map to __add__?</mark> 
        - 
        - .
            ```Python
            v1 + v2
#is turned, by Python, into
v1.__add__(v2)
            ```
        - These are exactly equivalent expressions. It means that the first variable calls the `__add__` method with the second variable passed as an argument
        - v1 is bound to `self`, v2 bound to `param2` 
        - 
    - <mark style="background:#AD21D9;">Calling __str__:</mark> 
        - 
        - When does the `__str__` method get called? Whenever a string representation of the instance is required:
            - <mark style="background:#AD21D9;">^Directly</mark>^, by saying  `str(my_instance)` 
            - <mark style="background:#AD21D9;">^Indirectly</mark>^, calling `print(my_instance)` 
            - 
        - 
    - <mark style="background:#AD21D9;">Simple Rational Number class:</mark> 
        - 
        - A <mark style="background:#AD21D9;">^Rational </mark>^is represented by two integers: the <mark style="background:#AD21D9;">^numerator </mark>^and the <mark style="background:#AD21D9;">^denominator</mark>^ 
        - We can apply many of the numeric operators to Rational
        - 
        - <mark style="background:#AD21D9;">Example - Fraction class:</mark> 
            - 
            - .
                ```Python
                class Fraction(object):
   """ Fraction with numerator and denominator. Denominator 
parameter defaults to 1"""

   def __init__(self, numer, denom=1):
       print('in constructor')
       self.numer = numer
       self.denom = denom

   def __str__(self):
       """ String representation for printing """
       print('in str')
       return str(self.numer) + '/' + str(self.denom)
                ```
            - 
        - 
    - <mark style="background:#AD21D9;">The __init__ method:</mark> 
        - 
        - Each instance gets an attribute `numer` and `denom` to represent the numerator and denominator of that instance's values  
        - .
            ```Python
            def __init__(self, numer, denom=1):
   print('in constructor')
   self.numer = numer
   self.denom = denom
            ```
        - 
    - <mark style="background:#AD21D9;">Rational number - Addition:</mark> 
        - 
        - Remember how we add fractions:
            - if the denominator is the same, add the numerators
            - if not, find a new common denominator that each denominator divides without remainder.
            - modify the numerators and add
            - 
        - <mark style="background:#AD21D9;">__add__:</mark> 
            - .
                ```Python
                def __add__(self, param):
   """ Add two Rationals . Allows int as a parameter"""
   print('in add')
   if type(param) <mark style="background:#AD21D9;"> int:  # convert ints to Rationals
       param = Fraction(param)
   if type(param) <mark style="background:#AD21D9;"> Fraction:
       # find a common denominator
       # ps: the optimal algorithm would find the lowest common denominator
       common_denominator = self.denom * param.denom
       numerator_sum = (common_denominator * self.numer / self.denom) + (
                   common_denominator * param.numer / param.denom)
       return Fraction(int(numerator_sum), common_denominator)
   else:
       print('wrong type')  # problem : some type we cannot handle
       raise (TypeError)
                ```
        - 
        - <mark style="background:#AD21D9;">__sub__:</mark> 
            - .
                ```Python
                def __sub__(self, param):
   """ Subtract two Rationals """
   print('in sub')
   # subtraction is the same but with '−' instead of '+'
   # ps: the optimal algorithm would find the lowest common 
# denominator
   common_denominator = self.denom * param.denom
   numerator_diff = (common_denominator * self.numer / self.denom) \  
                   - (common_denominator * param.numer / param.denom)
   return Fraction(int(numerator_diff), common_denominator)
                ```
            - 
        - <mark style="background:#AD21D9;">__eq__:</mark>
            - .
                ```Python
                def __eq__(self, param):
   """ Compare two Rationals for equality, return Boolean """
   print('in eq')
   return abs((self.numer / self.denom) \
              - (param.numer / param.denom)) < 0.0001
                ```
            - 
        - <mark style="background:#AD21D9;">Example:</mark> 
            - .
```Python
one_half = Fraction(1, 2)
two_fifths = Fraction(2, 5)

sum_Fraction = one_half + two_fifths
print(sum_Fraction) # 9/10

two = Fraction(2)
print(two - one_half) # 3/2

five_tenths = Fraction(5, 10)

if one_half <mark style="background:#AD21D9;"> five_tenths:
   print("equal")

multiplication = one_half * two_fifths
print(multiplication) # 2/10
                ```
            - 
        - 
    - <mark style="background:#AD21D9;">Summary:</mark> 
        - 
        - Overloading operators: A+B maps to `A.__add__(B)` 
        - which maps to `__add__(self, param)` by mapping A to self and mapping B to param
        - Expanded class organization:
        - .
            ```Python
            class ClassName(object):
  def __init__ (self,param):
      self.value <mark style="background:#AD21D9;"> param
  def __add__(self,param):
      the_sum = self.value + param.value
      return ClassName(the_sum)
  def __radd__(self,f):
      return self.__add__(f)
  def __str__(self):
      return str(self.value)
            ```
- 
