### Object References

**Objects of some Python _types_ are _immutable_.** An immutable object, once created, cannot be modified.

Some immutable types| &nbsp; | &nbsp; | &nbsp;
--- | ----------------------- | ------ | ------
`int` | `float` | `decimal` | `complex` |
 `bool` | `string` | `tuple` | `range` | 
`frozenset` |`bytes` |


**Objects of some other Python types are _mutable_.** A mutable object can be modified during its lifetime.

Some mutable types| &nbsp; | &nbsp; | &nbsp;
--- | ----------------------- | ------ | ------
`list` | `dict` | `set` | `bytearray` |

<tip-box> 

:package: In the example below, `i = 5` assigns an integer to `i`. Because integers are immutable, `i = i + 1` is not mutating the integer object `5`; rather, it is simply creating a new integer object `6` and assigning that to `i`. Similarly, `s = s + '  World!'` is not adding more letters to the existing string object `Hello`; ratehr, it is creating a new string object `'Hello World!'` and assigning that to `s`.

```python
i = 5
i = i + 1 # i is assigned a new integer object 6

s = 'Hello'
s = s + '  World!' # s is assigned a new string objet 'Hello World!'

numbers = [1, 2, 3]
numbers[0] = 4 # the existing list is being modified
```

However, lists are mutable. Therefore, `numbers[0] = 4` is changing the existing list `[1, 2, 3]` rather than creating a new list object.

</tip-box>

 **An _object reference_ is the address of the memory location where an object is currently stored. A variable is a _name_ that is bound to an object reference.** We can think of it as the variable _pointing to_ an object that is stored at the object reference.

<tip-box> 

:package: The variable `spam` is bound to the object reference `57207444` which is the memory location of the list object `[0, 1, 2, 3, 4, 5]`. i.e., `spam` is pointing to the object `[0, 1, 2, 3, 4, 5]` using the object reference `57207444`.

```python
spam = [0, 1, 2, 3, 4, 5]
```
![](https://automatetheboringstuff.com/images/000081.jpg)<br>
<sub>Image credit: [AtBSwP](https://automatetheboringstuff.com)</sub>

</tip-box>

**When you assign variables as `v1 = v2`, if `v2` is pointing to a mutable object, its object reference is copied to `v1`** so that now both `v1` and `v2` are pointing to the same object. However, **if `v2` is pointing to a mutable object, `v1 = v2` results in each variable pointing to its own copy of the object**.

<tip-box> 

:package: Continuing with the previous example, `cheese = spam` results in the object reference stored in `spam` being copied into the variable `cheese`. The end result is both variables are now pointing to the same list object.

```python
cheese = spam
```

![](http://automatetheboringstuff.com/images/000082.jpg)<br>
<sub>Image credit: [AtBSwP](https://automatetheboringstuff.com)</sub>

This means any change to the list pointed by `cheese` will be reflected as a change to the list pointed to by `spam` (because both are pointing to the same list object!).

<table> 
<tr>
  <td>

```python
cheese [1] = 'Hello!'
print('spam is:', spam)
print('cheese is:', cheese)
```
  </td>
  <td><br><br>&nbsp;→&nbsp;</td>
  <td><br><br>

```
spam is: [0, 'Hello!', 2, 3, 4, 5]
cheese is: [0, 'Hello!', 2, 3, 4, 5]
```
  </td>
</tr>
</table>

![](http://automatetheboringstuff.com/images/000071.jpg)<br>
<sub>Image credit: [AtBSwP](https://automatetheboringstuff.com)</sub>

However, the behavior is different when we do a similar variable assignment and update using integers instead of lists. Because integers are immutable, `cheese` points to a _copy_ of the integer pointed to by `spam`, not the same object.

<table> 
<tr>
  <td>

```python
spam = 5
cheese = spam
print('spam is:', spam)
print('cheese is:', cheese)

cheese = cheese + 1
print('spam is:', spam)
print('cheese is:', cheese)
```
  </td>
  <td><br><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br><br>

```
spam is: 5
cheese is: 5
spam is: 5
cheese is: 6
```
  </td>
</tr>
</table>

</tip-box>

**The behavior for passing arguments to a function is similar to that of assigning one variable to another.** If the argument is mutable, its object reference is assigned to the parameter. That means the code inside the function is able to modify the object passed as the argument and such changes remain after the function execution is over. 

<tip-box> 

:package: In the `foo` function below, when `foo(original)` is executed, the object reference of the argument `original` is copied to the parameter `items`.  Now the function is able to modify the list object now being pointed to by both `original` and `items`, and the changes remain in the list even after the function has finished.

<table> 
<tr>
  <td>

```python
def foo(items):
  items[0] = 'Hi'
  print('inside foo:', items)

original = [1, 2, 3]
foo(original)
print('after foo:', original)
```
  </td>
  <td><br><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br>

==<trigger trigger="click" for="modal:foo_items-pyTutor">[Visualize]</trigger>==%%[<a target="_blank" href="https://goo.gl/2E2uvp">alt link</a>]%%<br>

```
inside foo: ['Hi', 2, 3]
after foo: ['Hi', 2, 3]
```
  </td>
</tr>
</table>

<modal large title="`foo(items)`" id="modal:foo_items-pyTutor">

<iframe width="800" height="500" frameborder="0" src="http://pythontutor.com/iframe-embed.html#code=def%20foo%28items%29%3A%0A%20%20items%5B0%5D%20%3D%20'Hi'%0A%20%20print%28'inside%20foo%3A',%20items%29%0A%0Aoriginal%20%3D%20%5B1,%202,%203%5D%0Afoo%28original%29%0Aprint%28'after%20foo%3A',%20original%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=1&heapPrimitives=false&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

</modal>

Contrast the above example with the one below. The `bar(items)` function assigns a new list to `items` parameter. That means `items` is not longer pointing to the list object that was passed in as the argument. After the function is executed, the `original` list remains the same as before. 

<table> 
<tr>
  <td>

```python
def bar(items):
  items = ['a', 'b', 'c']
  print('inside bar:', items)
  
original = [1, 2, 3]
bar(original)
print('after bar:', original)
```
  </td>
  <td><br><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br>

%%<trigger trigger="click" for="modal:bar_items-pyTutor">[Visualize]</trigger>[<a target="_blank" href="https://goo.gl/4KHpPR">alt link</a>]%%<br>

```
inside bar: ['a', 'b', 'c']
after bar: [1, 2, 3]
```
  </td>
</tr>
</table>

<modal large title="`bar(items)`" id="modal:bar_items-pyTutor">

<iframe width="800" height="500" frameborder="0" src="http://pythontutor.com/iframe-embed.html#code=def%20bar%28items%29%3A%0A%20%20items%20%3D%20%5B'a',%20'b',%20'c'%5D%0A%20%20print%28'inside%20bar%3A',%20items%29%0A%20%20%0Aoriginal%20%3D%20%5B1,%202,%203%5D%0Abar%28original%29%0Aprint%28'after%20bar%3A',%20original%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=1&heapPrimitives=false&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

</modal>

</tip-box>

If the argument passed to a function is of an immutable type, the function receives the reference to a _copy_ of the argument. That means the code inside the function is unable to modify the object passed as the argument. However, it can return a new object that is based on the given object copy.

<tip-box> 

:package: In this example, the function `increment(age)` is given an immutable object `25` as the argument. Although the parameter `v` that received the argument is assigned a new object (i.e., `v = v + 1`) inside the function, that change is not reflected in the argument `age`. That is because `v` is given a reference to a _copy_ of `age`, not a reference to the actual object in `age`. 

<table> 
<tr>
  <td>

```python
def increment(v):
  v = v + 1
  return v
  
age = 25
new_age = increment(age)
print('age:', age)
print('new age:', new_age)
```
  </td>
  <td><br><br><br><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br><br><br>

%%<trigger trigger="click" for="modal:increment_v-pyTutor">[Visualize]</trigger>[<a target="_blank" href="https://goo.gl/9uR4eR">alt link</a>]%%<br>

```
age: 25
new age: 26
```
  </td>
</tr>
</table>

<modal large title="`increment(v)`" id="modal:increment_v-pyTutor">

<iframe width="800" height="500" frameborder="0" src="http://pythontutor.com/iframe-embed.html#code=def%20increment%28v%29%3A%0A%20%20v%20%3D%20v%20%2B%201%0A%20%20return%20v%0A%20%20%0Aage%20%3D%2025%0Anew_age%20%3D%20increment%28age%29%0Aprint%28'age%3A',%20age%29%0Aprint%28'new%20age%3A',%20new_age%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=1&heapPrimitives=false&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

</modal>

</tip-box>

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/objectReferences?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

<panel type="danger" header=":muscle: Exercise: Swap Ends" expanded no-close>
  <include src="e-swapEnds.md" />
</panel><p/>