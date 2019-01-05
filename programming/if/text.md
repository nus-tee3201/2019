### `if` Statements

Python uses the `if` statement to indicate that some code should only be executed if a certain condition is true.

Format:
```
if condition :
    statements_to_execute_if_true
```

:package: The code below has two `if` statements; one evaluates to `true` while the other doesn't.
```python
price = 55
print(price)
if price > 50:
    print('Expensive')

weight = 45
print(weight)
if weight > 100:
    print('Heavy')
    
print('Done')
```
Output :arrow_heading_down: <trigger trigger="click" for="modal:simpelIf-pyTutor">%%[Click here to visualize execution]%%</trigger>
```
50
Expensive
45
Done
```
<modal large title="Code with a simple `if` condition" id="modal:simpelIf-pyTutor">

Use the `Back` and `Forward` buttons to visualize execution one step at a time. 

If the space below is blank, you may need to configure your browser to allow loading the required javascript file. Alternatively you can go to [PythonTutor.com](http://pythontutor.com/visualize.html#mode=edit), copy-paste the above Python code there to see the execution steps.

<iframe width="800" height="500" frameborder="0" src="http://pythontutor.com/iframe-embed.html#code=price%20%3D%2055%0Aprint%28price%29%0Aif%20price%20%3E%2050%3A%0A%20%20%20%20print%28'Expensive'%29%0Aweight%20%3D%2045%0Aprint%28weight%29%0Aif%20weight%20%3E%20100%3A%0A%20%20%20%20print%28'Heavy'%29%0Aprint%28'Done'%29&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=0&heapPrimitives=false&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

</modal>

Note how the code to execute if the condition is true is indented (usually by 4 spaces). **Python uses indentation to indicate code _blocks_** (aka _clauses_) %%&nbsp;i.e., a sequence of statements that belong together%%. In the example below, lines 2-4 are in the same block because they are all indented by one level; if the condition is true, all three are executed; if the condition is false, all three are omitted. Line 5 goes back to the previous indentation level, indicating the end of the code block. 

```python
if name == 'Blue':          # line 1
    print("It's a color")   # line 2
    print("It's a feeling") # line 3
    print("It's a word")    # line 4
print('Done')               # line 5
```

<panel type="danger" header=":muscle: Exercise: Even Numbers" expanded>
  <include src="e-even.md" />
</panel><p/>

`if` statements can be <tooltip content="one _if_ statement within another">nested</tooltip>, using deeper indentation.

```python
age = 13
gender = 'F'
if (age > 12) and (age < 20):          
    print("Teenager")  # indented one level - new code block starts here 
    if gender == 'F':
        print('Female')# indented two levels - this block is nested within the first block
        print('Girl')  
    if gender == 'M':
        print('Male') # another block nested within the first block
        print('Boy')
    print('Gender code is ' + gender) 
print('Age is ' + str(age))               
```
:arrow_heading_down: <trigger trigger="click" for="modal:nestedIf-pyTutor">%%[visualize]%%</trigger>
```
Teenager
Female
Girl
Gender code is F
Age is 13
```

<modal large title="Nested blocks" id="modal:nestedIf-pyTutor">

<iframe width="800" height="500" frameborder="0" src="http://pythontutor.com/iframe-embed.html#code=age%20%3D%2013%0Agender%20%3D%20'F'%0Aif%20%28age%20%3E%2012%29%20and%20%28age%20%3C%2020%29%3A%20%20%20%20%20%20%20%20%20%20%0A%20%20%20%20print%28%22Teenager%22%29%20%20%23%20indented%20one%20level%20-%20new%20code%20block%20starts%20here%20%0A%20%20%20%20if%20gender%20%3D%3D%20'F'%3A%0A%20%20%20%20%20%20%20%20print%28'Female'%29%23%20indented%20two%20levels%20-%20this%20block%20is%20nested%20within%20the%20first%20block%0A%20%20%20%20%20%20%20%20print%28'Girl'%29%20%20%0A%20%20%20%20if%20gender%20%3D%3D%20'M'%3A%0A%20%20%20%20%20%20%20%20print%28'Male'%29%20%23%20another%20block%20nested%20within%20the%20first%20block%0A%20%20%20%20%20%20%20%20print%28'Boy'%29%0A%20%20%20%20print%28'Gender%20code%20is%20'%20%2B%20gender%29%20%0Aprint%28'Age%20is%20'%20%2B%20str%28age%29%29%20&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=0&heapPrimitives=false&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

</modal>

<panel type="seamless" header="%%:tv: Using `if`%%">

<iframe width="560" height="315" src="https://www.youtube.com/embed/lWeCgEbk-Ro?rel=0&showinfo=0&start=7&end=253&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

If a situation has only two <tooltip content="no more than one of them can be true at any time">mutually exclusive</tooltip> possibilities %%&nbsp;e.g. the value of `gender` can only be `M` or `F`%%, we can use the `else` statement to deal with both conditions together.

:package: In the example below, the entire `else` block will be skipped if the `if` condition is true.
```python
if gender == 'F':
    print('Female')
else:
    print('Not Female')               
```
<panel type="seamless" header="%%:tv: Using `else`%%">

<iframe width="560" height="315" src="https://www.youtube.com/embed/lWeCgEbk-Ro?rel=0&showinfo=0&start=254&end=336&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

If a situation has more than two mutually exclusive possibilities, we can bring in `elif` (an abbreviation of _else if_) blocks too.

:package: The example below shows how to use an `if-elif-else` construct to control the flow of the execution.
```python
if gender == 'F':
    print('Female')
elif gender == 'M':
    print('Male')
elif gender == 'O':
    print('Other')
else:
    print('Unrecognized value')             
```
<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/gender-if?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel><p/>

Note that in an `if-elif-else` construct no more than one block (the first one whose condition is true) will be executed.

<panel type="seamless" header="%%:tv: Using `elif`%%">
<iframe width="560" height="315" src="https://www.youtube.com/embed/lWeCgEbk-Ro?rel=0&showinfo=0&start=354&end=483&version=3" frameborder="0" allowfullscreen></iframe>

</panel><p/>

<panel type="danger" header=":muscle: Exercise: Grade Analyzer" expanded>
  <include src="e-grades.md" />
</panel>
<panel type="danger" header=":muscle: Exercise: Grade Analyzer (extended)" expanded>
  <include src="e-gradeAnalyzerExtended.md" />
</panel>