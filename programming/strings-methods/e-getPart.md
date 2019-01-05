#### Exercise : Get Part

Complete the `get_part(text, index)` function given below, to behave as follows:
1. Split `text` using `|` as the delimiter
1. Return the part indicated by the `index`

The return value should not have leading/trailing spaces.

```python
def get_part(text, index):
  #pass # REPLACE WITH YOUR CODE
```

Example usage:
<table> 
<tr>
  <td>

```python
print(get_part(' John Doe | Male |    X', 0))
print(get_part('John Doe | Male |    X', 2))
print(get_part('Dog|Cat', 0))
```
  </td>
  <td><br>&nbsp;→&nbsp;</td>
  <td><br>

```
John Doe
X
Dog
```
  </td>
</tr>
</table>


<panel type="seamless" header="%%:bulb: Partial solution%%">

```python
return text.split('|')...
```

</panel>