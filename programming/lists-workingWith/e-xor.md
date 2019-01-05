#### Exercise : XOR

%%:book: In case you didn't know: _XOR_ (short for eXclusive OR) is a logical operation, when applied to two booleans, that outputs `True` only when inputs differ (one is `True`, the other is `False`)%%

Complete the functions as described below:
* `xor(list1, list2, item)`: returns `True` if `item` is in ++only++ one of the two lists `list1` and `list2`. i.e., returns `False` if the `item` is absent from both lists or present in both lists.


<table>
<tr>
  <td>

```python
def xor(list1, list2, item):
  return

print(xor(['a','b'], ['a', 'c'], 'a'))
print(xor(['a','b'], ['a', 'c'], 'b'))
print(xor(['a','b'], ['a', 'c'], 'c'))
print(xor(['a','b'], ['a', 'c'], 'd'))
```
  </td>
  <td><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br>
  
```
False
True
True
False
```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:bulb: partial solution%%">

```python
return (item in list1 and item not in list2) or (...)
```
</panel>