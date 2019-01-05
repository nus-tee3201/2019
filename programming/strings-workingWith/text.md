### Working with Strings

As you have seen before, you can use `+` and `*` operators to concatenate and replicate strings<br>
%%e.g., `'abc' + '!'*5` evaluates to `'abc!!!!!'`%%.

You can **use indexes and slices to access characters of a string**, just like if a string is a simply a list of characters.

i.e., `'Hi there'` is same as a list:

H   | i | &nbsp; | t | h | e | r | e | !
--- |---|--------|---|---|---|---|---|---
0   | 1 | 2      | 3 | 4 | 5 | 6 | 7 | 8

<tip-box> 

:package: The code below shows how to use index and slice notations to get parts of a string.

<table> 
<tr>
  <td>

```python
s = 'Hi there!'
print(s[0])
print(s[-1])
print(s[3:6])
```
  </td>
  <td><br><br>&nbsp;→&nbsp;</td>
  <td><br><br>

```
H
!
the
```
  </td>
</tr>
</table>

</tip-box>

:exclamation: Strings are immutable. The following code will not work: `s[0] = 'h'`

<panel type="danger" header=":muscle: Exercise: Shorten String" expanded no-close>
  <include src="e-shortenString.md" />
</panel><p/>


You can **use the `in` and `not in` operator to see if one string is a sub-string of another**.

<tip-box> 

:package: Examples of checking for the existence of a sub-string:

<table> 
<tr>
  <td>

```python
s = 'Hi there!'
print('Hi' in s)
print('hi' in s) # matching is case-sensitive
print('Hello' not in s)
```
  </td>
  <td><br><br>&nbsp;→&nbsp;</td>
  <td><br><br>

```
True
False
True
```
  </td>
</tr>
</table>

</tip-box>

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/strings-workingWith?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel>

<panel type="danger" header=":muscle: Exercise: Has All Characters" expanded no-close>
  <include src="e-hasAllCharacters.md" />
</panel><p/>