### CSV files

**CSV files are often used as a simple way to save spreadsheet-like data.** Each line in a CSV file represents a row in the spreadsheet, and commas separate the cells in the row. They usually have the `.csv` extension and can be opened in spreadsheet programs such as Excel or in any text editor.

<tip-box> 

:package: Here is the content of a simple CSV file %%(click [here](deliveries.csv) to download a copy)%% and how it looks like when opened in Excel.

<table> 
<tr>
  <td>

```csv
4/11/2017,Alice Bee,4
5/11/2017,Chris Ding,12
5/11/2017,Brenda Chew,13
6/11/2017,Dan Pillai,5
```
  </td>
  <td>&nbsp;→&nbsp;</td>
  <td>

![]({{baseUrl}}/files-csv/images/deliveries.png =250x)
  </td>
</tr>
</table>

</tip-box> 

:bulb: If a value itself contains a comma %%e.g., `Foo, Emily`%%, it can be enclosed in double quotes %%e.g., `"Foo, Emily"`%%, to prevent it being misinterpreted as multiple values.

<tip-box> 

:package: This example shows how to use double quotes to handle commas inside a value:

* `7/11/2017,"Foo, Emily",5` interpreted as three values: `7/11/2017` and `Foo, Emily` and `5`
* `7/11/2017,Foo, Emily,5` interpreted as four values: `7/11/2017` and `Foo` and ` Emily` and `5`

</tip-box>

Although CSV files are text files that can be read/written using normal file access techniques covered earlier, **Python has an in-built module named `csv` that provides functions to deal with CSV files more conveniently.** For example, **it provides a way to read a CSV file as a `Reader` object that knows how to interpret a CSV file.**

<tip-box> 

:package: The code below shows how to use the `csv` module to read contents of a CSV file named `deliveries.csv`:

```python
import csv 

deliveries_file = open('deliveries.csv') # open file
deliveries_reader = csv.reader(deliveries_file) # create a Reader
for row in deliveries_reader: # access each line using the Reader
  print(row)
deliveries_file.close() # close file
```
:arrow_heading_down:
```
['4/11/2017', 'Alice Bee', '4']
['5/11/2017', 'Chris Ding', '12']
['5/11/2017', 'Brenda Chew', '13']
['6/11/2017', 'Dan Pillai', '5']
```
As you can see, `Reader` object returns content of a line as a list object with the value of each cell as an item in the list. Replacing the line,
```python
...
print(row)
...
``` 
... with the following line,
```python
...
print('Date:', row[0], '\tRecipient:', row[1], '\tQuantity:', row[2] )
...
```
... will give you the output shown below:
```
Date: 4/11/2017 	Recipient: Alice Bee 	Quantity: 4
Date: 5/11/2017 	Recipient: Chris Ding 	Quantity: 12
Date: 5/11/2017 	Recipient: Brenda Chew 	Quantity: 13
Date: 6/11/2017 	Recipient: Dan Pillai 	Quantity: 5
```

</tip-box> 

Note that all values read from a CSV files come as strings. If they are meant to represent other types, you need to convert the string to the correct type first.

<tip-box> 

:package: In this example the 3rd value of each row is converted to an int before adding them up.

```python
deliveries_file = open('deliveries.csv') 
deliveries_reader = csv.reader(deliveries_file) 
total = 0
for row in deliveries_reader:
  # convert 3rd cell to an int and add to total
  total = total + int(row[2]) 

print('Total quantity delivered:', total)
deliveries_file.close()
```
:arrow_heading_down:
```
Total quantity delivered: 34
```

</tip-box>

**The `csv` module also provide an easy way to write to CSV files, one row at a time, using a `Write` object.**

<tip-box> 

:package: The code below writes two rows to the `pricelist.csv` file.

```python
output_file = open('pricelist.csv', 'w', newline='') # open file in write mode
output_writer = csv.writer(output_file) # get a Writer object
output_writer.writerow(['apples', '1', '1.5', 'True']) # write one row
output_writer.writerow(['bananas', '3', '2.0', 'False']) # write another row
output_file.close() # close file
```
The `pricelist.csv` file will now contain:
```
apples,1,1.5,True
bananas,3,2.0,False
```

* :bulb: You can open a file in append mode if you want to append to it instead of overwriting current content. <br> e.g., `output_file = open('pricelist.csv', `==`'a',`==` newline='')`
* :bulb: The keyword argument `newline=''` need to be used when opening a CSV file in Windows. The reasoning behind it is beyond the scope of this book.
</tip-box>

<panel type="danger" header=":muscle: Exercise: Calcluate GST" expanded no-close>
  <include src="e-calculateGst.md" />
</panel><p/>