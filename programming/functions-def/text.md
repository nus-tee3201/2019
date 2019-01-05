### Writing Functions

**You can write your own functions in Python.** Function are useful when you want to execute a bunch of statements multiple times at different points of a program. 

Format:
```
def function_name():
    statement_1
    statement_2
    ...
```

<tip-box> 

:package: The code below defines a function named `say_hello` and calls it twice.

<table>
<tr>
  <td>
  
```python
def say_hello():
  print('Hello!')
  print('How are you?')
  print('Nice to meet you.')
  
# call the function twice
print('Going to call the function ...')
say_hello()
print('Going to repeat ...')
say_hello()
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>
  
```
Going to call the function ...
Hello!
How are you?
Nice to meet you.
Going to repeat ...
Hello!
How are you?
Nice to meet you.

```
<trigger trigger="click" for="modal:sayHelloFunction-pyTutor">%%[Visualize execution]%%</trigger> 

<modal large title="Calling functions" id="modal:sayHelloFunction-pyTutor">

<iframe width="800" height="500" frameborder="0" src="http://pythontutor.com/iframe-embed.html#code=def%20say_hello%28%29%3A%0A%20%20print%28'Hello!'%29%0A%20%20print%28'How%20are%20you%3F'%29%0A%20%20print%28'Nice%20to%20meet%20you.'%29%0A%20%20%0A%23%20call%20the%20function%20twice%0Aprint%28'Going%20to%20call%20the%20function%20...'%29%0Asay_hello%28%29%0Aprint%28'Going%20to%20repeat%20...'%29%0Asay_hello%28%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=0&heapPrimitives=false&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

</modal>
  </td>
</tr>
</table>

Note how the statements inside the function are not executed unless the method is called. 

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/hello-function?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

</tip-box>

The function definition should appear in the code _before_ it is called.
 
<tip-box> 

<table>
<tr>
  <td>

:+1: this works
```python
print('starting ...')

def say_hello():
  print('Hello!')

print('Going to say hello ...')

say_hello()
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>
  
:-1: this doesn't work
```python
print('starting ...')
print('Going to say hello ...')

# call appears before definition
say_hello() 

def say_hello():
  print('Hello!')
```
  </td>
</tr>
</table>

</tip-box>

<panel type="seamless" header="%%:tv: Defining your own functions%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/WB4hJJkfhLU?rel=0&showinfo=0&start=13&end=199&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<panel type="danger" header=":muscle: Exercise: Hip Hip Hooray!" expanded no-close>
  <include src="e-hooray.md" />
</panel><p/>