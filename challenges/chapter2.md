---
title: 'Deep dive into classes and objects'
description: ""
---

## [MC] E1 General Class Structure

```yaml
type: MultipleChoiceChallenge
key: 13890a88b1
```

`@assignment1`
Which one of these options is NOT a component of a class:

`@options1`
- Class Constructor Method
- [Class Templates]
- Class Methods
- Class Attributes

---

## [OC] E2 Basic Class Creation

```yaml
type: OutputChallenge
key: 2038bf119f
```

`@context`


`@code1`
```{python}
class Dog:
    def __init__(self):
    	print('Dog object: Woof!')
dog_obj = Dog()
```

`@code2`
```{python}
class Cat:
    def __init__(self):
    	print('Cat object: Meow!')
cat_obj = Cat()
```

`@code3`
```{python}
class Cow:
    def __init__(self):
    	print('Cow object: Moo!')
cow_obj = Cow()
```

`@pre_challenge_code`
```{python}

```

`@variables`
```yaml

```

---

## [BC] E3 Simple Class Instantiation

```yaml
type: BlanksChallenge
key: 95d9e55938
```

`@context`


`@code1`
```{python}
class SimpleClass:
	print('Really Simple Object')
	pass

# Create an object with SimpleClass
simple_object =  {{_op}}
```

`@pre_challenge_code`
```{python}

```

`@variables`
```yaml
op:
- 'SimpleClass()'
```

`@distractors`
```yaml
op:
- 'simpleclass()'
- 'SimpleClass'
- 'Intantiate.SimpleClass()'
```

---

## [BC] E4 Constructor __init__ method

```yaml
type: BlanksChallenge
key: fe94f8a59a
```

`@context`


`@code1`
```{python}
class Lion:
    def {{_op}}(self):
      self.animal_group = 'Mammal'
      self.sound = 'Roar!!!'     
    def MakeSound(self):
      print(self.sound)    


lion_object =  Lion()
lion_object = lion_object.MakeSound()
```

`@pre_challenge_code`
```{python}

```

`@variables`
```yaml
op:
- '__init__'
```

`@distractors`
```yaml
op:
- '__str__'
- 'cons'
- 'init'
- '__cons__'
```

---

## [BC] E5 Use of 'SELF' for Instance Variable

```yaml
type: BlanksChallenge
key: e792867b03
```

`@context`


`@code1`
```{python}
class Frog:
    def __init__(self):
      {{_op2}} = 'Amphibian'
      {{_op}} = 'Croak!!!' 
    def MakeSound(self):
      print({{_op}})

frog_object =  Frog()
frog_object = frog_object.MakeSound()
```

`@pre_challenge_code`
```{python}

```

`@variables`
```yaml
op:
- 'self.sound'

op2:
- 'self.animal_group'
```

`@distractors`
```yaml
op:
- 'sound'
- 'self'
- 'animal_group.self'
```

---

## [MC] E6 'SELF' is not a keyword

```yaml
type: MultipleChoiceChallenge
key: 050db5c747
```

`@assignment1`
Which word MUST be used to reference an object inside a class definition:

`@options1`
- `self`
- [Any non-keyword in Python can be used but the use of `self` is common practice]
- `object`
- Any Python keyword can be used

---

## [BC] E7 Instance Variable Definition

```yaml
type: BlanksChallenge
key: 4dbc1d1ef9
```

`@context`


`@code1`
```{python}
class Bat:
    def __init__(self):
        # Define an instance variable
        {{_op}} = 'Mammal'
        print('Bat object created')

# Instantiate a class
bat_obj = Bat()
```

`@code2`
```{python}
class Parrot:
    def __init__(self):
        # Define an instance variable
        {{_op}} = 'Bird'
        print('Parrot object created')

# Instantiate a class
parrot_obj = Parrot()
```

`@code3`
```{python}
class Shark:
    def __init__(self):
        # Define an instance variable
        {{_op}} = 'Fish'
        print('Shark object created')

# Instantiate a class
shark_obj = Shark()
```

`@pre_challenge_code`
```{python}

```

`@variables`
```yaml
op:
- 'self.animal_group'
```

`@distractors`
```yaml
op:
- 'animal_group.self'
- 'self'
- 'class.animal_group'
```

---

## [BC] E8 Printing Instance Variable Short

```yaml
type: BlanksChallenge
key: fbd873d8d5
```

`@context`


`@code1`
```{python}
class Snake:	
    def __init__(self):
    	self.sound = 'Hiss!'
    def MakeSound(self):
    	print({{_op}})

snake_obj = Snake()
snake_obj.MakeSound()
```

`@code2`
```{python}
class Duck:	
    def __init__(self):
    	self.sound = 'Quack!'
    def MakeSound(self):
    	{{_op1}}

duck_obj = Duck()
print(duck_obj.MakeSound())
```

`@code3`
```{python}
class Wolf:
    def __init__(self):
    	self.sound = 'Howl!'   
    def MakeSound(self):
    	return self.sound

wolf_obj = Wolf()
{{_op2}}(wolf_obj.MakeSound())
```

`@pre_challenge_code`
```{python}

```

`@variables`
```yaml
op:
- 'self.sound'

op1:
- 'return self.sound'

op2:
- 'print'
```

`@distractors`
```yaml
op:
- 'sound.self'
- 'sound'
- 'self'

op1:
- 'self.sound'
- 'print(self.sound)'

op2:
- 'Wolf'
- 'output'
- 'self.sound'
```

---

## [MC] E9 Instance vs Static Variables

```yaml
type: MultipleChoiceChallenge
key: 60d5c61b29
```

`@assignment1`
In the following `class` definition:

	class Duck:
    	animal = TRUE
    	def __init__(self):
    		self.animal_group = 'Bird'
    		self.sound = 'Quack!'
            self.legs = 2

Which variable is STATIC?

`@options1`
- [animal]
- self.animal_group
- self.sound
- self.legs

---

## [BC] E10 Define a Method

```yaml
type: BlanksChallenge
key: d570fb7da1
```

`@context`


`@code1`
```{python}
class Shark:
    def __init__(self):
    	self.animal_group = 'Fish'
    {{_op}}
    	return self.animal_group
shark = Shark()
print("Group:",shark.getAnimalGroup())
```

`@code2`
```{python}
class Snake:
    def __init__(self):
    	self.animal_group = 'Reptile'
    {{_op}}
    	return self.animal_group

snake = Snake()
print("Group:",snake.getAnimalGroup())
```

`@pre_challenge_code`
```{python}

```

`@variables`
```yaml
op:
- 'def getAnimalGroup(self):'
```

`@distractors`
```yaml
op:
- 'def getAnimalGroup(Shark)'
- 'def getAnimalGroup(animal_group)'
```

---

## [BC] E11 Calling a Method

```yaml
type: BlanksChallenge
key: ccd8625576
```

`@context`


`@code1`
```{python}
class Bear: 
    def __init__(self):
        self.animal_group = 'Mammal'
        self.sound = 'Roar!!!'    
    def getGroup(self):
        return self.animal_group
    def getSound(self):
        return self.sound
      
bear_obj = Bear()
print("The Bear is angry:", {{_op}})
```

`@pre_challenge_code`
```{python}

```

`@variables`
```yaml
op:
- 'bear_obj.getSound()'
```

`@distractors`
```yaml
op:
- 'bear_obj.getGroup()'
- 'self.sound'
```

---

## [BC] E12 Method with Argument

```yaml
type: BlanksChallenge
key: 617fc4b6c9
```

`@context`


`@code1`
```{python}
class Platypus:
    def __init__(self):
        self.animal_group = 'Uknown'
    def setAnimalGroup(self, group):
        self.animal_group = group

platypus = Platypus()
{{_op}}('Mammal')
print("The platypus is a", {{_op2}})
```

`@pre_challenge_code`
```{python}

```

`@variables`
```yaml
op:
- 'platypus.setAnimalGroup'

op2:
- 'platypus.animal_group'
```

`@distractors`
```yaml
op:
- 'platypus.__init__'
- 'platypus.animal_group'
```
