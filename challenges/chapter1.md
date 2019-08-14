---
title: 'Getting ready for object-oriented programming'
output: html_document
description: ""
---

## [MC] E1 OOP Definition

```yaml
type: MultipleChoiceChallenge
key: e903e29552
```

`@assignment1`
Complete the following statement:
"O.O.P. is a way to make logical groups of variables and functions `...`"

`@options1`
- Unique for generalized tasks.
- [Reusable for generalized tasks.]
- Non-reusable for generalized tasks, as opposed to Imperative Programming.
- Reusable for generalized tasks, just like Imperative Programming.

---

## [MC] E2 OOP Object Importance

```yaml
type: MultipleChoiceChallenge
key: 5275b3e715
```

`@assignment1`
Which of the following is NOT an Object in Python?

`@options1`
- Variable
- List
- Arrays
- DataFrames
- [Everything is an Object in Python]

---

## [OC] E3 Simple List Operations

```yaml
type: OutputChallenge
key: 2eac5ec537
```

`@context`


`@code1`
```{python}
def extendList(a): 
  return 2*a

print(extendList({{$l1}}))
```

`@code2`
```{python}
def addList(a):
  return sum(a)

print(addList({{$l1}}))
```

`@code3`
```{python}
def takeAverage(a):
  return sum(a)/len(a)

print(takeAverage({{$l1}}))
```

`@pre_challenge_code`
```{python}
import dccpu.generators as g
```

`@variables`
```yaml
l1:
- '!expr g.int_vector(size=3)'
l2:
- '!expr g.int_vector(size=3)'
n:
- '!expr g.rand_int(hi=2)'
```

---

## [OC] E4 List Concatenation

```yaml
type: OutputChallenge
key: 40ea1f99db
```

`@context`


`@code1`
```{python}
def concatA(a,b):
  return a + b

print(concatA({{$l1}},{{$l2}}))
```

`@code2`
```{python}
def concatB(a,b):
  return 2*a + b

print(concatB({{$l1}},{{$l2}}))
```

`@code3`
```{python}
def concatC(a,b):
  return a + 2*b

print(concatC({{$l1}},{{$l2}}))
```

`@pre_challenge_code`
```{python}
import dccpu.generators as g
```

`@variables`
```yaml
l1:
- '!expr g.int_vector(size=3)'
l2:
- '!expr g.int_vector(size=3)'
n:
- '!expr g.rand_int(hi=2)'
```

---

## [BC] E5 Importing Numpy

```yaml
type: BlanksChallenge
key: 008d99ae84
```

`@context`


`@code1`
```{python}
import {{_op}} as np

l1 = np.array({{l1}})
l2 = np.array({{l2}})
result = l1 + l2
print(result)
```

`@pre_challenge_code`
```{python}
import dccpu.generators as g
```

`@variables`
```yaml
l1:
- '!expr g.int_vector(size=3)'
l2:
- '!expr g.int_vector(size=3)'
op:
- 'numpy'
```

`@distractors`
```yaml
op:
- 'statistics'
- 'pandas'
- 'random'
```

---

## [OC] E6 Simple List Operations I

```yaml
type: OutputChallenge
key: f3a9aa06ec
```

`@context`
Assume `numpy` has already been imported

`@code1`
```{python}
l1 = np.array({{$l1}})
l2 = np.array({{$l2}})
print(l1 + l2)
```

`@code2`
```{python}
l1 = np.array({{$l1}})
l2 = np.array({{$l2}})
print(l1 * l2)
```

`@code3`
```{python}
l1 = np.array({{$l1}})
l2 = np.array({{$l2}})
print(l1 - l2)
```

`@code4`
```{python}
l1 = {{$l1}}
l2 = {{$l2}}
print(l1 + l2)
```

`@pre_challenge_code`
```{python}
import dccpu.generators as g
import numpy as np
```

`@variables`
```yaml
l1:
- '!expr g.int_vector(size=3)'
l2:
- '!expr g.int_vector(size=3)'
```

---

## [OC] E7 Simple List Operations II

```yaml
type: OutputChallenge
key: 20805de9ea
```

`@context`
Assume `numpy` has already been imported

`@code1`
```{python}
l1 = np.array({{$l1}})
l2 = np.array({{$l2}})
print(l1 + l2)
```

`@code2`
```{python}
l1 = np.array({{$l1}})
l2 = np.array({{$l2}})
print(l1 * l2)
```

`@code3`
```{python}
l1 = np.array({{$l1}})
l2 = np.array({{$l2}})
print(l1 - l2)
```

`@pre_challenge_code`
```{python}
import dccpu.generators as g
import numpy as np
```

`@variables`
```yaml
l1:
- '!expr g.int_vector(size=4)'
l2:
- '!expr g.int_vector(size=1)'
```

---

## [BC] E8 Trivial Class Definition

```yaml
type: BlanksChallenge
key: 4b12959a81
```

`@context`


`@code1`
```{python}
{{_op}} TrivialClass:
  
  def __init__(self):
    print('Instantiate a Trivial Class')
    pass

# Instantiate Trivial Class
trivial_object = TrivialClass()
```

`@pre_challenge_code`
```{python}
import dccpu.generators as g
```

`@variables`
```yaml
op:
- 'class'
```

`@distractors`
```yaml
op:
- '__init__'
- 'def'
- 'Object'
```

---

## [MC] E9 Class Definition

```yaml
type: MultipleChoiceChallenge
key: d6be6f3576
```

`@assignment1`
Complete the following statement:
"In the context of Object Oriented Programming, a "class" is `...`"

`@options1`
- a function in Python
- a Python package
- [a code template for creating objects]
- an instance variable
- a synonym for methods

---

## [MC] E10 Class Structure

```yaml
type: MultipleChoiceChallenge
key: 8771739ceb
```

`@assignment1`
Choose the option that better fills the gaps:

"Class Variables are usually referred as `...` while Class Functions are usually referred as `...`"

`@options1`
- [Attributes/Methods]
- Instances/Objects
- Arrays/DataFrames
- Methods/Instances
- Attributes/Packages

---

## [BC] E11 Instantiation of a Class

```yaml
type: BlanksChallenge
key: 7892ce3607
```

`@context`


`@code1`
```{python}
class ListClass:
  
  def __init__(self,l1):
    self.new_list = l1
    print('List Object Created')

# Instantiate the Class
list_object = {{_op}}({{l1}})
```

`@pre_challenge_code`
```{python}
import dccpu.generators as g
```

`@variables`
```yaml
l1:
- '!expr g.int_vector(size=3)'

op:
- 'ListClass'
```

`@distractors`
```yaml
op:
- '__init__'
- '__init__.ListClass'
- 'Object'
```

---

## [MC] E12 Class/Object Relationship

```yaml
type: MultipleChoiceChallenge
key: cb70297c6f
```

`@assignment1`
Given an object is created using the constructor of a certain class, we can say that:

`@options1`
- The Object is a METHOD of the Class
- The Object is an ATTRIBUTE of the Class
- [The Object is an INSTANCE of the Class]
- The Class is an INSTANCE of the Object
