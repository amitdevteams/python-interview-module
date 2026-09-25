# Python Complete Notes (Hinglish)

**Beginner → Intermediate → Advanced**

Ye notes Hinglish mein likhe gaye hain — beginner se advanced tak Python cover karte hain, saath mein examples, output aur ek learning roadmap bhi diya gaya hai.

## Contents

1. [Introduction to Python](#1-introduction-to-python)
2. [Installing Python](#2-installing-python)
3. [First Python Program](#3-first-python-program)
4. [Comments](#4-comments)
5. [Variables](#5-variables)
6. [Data Types](#6-data-types)
7. [Type Conversion](#7-type-conversion)
8. [Input and Output](#8-input-and-output)
9. [Operators](#9-operators)
10. [Strings](#10-strings)
11. [If / Else Conditions](#11-if--else-conditions)
12. [Lists](#12-lists)
13. [Tuples](#13-tuples)
14. [Sets](#14-sets)
15. [Dictionaries](#15-dictionaries)
16. [For Loops](#16-for-loops)
17. [While Loops](#17-while-loops)
18. [Break / Continue / Pass](#18-break--continue--pass)
19. [Functions](#19-functions)
20. [Function Arguments](#20-function-arguments)
21. [Scope](#21-scope)
22. [Modules and Imports](#22-modules-and-imports)
23. [Exception Handling](#23-exception-handling)
24. [File Handling](#24-file-handling)
25. [Object-Oriented Programming](#25-object-oriented-programming)
26. [Classes and Objects](#26-classes-and-objects)
27. [Inheritance](#27-inheritance)
28. [Polymorphism](#28-polymorphism)
29. [Encapsulation](#29-encapsulation)
30. [List Comprehension](#30-list-comprehension)
31. [Lambda Functions](#31-lambda-functions)
32. [map() / filter() / reduce()](#32-map--filter--reduce)
33. [Iterators](#33-iterators)
34. [Generators](#34-generators)
35. [Decorators](#35-decorators)
36. [JSON](#36-json)
37. [Dates and Times](#37-dates-and-times)
38. [Regular Expressions](#38-regular-expressions)
39. [Virtual Environments](#39-virtual-environments)
40. [pip and Packages](#40-pip-and-packages)
41. [APIs](#41-apis)
42. [Databases](#42-databases)
43. [SQLite](#43-sqlite)
44. [Testing](#44-testing)
45. [Debugging](#45-debugging)
46. [Useful Built-in Functions](#46-useful-built-in-functions)
47. [Python Project Ideas](#47-python-project-ideas)
48. [Learning Roadmap](#48-learning-roadmap)
- [Daily Practice Plan](#daily-practice-plan)
- [Important Python Rules](#important-python-rules)
- [Beginner Cheat Sheet](#beginner-cheat-sheet)
- [Final Advice](#final-advice)

---

## 1. Introduction to Python

Python ek programming language hai. Iska syntax simple aur English jaisa hai, isliye beginners ke liye best hai.

Python ka use commonly in kaamo ke liye hota hai:

- Web development
- Automation
- Data analysis
- Artificial Intelligence
- Machine Learning
- Backend development
- Scripting
- Desktop applications
- Testing

Example:

```python
print("Hello World")
```

Output:

```
Hello World
```

## 2. Installing Python

Python yahan se download karo: https://www.python.org/

Install hone ke baad version check karo:

```
python --version
```

ya kabhi-kabhi (Mac/Linux par):

```
python3 --version
```

Example output:

```
Python 3.14.x
```

> **Note:** Windows par install karte time "Add Python to PATH" wala checkbox zaroor tick karna.

## 3. First Python Program

Ek file banao: `hello.py`

Usme likho:

```python
print("Hello World")
```

Terminal mein run karo:

```
python hello.py
```

Output:

```
Hello World
```

## 4. Comments

Comments ko Python ignore kar deta hai. Ye sirf humare samajhne ke liye hote hain (code explain karne ke liye).

Single-line comment:

```python
# This is a comment
```

Example:

```python
# Print hello
print("Hello")
```

Output:

```
Hello
```

Multi-line documentation triple quotes se likh sakte ho:

```python
"""
This is a multi-line
string/documentation.
"""
```

(Technically ye ek string hai, comment nahi — lekin docstring/notes ke liye isko aise hi use karte hain.)

## 5. Variables

Variable ek dabba (container) hai jisme hum value store karte hain.

Example:

```python
name = "Rahul"
age = 20
price = 99.50

print(name)
print(age)
print(price)
```

Output:

```
Rahul
20
99.5
```

(Note: Python 99.50 ko 99.5 print karta hai — extra zero hat jaata hai.)

Variable ki value change kar sakte ho:

```python
age = 20
age = 21

print(age)
```

Output:

```
21
```

### Variable Naming Rules

Sahi (Correct):

```python
name = "Rahul"
user_age = 20
total_price = 100
```

Galat (Incorrect):

```python
2name = "Rahul"      # number se start nahi kar sakte
user-age = 20        # hyphen (-) allowed nahi, underscore (_) use karo
```

Python case-sensitive hai:

```python
name = "Rahul"
Name = "Amit"
```

Ye dono alag-alag variables hain.

## 6. Data Types

Python ke main data types:

| Type | Meaning |
|---|---|
| `str` | Text |
| `int` | Whole Number / poora number |
| `float` | Decimal number |
| `bool` | True/False |
| `list` | Changeable Collection — badal sakte hain |
| `tuple` | Fixed Collection — badal nahi sakte |
| `set` | Unique Values — duplicate nahi |
| `dict` | Key-Value Pairs |
| `NoneType` | No Value — kuch nahi |

### String

```python
name = "Rahul"
```

### Integer

```python
age = 20
```

### Float

```python
price = 99.99
```

### Boolean

```python
is_student = True
is_logged_in = False
```

(Dhyan do: True aur False ka pehla letter capital hota hai.)

### Check Type

`type()` se pata chalta hai ki variable kis type ka hai.

```python
x = 10

print(type(x))
```

Output:

```
<class 'int'>
```

## 7. Type Conversion

Ek data type ko doosre data type mein badalna.

String se integer:

```python
age = "20"
age = int(age)

print(age, type(age))
```

Output:

```
20 <class 'int'>
```

Integer se string:

```python
age = 20
age = str(age)

print(age, type(age))
```

Output:

```
20 <class 'str'>
```

Integer se float:

```python
x = 10
x = float(x)

print(x)
```

Output:

```
10.0
```

Float se integer:

```python
x = 10.5
x = int(x)

print(x)
```

Output:

```
10
```

(Note: `int()` round nahi karta, decimal part seedha kaat deta hai.)

Boolean:

```python
x = 1

print(bool(x))
```

Output:

```
True
```

(`0`, `""` (empty string), `[]` (empty list) aur `None` → `False` hote hain. Baaki almost sab kuch → `True`.)

## 8. Input and Output

### Output

```python
print("Hello")
```

Output:

```
Hello
```

### Input

`input()` se user se value lete hain.

```python
name = input("Enter your name: ")

print("Hello", name)
```

Output (agar user "Rahul" type kare):

```
Enter your name: Rahul
Hello Rahul
```

### Important

`input()` hamesha string return karta hai.

Example:

```python
age = input("Enter age: ")
```

Agar user `20` type kare: `age` ki value `"20"` (string) hogi, integer `20` nahi.

Isko convert karo:

```python
age = int(input("Enter age: "))
```

Example program:

```python
name = input("Name: ")
age = int(input("Age: "))

print("Name:", name)
print("Age:", age)
```

Output (agar user Rahul aur 20 daale):

```
Name: Rahul
Age: 20
Name: Rahul
Age: 20
```

(Pehli 2 lines input ke time dikhti hain, last 2 lines print se aati hain.)

## 9. Operators

### Arithmetic Operators

| Operator | Meaning | Example | Result |
|---|---|---|---|
| `+` | Addition — numbers ko jodna | `10 + 5` | `15` |
| `-` | Subtraction — ek number se doosra ghataana | `10 - 5` | `5` |
| `*` | Multiplication — numbers ko multiply karna | `10 * 5` | `50` |
| `/` | Division — number ko divide karna | `10 / 5` | `2.0` |
| `//` | Floor Division — division ka floor/whole result | `10 // 3` | `3` |
| `%` | Remainder — division ke baad bacha hua | `10 % 3` | `1` |
| `**` | Power — kisi number ki power nikalna | `2 ** 3` | `8` |

Examples:

```python
print(10 + 5)
print(10 - 5)
print(10 * 5)
print(10 / 5)
print(10 // 3)
print(10 % 3)
print(2 ** 3)
```

Output:

```
15
5
50
2.0
3
1
8
```

(Note: `/` hamesha float deta hai, isliye `10 / 5 = 2.0` aata hai, `2` nahi.)

### Comparison Operators

Ye do values compare karte hain aur True/False dete hain.

| Operator | Meaning |
|---|---|
| `==` | Equal (barabar) |
| `!=` | Not equal (barabar nahi) |
| `>` | Greater than (bada) |
| `<` | Less than (chhota) |
| `>=` | Greater/equal (bada ya barabar) |
| `<=` | Less/equal (chhota ya barabar) |

Example:

```python
age = 20

print(age == 20)
print(age > 18)
```

Output:

```
True
True
```

### Logical Operators

- `and` → dono conditions True honi chahiye
- `or` → koi ek condition True ho to kaafi hai
- `not` → result ulta kar deta hai (True → False)

Example:

```python
age = 20

print(age > 18 and age < 30)
```

Output:

```
True
```

### Assignment Operators

| Operator | Meaning |
|---|---|
| `=` | value assign karna |
| `+=` | `x += 5` matlab `x = x + 5` |
| `-=` | `x -= 5` matlab `x = x - 5` |
| `*=` | `x *= 5` matlab `x = x * 5` |
| `/=` | `x /= 5` matlab `x = x / 5` |

Example:

```python
x = 10
x += 5

print(x)
```

Output:

```
15
```

## 10. Strings

String mein text hota hai.

```python
name = "Rahul"
```

Single ya double quotes dono chalte hain:

```python
name = 'Rahul'
name = "Rahul"
```

### String Indexing

Har character ki ek position (index) hoti hai, jo 0 se start hoti hai.

```python
text = "Python"
```

Positions:

```
P  y  t  h  o  n
0  1  2  3  4  5
```

```python
print(text[0])
```

Output:

```
P
```

Negative indexing (peeche se count, `-1` = last character):

```python
print(text[-1])
```

Output:

```
n
```

### String Slicing

`text[start:end]` → start se le kar end se PEHLE tak (end include nahi hota).

```python
text = "Python"

print(text[0:3])
```

Output:

```
Pyt
```

```python
print(text[2:])
```

Output:

```
thon
```

```python
print(text[:4])
```

Output:

```
Pyth
```

### String Methods

```python
text = "hello world"

print(text.upper())         # sab capital
print(text.lower())         # sab small
print(text.capitalize())    # sirf pehla letter capital
print(text.title())         # har word ka pehla letter capital

print(text.replace("world", "Python"))
```

Output:

```
HELLO WORLD
hello world
Hello world
Hello World
hello Python
```

### Strip

`strip()` ka use string ke starting aur ending ke extra spaces/whitespace ko remove karne ke liye hota hai.

```python
text = "  hello  "

print(text.strip())
```

Output:

```
hello
```

### Split

`split()` ka use string ko todkar list banane ke liye hota hai.

```python
text = "apple,banana,mango"

items = text.split(",")

print(items)
```

Output:

```
['apple', 'banana', 'mango']
```

### Join

`join()` split ka ulta hai — list ko jodkar ek string banata hai.

```python
items = ["apple", "banana", "mango"]

text = ", ".join(items)

print(text)
```

Output:

```
apple, banana, mango
```

### F-strings

F-string matlab formatted string literal. Iska use string ke andar variables ya expressions aasani se daalne ke liye hota hai. String ke aage `f` lagao aur variable ko `{}` mein likho.

```python
name = "Rahul"
age = 20

print(f"My name is {name} and I am {age} years old.")
```

Output:

```
My name is Rahul and I am 20 years old.
```

## 11. If / Else Conditions

Conditions se Python decisions leta hai — "agar ye sach hai to ye karo".

Example:

```python
age = 20

if age >= 18:
    print("Adult")
```

Output:

```
Adult
```

### If / Else

```python
age = 15

if age >= 18:
    print("Adult")
else:
    print("Minor")
```

Output:

```
Minor
```

### If / Elif / Else

Upar se neeche check hota hai — jo pehli condition True mili, wahi chalegi, baaki skip.

```python
marks = 75

if marks >= 90:
    print("A")
elif marks >= 75:
    print("B")
elif marks >= 50:
    print("C")
else:
    print("Fail")
```

Output:

```
B
```

### Important

Python mein indentation (aage ka space, usually 4 spaces) bahut zaroori hai. Yahi batata hai ki kaunsa code `if` ke andar hai.

Sahi (Correct):

```python
if age >= 18:
    print("Adult")
```

Galat (Incorrect) — `IndentationError` aayega:

```python
if age >= 18:
print("Adult")
```

## 12. Lists

List mein multiple values ek saath store hoti hain. List changeable hoti hai.

```python
numbers = [10, 20, 30, 40]

print(numbers)
```

Output:

```
[10, 20, 30, 40]
```

Access:

```python
print(numbers[0])
```

Output:

```
10
```

Change:

```python
numbers[0] = 100

print(numbers)
```

Output:

```
[100, 20, 30, 40]
```

### List Methods

```python
numbers = [30, 10, 20, 40]

numbers.append(50)    # end mein add          → [30, 10, 20, 40, 50]
numbers.insert(0, 5)  # specific position par add → [5, 30, 10, 20, 40, 50]
numbers.remove(20)    # value se remove       → [5, 30, 10, 40, 50]
numbers.pop()         # last item remove      → [5, 30, 10, 40]
                       # pop(index) se kisi bhi position ka item hata sakte ho
numbers.sort()        # ascending order       → [5, 10, 30, 40]
numbers.reverse()     # order ulta            → [40, 30, 10, 5]

print(numbers)
print(len(numbers))   # total items
```

Output:

```
[40, 30, 10, 5]
4
```

### Loop Through List

```python
fruits = ["apple", "banana", "mango"]

for fruit in fruits:
    print(fruit)
```

Output:

```
apple
banana
mango
```

## 13. Tuples

Tuple list jaisa hi hai, lekin banne ke baad change nahi hota. Tuple `()` round brackets se banta hai.

```python
numbers = (10, 20, 30)

print(numbers[0])
```

Output:

```
10
```

Agar change karne ki koshish karo:

```python
numbers[0] = 100
```

Output (Error):

```
TypeError: 'tuple' object does not support item assignment
```

Tuple tab use karo jab data fixed rehna chahiye (jaise week ke din).

## 14. Sets

Set mein sirf unique values store hoti hain. Set `{}` curly brackets se banta hai.

```python
numbers = {1, 2, 3, 3, 4}

print(numbers)
```

Output:

```
{1, 2, 3, 4}
```

Duplicate values (yahan extra `3`) apne aap hat jaati hain.

(Note: set ka order fixed nahi hota, isliye indexing `numbers[0]` nahi chalti.)

Useful methods:

- `add()` → value add karna
- `remove()` → value hatana (value na mile to error)
- `discard()` → value hatana (value na mile to bhi error nahi)

Example:

```python
numbers = {1, 2, 3}

numbers.add(4)

print(numbers)
```

Output:

```
{1, 2, 3, 4}
```

## 15. Dictionaries

Dictionary mein data key-value pairs mein store hota hai (jaise real dictionary: word → meaning).

```python
person = {
    "name": "Rahul",
    "age": 20,
    "city": "Kolkata"
}
```

Access:

```python
print(person["name"])
```

Output:

```
Rahul
```

Change:

```python
person["age"] = 21
```

Add:

```python
person["job"] = "Developer"

print(person)
```

Output:

```
{'name': 'Rahul', 'age': 21, 'city': 'Kolkata', 'job': 'Developer'}
```

### Dictionary Methods

```python
print(person.keys())      # sirf keys
print(person.values())    # sirf values
print(person.items())     # key-value dono
```

Output:

```
dict_keys(['name', 'age', 'city', 'job'])
dict_values(['Rahul', 21, 'Kolkata', 'Developer'])
dict_items([('name', 'Rahul'), ('age', 21), ('city', 'Kolkata'), ('job', 'Developer')])
```

### Loop

```python
for key, value in person.items():
    print(key, value)
```

Output:

```
name Rahul
age 21
city Kolkata
job Developer
```

## 16. For Loops

For loop code ko baar-baar repeat karta hai.

```python
for i in range(5):
    print(i)
```

Output:

```
0
1
2
3
4
```

### Range

`range(start, stop, step)` — stop wala number include NAHI hota.

- `range(5)` → 0 se 4 tak
- `range(1, 6)` → 1 se 5 tak
- `range(1, 10, 2)` → 1 se start, har baar 2 badhao:

```
1
3
5
7
9
```

Example:

```python
for i in range(1, 11):
    print(i)
```

Output:

```
1
2
3
4
5
6
7
8
9
10
```

## 17. While Loops

While loop tab tak chalta hai jab tak condition True hai.

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```

Output:

```
1
2
3
4
5
```

**Important:** Dhyan rakho ki condition kabhi na kabhi False ho jaaye. Warna infinite loop ban jayega (program kabhi nahi rukega). (Ctrl + C dabake infinite loop rok sakte ho.)

## 18. Break / Continue / Pass

### Break

`break` loop ko turant rok deta hai.

```python
for i in range(10):

    if i == 5:
        break

    print(i)
```

Output:

```
0
1
2
3
4
```

### Continue

`continue` current round skip karke next round par chala jaata hai.

```python
for i in range(5):

    if i == 2:
        continue

    print(i)
```

Output:

```
0
1
3
4
```

### Pass

`pass` kuch nahi karta. Jab code ki jagah khaali chhodni ho (baad mein likhenge), tab placeholder ki tarah use karte hain.

```python
if True:
    pass
```

Output:

```
(kuch print nahi hoga)
```

## 19. Functions

Function reusable code hota hai — ek baar likho, baar-baar use karo. Function `def` keyword se banta hai.

Example:

```python
def hello():
    print("Hello")

hello()
```

Output:

```
Hello
```

### Function with Parameters

```python
def greet(name):
    print("Hello", name)

greet("Rahul")
```

Output:

```
Hello Rahul
```

### Return Value

`return` function se value wapas bhejta hai.

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result)
```

Output:

```
30
```

## 20. Function Arguments

### Positional Arguments

Values order ke hisaab se jaati hain (pehli value → a, doosri → b).

```python
def add(a, b):
    return a + b

print(add(10, 20))
```

Output:

```
30
```

### Keyword Arguments

Naam ke saath value do — order matter nahi karta.

```python
def greet(name, age):
    print(name, age)

greet(name="Rahul", age=20)
```

Output:

```
Rahul 20
```

### Default Argument

Agar value na do, to default value use hogi.

```python
def greet(name="User"):
    print("Hello", name)

greet()
greet("Rahul")
```

Output:

```
Hello User
Hello Rahul
```

### *args

`*args` se function kitni bhi values le sakta hai (tuple ki tarah milti hain).

```python
def add(*numbers):
    total = 0

    for number in numbers:
        total += number

    return total

print(add(1, 2, 3, 4))
```

Output:

```
10
```

### **kwargs

`**kwargs` se kitne bhi key=value arguments le sakte ho (dictionary ki tarah milte hain).

```python
def person(**data):
    print(data)

person(name="Rahul", age=20)
```

Output:

```
{'name': 'Rahul', 'age': 20}
```

## 21. Scope

Scope matlab variable kahan tak accessible hai.

### Local Variable

Function ke andar bana variable sirf function ke andar chalega.

```python
def test():
    x = 10
    print(x)

test()
```

Output:

```
10
```

(Function ke bahar `print(x)` likhoge to `NameError` aayega.)

### Global Variable

Function ke bahar bana variable har jagah padha ja sakta hai.

```python
x = 10

def test():
    print(x)

test()
```

Output:

```
10
```

Jahan tak ho sake, local variables use karo.

## 22. Modules and Imports

Module ek Python file hoti hai jisme ready-made code hota hai. `import` karke usko use kar sakte ho.

Example:

```python
import math

print(math.sqrt(25))
```

Output:

```
5.0
```

### Import Specific Function

Sirf ek function import karo:

```python
from math import sqrt

print(sqrt(25))
```

Output:

```
5.0
```

### Alias

Module ko chhota naam (nickname) de do:

```python
import math as m

print(m.sqrt(25))
```

Output:

```
5.0
```

## 23. Exception Handling

Program chalte time errors aa sakte hain. `try`/`except` se hum error ko handle karte hain taaki program crash na ho.

Example:

```python
try:
    number = int(input("Enter number: "))
    print(number)

except ValueError:
    print("Please enter a valid number.")
```

Output (agar user "abc" daale):

```
Enter number: abc
Please enter a valid number.
```

Output (agar user 25 daale):

```
Enter number: 25
25
```

### Finally

`finally` wala block hamesha chalta hai — error aaye ya na aaye.

```python
try:
    print("Hello")
except:
    print("Error")
finally:
    print("Finished")
```

Output:

```
Hello
Finished
```

### Raising Error

`raise` se hum khud error throw kar sakte hain.

```python
age = -1

if age < 0:
    raise ValueError("Age cannot be negative")
```

Output (Error):

```
ValueError: Age cannot be negative
```

Bare `except:` se bacho — jab possible ho, specific exception (jaise `ValueError`) catch karo.

## 24. File Handling

### Write File

`"w"` mode file banata hai (ya purana content mita ke naya likhta hai).

```python
with open("test.txt", "w") as file:
    file.write("Hello Python")
```

### Read File

```python
with open("test.txt", "r") as file:
    content = file.read()

print(content)
```

Output:

```
Hello Python
```

### Append

`"a"` mode purane content ke end mein naya content jodta hai.

```python
with open("test.txt", "a") as file:
    file.write("\nNew line")
```

Ab file padhoge to:

```
Hello Python
New line
```

### Common Modes

| Mode | Meaning |
|---|---|
| `r` | read (padhna) |
| `w` | write (likhna — purana data mit jaata hai) |
| `a` | append (end mein jodna) |
| `x` | create (nayi file banana — file pehle se ho to error) |

(`with` use karne se file apne aap close ho jaati hai.)

## 25. Object-Oriented Programming

OOP matlab Object-Oriented Programming. Isme code ko real-world cheezon (objects) ki tarah organize karte hain.

Main concepts:

- **Class** → blueprint/design (jaise car ka design)
- **Object** → class se bani real cheez (jaise ek actual car)
- **Attribute** → object ka data (jaise color, model)
- **Method** → object ka function/kaam (jaise `drive()`)
- **Inheritance** → ek class doosri class ki cheezein le sakti hai
- **Encapsulation** → data ko protect/control karna
- **Polymorphism** → same method naam, alag-alag kaam

## 26. Classes and Objects

Class banao:

```python
class Person:

    def __init__(self, name, age):
        self.name = name
        self.age = age

    def introduce(self):
        print(f"My name is {self.name}")
```

(`__init__` constructor hai — object bante hi apne aap chalta hai. `self` matlab "ye wala object".)

Object banao:

```python
person1 = Person("Rahul", 20)

print(person1.name)
print(person1.age)

person1.introduce()
```

Output:

```
Rahul
20
My name is Rahul
```

## 27. Inheritance

Inheritance se ek class (child) doosri class (parent) ke methods/features use kar sakti hai.

```python
class Animal:

    def speak(self):
        print("Animal speaks")


class Dog(Animal):

    def bark(self):
        print("Dog barks")


dog = Dog()

dog.speak()
dog.bark()
```

Output:

```
Animal speaks
Dog barks
```

(Dog class mein `speak()` nahi likha, phir bhi chal gaya — Animal se mila.)

## 28. Polymorphism

Alag-alag classes same method naam use kar sakti hain, lekin har class ka kaam alag hota hai.

```python
class Dog:

    def speak(self):
        print("Woof")


class Cat:

    def speak(self):
        print("Meow")


animals = [Dog(), Cat()]

for animal in animals:
    animal.speak()
```

Output:

```
Woof
Meow
```

## 29. Encapsulation

Encapsulation matlab class ke internal data ka access control karna.

Python mein iske liye naming conventions use hote hain:

Single underscore (`_`) → "ye internal hai, bahar se mat chhedo" (sirf ishara hai):

```python
class Person:

    def __init__(self):
        self._name = "Rahul"
```

Double underscore (`__`) → name mangling hota hai, bahar se directly access nahi hota:

```python
class Person:

    def __init__(self):
        self.__secret = "value"


p = Person()
print(p.__secret)
```

Output (Error):

```
AttributeError: 'Person' object has no attribute '__secret'
```

## 30. List Comprehension

List comprehension se ek line mein list bana sakte ho.

Normal tarika:

```python
numbers = []

for i in range(5):
    numbers.append(i)
```

List comprehension (same kaam, ek line mein):

```python
numbers = [i for i in range(5)]

print(numbers)
```

Output:

```
[0, 1, 2, 3, 4]
```

Example:

```python
squares = [x * x for x in range(10)]

print(squares)
```

Output:

```
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

### With Condition

```python
even = [x for x in range(10) if x % 2 == 0]

print(even)
```

Output:

```
[0, 2, 4, 6, 8]
```

## 31. Lambda Functions

Lambda ek chhota, bina naam ka (anonymous) function hai.

Jab logic bahut chhota ho aur sirf thodi der ke liye chahiye, to alag se `def` wala function banane ki jagah lambda use karte hain.

Normal function:

```python
def double(x):
    return x * 2

print(double(5))
```

Output:

```
10
```

Lambda se same kaam:

```python
double = lambda x: x * 2

print(double(5))
```

Output:

```
10
```

Ya seedha ek line mein:

```python
print((lambda x: x * 2)(5))
```

Output:

```
10
```

## 32. map() / filter() / reduce()

### Map

`map()` ka use tab karte hain jab list ke har element par same operation lagana ho.

```python
numbers = [1, 2, 3, 4]

result = map(lambda x: x * 2, numbers)

print(list(result))
```

Output:

```
[2, 4, 6, 8]
```

### Filter

`filter()` ka use list mein se sirf woh elements select karne ke liye hota hai jo kisi condition ko satisfy karte hain.

```python
numbers = [1, 2, 3, 4, 5]

result = filter(lambda x: x % 2 == 0, numbers)

print(list(result))
```

Output:

```
[2, 4]
```

### Reduce

`reduce()` multiple elements ko combine karke ek single value banata hai. (Isko `functools` se import karna padta hai.)

```python
from functools import reduce

numbers = [1, 2, 3, 4]

result = reduce(lambda a, b: a + b, numbers)

print(result)
```

Output:

```
10
```

(Kaise: `1+2 = 3` → `3+3 = 6` → `6+4 = 10`)

## 33. Iterators

Iterator ek-ek karke values deta hai. `next()` se agli value milti hai.

```python
numbers = iter([1, 2, 3])

print(next(numbers))
print(next(numbers))
print(next(numbers))
```

Output:

```
1
2
3
```

(Values khatam hone ke baad `next()` chalaoge to `StopIteration` error aayega.)

## 34. Generators

Generator ek aisa function hai jo saari values ek saath return nahi karta. Woh values ko ek-ek karke produce karta hai, jab unki zarurat hoti hai (isko "lazily" kehte hain). Generator mein `return` ki jagah `yield` use hota hai.

```python
def numbers():
    yield 1
    yield 2
    yield 3

for number in numbers():
    print(number)
```

Output:

```
1
2
3
```

Generators kyun? Bahut bade data ke saath kaam karte time ye memory bachate hain, kyunki saara data ek saath memory mein load nahi hota.

### Iterator vs Generator — Difference

Iterator = ek object jo values ek-ek karke deta hai.
Generator = `yield` use karke iterator banane ka aasaan tarika.

**1. Iterator** — List se `iter()` use karke iterator bana sakte ho:

```python
numbers = iter([1, 2, 3])

print(next(numbers))
print(next(numbers))
print(next(numbers))
```

Output:

```
1
2
3
```

**2. Generator** — Generator usually `yield` wale function se banta hai:

```python
def numbers():
    yield 1
    yield 2
    yield 3

for number in numbers():
    print(number)
```

Output:

```
1
2
3
```

## 35. Decorators

Decorator ek function ko modify/enhance karta hai bina us function ke original code ko change kiye.

Normal function:

```python
def greet():
    print("Hello Rahul")

greet()
```

Output:

```
Hello Rahul
```

Ab tum chahte ho ki `greet()` chalne se pehle aur baad mein kuch extra kaam ho, yaani output aisa aaye:

```
Before function
Hello Rahul
After function
```

Iske liye hum decorator bana sakte hain:

```python
def my_decorator(func):

    def wrapper():
        print("Before function")

        func()

        print("After function")

    return wrapper
```

Ab decorator ko use karte hain (function ke upar `@decorator_name` likho):

```python
@my_decorator
def greet():
    print("Hello Rahul")

greet()
```

Output:

```
Before function
Hello Rahul
After function
```

## 36. JSON

JSON ka use commonly applications ke beech data exchange karne ke liye hota hai (jaise API se data aana/jaana).

Example JSON:

```json
{
    "name": "Rahul",
    "age": 20
}
```

### Python to JSON

`json.dumps()` → Python dictionary ko JSON string banata hai.

```python
import json

data = {
    "name": "Rahul",
    "age": 20
}

text = json.dumps(data)

print(text)
```

Output:

```
{"name": "Rahul", "age": 20}
```

### JSON to Python

`json.loads()` → JSON string ko wapas Python dictionary banata hai.

```python
data = json.loads(text)

print(data["name"])
```

Output:

```
Rahul
```

(Yaad rakhne ka trick: dumps / loads mein "s" = string.)

## 37. Dates and Times

Date aur time ke liye `datetime` module use karo.

```python
from datetime import datetime

now = datetime.now()

print(now)
```

Output (example — tumhare run karne ke time ke hisaab se alag aayega):

```
2026-09-25 10:30:45.123456
```

Sirf aaj ki date:

```python
from datetime import date

today = date.today()

print(today)
```

Output (example):

```
2026-09-25
```

## 38. Regular Expressions

Regular expressions (regex) ka use text mein pattern dhoondhne ke liye hota hai (jaise numbers, emails, phone numbers).

```python
import re

text = "My phone number is 12345"

result = re.search(r"\d+", text)

if result:
    print(result.group())
```

Output:

```
12345
```

(`\d+` matlab "ek ya zyada digits".)

Common patterns:

| Pattern | Meaning |
|---|---|
| `\d` | digit (0-9) |
| `\w` | word character (letter, digit, underscore) |
| `\s` | whitespace (space, tab) |
| `.` | koi bhi character |
| `+` | ek ya zyada baar |

## 39. Virtual Environments

Virtual environment har project ki dependencies (packages) ko alag rakhta hai, taaki ek project ke packages doosre se mix na hon.

Create:

```
python -m venv venv
```

Activate — Windows:

```
venv\Scripts\activate
```

Activate — Linux/macOS:

```
source venv/bin/activate
```

(Activate hone par terminal mein aage `(venv)` dikhne lagta hai.)

Deactivate:

```
deactivate
```

## 40. pip and Packages

`pip` se Python packages install hote hain.

Example:

```
pip install requests
```

Installed packages dekho:

```
pip list
```

Package hatao:

```
pip uninstall requests
```

Dependencies save karo (file mein):

```
pip freeze > requirements.txt
```

requirements file se sab install karo:

```
pip install -r requirements.txt
```

## 41. APIs

API matlab Application Programming Interface — do programs ke beech baat karne ka tarika.

Python web APIs se data le/bhej sakta hai.

Example (`requests` use karke):

```python
import requests

response = requests.get("https://example.com")

print(response.status_code)
```

Output:

```
200
```

(200 = request successful. 404 = page nahi mila. 500 = server error.)

JSON API ke liye:

```python
response = requests.get("API_URL")

data = response.json()

print(data)
```

(Yahan "API_URL" ki jagah asli API ka link daalna hai.)

**Important:** Real APIs ke saath kaam karte time unke authentication, rate-limit, privacy aur usage rules follow karo.

## 42. Databases

Database mein data permanently store hota hai.

Examples:

- SQLite
- PostgreSQL
- MySQL
- MongoDB

Python mein SQLite ka support pehle se built-in hai (kuch install nahi karna).

## 43. SQLite

### Table Banana

```python
import sqlite3

connection = sqlite3.connect("database.db")

cursor = connection.cursor()

cursor.execute("""
CREATE TABLE IF NOT EXISTS users (
    id INTEGER PRIMARY KEY,
    name TEXT,
    age INTEGER
)
""")

connection.commit()

connection.close()
```

### Insert Data

```python
connection = sqlite3.connect("database.db")

cursor = connection.cursor()

cursor.execute(
    "INSERT INTO users (name, age) VALUES (?, ?)",
    ("Rahul", 20)
)

connection.commit()
connection.close()
```

### Read Data

```python
connection = sqlite3.connect("database.db")

cursor = connection.cursor()

cursor.execute("SELECT * FROM users")

rows = cursor.fetchall()

for row in rows:
    print(row)

connection.close()
```

Output:

```
(1, 'Rahul', 20)
```

**Important:** User input ko SQL string mein jodkar query mat banao. Hamesha parameterized queries (`?` wala tarika) use karo — isse SQL injection attack se bachav hota hai.

## 44. Testing

Testing se check karte hain ki program sahi kaam kar raha hai ya nahi.

Simple example (`assert`):

```python
def add(a, b):
    return a + b

assert add(2, 3) == 5
```

(Agar result sahi hai to kuch print nahi hoga. Galat hua to `AssertionError` aayega.)

Python mein `unittest` bhi hota hai:

```python
import unittest


class TestMath(unittest.TestCase):

    def test_add(self):
        self.assertEqual(2 + 3, 5)


if __name__ == "__main__":
    unittest.main()
```

Output:

```
.
----------------------------------------------------------------------
Ran 1 test in 0.000s

OK
```

Pytest ek aur popular testing framework hai.

## 45. Debugging

Debugging matlab code mein galti (bug) dhoondhna aur fix karna.

Simple debugging (print se value check karo):

```python
x = 10

print("x =", x)
```

Output:

```
x = 10
```

Python mein built-in debugger bhi hai.

Example:

```python
breakpoint()
```

Jab Python `breakpoint()` par pahunchta hai, program ruk jaata hai taaki tum variables check kar sako. (`c` dabao → aage chalao, `q` dabao → quit.)

### Common Errors

| Error | Meaning |
|---|---|
| `SyntaxError` | code likhne mein galti (jaise colon bhool gaye) |
| `NameError` | variable define hi nahi kiya |
| `TypeError` | galat type use kiya (jaise `"5" + 5`) |
| `ValueError` | type sahi, value galat (jaise `int("abc")`) |
| `IndexError` | list mein woh index hai hi nahi |
| `KeyError` | dictionary mein woh key nahi hai |
| `FileNotFoundError` | file mili nahi |

## 46. Useful Built-in Functions

| Function | Meaning |
|---|---|
| `print()` | output dikhana |
| `input()` | user se input lena |
| `len()` | length/count |
| `type()` | data type batana |
| `int()` | integer mein convert |
| `float()` | float mein convert |
| `str()` | string mein convert |
| `bool()` | boolean mein convert |
| `range()` | numbers ki sequence |
| `sum()` | sabka total |
| `min()` | sabse chhota |
| `max()` | sabse bada |
| `sorted()` | sorted nayi list |
| `abs()` | positive value (`abs(-5) = 5`) |
| `round()` | round off (`round(3.7) = 4`) |
| `enumerate()` | index + value dono |
| `zip()` | do lists ko jodna |
| `any()` | koi ek True ho to True |
| `all()` | sab True hon to True |

Examples:

```python
numbers = [10, 20, 30]

print(len(numbers))
print(sum(numbers))
print(max(numbers))
print(min(numbers))
```

Output:

```
3
60
30
10
```

### Enumerate

Loop mein index aur value dono chahiye ho to `enumerate()` use karo.

```python
fruits = ["apple", "banana", "mango"]

for index, fruit in enumerate(fruits):
    print(index, fruit)
```

Output:

```
0 apple
1 banana
2 mango
```

### Zip

Do lists ko saath-saath chalane ke liye `zip()` use karo.

```python
names = ["Rahul", "Amit"]
ages = [20, 25]

for name, age in zip(names, ages):
    print(name, age)
```

Output:

```
Rahul 20
Amit 25
```

## 47. Python Project Ideas

### Beginner Projects

1. Calculator
2. Number guessing game
3. Simple quiz
4. To-do list
5. Unit converter
6. Password generator
7. Simple expense tracker
8. Contact book
9. Rock-paper-scissors
10. Digital clock

### Intermediate Projects

1. File organizer
2. Weather application
3. Currency converter
4. Web scraper
5. REST API client
6. SQLite CRUD application
7. Blog backend
8. Chat application
9. Expense management system
10. Inventory management system

### Advanced Projects

1. Web application
2. REST API
3. Data analysis application
4. Machine learning project
5. Automation system
6. Database-backed application
7. Authentication system
8. Task management API
9. Large-scale data processing tool
10. Full-stack Python application

## 48. Learning Roadmap

### Phase 1 — Absolute Beginner

Seekho: `print()`, comments, variables, strings, integers, floats, booleans, `input()`, `type()`, type conversion

Practice karo: Hello World, name and age program, simple calculator

### Phase 2 — Control Flow

Seekho: `if`, `elif`, `else`, comparison operators, logical operators, `for`, `while`, `break`, `continue`

Practice karo: even/odd checker, grade calculator, number guessing game, multiplication table

### Phase 3 — Data Structures

Seekho: list, tuple, set, dictionary, indexing, slicing, methods

Practice karo: shopping list, contact book, student records

### Phase 4 — Functions

Seekho: `def`, parameters, arguments, `return`, default arguments, `*args`, `**kwargs`, scope

Practice karo: calculator using functions, banking functions, student management functions

### Phase 5 — Files and Errors

Seekho: `open()`, read, write, append, `with`, `try`, `except`, `finally`, `raise`

Practice karo: notes application, to-do list saved to file, expense tracker

### Phase 6 — OOP

Seekho: class, object, `__init__`, `self`, methods, inheritance, polymorphism, encapsulation

Practice karo: bank account, library system, student management system

### Phase 7 — Intermediate Python

Seekho: modules, packages, comprehensions, lambda, `map`, `filter`, generators, decorators, iterators, JSON

Practice karo: API client, data processing application

### Phase 8 — Real-World Python

Seekho: pip, virtual environments, APIs, databases, SQLite, testing, debugging, Git

Practice karo: database application, REST API, automation project

### Phase 9 — Choose a Specialization

Core Python seekhne ke baad ek direction choose karo.

**Web Development** — Seekho: HTTP, HTML/CSS basics, Flask ya Django, REST APIs, databases, authentication

**Data Science** — Seekho: NumPy, pandas, Matplotlib, statistics, data cleaning

**AI / Machine Learning** — Seekho: NumPy, pandas, scikit-learn, mathematics/statistics, model evaluation, neural networks

**Automation** — Seekho: file handling, APIs, subprocess, scheduling, browser automation (jahan appropriate ho)

## Daily Practice Plan

| Day | Topic |
|---|---|
| 1 | Variables + `print()` |
| 2 | Data types + `input()` |
| 3 | Operators |
| 4 | Strings |
| 5 | if / else |
| 6 | for loops |
| 7 | while loops |
| 8 | Lists |
| 9 | Tuples + sets |
| 10 | Dictionaries |
| 11 | Functions |
| 12 | Function arguments |
| 13 | File handling |
| 14 | Exception handling |
| 15 | Mini project |
| 16 | OOP |
| 17 | Classes and objects |
| 18 | Inheritance |
| 19 | Modules |
| 20 | JSON |
| 21 | APIs |
| 22 | SQLite |
| 23 | Testing |
| 24 | Debugging |
| 25 | Project |

## Important Python Rules

1. Python case-sensitive hai (`name` aur `Name` alag hain).
2. Indentation matter karta hai.
3. Variable names meaningful rakho (`x` ki jagah `total_price`).
4. Bina zarurat global variables mat use karo.
5. Reusable logic ke liye functions banao.
6. Errors ko properly handle karo.
7. Functions chhote aur samajhne layak rakho.
8. Sirf notes mat padho — code likh ke practice karo.
9. Error messages dhyan se padho — wahi batate hain galti kahan hai.
10. Har bada topic seekhne ke baad ek project banao.

## Beginner Cheat Sheet

**Print:**

```python
print("Hello")
```

**Variable:**

```python
name = "Rahul"
```

**Input:**

```python
name = input("Name: ")
```

**Integer input:**

```python
age = int(input("Age: "))
```

**Condition:**

```python
if age >= 18:
    print("Adult")
else:
    print("Minor")
```

**For loop:**

```python
for i in range(5):
    print(i)
```

**While:**

```python
while condition:
    # code
    pass
```

**List:**

```python
items = [1, 2, 3]
```

**Dictionary:**

```python
person = {"name": "Rahul", "age": 20}
```

**Function:**

```python
def add(a, b):
    return a + b
```

**Class:**

```python
class Person:

    def __init__(self, name):
        self.name = name
```

**Try/except:**

```python
try:
    # code
    pass
except ValueError:
    # handle error
    pass
```

**File:**

```python
with open("file.txt", "r") as file:
    data = file.read()
```

**Import:**

```python
import math
```

## Final Advice

Saare notes ratne (memorize karne) ki koshish mat karo.

Is order mein seekho:

Python basics → Variables → Data types → Input/output → Operators → Strings → Conditions → Loops → Lists → Tuples/Sets → Dictionaries → Functions → Files → Exceptions → Modules → OOP → Intermediate Python → APIs → Databases → Testing → Projects → Specialization

**Sabse important:**

**READ → WRITE CODE → MAKE MISTAKES → DEBUG → BUILD PROJECTS**

Sirf Python notes mat padho. Har topic ke liye kam se kam 5-10 chhote programs khud likho.

---

*Source: [`python_notes.txt`](./python_notes.txt) in this repository.*
