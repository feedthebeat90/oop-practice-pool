---
title: 'Inheritance, polymorphism and composition'
description: ""
---

## [MC] E1 Inheritance Definition

```yaml
type: MultipleChoiceChallenge
key: 853643f11a
```

`@assignment1`
Complete the following statement:
"In the context of inheritance, a "child" class is `...`"

`@options1`
- A class that gives its attributes to both of its parent classes.
- [A class that takes on attributes from another "parent" class and adds some more of its own.]
- A class that shares attributes with other classes of its kind.
- A class with unique attributes amongst other classes in a package.

---

## [MC] E2 Inheritance Usefulness

```yaml
type: MultipleChoiceChallenge
key: 7a1efabd94
```

`@assignment1`
Why would we want to declare a class that  inherits from another class?

`@options1`
- To modularize our original class in two "subclasses".
- [To extend the functionality of the base class without modifying it.]
- To limit the functionality of the parent "superclass".
- Because it is the last trend in fashion-programming circles.

---

## [BC] E3 Child Class

```yaml
type: BlanksChallenge
key: 89b8fe788a
```

`@context`
A "child" class `Bird` inherits attributes from a "parent" class `Vertebrate` and adds some more of its own.

`@code1`
```{python}
class Vertebrate:
    spinal_cord = True
    def __init__(self, name):
        self.name = name

class Bird({{_op}}):
    def __init__(self, name, kind):
        self.animal_type = kind
        self.can_lay_egg = True
```

`@pre_challenge_code`
```{python}

```

`@variables`
```yaml
op:
- 'Vertebrate'
```

`@distractors`
```yaml
op:
- 'Object'
- '()'
- 'Invertebrate'
```

---

## [MC] E4 Polymorphic Classes Definition

```yaml
type: MultipleChoiceChallenge
key: 3154c1958e
```

`@assignment1`
In the context of OOP, which of the following statements is TRUE if two classes that inherit from the same class are 'polymorphic'?"

`@options1`
- They must be identical.
- [They will have some differences between each other.]
- They will not share any of their attributes.
- Nothing can be said about those classes.

---

## [BC] E5 Polymorphic Classes

```yaml
type: BlanksChallenge
key: b8b4acd4f0
```

`@context`
`Bird` and `Mammal` are two "polymorphic" classes  that inherit from the same class `Vertebrate` but have different characteristics.

`@code1`
```{python}
class Mammal({{_op}}):
    def __init__(self, name, kind):
        self.animal_type = kind
        self.can_lay_egg = False

class Bird(Vertebrate):
    def __init__(self, name, kind):
        self.animal_type = kind
        self.can_lay_egg = {{_op2}}
```

`@pre_challenge_code`
```{python}
# Create a class Vertebrate
class Vertebrate:
    spinal_cord = True
    def __init__(self, name):
        self.name = name
```

`@variables`
```yaml
op:
- 'Vertebrate'

op2:
- 'True'
```

`@distractors`
```yaml
op:
- 'Invertebrate'

op2:
- 'False'
```

---

## [BC] E6 Parent Initialization

```yaml
type: BlanksChallenge
key: be39130693
```

`@context`
A "child" class `Mammal` inherits attributes from a "parent" class `Vertebrate` and adds some more of its own.

`@code1`
```{python}
class Vertebrate:
    spinal_cord = True
    def __init__(self, name):
        self.name = name
        
class Mammal(Vertebrate):
    def __init__(self, name):
        {{_op}}.name = name
        self.can_lay_egg = False
```

`@pre_challenge_code`
```{python}

```

`@variables`
```yaml
op:
- 'Vertebrate'
```

`@distractors`
```yaml
op:
- '__init__'
- 'Invertebrate'
```

---

## [BC] E7 Expand Functionality

```yaml
type: BlanksChallenge
key: 5f4e851aa7
```

`@context`
A "child" class `Bird` can expand the functionality of its "parent" class `Vertebrate` by incorporating the `fly` method.

`@code1`
```{python}
class Bird({{_op}}):
    def __init__(self, name):
        Vertebrate.name = name
        self.can_lay_egg = False
    {{_op2}} fly(self):
        print('Birds can Fly!!!')
```

`@pre_challenge_code`
```{python}
# Parent Class "Vertebrate"
class Vertebrate:
    spinal_cord = True
    def __init__(self, name):
        self.name = name
```

`@variables`
```yaml
op:
- 'Vertebrate'

op2:
- 'def'
```

`@distractors`
```yaml
op:
- 'Invertebrate'

op2:
- 'method'
```

---

## [MC] E8 Composition Definition

```yaml
type: MultipleChoiceChallenge
key: 7cdc01b8a1
```

`@assignment1`
Complete the following statement:
"In OOP the concept of Composition refers to `...`"

`@options1`
- A class that takes on attributes from another, "parent" class and adds some more of its own.
- [A class that takes elements of several other classes to create a more complex one.]
- A class that share two or more attributes with other classes of its kind.
- A class with unique attributes amongst other classes in a package.

---

## [BC] E9 Composite Class I

```yaml
type: BlanksChallenge
key: 4131b06978
```

`@context`
A class can be composed with methods of other classes from libraries such as `numpy`.

`@code1`
```{python}
class MaxVal:
  def __init__(self, array_1):
    self.A = array_1  
  def MaximumValue(self):
    """Returns the maximum 
    value of an array."""
    return {{_op}}(self.A)

op_obj = MaxVal(np.array({{l1}}))
print(op_obj.MaximumValue())
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

op:
- 'np.amax'
```

`@distractors`
```yaml
op:
- 'np.array'
- 'np.exp'
- 'np.log'
```

---

## [BC] E10 Composite Class II

```yaml
type: BlanksChallenge
key: 8e8b7acb73
```

`@context`
Build a composite class with a `pandas` method.

`@code1`
```{python}
class DataShell:
  def __init__(self, filename):
    self.filename = filename 
  def read_datashell(self):
    """Reads a .csv file with pandas"""
    return {{_op}}(self.filename)

op_obj = DataShell(filepath)
print(op_obj.read_datashell().head(2))
```

`@pre_challenge_code`
```{python}
import pandas as pd

filepath = "https://assets.datacamp.com/production/repositories/5164/datasets/5114fd41444ba63633d3d6660bb5a41512552404/zoo.csv"
```

`@variables`
```yaml
op:
- 'pd.read_csv'
```

`@distractors`
```yaml
op:
- 'pd.describe'
- 'pd.df'
```

---

## [MC] E11 Review Inheritance Syntax

```yaml
type: MultipleChoiceChallenge
key: a45d8481c2
```

`@assignment1`
What does an inherited class that takes a parent class as a parameter look like?

`@options1`
- class Vertebrate
- [class Reptile(Vertebrate)]
- class Reptile(Object)
- class Vertebrate(Object)

---

## [BC] E12 Review Build a Class

```yaml
type: BlanksChallenge
key: 53afaa9253
```

`@context`


`@code1`
```{python}
{{_op1}} Phoenix:
    def {{_op2}}(self, name):
        {{_op3}}.name = name      
    def resurrection(self):
        print(self.{{_op4}},'has reborn!')

phoenix_ob = {{_op5}}('Fawkes')
phoenix_ob.{{_op6}}
```

`@pre_challenge_code`
```{python}

```

`@variables`
```yaml
op1:
- 'class'

op2:
- '__init__'

op3:
- 'self'

op4:
- 'name'

op5:
- 'Phoenix'

op6:
- 'resurrection()'
```

`@distractors`
```yaml
op1:
- 'name'
```
