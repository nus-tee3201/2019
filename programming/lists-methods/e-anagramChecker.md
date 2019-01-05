#### Exercise : Anagram Checker

Complete the functions as described below:
* `is_anagram(word1, word2)`: returns `True` if `word1` is an anagram of `word2`(i.e., letters of `word1` can be rearranged to get `word2` e.g., `ton` and `not` are anagrams).

You may find these built-in functions useful to this exercise:
* `list(string)`: splits a string into a list of letters.<br>
  e.g., `'quick'.split()` → `['q', 'u', 'i', 'c', 'k']`

<table>
<tr>
  <td>

```python
def is_anagram(word1, word2):
  return 

print(is_anagram('santa', 'damith'))
print(is_anagram('santa', 'satan'))
```
  </td>
  <td><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br>
  
```
False
True
```
  </td>
</tr>
</table>

<panel type="seamless" header="%%:bulb: Hint%%">

Convert each word into a list of letters and sort the letters. If the words are anagrams, sorted letters of one word should be same as the sorted letters of the others.

Example:
* `'ton'` → convert to list of letters → `['t', 'o', 'n']` → sort → `['n', 'o', 't']`
* `'not'` → convert to list of letters → `['n', 'o', 't']` → sort → `['n', 'o', 't']`

</panel>

<panel type="seamless" header="%%:bulb: Partial solution%%">

```python
def letters_sorted(word):
  letters = list(word)
  letters.sort()
  return letters
  
def is_anagram(word1, word2):
  return letters_sorted(word1) == ...
```

</panel>