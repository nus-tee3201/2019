### String Methods

String objects have many methods (the full list is [here](https://docs.python.org/3/library/stdtypes.html#string-methods)).

Here are some string methods related to the nature of the string.
* `upper()`: returns a string with all characters in upper case
* `lower()`: returns a string with all characters in lower case
* `isupper()`: returns `True` if all characters are in upper case
* `islower()`: returns `True` if all characters are in lower case
* `isalpha()`: returns `True` if the string consists only of letters and is not blank.
* `isalnum()`: returns `True` if the string consists only of letters and numbers and is not blank.
* `isdecimal()`: returns `True` if the string consists only of numeric characters and is not blank.
* `isspace()`: returns `True` if the string consists only of spaces, tabs, and new-lines and is not blank.
* `startswith(s)`: returns `True` if the substring `s` appears at the start of the string
* `endswith(s)`: returns `True` if the substring `s` appears at the end of the string

<tip-box> 

:package: Examples of string methods mentioned above:

<table> 
<tr>
  <td>

```python
print('Hi there!'.upper())
print('Hi there!'.lower())
```
  </td>
  <td><br>&nbsp;→&nbsp;</td>
  <td><br>

```
HI THERE!
hi there!
```
  </td>
</tr>

<tr>
  <td>

```python
print('ABC'.isupper(), 'Abc'.isupper())
print('abc'.islower(), 'Abc'.islower())
print('abc'.isalpha(), 'A12'.isalpha())
print('A23'.isalnum(), 'A+1'.isalnum())
print('123'.isdecimal(), 'A12'.isdecimal())
print(' \t\n'.isspace(), 'a b'.isspace())
```
  </td>
  <td><br>&nbsp;→&nbsp;</td>
  <td><br>

```
True False
True False
True False
True False
True False
True False
```
  </td>
</tr>

<tr>
  <td>

```python
s = 'Hi there!'
print(s.startswith('Hi'), s.startswith('hi'))
print(s.endswith('!'), s.endswith('?'))
```
  </td>
  <td><br><br>&nbsp;→&nbsp;</td>
  <td><br><br>

```
True False
True False
```
  </td>
</tr>
</table>

</tip-box>

<panel type="danger" header=":muscle: Exercise: Rectify Case" expanded no-close>
  <include src="e-rectifyCase.md" />
</panel><p/>
<panel type="danger" header=":muscle: Exercise: Is Doctor" expanded no-close>
  <include src="e-isDoctor.md" />
</panel><p/>

**The `find(s)` method gives index of `s` in the string**, if it is found. It returns `-1` if `s` is not found.

<tip-box> 

:package: Examples of the `find()` method:

<table> 
<tr>
  <td>

```python
s = 'Monty Python'
print(s.find('Monty'))
print(s.find('Python'))
print(s.find('Spam'))
```
  </td>
  <td><br><br>&nbsp;→&nbsp;</td>
  <td><br><br>

```
0
6
-1
```
  </td>
</tr>
</table>

</tip-box>

<panel type="danger" header=":muscle: Exercise: Remove From Word" expanded no-close>
  <include src="e-removeFromWord.md" />
</panel><p/>

**The `join()` method joins a list of string items while using the <tooltip content="the string object upon which the method was called">target string object</tooltip> as a <tooltip content="the string that is placed in between each pair of items">delimiter</tooltip>.**

<tip-box> 

:package: Examples of the `join()` method:

<table> 
<tr>
  <td>

```python
print(', '.join(['tom', 'dick', 'harry']))
print('-'.join(['one', 'to', 'one']))
```
  </td>
  <td><br>&nbsp;→&nbsp;</td>
  <td><br>

```
tom, dick, harry
one-to-one
```
  </td>
</tr>
</table>

</tip-box>

**The `split()` method is the opposite of `join()`.** It splits a string into a list of strings based on a given delimiter string. If no delimiter is given, any <tooltip content="space, tab, or newline characters">whitespace</tooltip> in the string are used as delimiters.

<tip-box> 

:package: Some examples of using the `split()` method:

<table> 
<tr>
  <td>

```python
print('hi, how are you?'.split())
print('A1\t\tA2\nA3'.split())
print('''Todo:
1. eat
2. sleep'''.split('\n')) # split into lines
print('1-to-1-talk'.split('-'))
```
  </td>
  <td><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br>

```
['hi,', 'how', 'are', 'you?']
['A1', 'A2', 'A3']
['Todo:', '1. eat', '2. sleep']
['1', 'to', '1', 'talk']
```
  </td>
</tr>
</table>

</tip-box>


**There are some string methods to help you to strip trailing/leading spaces.**

<tip-box> 

:package: Examples of stripping leading/trailing spaces from a string:

<table> 
<tr>
  <td>

```python
s = '  hello  there!  '
print('['+ s.strip() + ']')
print('['+ s.lstrip() + ']') #left side strip
print('['+ s.rstrip() + ']') #right side strip
```
  </td>
  <td><br><br>&nbsp;→&nbsp;</td>
  <td><br><br>

```
[hello  there!]
[hello  there!  ]
[  hello  there!]
```
  </td>
</tr>
</table>

</tip-box>

<panel type="danger" header=":muscle: Exercise: Get Part" expanded no-close>
  <include src="e-getPart.md" />
</panel><p/>

**The `replace()` method can replace a character (or a phrase) with another character/phrase**. 

<tip-box> 

:package: Some examples of using `replace()` method:

```python
print('face to face'.replace(' ', '-'))  # replace space with a dash
print('1,2,3,4'.replace(',', '\t'))  # replace comma with a tab
print('Yup, Yup, I agree'.replace('Yup', 'Yes'))
```
:arrow_heading_down:
```
face-to-face
1	2	3	4
Yes, Yes, I agree
```

</tip-box>

**There are some string methods to help you to align text.**

<tip-box> 

:package: Examples of aligning text using string methods:

<table> 
<tr>
  <td>

```python
print('Here:'.rjust(20, '>')) # right-justify
print('Price'.ljust(20, '=')) # left-justify
print('Title'.center(20, ':')) # center
```
  </td>
  <td><br>&nbsp;→&nbsp;</td>
  <td><br>

```
>>>>>>>>>>>>>>>Here:
Price===============
:::::::Title::::::::
```
  </td>
</tr>
</table>

</tip-box>



<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/strings-methods?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel>

<panel type="danger" header=":muscle: Exercise: Print Formatted Item" expanded no-close>
  <include src="e-printFormattedItem.md" />
</panel>
<panel type="danger" header=":muscle: Exercise: Inventory Report" expanded no-close>
  <include src="e-inventoryReport.md" />
</panel><p/>