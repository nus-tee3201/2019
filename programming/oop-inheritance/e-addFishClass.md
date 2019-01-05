#### Exercise : Add `Fish` Class

Add a `Fish` class that inherits from the `Animal` class so that the code below produces the given output.

<table>
<tr>
  <td>

```python
class Animal:
  def __init__(self, name):
    self.name = name
    
  def info(self):
    print("I'm a", self.name)
    
# ADD YOUR CODE HERE
    
tuna = Fish('Tuna')
tuna.info()
tuna.move()
guppy = Fish('Guppy')
guppy.info()
guppy.move()
```
  </td>
  <td valign="bottom">&nbsp;→&nbsp;<br><br></td>
  <td valign="bottom"> 

```
I'm a Tuna
I'm swimming
I'm a Guppy
I'm swimming
```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:bulb: Partial solution%%">

```python
class Fish(Animal):
  def move(self):
    ...
```

</panel>