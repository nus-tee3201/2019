### `while` Statements

**Python uses the `while` statement to repeat a code block until a certain condition is true. Such an execution path is also known as a _loop_ and each execution of the code block is called an _iteration_.**

Format:
```
while condition :
    statements_to_execute_if_condition_is_true
```
<tip-box>

:package: the code below prints 'Hello' 3 times (i.e., the loop is executed for 3 iterations), followed by 'Done'.

<table>
<tr>
  <td>

```python
counter = 0
while counter < 3:
    print('Hello')
    counter = counter + 1
print('Done')
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>
  
```
Hello
Hello
Hello
Done
```
<trigger trigger="click" for="modal:multipleHello-pyTutor">%%[Visualize execution]%%</trigger>  
  </td>
</tr>
</table>

<modal large title="Code with a simple `if` condition" id="modal:multipleHello-pyTutor">

<iframe width="800" height="500" frameborder="0" src="http://pythontutor.com/iframe-embed.html#code=counter%20%3D%200%0Awhile%20counter%20%3C%203%3A%0A%20%20%20%20print%28'Hello'%29%0A%20%20%20%20counter%20%3D%20counter%20%2B%201%0Aprint%28'Done'%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=10&heapPrimitives=false&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

</modal>

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/hello-thrice?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

</tip-box>

<panel type="seamless" header="%%:tv: Basic `while` loops%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/885qKiiKisI?rel=0&showinfo=0&start=8&end=107&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<tip-box>

**:exclamation: Infinite Loops**: Sometimes programming mistakes can result in _infinite loops_ %%&nbsp;i.e., loops that never terminate.%% In the example below, the condition `counter < 3` always evaluates to `True` (because the statement to increment `counter` has been left out by mistake)

```python
counter = 0
while counter < 3:
    print('Hello')
```

:bulb: When using IDLE, if a bug in your code caused it to go into an infinite loop,  you can use `Ctrl + C` to force it to stop executing.

<panel type="seamless" header="%%:tv: Infinite loops%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/885qKiiKisI?rel=0&showinfo=0&start=297&end=340&version=3" frameborder="0" allowfullscreen></iframe>

</panel>

</tip-box>

<panel type="danger" type="danger" header=":muscle: Exercise: Vending Machine - Add Loop" expanded no-close>
  <include src="e-vending-oneCoin.md" />
</panel>
<panel type="danger" header=":muscle: Exercise: Vending Machine - Accept Multiple Coins" expanded no-close>
  <include src="e-vending-multipleCoins.md" />
</panel><p/>  

**You can use a `break` statement to break out of a loop.**

<tip-box> 

:package: The code below uses the `break` statement to break out of the loop when the password given is `abcd`. Without the `break` statement, the loop will repeat forever because the condition in `while True:` is always `True`. 

```python
while True:
  password = input('What is the password?')
  if password == 'abcd':
    break # exit the loop
  else:
    print('Password incorrect. Try again.')
print('Password correct. You may proceed.')
```

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/password-loop?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

</tip-box>

<panel type="seamless" header="%%:tv: `break` inside `while` loops%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/885qKiiKisI?rel=0&showinfo=0&start=346&end=409&version=3" frameborder="0" allowfullscreen></iframe>

</panel>

<panel type="danger" header=":muscle: Exercise: Vending Machine - Allow Abort" expanded no-close>
  <include src="e-vending-allowAbort.md" />
</panel><p/> 

**You can use a `continue` statement to skip the remainder of the current iteration** and go back to the `while` condition.

<tip-box> 

:package: The code below is for reading three words from the user and printing all three at the end. It uses the `continue` statement to skip the remainder of the iteration if the word entered is too short (i.e., shorter than 4 letters). 

```python
accepted_words = ''
count = 0
while count < 3:
  word = input('Enter a word (with 4 letters or more):')
  if len(word) < 4:
    print('Too short. Ignored.')
    continue # skip the remainder of the iteration
  accepted_words = accepted_words + ' ' + word
  count = count + 1
print('Accepted words: ' + accepted_words)
```

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/three-words?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

</tip-box>

<panel type="seamless" header="%%:tv: `continue` inside `while` loops%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/885qKiiKisI?rel=0&showinfo=0&start=449&end=545&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<panel type="danger" header=":muscle: Exercise: Vending Machine - Legit Coins" expanded no-close>
  <include src="e-vending-legitCoins.md" />
</panel><p/>