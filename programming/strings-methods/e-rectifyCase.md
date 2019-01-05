#### Exercise : Rectify Case

Complete the `rectify_case(text)` function given below, to behave as follows:
* If `text` is all upper case, return `text` in lower case
* If `text` is all lower case, return `text` in upper case
* Return `text` otherwise

```python
def rectify_case(text):
  #pass # REPLACE WITH YOUR CODE

```

Example usage:
<table> 
<tr>
  <td>

```python
print(rectify_case('Mrs. Fox'))
print(rectify_case('MR. FOX'))
print(rectify_case('baby fox'))
```
  </td>
  <td><br>&nbsp;→&nbsp;</td>
  <td><br>

```
Mrs. Fox
mr. fox
BABY FOX
```
  </td>
</tr>
</table>


<panel type="seamless" header="%%:bulb: Partial solution%%">

```python
  if text.isupper(): 
    return text.lower()
  ...
```

</panel>