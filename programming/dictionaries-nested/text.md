### Nested Dictionaries

**Dictionaries and lists can be nested in each other to create more complicated data structures.**

<tip-box> 

:package: This dictionary keeps track of assignments of each subject. Note how the value is a list rather than a simple value such as int or string.

```python
assignments = {'TE3201': ['do exercises', 'submit project'],
               'CS2103': [],
               'CS3281': ['do presentation']}
```
:bulb: Python ignores line breaks and indentations in the middle of a dictionary/list definition. %%The intention is to allow you to structure the code into a more readable format (e.g., one key-value pair per line).%%

As the values in this dictionary are lists, you can do list operations on them, e.g., `append()`, `len()`

```python
print('CS3281 assignments:', assignments['CS3281'])

assignments['CS3281'].append('study for exams')
print(assignments['CS3281'])

print('How many things to do in TE3201?', len(assignments['TE3201']))

# calculate total assignments
total = 0
for a in assignments.values():
  total = total + len(a)
print('total tasks to do:', total)
```
:arrow_heading_down:
```
CS3281 assignments: ['do presentation']
['do presentation', 'study for exams']
How many things to do in TE3201? 2
total tasks to do: 4
```

</tip-box>

<panel type="danger" header=":muscle: Exercise: Inning-Scores" expanded no-close>
  <include src="e-inningScores.md" />
</panel><p/>

<tip-box> 

:package: This dictionary uses dictionaries as values (i.e., nesting dictionaries inside dictionaries). It stores details of a group of persons.

```python
friends = {'john': {'name': 'John Doe', 'birthday': 'Jan 12'},
           'sara': {'name': 'Sara Parker', 'birthday': 'Jun 30'},
           'betty': {'name': 'Betsy Sims', 'birthday': 'Jan 12'}}
           
print(friends['john']['birthday'])

# print friends whose birthday is Jan 12

for f in friends.keys():
  details = friends[f]
  if details['birthday'] == 'Jan 12':
    print(details['name'])
```
:arrow_heading_down:
```
Jan 12
John Doe
Betsy Sims
```

:bulb: As `friends['john']` evaluates to a dictionary, you can use the `['birthday']` notation to find the birthday of that person.<br>
`friends['john']['birthday']`<br>
→ `{'name': 'John Doe', 'birthday': 'Jan 12'}['birthday']`<br>
→ `'Jan 12'`

</tip-box>

<panel type="seamless" header="%%:computer: Try your own%%">

<iframe height="400px" width="100%" src="https://repl.it/@pythonbasics/dictionaries-nested?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

</panel>

<panel type="danger" header=":muscle: Exercise: Player Stats" expanded no-close>
  <include src="e-playerStats.md" />
</panel>
<panel type="danger" header=":muscle: Exercise: Grade Report" expanded no-close>
  <include src="e-gradeReport.md" />
</panel><p/>