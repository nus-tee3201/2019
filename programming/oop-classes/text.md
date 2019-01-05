### Classes

As you have seen already, Python has some built in object types (i.e., classes) such as `list`, `int`, `str`, etc. In addition, **you can define your own classes** in Python.

The syntax for defining a class:
```python
class ClassName:
  # <statement-1>
  .
  .
  .
  # <statement-N>
```
:bulb: It is customary to use <trigger trigger="click" for="modal:classes-camelcase">Upper Camel Case</trigger> for class names.

The syntax for **creating (also called _instantiating_) an object** of the class is `ClassName()`.

<modal title="CamelCase" id="modal:classes-camelcase">

![](https://upload.wikimedia.org/wikipedia/commons/e/ef/CamelCase.svg =200x)<br>

Camel Case refers to a styling text writing compound words or phrases such that each word or abbreviation in the middle of the phrase begins with a capital letter, with no intervening spaces or punctuation e.g., `freshAppleJuice`. _Upper Camel Case_ (also called _Pascal Case_) is similar to Camel Case except the first letter is capitalized as well e.g., `FreshAppleJuice`.

<sub>[source: [Wikipedia](https://en.wikipedia.org/wiki/Camel_case)]</sub>
</modal>

<tip-box> 

:package: The code below defines a class named `Employee`, creates two employee objects, and prints the class/type of each object.

```python
class Employee:
  pass # an empty class

john = Employee() # create an Employee object
print(type(john)) # print type of the john object
alice = Employee()
print(type(alice))
```
:arrow_heading_down: %%Note how the type of each object is given as `<class 'Employee'>` i.e., a class with name `Employee`.%%
```
<class 'Employee'>
<class 'Employee'>
```
</tip-box>

You can add methods to the class by defining them inside the class definition. Note that a method of a class always take `self` as the first parameter. `self` refers to the object itself. When calling the method, there is no need to supply an argument for the `self` parameter as the target object is implicitly taken as the argument for that parameter.

<tip-box> 

:package: In the example below,<br>
`write(self, text)` method is called as `p.write('It was a dark night ...')`.<br>
This is how the arguments are matched with the parameters: 
* `self` → `p`
* `text` → `'It was a dark night ...'`

<table> 
<tr>
  <td>

```python
class Pen:
  
  def write(self, text):
    print('writing:', text)
    
p = Pen()
p.write('It was a dark night ...')
```
  </td>
  <td valign="bottom">&nbsp;→&nbsp;<br><br></td>
  <td valign="bottom">

```
writing: It was a dark night ...
```
  </td>
</tr>
</table>

</tip-box>

**You can specify how to initialize an object of a class by defining an `__init__()` method in the class.** Here are the important things to note about the `__init__()` method: 
1. There are two underscores in front and two behind the word `init`.<br>
   :x: `_init_()`<br>
   :white_check_mark: `__init__()`
1. It will be called every time you create an instance of the class.
1. If it has parameters, you need to provide arguments for those parameters when you instantiate an object of that class.

<tip-box> 

:package: This example shows an `__init__` method added to a `Person` class.

<table> 
<tr>
  <td>

```python
class Person:
  
  def __init__(self, name):
    print('Person object', name, 'initialized!')
    
tom = Person('Tom')
```
  </td>
  <td valign="bottom">&nbsp;→&nbsp;<br><br></td>
  <td valign="bottom">

```
Person object Tom initialized!
```
  </td>
</tr>
</table>
</tip-box>

The code within a class needs to use the `self.` to refer to its own attributes and methods. Furthermore, the best place to initialize attributes is the `__init__()` method.

<tip-box> 

:package: Note how the `__init__()` method of the `Book` class initializes its two attributes and calls another of its own methods i.e., `self.describe()`.

```python
class Book:
  
  def __init__(self, book_title, book_author):
    self.title = book_title # initialize attribute title
    self.author = book_author # initialize attribute author
    self.describe() # call another method of the class
    
  def describe(self):
    print('Book info:', self.title, '/by', self.author) # use attributes of the class
    
book1 = Book('The Jungle Book', 'Leo Tolstoy')
book2 = Book('The Art of War', 'Sun Tzu')
```
:arrow_heading_down:
```
Book info: The Jungle Book /by Leo Tolstoy
Book info: The Art of War /by Sun Tzu
```
</tip-box>

Attributes and methods of the objects can be accessed using `objectname.` syntax, as you would do with objects of built-in classes.

<tip-box> 

:package: This example shows how you can access the attributes and methods of the `book1` object (an object of class `Book`) defined in a previous example:

<table> 
<tr>
  <td>

```python
print('Title:', book1.title) 
print('Author:', book1.author)
book1.describe()
```
  </td>
  <td valign="bottom">&nbsp;→&nbsp;<br><br></td>
  <td valign="bottom">

```
Title: The Jungle Book
Author: Leo Tolstoy
Book info: The Jungle Book /by Leo Tolstoy
```
  </td>
</tr>
</table>

</tip-box>

As to be expected, you can get your classes to work with each other.

<tip-box> 

:package: In this example we define a `ReadingList` class that can store a list of `Book` objects.
<table> 
<tr>
  <td>

```python
class ReadingList:
  
  def __init__(self, initial_list):
    self.books = initial_list
    
  def add_book(self, book):
    self.books.append(book)
    
  def show_authors(self):
    for b in self.books:
      print(b.author)
      
my_list = ReadingList([book1]) # book1 defined in a previous example 
my_list.add_book(book2) # book2 defined in a previous example
my_list.show_authors()
```
  </td>
  <td valign="bottom">&nbsp;→&nbsp;<br><br></td>
  <td valign="bottom">

```
Leo Tolstoy
Sun Tzu
```
  </td>
</tr>
</table>

</tip-box>

<panel type="danger" header=":muscle: Exercise: Create `StockItem` Class" expanded no-close>
  <include src="e-createStockItemClass.md" />
</panel><p/>