### Function Parameters

**You can configure a function to have _parameters_**. The parameters can be used by the code inside the function like a variable. That means we can pass arguments (i.e., values for those parameters) to affect the behavior of a function so that the function behaves differently each time it is executed. 

Format:
```
def function_name(parameter1_name, parameter2_name, ...):
    ...
```

A note about terminology: a function can have _parameters_ and when we call the function we can assign _arguments_ (i.e. values) to each of those parameters.

<tip-box> 

:package: The `say_hello` function below takes one parameter. The first time we call it we pass the argument `Gina` to that parameter, and the next time we pass a different argument `John` to the same parameter.

<table>
<tr>
  <td>
  
```python
def say_hello(name):
  print('Hello ' + name)
  print('How are you', name, '?')
  
say_hello('Gina')
say_hello('John')
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>
  
```
Hello Gina
How are you Gina ?
Hello John
How are you John ?

```
<trigger trigger="click" for="modal:sayHelloFunctionWithName-pyTutor">%%[Visualize execution]%%</trigger> 

<modal large title="Calling functions with arguments" id="modal:sayHelloFunctionWithName-pyTutor">

<iframe width="800" height="500" frameborder="0" src="http://pythontutor.com/iframe-embed.html#code=def%20say_hello%28name%29%3A%0A%20%20print%28'Hello%20'%20%2B%20name%29%0A%20%20print%28'How%20are%20you',%20name,%20'%3F'%29%0A%20%20%0Asay_hello%28'Gina'%29%0Asay_hello%28'John'%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=0&heapPrimitives=false&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

</modal>
  </td>
</tr>
</table>

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/hello-name?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

:package: The code below has one function that takes one parameter and one that takes two. Furthermore, note how one function calls the other.

```python
def say_hello(name):
  print('Knock knock ' + name)

def repeat_hello(name, times):
  print('Greeting ', name, times, 'times')
  for i in range(times):
    say_hello(name)
  
repeat_hello('Penny', 3)
say_hello('Sheldon')
```

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/hello-given-times?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

<panel type="seamless" header="%%:laughing: See human version of the above code%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/jrzUsHNGZHc?rel=0&showinfo=0&start=0&end=15&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

</tip-box>

**Parameter values are are forgotten after the function returns**.

<tip-box> 

:package: The code below produces an error because variable `v1` is not available after the function has returned.

```python
def print_uniqueness(v1, v2, v3):
  print(v1 != v2 and v2 != v3 and v3 != v1)
  
print_uniqueness(1,2,4) # True
print_uniqueness(1,1,2) # False

# Error. v1 is not available after function returns
print(v1) 
```

</tip-box>

<panel type="seamless" header="%%:tv: Function parameters%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/WB4hJJkfhLU?rel=0&showinfo=0&start=199&end=315&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<panel type="danger" header=":muscle: Exercise: Grader `print_score` function" expanded no-close>
  <include src="e-grader-printScoreFunction.md" />
</panel><p/>