#### Exercise : Get Body

Complete the functions as described below:
* `get_body(item_list)`: returns a sublist of `item_list` parameter, without the first and the last items.
* `get_without_head(item_list)`: returns a sublist of `item_list` parameter, without the first item.
* `get_without_tail(item_list)`: returns a sublist of `item_list` parameter, without the last item.

<table>
<tr>
  <td>

```python
def get_body(item_list):
  return # ADD CODE HERE
  
def get_without_head(item_list):
  return # ADD CODE HERE
  
def get_without_tail(item_list):
  return # ADD CODE HERE
  
print(get_body([0, 1, 2, 3, 4]))
print(get_without_head([0, 1, 2, 3, 4]))
print(get_without_tail([0, 1, 2, 3, 4]))
```
  </td>
  <td><br><br><br><br><br><br><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br><br><br><br><br><br><br>
  
```
[1, 2, 3]
[1, 2, 3, 4]
[0, 1, 2, 3]
```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:bulb: Partial solution%%">

```python
def get_without_head(item_list):
  return item_list[1:]
```

</panel>