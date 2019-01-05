#### Exercise : Has All Characters

Complete the function given below so that it returns `True` if `text` has all the characters in the list `characters`.

```python
def has_all_characters(text, characters):
  #pass # REPLACE WITH YOUR CODE

```

Example usage:
<table> 
<tr>
  <td>

```python
print(has_all_characters('abccde', ['a', 'c']))
print(has_all_characters('ab cde', ['a', 'a', ' ']))
print(has_all_characters('apple', ['a', 'f']))
```
  </td>
  <td><br>&nbsp;→&nbsp;</td>
  <td><br>

```
True
True
False
```
  </td>
</tr>
</table>


<panel type="seamless" header="%%:bulb: Partial solution%%">

```python
def has_all_characters(text, characters):
  for c in characters:
    if ...
      return False
  return True
```

</panel>