### List Methods

Here are some useful list methods:

Method | Description
------ | -----------
`index()` | finds the index of an item in a list
`append()` | adds an item to the end of the list
`insert()` | inserts an item to a specific position in the list
`remove()` | removes the specified item from the list
`sort()` | sorts items in the list

<tip-box> 

:package: Here are some examples of how those list methods can be used:

```python
pets = ['Cats', 'Dogs', 'Hamsters']
print('Hamster is at', pets.index('Hamsters'))
print('Dog is at', pets.index('Dogs'))

pets.append('Parrots')
print('After apending Parrots', pets)

pets.insert(1, 'Rabbits')
print('After inserting Rabbits', pets)

pets.remove('Cats')
print('After removing Cats', pets)

pets.sort()
print('After sorting', pets)

pets.sort(reverse=True)
print('After reverse-sorting', pets)
```
:arrow_heading_down:
```
Hamster is at 2
Dog is at 1
After apending Parrots ['Cats', 'Dogs', 'Hamsters', 'Parrots']
After inserting Rabbits ['Cats', 'Rabbits', 'Dogs', 'Hamsters', 'Parrots']
After removing Cats ['Rabbits', 'Dogs', 'Hamsters', 'Parrots']
After sorting ['Dogs', 'Hamsters', 'Parrots', 'Rabbits']
After reverse-sorting ['Rabbits', 'Parrots', 'Hamsters', 'Dogs']
```
<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/lists-methods?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel>

</tip-box>

Note how in the example above `sort(reverse=True)` sorts the list in the reverse order. This notation of **`method(parameter_name=argument)` is known as passing a _keyword argument_.** Explanation: Some methods/functions has optional parameters. To specify an argument for such an optional parameter, we have to specify which parameter we are supplying. In the case of `sort(reverse=True)`, we are supplying the boolean argument `True` to the optional parameter named `reverse`.

<tip-box> 

:package: The `print` function takes an optional parameter `end`. If you provide it with an empty string i.e., `end=''`, the function will not print a line break at the end. The example below illustrates the difference it makes. 

<table> 
<tr>
  <td>

```python
pets = ['Rabbits', 'Parrots', 'Hamsters']

for animal in pets:
  print('{' + animal + '}')
  
for animal in pets:
  print('{' + animal + '}', end='')
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>

```



{Rabbits}
{Parrots}
{Hamsters}
{Rabbits}{Parrots}{Hamsters}

```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/lists-methods?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel>

</tip-box>
 
<panel type="seamless" header="%%:tv: List methods%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/Z9IxxW7428A?rel=0&showinfo=0&start=11&end=666&version=11" frameborder="0" allowfullscreen></iframe>

</panel><p/>

Note that **some methods <tooltip content="changes the value(s) of the object">mutates</tooltip> the object while other methods don't**.

<tip-box> 

:package: In the example below, `lower()` (a _non-mutating_ method) returns a new string that is in lower case while the original string remains unchanged. However, `sort()` (a _mutating_ method) changes the list object it is attached to (and does not return anything).

<table> 
<tr>
  <td>

```python
name = 'JOHN DOE'
print(name.lower()) # lower() is a non-mutating method
print(name) 
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>

```


john doe
JOHN DOE
```
  </td>
</tr>
<tr>
  <td>

```python
names = ['Zoe', 'Adam', 'Norm']
names.sort() # sort() is a mutating method
print(names)
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>

```



['Adam', 'Norm', 'Zoe']
```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/methods-mutating?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel>

</tip-box>

<panel type="danger" header=":muscle: Exercise: Anagram Checker" expanded no-close>
  <include src="e-anagramChecker.md" />
</panel><p/>
<panel type="danger" header=":muscle: Exercise: Word Game" expanded no-close>
  <include src="e-wordGame.md" />
</panel><p/>