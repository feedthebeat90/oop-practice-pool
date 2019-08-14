---
title: 'Fancy classes, fancy objects'
description: ""
---

## [BC] E1 Printing vs. Methods

```yaml
type: BlanksChallenge
key: a6d9165ebf
```

`@context`


`@code1`
```{python}
class Bee:
    def __init__(self):
    	self.sound = 'Buzz!'
    def MakeSound(self):
    	print(self.sound)

bee_obj = Bee()
{{_op}}
```

`@pre_challenge_code`
```{python}

```

`@variables`
```yaml
op:
- 'print(bee_obj)'
```

`@distractors`
```yaml
op:
- 'bee_obj.MakeSound()'
- 'Bee(self.sound)'
- 'metadata.bee_obj()'
```

---

## [BC] E2 Shorten Class + NumPy

```yaml
type: BlanksChallenge
key: e951aecc9c
```

`@context`


`@code1`
```{python}
class Operations:
  def __init__(self, array_1, array_2):
    self.A = array_1 
    self.B = array_2
  def Multiply(self):
    """ Multiplies two arrays"""
    return {{_op1}}

op_obj = Operations(np.array({{l1}}), np.array({{l2}}))
print(op_obj.Multiply())
```

`@code2`
```{python}
class Operations:
  def __init__(self, array_1):
    self.A = array_1 
  def Maximum(self):
    """Returns maximum
       value of an array"""
    return {{_op2}}

op_obj = Operations(np.array({{l1}}))
print(op_obj.Maximum())
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

op1:
- 'self.A * self.B'

op2:
- 'np.amax(self.A)'
```

`@distractors`
```yaml
op1:
- 'self.A - self.B'
- 'self.A / self.B'
- 'self.A + self.B'

op2:
- 'np.amin(self.A)'
- 'np.argmax(self.A)'
- 'np.argmin(self.A)'
```

---

## [BC] E3 Build Numpy Array from CSV

```yaml
type: BlanksChallenge
key: 05f899bf49
```

`@context`
Complete `create_datashell` method that allows building a NumPy array from a `.csv` file.

`@code1`
```{python}
class DataShell:
    def __init__(self, filename):
        self.file = filename
    def create_datashell(self):
        self.array = {{_op}}[1:,1:]
        return self.array
      
data_obj = DataShell(filepath)
data_obj.create_datashell()
```

`@pre_challenge_code`
```{python}
filepath = "https://assets.datacamp.com/production/repositories/5164/datasets/5114fd41444ba63633d3d6660bb5a41512552404/zoo.csv"

import numpy as np
```

`@variables`
```yaml
op:
- 'np.genfromtxt(self.file, delimiter=",")'
```

`@distractors`
```yaml
op:
- 'np.read_csv(self.file)'
- 'np.read_csv(self.file, delimiter=",")'
```

---

## [BC] E4 Usage of Type

```yaml
type: BlanksChallenge
key: 3fdb272fc9
```

`@context`
Complete the method to return the right `type`

`@code1`
```{python}
class Operations:
  def __init__(self, array_1):
    self.A = array_1 
  def DoubleArray(self):
    """Doubles each element 
    of an array """
    return {{_op}}

op_obj = Operations(np.array({{l1}}))
print(type(op_obj.DoubleArray()))
```

`@code2`
```{python}
class Operations:
  def __init__(self, array_1):
    self.A = array_1 
  def First_to_String(self):
    """Returns first element 
    of an array as a string"""
    return "'"+{{_op2}}+"'"

op_obj = Operations(np.array({{l1}}))
print(type(op_obj.First_to_String()))
```

`@code3`
```{python}
class Operations:
  def __init__(self, array_1):
    self.A = array_1 
  def GetMaximum(self):
    """Returns the maximum 
    value of an array"""
    return {{_op3}}

op_obj = Operations(np.array({{l1}}))
print(type(op_obj.GetMaximum()))
```

`@pre_challenge_code`
```{python}
filepath = "https://assets.datacamp.com/production/repositories/5164/datasets/5114fd41444ba63633d3d6660bb5a41512552404/zoo.csv"

import dccpu.generators as g
import numpy as np
```

`@variables`
```yaml
l1:
- '!expr g.int_vector(size=3)'

op:
- '2*(self.A)'

op2:
- 'str(self.A[0])'

op3:
- 'np.amax(self.A)'
```

`@distractors`
```yaml
op:
- 'str(self.A[0])'
- 'np.amax(self.A)'
- 'np.exp(self.A)'

op2:
- '2*(self.A)'
- 'np.amax(self.A)'
- 'np.exp(self.A)'

op3:
- '2*(self.A)'
- 'str(self.A[0])'
- 'np.exp(self.A)'
```

---

## [BC] E5 Build DataFrame from CSV

```yaml
type: BlanksChallenge
key: ccaddc26b8
```

`@context`
Complete `df_from_csv` method below so that it can be used to build a DataFrame from a `.csv` file.

`@code1`
```{python}
class DataShell:
    def __init__(self, inputFile):
        self.file = inputFile  
    def df_from_csv(self):
        self.df = {{_op}}(self.file)
        return self.df

data_shell = DataShell(filepath)
data_shell.df_from_csv().head(3)
```

`@pre_challenge_code`
```{python}
filepath = "https://assets.datacamp.com/production/repositories/5164/datasets/5114fd41444ba63633d3d6660bb5a41512552404/zoo.csv"

# Import pandas package
import pandas as pd
```

`@variables`
```yaml
op:
- 'pd.read_csv'
```

`@distractors`
```yaml
op:
- 'pd.genfromtxt'
- 'pd.write_csv'
- 'pd.csv_to_txt'
```

---

## [BC] E6 Return DataFrame from CSV

```yaml
type: BlanksChallenge
key: df0f5b7da4
```

`@context`
Complete `df_from_csv` method below so that it can be used to return a DataFrame.

`@code1`
```{python}
class DataShell:
    def __init__(self, inputFile):
        self.file = inputFile
    def df_from_csv(self):
        self.df = pd.read_csv(self.file)
        {{_op}}

data_shell = DataShell(filepath)
data_shell.df_from_csv().head(3)
```

`@pre_challenge_code`
```{python}
filepath = "https://assets.datacamp.com/production/repositories/5164/datasets/5114fd41444ba63633d3d6660bb5a41512552404/zoo.csv"

# Import pandas package
import pandas as pd
```

`@variables`
```yaml
op:
- 'return self.df'
```

`@distractors`
```yaml
op:
- 'print(df)'
- 'return pd.df'
- 'return self.file'
```

---

## [BC] E7 Store DF as Instance Variable

```yaml
type: BlanksChallenge
key: 3ce275bcd3
```

`@context`
Complete `store_df_from_csv` method below so that it can be used to store a DataFrame as an instance variable.

`@code1`
```{python}
class DataShell:
    def __init__(self, inputFile):
        self.file = inputFile
        self.df = None       
    def store_df_from_csv(self):
        {{_op}} = pd.read_csv(self.file)

data_shell = DataShell(filepath)
data_shell.store_df_from_csv()
data_shell.df.head(3)
```

`@pre_challenge_code`
```{python}
filepath = "https://assets.datacamp.com/production/repositories/5164/datasets/5114fd41444ba63633d3d6660bb5a41512552404/zoo.csv"

# Import pandas package
import pandas as pd
```

`@variables`
```yaml
op:
- 'self.df'
```

`@distractors`
```yaml
op:
- 'pd.df'
- 'self.file'
- 'df'
```

---

## [BC] E8 Change Column Name

```yaml
type: BlanksChallenge
key: 796e330fd1
```

`@context`
Complete the method `rename` that allows changing the name of a column in a DataFrame.

`@code1`
```{python}
class DataShell:
    def __init__(self, inputFile):
        self.df = pd.read_csv(inputFile)
    def rename(self, old, new):
        self.df.columns = {{_op}}
        print('Column has been renamed')

        
DS = DataShell(filepath)
DS.rename('class_type', 'animal_group')
```

`@pre_challenge_code`
```{python}
filepath = "https://assets.datacamp.com/production/repositories/5164/datasets/5114fd41444ba63633d3d6660bb5a41512552404/zoo.csv"

# Import pandas package
import pandas as pd
```

`@variables`
```yaml
op:
- 'self.df.columns.str.replace(old, new)'
```

`@distractors`
```yaml
op:
- 'self.df.str.replace(old, new)'
- 'self.df.columns.replace(old, new)'
```

---

## [BC] E9 DF Descriptive Statistics

```yaml
type: BlanksChallenge
key: 2418b19a53
```

`@context`
Complete `Statistics` method below so that it can output  descriptive statistics of the columns in a DataFrame.

`@code1`
```{python}
class DataShell:
    def __init__(self, inputFile):
        self.file = inputFile
        self.df = pd.read_csv(self.file)   
    def Statistics(self):
        return {{_op}}

data_shell = DataShell(filepath)
data_shell.Statistics()['hair']
```

`@pre_challenge_code`
```{python}
filepath = "https://assets.datacamp.com/production/repositories/5164/datasets/5114fd41444ba63633d3d6660bb5a41512552404/zoo.csv"

import pandas as pd
```

`@variables`
```yaml
op:
- 'self.df.describe()'
```

`@distractors`
```yaml
op:
- 'self.describe()'
- 'self.df.statistics()'
- 'df.describe()'
```

---

## [MC] E10 Docstring Importance

```yaml
type: MultipleChoiceChallenge
key: 685dfbc77f
```

`@assignment1`
What is a "docstring" ?

`@options1`
- It is a synonym for code comments.
- [It is a string literal specified in source code that is used to explain or document a specific segment of code.]
- It is a Class Method that allows working with String documents. 
- It is an alternative name for Instance Variables of type String appearing in Classes.

---

## [MC]  E11 PEP8 Docstring

```yaml
type: MultipleChoiceChallenge
key: cab859fccd
```

`@assignment1`
Which one of the following classes has an appropriate docstring?

```{python}

class Ant():
	"""
    A class to create Ant objects.
    """ 
    
class Bear():

    # A class to create Bear objects. 
  
class Eagle():
    
    A class to create Eagle objects.


```

`@options1`
- [Ant]
- Bear 
- Eagle

---

## [MC] E12 PEP8 Guidelines

```yaml
type: MultipleChoiceChallenge
key: c55a3d4d10
```

`@assignment1`
Which one of the following is not included in PEP8 Guidelines?

`@options1`
- Usage of spaces as an indentation style.
- [Files should preferably be in `.csv` format]
- Limit Maximum code line length to 79 characters. 
- Usage of docstrings to document classes, methods, functions, etc.
