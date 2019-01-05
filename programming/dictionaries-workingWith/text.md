### Working with Dictionaries

**You can use keys to access values in a dictionary.**

<tip-box> 

:package: Some examples of retrieving values based on the key:

<table> 
<tr>
  <td>

```python
numbers = {1: 'one', 2: 'two', 3: 'three'}
prices = {'bread': 3.5, 'butter': 5.0, 'banana': 0.15}
print(type(numbers))
print(numbers[1])
print(prices['butter'])
```
  </td>
  <td><br><br>&nbsp;→&nbsp;</td>
  <td><br><br>

```
<class 'dict'>
one
5.0
```
  </td>
</tr>
</table>

:package: Examples of adding, updating, and deleting dictionary entries:

<table> 
<tr>
  <td>

```python
grades = {'TE3201': 'A'}
grades['CS2103'] = 'B'
print('After adding:',grades)
grades['TE3201'] = 'A+'
print('After updating:',grades)
del grades['CS2103']
print('After deleting:', grades)
```
  </td>
  <td><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br>

```
After adding: {'TE3201': 'A', 'CS2103': 'B'}
After updating: {'TE3201': 'A+', 'CS2103': 'B'}
After deleting: {'TE3201': 'A+'}
```
  </td>
</tr>
</table>
</tip-box>

<panel type="danger" header=":muscle: Exercise: Get Set Delete Score" expanded no-close>
  <include src="e-getSetDeleteScore.md" />
</panel><p/>

**Trying to access a value for a non-existent key raises a `KeyError` exception.**

<tip-box> 

:package: This exampls raises an exception because the key `'santa'` does not exist in the dictionary `is_nice`:

<table> 
<tr>
  <td>

```python
is_nice = {'jane': False, 'hakim': True}
print(is_nice['santa'])
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>

```
Traceback (most recent call last):
  File "python", line 9, in <module>
KeyError: 'santa'
```
  </td>
</tr>
</table>

</tip-box>

<panel type="danger" header=":muscle: Exercise: Get Score with Error Handling" expanded no-close>
  <include src="e-getScoreWithErrorHandling.md" />
</panel><p/>

**You can use `keys()` and `values()` methods to iterate through keys and values of a dictionary, respectively.**

<tip-box> 

:package: The code below shows how to iterate through keys/values of a dictionary.

<table> 
<tr>
  <td>

```python
prices = {'bread': 3.5, 'butter': 5.0, 'banana': 0.15}
for k in prices.keys():
  print(k, '->', prices[k])
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>

```
bread -> 3.5
butter -> 5.0
banana -> 0.15
```

  </td>
</tr> 
<tr>
  <td>

```python
prices = {'bread': 3.5, 'butter': 5.0, 'banana': 0.15}
for v in prices.values():
  print(v)
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>

```
3.5
5.0
0.15
```
  </td>
</tr>
</table>

</tip-box>

You can **use the `sorted()` function to sort the keys/values before iterating through them**.

<tip-box> 

:package: The code below shows how to iterate through keys/values of a dictionary.

<table> 
<tr>
  <td>

```python
prices = {'bread': 3.5, 'butter': 5.0, 'banana': 0.15}
for k in sorted(prices.keys()):
  print(k, '->', prices[k])
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>

```
banana -> 0.15
bread -> 3.5
butter -> 5.0
```

  </td>
</tr> 
</table>

</tip-box>

<panel type="danger" header=":muscle: Exercise: Print Scorecard" expanded no-close>
  <include src="e-printScorecard.md" />
</panel><p/>

As usual, you can **use `in` and `not in` to check whether a key or a value is in a dictionary**.

<tip-box> 

:package: The code below shows how to check if a certain key or a value exists in a dictionary.

<table> 
<tr>
  <td>

```python
prices = {'bread': 3.5, 'butter': 5.0, 'banana': 0.15}
print('bread' in prices.keys())
print('sugar' not in prices.keys())
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>

```

True
True
```
  </td>
</tr>
<tr>
  <td>

```python
prices = {'bread': 3.5, 'butter': 5.0, 'banana': 0.15}
print(3.5 in prices.values())
print(6.0 in prices.values())
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>

```

True
False
```
  </td>
</tr>
</table>

</tip-box>

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/dictionaries-workingWith?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel>

<panel type="danger" header=":muscle: Exercise: Add Bonus" expanded no-close>
  <include src="e-addBonus.md" />
</panel><p/>