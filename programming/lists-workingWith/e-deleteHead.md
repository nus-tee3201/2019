#### Exercise : Delete Head, Delete Tail

Complete the functions as described below:
* `delete_head(item_list)`: deletes the first item in the list passed as `item_list` parameter.
* `delete_tail(item_list)`: deletes the last item in the list passed as `item_list` parameter.

<table>
<tr>
  <td>

```python
def delete_head(item_list):
  pass # REPLACE THIS WITH YOUR CODE
  
def delete_tail(item_list):
  pass # REPLACE THIS WITH YOUR CODE
  
letters = ['a', 'b', 'c']
print(letters)
delete_head(letters)
print(letters)
delete_tail(letters)
print(letters)
```
  </td>
  <td><br><br><br><br><br><br><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br><br><br><br><br><br><br>
  
```
['a', 'b', 'c']
['b', 'c']
['b']
```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:bulb: Partial solution%%">

```python
def delete_head(item_list):
  del item_list[0]
```

</panel>