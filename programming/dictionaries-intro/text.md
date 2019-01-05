### The Dictionary Data Structure

**A _dictionary_ (python type: `dict`) is a collection of many values that can be indexed by any object type**, unlike lists that are automatically indexed by integers. **Indexes for dictionaries are called _keys_**, and a key with its associated value is called a _key-value pair_. Python **dictionaries use curly braces notation `{ key1: value1, key2: value2, ...}`**.

<tip-box> 

:package: A list containing names of animals `['cat', 'dog', 'hen', 'fish']`

Index | Value
----- | -----
`0` | `'cat'`
`1` | `'dog'`
`2` | `'hen'`
`3` | `'fish'`

:package: A dictionary containing ages of three people `{'john': 12, 'sara': 14.5, 'colin': 13}`. `john`-`12` is a key-value pair.

Key | Value
----- | -----
`'john'` | `12`
`'sara'` | `14.5`
`'colin'` | `13`

:package: A dictionary containing details of a person `{'name': 'john', 'age': 14.5, 'sex': 'F', 'citizen': True}`

Key | Value
----- | -----
`'name'` | `'john'`
`'age'` | `14.5`
`'gender'` | `'F'`
`'citizen'` | `True`

</tip-box>

<tip-box> 

:package: Some examples of defining dictionaries.


```python
friends = {} # empty dictionary
grades = {'TE3201': 'A'}
numbers = {1: 'one', 2: 'two', 3: 'three'}
is_nice = {'jane': False, 'hakim': True, 'ravi': True}
prices = {'bread': 3.5, 'butter': 5.0, 'banana': 0.15}
```

</tip-box>

Unlike lists which contain an ordered sequence of items, **dictionaries are not ordered** i.e., we cannot force a key-value pair in a dictionary to be at a specific position %%e.g., in the example above, there is no guarantee that `'bread'`:`'3.50'` pair will be at the first position of the dictionary `prices` after adding more key-value pairs to it%%.

<panel type="danger" header=":muscle: Exercise: Get Subject Info" expanded no-close>
  <include src="e-getSubjectInfo.md" />
</panel><p/>