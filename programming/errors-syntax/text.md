### Syntax Errors

**A _syntax error_, also known as a _parsing error_, is when your code does not follow rules for writing Python code.** Python interpreter shows an error message when it encounters a syntax error.

<tip-box> 

:package: The code below has a syntax error because it breaks the Python rule that requires a `:` to follow the condition of an `if` statement.

<table> 
<tr>
  <td>

```python
if 5 > 4
  print('Greater')
  
  
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>

```
Traceback (most recent call last):
  File "python", line 1
    if 5 > 4
           ^
SyntaxError: invalid syntax
```
  </td>
</tr>
</table>

</tip-box>

Some Python editors (e.g., REPL) flag syntax errors even before you run the code.

<tip-box> 

:package: Note how REPL Python editor points out the syntax error using a red :x: in the _<tooltip content="the column on the extreme left of the editor">gutter</tooltip>_ of the editor.

![]({{baseUrl}}/errors-syntax/images/syntaxErrorInRepl.png =250x)

</tip-box>