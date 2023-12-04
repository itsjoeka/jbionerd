WELCOME TO PYTHON LIST TUTORIAL,
INSTRUCTOR: JONATHAN KALAMI

PYTHON LISTS


```python
#creating a list
flis = ["first", 35, 2023]
#printing the list
print(flis)
flis
```

    ['first', 35, 2023]
    




    ['first', 35, 2023]




```python
print("positive and negative indexing of the first element\n-positive index: ",flis[0], "\n-negative index: ",flis[-3])
```

    positive and negative indexing of the first element
    -positive index:  first 
    -negative index:  first
    

exercise: create a list of four items and return the positive and negative index of the last element


```python
slis = ["second", 45, 3.5, 888]
print("positive and negative index of the last element \n-positive index:",slis[3],"\n-negative index:",slis[-1])
```

    positive and negative index of the last element 
    -positive index: 888 
    -negative index: 888
    

Lists can contain strings, floats, integers, boolean, nested list, nested tuples and other data types


```python
tlis = ["third", 3.14, 2023, [2,4,6,8], ("hello, world!", 1,3,4)]
tlis
```




    ['third', 3.14, 2023, [2, 4, 6, 8], ('hello, world!', 1, 3, 4)]



LIST OPERATIONS; slicing, extending, appending, len, count, insert, del, index


```python
#slicing
print(tlis[0:4])
print(tlis[2])
```

    ['third', 3.14, 2023, [2, 4, 6, 8]]
    2023
    


```python
#extending: add more than one element to an existing list
tlis.extend(["extend", 65, 3.55])
print(tlis)
```

    ['third', 3.14, 2023, [2, 4, 6, 8], ('hello, world!', 1, 3, 4), 'extend', 65, 3.55]
    


```python
#append: this is used to add one item to an already existing list
tlis.append(["append", 4, 6])
print(tlis)
```

    ['third', 3.14, 2023, [2, 4, 6, 8], ('hello, world!', 1, 3, 4), 'extend', 65, 3.55, ['append', 4, 6]]
    


```python
folis = [1,2,3,4,5,6,7]
print(folis)

#len: length of list
print(len(folis))

#append
folis.append(4)
print(folis)

#count: a particular element
folis.count(4)

#index: index of a particular element
print(folis.index(2))

#insert: add a new element to a index (i,n)
folis.insert(8,9)
print(folis)

#max and min: returns the maximum and minimum elements of a list
print(max(folis))
print(min(folis))

#sum of the items in a list
print(sum(folis))
```

    [1, 2, 3, 4, 5, 6, 7]
    7
    [1, 2, 3, 4, 5, 6, 7, 4]
    1
    [1, 2, 3, 4, 5, 6, 7, 4, 9]
    9
    1
    41
    

The items in a list are mutable therefore they can be changed


```python
#changing
filis = ["fifth", 35, 23, 56, "original"] 
print("Before changing the item: ", filis)
filis[4] = "changed"
print("After changing the item: ", filis)
print(filis.index("fifth"))

#deleting; del()
print("before deleting: ", filis)
del(filis[4])
print("after deleting: ", filis)
```

    Before changing the item:  ['fifth', 35, 23, 56, 'original']
    After changing the item:  ['fifth', 35, 23, 56, 'changed']
    0
    before deleting:  ['fifth', 35, 23, 56, 'changed']
    after deleting:  ['fifth', 35, 23, 56]
    

Conversion of a string into a list using split()


```python
message_one = "Python is an interesting programming language"
message_one.split()
#by default, the split function receives space as an argument. can specify it to comma
```




    ['Python', 'is', 'an', 'interesting', 'programming', 'language']




```python
#using split with a delimeter
text = "p,y,t,h,o,n"
samp ="p y t h o n"
#without delimeter, it converts into one element
print(text.split())
print(samp.split())
#with a delimeter, converts into multiple elements
text.split(",")
```

    ['p,y,t,h,o,n']
    ['p', 'y', 't', 'h', 'o', 'n']
    




    ['p', 'y', 't', 'h', 'o', 'n']




```python
#SOME BASIC LIST OPERATIONS
list_one = "a b hello python"
new_list = list_one.split()
print(new_list)
lis_two = [1,2,3,4,5,6]
print(new_list+lis_two)

#printing a list n number of times
print(new_list*3)
print(lis_two*4)

#copying a list
copy_list = new_list
print("-original list: ",new_list, "\n-copied list: ",copy_list)

#cloning: clone is a new copy of the original list
clone_list = new_list[:]
print(clone_list)
print(new_list+clone_list)
```

    ['a', 'b', 'hello', 'python']
    ['a', 'b', 'hello', 'python', 1, 2, 3, 4, 5, 6]
    ['a', 'b', 'hello', 'python', 'a', 'b', 'hello', 'python', 'a', 'b', 'hello', 'python']
    [1, 2, 3, 4, 5, 6, 1, 2, 3, 4, 5, 6, 1, 2, 3, 4, 5, 6, 1, 2, 3, 4, 5, 6]
    -original list:  ['a', 'b', 'hello', 'python'] 
    -copied list:  ['a', 'b', 'hello', 'python']
    ['a', 'b', 'hello', 'python']
    ['a', 'b', 'hello', 'python', 'a', 'b', 'hello', 'python']
    

NOTE: the element in the copied list also changed when the element in the original list is changed but it does not change in a cloned list


```python
new_list[0] = "A"
print(new_list)
print(copy_list)
print(clone_list)
```

    ['A', 'b', 'hello', 'python']
    ['A', 'b', 'hello', 'python']
    ['a', 'b', 'hello', 'python']
    


```python
#Concatenating a list
a_list = ["boston", "ohio", ["new york", "philly"], "new jersey"]
b_list = [1,2,3,4,5,6, ("tube"), 4,5]
new = a_list+b_list
print(new)
```

    ['boston', 'ohio', ['new york', 'philly'], 'new jersey', 1, 2, 3, 4, 5, 6, 'tube', 4, 5]
    

THE INPUT FUNCTION


```python
#the input function provide the user an option to supply an input to the program runtime
text = input("what is your name:")
print("The name you entered is:",text)
```

    what is your name: joe
    

    The name you entered is: joe
    


```python
number = int(input("type a number:"))
print(type(number))
```

    type a number: 67
    

    <class 'int'>
    


```python
#eval(): aims at converting a string into an integer or a float
expression = '8+5'
total = eval(expression)
print("sum of the expression is:",total)
print(type(expression))
print(type(total))
```

    sum of the expression is: 13
    <class 'str'>
    <class 'int'>
    


```python
#format: helps format the output on the screen with good look and attractiveness
a = int(input("Enter your age:"))
b = int(input("Enter your mother's age:"))
total = a+b
print("the sum of your age: {}, and your mother's age: {} is {}".format(a,b,total)) 
```

    Enter your age: 22
    Enter your mother's age: 42
    

    the sum of your age: 22, and your mother's age: 42 is 64
    


```python
e = input("what is your name:")
c = input("Enter your favorite fruit:")
d = input("Enter your favorite food:")
print("{} said his favorite fruit and food are {} and {} respectively.".format(e,c,d))
```

    what is your name: jonat
    Enter your favorite fruit: apple
    Enter your favorite food: rice
    

    jonat said his favorite fruit and food are apple and rice respectively.
    


```python
#COMPARISON
"""
the opereation that are used for comparison are as follows:
>,<, <=, >=, ==, != compares items and return True or False
"""
a = 6.55
b = 48
c = int(6.55)
print(float(c))
print("a==c is:",a==c)
print("a==float(c) is:",a==float(c))
print("a!=b is:",a!=b)
```

    6.0
    a==c is: False
    a==float(c) is: False
    a!=b is: True
    


```python
#LOGICAL OPERATORS
#they inlcude and, or, not. they are utilized to bring two conditions together and assess them
#they return the values True or False as well
print(a > b and c < a)
print(a!=b and a!=c)
print(a<c or b>a)
print(not a==b)
```

    False
    True
    True
    True
    


```python
#ASSIGNMENT OPERATORS
"""The operators including =, +=, -=, =, /=, %=, //=, *=, &=, |=, ^=, >>=, and <<= 
are employed to evaluate a value to a variable.
"""
x = 9
x += 1
print(x)

y = 5
y -= 8
print(y)

z = 30.33
z *= 10
print(z)

w = 9
w /= 3
print(w)

v = 60
v %= 10
print(v)

u = 8
u //= 5
print(u)

t = 9
t |= 3
print(t)
```

    10
    -3
    303.29999999999995
    3.0
    0
    1
    11
    


```python
#IDENTITY OPERATORS: is and is not
h = 3.14
j = 1.618
print(a is b)
print(a is not b)
message1 = "Hello, python"
message2 = "hello, python"
print( message1 is not message2)
```

    False
    True
    True
    


```python
#MEMBERSHIP OPERATORS
#includes in or not in are employed to check if a certain value is present in the sequence
#returns True or False
final_list = ["jonathan", "tayyiba", "biigba", "andrews"]
print("andrews is present:","andrews" in final_list)
print("edwin is not present:","edwin" not in final_list)
```

    andrews is present: True
    edwin is not present: True
    

THANK YOU
jbio nerd
