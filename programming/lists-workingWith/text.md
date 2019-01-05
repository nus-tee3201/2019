### Working with Lists

**You can use the _slice_ notation `list_name[start_index:end_index]` to copy a _<tooltip content="a portion of a list">sublist</tooltip>_ into a new list.** If the `start_index` is omitted, it means 'from the beginning of the list'. If the `end_index` is omitted, it means 'till the end of the list'.

<tip-box> 

:package: Some example of slicing to get a sub list:
  
```python
letters = ['0a', '1b', '2c', '3d', '4e']
sublist = letters[0:3]
print(sublist) # print items 0, 1, 2
print(letters[:3]) # same as above (first 3 items)
print(letters[1:4]) # print items 1, 2, 3
print(letters[3:]) # print from item 3 till end
print(letters[-2:]) # print last two items
print(letters[1:-1]) # print from item 1 to 2nd last item
```
:arrow_heading_down:
```
['0a', '1b', '2c']
['0a', '1b', '2c']
['1b', '2c', '3d']
['3d', '4e']
['3d', '4e']
['1b', '2c', '3d']
```
<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/lists-slicing?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

</tip-box>

Note that slicing gives you a _copy_ of a portion of the original list i.e., you get a new list.

<tip-box> 

:package: In the example below, the first item `0a` of the list `letters` is deleted after taking the first two elements as a sub list. Note how the item `0a` still remains in the sub list after it has been deleted from the original list.
  
```python
letters = ['0a', '1b', '2c', '3d', '4e']
first_two_letters = letters[:2]
print('original list:', letters)
print('sub list     :', first_two_letters)
del letters[0] # delete first element in original list
print('original list:', letters)
print('sub list     :', first_two_letters)
```
:arrow_heading_down:
```
original list: ['0a', '1b', '2c', '3d', '4e']
sub list     : ['0a', '1b']
original list: ['1b', '2c', '3d', '4e']
sub list     : ['0a', '1b']
```
<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/lists-slicing?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

</tip-box>

</tip-box>

<panel type="seamless" header="%%:tv: Accessing multiple items from a list%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/5n6o1MaXDoE?rel=0&showinfo=0&start=317&end=534&version=11" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<panel type="danger" header=":muscle: Exercise: Get Body" expanded no-close>
  <include src="e-getBody.md" />
</panel><p/>

**You can use `del` to delete an item at a specific position of a list.**

<tip-box>

:package: The code below shows how to use `del` to delete items in a list.

<table>
<tr>
  <td>
  
```python
spam = ['foo', 45.0, True]
del spam[-1] # delete last item
print(spam)
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>
  
```


['foo', 45.0]

```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/lists-access-using-index?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

</tip-box>

<panel type="seamless" header="%%:tv: Deleting items from a list%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/5n6o1MaXDoE?rel=0&showinfo=0&start=534&end=581&version=11" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<panel type="danger" header=":muscle: Exercise: Delete Head, Delete Tail" expanded no-close>
  <include src="e-deleteHead.md" />
</panel><p/>


**You can use the `len` function to find the number of items in a list.**

<tip-box> 

<table>
<tr>
  <td>
  
```python
spam = ['a','b']
print('Length is:', len(spam))
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>
  
```

Length is: 2

```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/lists-len-plus-star-for?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel>

</tip-box>

<panel type="danger" header=":muscle: Exercise: Get Mid" expanded no-close>
  <include src="e-getMid.md" />
</panel><p/>

**You can use the `+` operator to combine two lists into a new list.**

<tip-box> 

<table>
<tr>
  <td>
  
```python
girls = ['Amy', 'Betsy', 'Clara']
boys = ['Adam', 'Ben']
friends = girls + boys
print(friends)
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>
  
```



['Amy', 'Betsy', 'Clara', 'Adam', 'Ben']

```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/lists-len-plus-star-for?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel>

</tip-box>

**You can use the `*` operator to create a new list by replicating an existing list multiple times.**

<tip-box> 

<table>
<tr>
  <td>
  
```python
steps = ['left', 'right']
walking = steps*3
print(walking)
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>
  
```


['left', 'right', 'left', 'right', 'left', 'right']

```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/lists-len-plus-star-for?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel>

</tip-box>

<panel type="seamless" header="%%:tv: Length of a list, list concatenation, list replication%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/5n6o1MaXDoE?rel=0&showinfo=0&start=581&end=635&version=11" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<panel type="danger" header=":muscle: Exercise: Expand to Fill" expanded no-close>
  <include src="e-expandToFill.md" />
</panel><p/>

**You can use `in` or `not in` to check if an item is in a list**. 

<tip-box> 


```python
valid_responses = ['Yes', 'No', 'Maybe']
response = ''
while response not in valid_responses:
  response = input('What is your response?')
print('Your response:', response)

current_drinks = ['Tea', 'Coffee']
suggested_drink = input('Suggest a new drink:')
if suggested_drink in current_drinks:
  print(suggested_drink, 'is already in the list')
```
:arrow_heading_down:
```
What is your response? abc
What is your response? Yes
Your response: Yes
Suggest a new drink: Tea
Tea is already in the list
```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/lists-in-not-in?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel>

</tip-box>

<panel type="seamless" header="%%:tv: Checking if an item is in a list%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/5n6o1MaXDoE?rel=0&showinfo=0&start=675&end=742&version=11" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<panel type="danger" header=":muscle: Exercise: XOR" expanded no-close>
  <include src="e-xor.md" />
</panel><p/>

**You can traverse through items in a list using the `for item_name in list_name:` notation**.

<tip-box> 

<table>
<tr>
  <td>
  
```python
pets = ['Cats', 'Dogs', 'Hamsters']
for animal in pets:
  print('Do you sell '+ animal +'?')
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>
  
```

Do you sell Cats?
Do you sell Dogs?
Do you sell Hamsters?
```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/lists-len-plus-star-for?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel>

</tip-box>

<panel type="danger" header=":muscle: Exercise: Print Card Deck" expanded no-close>
  <include src="e-printCardDeck.md" />
</panel><p/>

**The `enumerate` function can help you easily maintain an iteration counter while traversing a list**.

<tip-box> 

<table>
<tr>
  <td>
  
```python
pets = ['Cats', 'Dogs', 'Hamsters']
for i, animal in enumerate(pets):
  print(i+1, 'Can I buy '+ animal +'?')
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>
  
```

1 Can I buy Cats?
2 Can I buy Dogs?
3 Can I buy Hamsters?
```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/lists-len-plus-star-for?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel>

</tip-box>

<panel type="danger" header=":muscle: Exercise: First Quarter" expanded no-close>
  <include src="e-firstQuarter.md" />
</panel><p/>