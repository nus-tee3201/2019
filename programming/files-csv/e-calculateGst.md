#### Exercise : Calculate GST

Suppose there is a CSV file in this format:

<table> 
<tr>
  <td>

`itemlist1.csv`:
```
item,price
book,10.0
bag,50.0
"pens, pencils", 5.0
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>

item|price
 ----|-----
 book|10.0
 bag|50.0
 pens, pencils| 5.0

  </td>
</tr>
</table>

Write a program to calculate GST for each item at 7% and give the value as an additional column. The ouput should be in a new file.

<table> 
<tr>
  <td>

`updated_itemlist1.csv`:
```
item,price,GST
book,10.0,0.7
bag,50.0,3.5
"pens, pencils", 5.0,0.35
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>

item|price|GST
----|-----|---
book|10.0|0.7
bag|50.0|3.5
pens, pencils| 5.0|0.35

  </td>
</tr>
</table>



<panel type="seamless" header="%%:bulb: Python hints%%">

```python
import csv

def calculate_GST(source_file, target_file):
  """Read the data from the CSV file source_file and write 
  the data, including the calculated GST values, to the CSV file target_file
  """
  input_lines = read_csv_lines(source_file)
  updated_lines = []
  
  # ADD YOUR CODE HERE
  
  write_to_csv_file(updated_lines, target_file)
   
  
def read_csv_lines(filename):
  """Return the values in the csv file (specified by the filename) as a list of lists
  each list representing a row of the file.
  
  Example: If the file file1.csv has the following contents,
  item,price
  book,10.0
  read_csv_lines('file1.csv') returns [['item', 'price']['book', '10.0']]
  
  """
  return [] # REPLACE WITH YOUR CODE
  
  
def write_to_csv_file(lines, filename):
  """Write the given lines (a list of lists) to the CSV file (specified by filename)
  
  Example:
  write_to_csv_file([['item', 'price', 'GST']['book', '10.0', '0.7']], 'file2.txt')
  
  """
  pass # REPLACE WITH YOUR CODE
  

def process(source_file, target_file):
  
  calculate_GST(source_file, target_file)
  print(read_csv_lines(target_file))
  
  
process('itemlist1.csv', 'updated_itemlist1.csv')
process('itemlist2.csv', 'updated_itemlist2.csv')
```

</panel>