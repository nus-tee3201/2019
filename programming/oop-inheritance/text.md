### Inheritance

**You can make a class <tooltip content="define a new class based on an existing class">inherit</tooltip> from another class.** If you do, it is as if the <tooltip content="the new class">_child class_</tooltip> already has all the attributes and methods of the <tooltip content="the class that was inherited from">_parent class_</tooltip>.

Syntax:
```python
class ChildClassName(ParentClassName):
  # statements of the class
```

<tip-box> 

<table> 
<tr>
  <td>

```python
class Person:
  def __init__(self, name):
    self.name = name
    
  def print_info(self):
    print('My name is', self.name)

amy = Person('Amy')
amy.print_info()
```
  </td>
  <td valign="bottom">&nbsp;→&nbsp;<br><br></td>
  <td valign="bottom">

```
My name is Amy
```
  </td>
</tr>
</table>

:package: Note how the `Teacher` class below inherits from the `Person` class given above. Observe how,
 * a `Teacher` object can use the `print_info()` method defined in the parent class.
 * the statement `dan = Teacher('Dan')` invokes the `__init__()` method defined in the parent class too.
 * the statement `print('the name is', dan.name)` is accessing the attribute `name` from a `Teacher` object although the attribute is defined in the parent class.
 * the method `teach` accesses the attribute `name` using `self.name` although the attribute is defined in teh parent class.

<table> 
<tr>
  <td>

```python
class Teacher(Person):
  
  def teach(self):
    print(self.name, 'is teaching')

dan = Teacher('Dan')
dan.print_info()
dan.teach()
print('the name is', dan.name)
```
  </td>
  <td valign="bottom">&nbsp;→&nbsp;<br><br></td>
  <td valign="bottom">

```
My name is Dan
Dan is teaching
the name is Dan
```
  </td>
</tr>
</table>

</tip-box>

<panel type="danger" header=":muscle: Exercise: Add `Fish` Class" expanded no-close>
  <include src="e-addFishClass.md" />
</panel><p/>

**A child class can _override_ a method defined in the parent class.** That way, a child object can change a behavior defined in the parent class.

<tip-box> 

:package: Note how the `Student` class below overrides the `__init__()` method and the `print_info()` method of the parent class `Person`.  

<table> 
<tr>
  <td>

```python
class Student(Person):
  def __init__(self, name, matric):
    self.name = name
    self.matric = matric
    
  def learn(self):
    print(self.name, 'is learning')
    
  def print_info(self):
    print(self.name, 'is a student')

ben = Student('Ben', 'A12345')
ben.print_info()
ben.learn()
```
  </td>
  <td valign="bottom">&nbsp;→&nbsp;<br><br></td>
  <td valign="bottom">

```
Ben is a student
Ben is learning
```
  </td>
</tr>
</table>

</tip-box>

When overriding methods, you can reuse the parent's definition of the same method using the `super().` prefix.

<tip-box> 


```python
class Person:
  def __init__(self, name):
    self.name = name
```
:package: Given that `Person` class has the initializer method given above, the following two versions of the `Student` class are equivalent.

<table> 
<tr>
  <td>

Override without reusing parent's method :arrow_heading_down:
```python
class Student(Person):
  def __init__(self, name, matric):
    self.name = name
    self.matric = matric
```
  </td>
  <td valign="bottom">&nbsp;=&nbsp;<br><br></td>
  <td valign="bottom">

Override but reuse parent's method :arrow_heading_down:
```python
class Student(Person):
  def __init__(self, name, matric):
    super().__init__(name) # reuse parent's method
    self.matric = matric
```
  </td>
</tr>
</table>

</tip-box>

<panel type="danger" header=":muscle: Exercise: Add `FlightlessBird` Class" expanded no-close>
  <include src="e-addFlightlessBirdClass.md" />
</panel><p/>


**Note that all python classes automatically inherits from the built-in class `object`** even if you did not specify it as the parent class. The `object` class has a `__str__()` method that you can ovrride in your classes to customize how the `print` function will print an object of your class.

<tip-box> 

:package: The `Book` class below overrides the `__str__()` method so that `Book` objects can be printed in a specific format.

<table> 
<tr>
  <td>

```python
class Book:
  def __init__(self, title):
    self.title = title
    
  def __str__(self):
    return 'Book title: ' + self.title
    
book = Book('Python for Beginners')
print(book)
```
  </td>
  <td valign="bottom">&nbsp;→&nbsp;<br><br></td>
  <td valign="bottom">

```
Book title: Python for Beginners
```
  </td>
</tr>
</table>

</tip-box>

<panel type="danger" header=":muscle: Exercise: Override `__str__()` Method" expanded no-close>
  <include src="e-overrideStr.md" />
</panel><p/>


**A class can inherit from multiple classes.** If multiple parent classes have the same method, the one that is given first (in the order of inheritance) will be used.

<tip-box> 



<table> 
<tr>
  <td>

```python
class Person:
  def __init__(self, name):
    self.name = name
    
  def print_info(self):
    print('My name is', self.name)
```
```python
class Teacher(Person):
  
  def teach(self):
    print(self.name, 'is teaching')
    
  def print_info(self):
    print(self.name, 'is a teacher')
    
```
  </td>
  <td valign="bottom">&nbsp;&nbsp;<br><br></td>
  <td>

```python
class Student(Person):
  def __init__(self, name, matric):
    super().__init__(name)
    self.matric = matric
    
  def learn(self):
    print(self.name, 'is learning')
    
  def print_info(self):
    print(self.name, 'is a student')
```
```python
class TeachingAssistant(Teacher, Student):
  
  def grade(self):
    print(self.name, 'is grading')
```
  </td>
  </tr>
</table>

:package: The `TeachingAssistant` class above inherits from both `Student` class and the `Parent` class both of which inherit from the `Person` class. That means a `TeachingAssistant` object can use methods from classes `object`, `Person`, `Student`, `Teacher`, and `TeachingAssistant`.

<table>
  <tr>
  <td>

```python
elsie = TeachingAssistant('Elsie', 'A223344')
elsie.print_info()
elsie.teach()
elsie.learn()
elsie.grade()
```
  </td>
  <td valign="bottom">&nbsp;→&nbsp;<br><br></td>
  <td valign="bottom">

```
Elsie is a teacher
Elsie is teaching
Elsie is learning
Elsie is grading
```
  </td>
</tr>
</table>

As both `Teacher` and `Student` classes have the `print_info()` method, the method from the `Teacher` class will be used as it comes first in the inheritance order `(Teacher, Student)`; that is why you see `Elsie is a teacher` in the output instead of `Elsie is a student`.

</tip-box>

<panel type="danger" header=":muscle: Exercise: Add `SmartPhone` Class" expanded no-close>
  <include src="e-addSmartPhoneClass.md" />
</panel><p/>