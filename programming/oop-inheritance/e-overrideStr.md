#### Exercise : Override `__str__()` Method

Override the `__str()__` of the `Person` class so that the code below produces the given output.

<table>
<tr>
  <td>

```python
class Person:
  
  def __init__(self, name, age):
    self.name = name
    self.age = age
  
  # OVERRIDE __str__ METHOD HERE
    
print(Person('Amy', 25))
print(Person('Ben', 26))
```
  </td>
  <td valign="bottom">&nbsp;→&nbsp;<br><br></td>
  <td valign="bottom"> 

```
Amy (25years)
Ben (26years)
```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:bulb: Partial solution%%">

```python
def __str__(self):
    return self.name + ...
```

</panel>