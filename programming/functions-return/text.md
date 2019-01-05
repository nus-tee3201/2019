### Return Value

**You can use a `return` statement to make a function return a value**.

<tip-box> 

:package: The `play()` function below returns one of the strings `Rock`, `Paper`, `Scissors` randomly.

```python
import random

def play():
  value = random.randint(1,3)
  if value == 1:
    return 'Rock'
  elif value == 2:
    return 'Paper'
  else:
    return 'Scissors'
  
print('Player1 response : ' + play())
print('Player2 response : ' + play())
```

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/rps-play-only?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

</tip-box>

**You can use an empty `return` statement to return from the function without executing the remainder of the function**.

<tip-box> 

:package: The `print_all_products` function below uses an empty `return` statement to return from the function early if one of the arguments is `0`:

```python
def print_product(a, b):
  print(a, 'x', b, '=', a*b)

def print_all_products(n1, n2, n3):
  # return early if any value is 0
  if n1 == 0 or n2 == 0 or n3 == 0:
    print('Values cannot be zeros')
    return
  
  # print all possible products
  print_product(n1, n2)
  print_product(n2, n3)
  print_product(n3, n1)
  
  
print_all_products(2,3,4)
print_all_products(0,2,3)
```

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/print-all-products?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

</tip-box>

<panel type="seamless" header="%%:tv: Returning values from functions%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/WB4hJJkfhLU?rel=0&showinfo=0&start=315&end=462&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<panel type="danger" header=":muscle: Exercise: Grader - `calculate_grade` function" expanded no-close>
  <include src="e-grader-calculateGradeFunction.md" />
</panel><p/>
