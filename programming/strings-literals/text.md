### String Literals

A <tooltip content="a string value, not a variable">string literal</tooltip> can normally be specified by enclosing it within a pair of `''` or a pair of `""` %%e.g., `'How is life?'`%%. However, this will not work if the string has a <tooltip content="a character that has special meaning in Python">special character</tooltip> in it %%e.g., `'How's life?'` is not acceptable to Python because it contains a `'` which has the special meaning 'end of string', confusing Python as to which `'` of the string literal indicates the end of the string. This is similarly confusing: `"Say "wow""`%%.

<div id="strings-escape">

An escape sequence is a sequence of characters in a string literal that is taken together and interpreted in a special way. You can **use an _escape sequence_  to include a special character in a string literal** without interpreting it as a special character.  Given below are some examples:

Escape Sequence | Meaning | Example | Output
--------------- | ------- | ------- | ------
`\'` | single quote | `print('How\'s Life')` | `How's Life?`
`\"` | double quote | `print("Say \"wow\"")` | `Say "wow"`
`\\` | back slash | `print('files\\text')` | `files\text`

Another use of escape sequences is to give a special meaning to a character that normally does not have a special meaning. Here are some examples:

Escape Sequence | Meaning | Example | Output
--------------- | ------- | ------- | ------
`\t` | horizontal tab | `print('aaa\tbbb')` | `aaa` `  ` `bbb`
`\n` | line break | `print('hi\nthere!')` | `hi`<br>`there!`

</div>

<panel type="danger" header=":muscle: Exercise: Escape Sequences" expanded no-close>
  <include src="e-escapeSequences.md" />
</panel><p/>

You can **use a pair of triple quotes to indicate a multi-line string literal**. 

<tip-box> 

:package: Here is an example multi-line string that uses triple quotes.

<table> 
<tr>
  <td>

```python
print('''Hi,
How's life?
bye!
-me''')
```
  </td>
  <td><br>&nbsp;→&nbsp;</td>
  <td><br>

```
Hi,
How's life?
bye!
-me
```
  </td>
</tr>
</table>

<table> 
<tr>
  <td>

```python
def get_email_body():
  body = '''This is the first line of the email.
This is the second line.
This is the third line.
          - bye!'''
  return body

print(get_email_body())
```
  </td>
  <td><br><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br><br>

```
This is the first line of the email.
This is the second line.
This is the third line.
          - bye!
```
  </td>
</tr>
</table>

</tip-box>

It is optional to escape `'` and `"` inside a mult-line string within triple quotes e.g., `How's life?` in the example above.

<panel type="danger" header=":muscle: Exercise: Multi-Line String" expanded no-close>
  <include src="e-multiLineString.md" />
</panel><p/>

**Triple double-quotes (`"""`) are commonly used to show documentation of code. Such comments are called _docstrings_.**

<tip-box> 

:package: The `remove_head(items)` function below has a docstring that explains its behavior.

```python
def remove_head(items):
  """Remove the first item of the items.

  The list should have at least one item.
  Arguments:
  items -- (type: list) the list of items to be modified
  """
  print('removing head of list ', items)
  del items[0]
```


</tip-box>

:paperclip: Vist [this page](https://www.python.org/dev/peps/pep-0257/) to learn more about docstrings

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/strings-literals?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel>
