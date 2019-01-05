### Raising Exceptions

**You can `raise` an exception yourself to indicate an error**.

<tip-box> 

:package: The `get_body(items)` function below raises an exception when it receives a list that has fewer than 3 items. That exception is 'caught' and handled by the `hide_ends(items)` function. <br>
:bulb: Also note how an `except` clause can assign a name to the exception using `as temporary_name` (as done by `except ValueError as e:`) so that the exception object can be referenced later (as done in `print('Cannot hide ends', str(e))`)


<table> 
<tr>
  <td>

```python
def get_body(items):
  if len(items) < 3:
    raise ValueError('Not enough items')
  
  return items[1:-1]
  
def hide_ends(items):
  try:
    body = get_body(items)
    print(['_'] + body + ['_'])
  except ValueError as e:
    print('Cannot hide ends:', str(e))

hide_ends([0, 1])
hide_ends([0, 1, 2, 3, 4])
```
  </td>
  <td><br><br><br><br><br><br><br><br><br><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br><br><br><br><br><br><br><br><br>

[<a target="_blank" href="https://goo.gl/tsteqe">visualize</a>]<br>
```
Cannot hide ends: Not enough items
['_', 1, 2, 3, '_']
```
  </td>
</tr>
</table>

</tip-box>

**It is also possible to catch an exception, do something, and then raise it again** so that the exception propagates to the caller.

<tip-box> 

:package: The code `hide_ends2(items)` function below catches the `ValueError` exception, prints an error message, and raises it again so that the code that called the function can catch the exception again. Also note how the line `hide_ends2([0, 1, 2, 3, 4])` is never executed due to the exception raised by the line just above it.

<table> 
<tr>
  <td>

```python
def hide_ends2(items):
  try:
    body = get_body(items)
    print(['_'] + body + ['_'])
  except ValueError as e:
    print('Cannot hide ends:', str(e))
    raise
  
try:
  hide_ends2([0])
  hide_ends2([0, 1, 2, 3, 4])
except ValueError as e:
  print('hide_ends2 failed:', str(e))
```
  </td>
  <td><br><br><br><br><br><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br><br><br><br><br><br><br>

[<a target="_blank" href="https://goo.gl/EGkxAW">visualize</a>]<br>

```
Cannot hide ends: Not enough items
hide_ends2 failed: Not enough items
```
  </td>
</tr>
</table>

</tip-box>


<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/errors-exceptions-raising?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel>

<panel type="danger" header=":muscle: Exercise: Is Even-Integer in Range" expanded no-close>
  <include src="e-isEvenIntegerInRange.md" />
</panel>
<panel type="danger" header=":muscle: Exercise: Flexible Word Game" expanded no-close>
  <include src="e-flexibleWordGame.md" />
</panel><p/>