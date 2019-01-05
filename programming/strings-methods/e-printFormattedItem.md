#### Exercise : Print Formatted Item

Complete the `print_formatted_item(name, count, width)` function given below, to behave as follows:
* Print `name` and `count` in the format `name.................: count`
* Width used for printing should be `width` (counted in number of characters)
* Use 3 spaces for `count` i.e., assume `count` is `0..999`
* Left-justify the `name` and right-justify the `count`
* Replace any square brackets `[]` in the `name` with normal brackets `()`

```python
def print_formatted_item(name, count, width):
  print('') # REPLACE WITH YOUR CODE
```

Example usage:
<table> 
<tr>
  <td>

```python
w = 25
print_formatted_item('pens', 2, w)
print_formatted_item('books[old]', 50, w)
print_formatted_item('pins[new]', 110, w)
```
  </td>
  <td><br><br>&nbsp;→&nbsp;</td>
  <td><br><br>
```
pens.................:  2
books(old)...........: 50
pins(new)............:110
```
  </td>
</tr>
<tr>
  <td>

```python
w = 20
print_formatted_item('pens', 2, w)
print_formatted_item('books[old]', 50, w)
print_formatted_item('pins[new]', 110, w)

```
  </td>
  <td><br><br>&nbsp;→&nbsp;</td>
  <td><br><br>

```
pens............:  2
books(old)......: 50
pins(new).......:110
```
  </td>
</tr>
</table>


<panel type="seamless" header="%%:bulb: Partial solution%%">

```python
def print_formatted_item(name, count, width):
  name = name.replace('[', '(').replace(...)
  print(name.ljust(width-4, '.') + ...)
```

</panel>