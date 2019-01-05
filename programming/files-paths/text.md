### File Paths

A file has a _filename_ and a _path_. **The _path_ specifies the location of a file on the computer**, as a hierarchy of _folders_ (also called _directories_).

<tip-box> 

<tabs> 
  <tab header="Windows">

:package: File `C:\photos\2018\home.jpg`

* Filename: `home.jpg`
* Path: `C:\photos\2018` (Windows uses the back slash `\` as the _separator_ symbol in paths )
* Folders in the path (`C:` is called the _root folder_): 
  ```
  C: {root}
    ˪ photos
        ˪ 2018
  ```
  
:exclamation: Windows file names and paths are not case sensitive: `C:\photos\2018\home.jpg` is same as `C:\PHOTOS\2018\HOME.JPG`.
  </tab>
  <tab header="OS-X/Linux">

:package: File `/Users/john/home.jpg`

* Filename: `home.jpg`
* Path: `/Users/john` (OS-X/Linux uses the forward slash `/` as the _separator_ symbol in paths )
* Folders in the path (the `/` at the start of the path is considered the _root folder_): 
  ```
  / {root}
    ˪ Users
        ˪ john
  ```
:exclamation: OS-X/Linux file names and paths are case sensitive. `/Users/john/home.jpg` is NOT the same as `/USERS/JOHN/HOME.JPG`

  </tab>
</tabs>

</tip-box>

The Python module `os` contains functions for dealing with files and folders. For example, you can use `os.getcwd()` to get the <tooltip content="A program has a _working directory_ at any time; it can change over time">current working directory</tooltip> and `os.chdir()` to change the working directory to a different location.

<tip-box> 

:package: Example code showing how to print/change current working directory

<table> 
<tr>
  <td>

```python
import os

cwd = os.getcwd() # store current working dir
print(cwd) # print current working dir
os.chdir('C:\\temp\\python') # change dir
print(os.getcwd()) # print current working dir
os.chdir(cwd) # change working dir back to original
print(os.getcwd())
```
  </td>
  <td><br><br><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br><br><br>

```
C:\modules\te3201
C:\temp\python
C:\modules\te3201
```
  </td>
</tr>
</table>

:bulb: Note how the path `'C:\\temp\\python'` uses double slash to <trigger trigger="click" for="modal:filePaths-stringsEscape">escape</trigger> the `\`. In OS-X or Linux, it can be something like `/user/john/python` (no need for double slash).

<modal large title="**Escape Sequences** %%(extrat from Strings → String Literals)%%" id="modal:filePaths-stringsEscape">
  <include src="../strings-literals\text.md#strings-escape"/>
</modal>

</tip-box>

**A path that specifies all folders starting from the root is an _absolute path_. A path that is specified relative to the current working directory is a _relative_ path.**

<tip-box> 

:package: Assume the current working directory is `C:\modules\te3201` and you created a new folder inside it named `exercises` and put a `ex.txt` file in that folder.

* Absolute path of the file: `C:\modules\te3201\exercises\ex1.txt`
* Relative path of the file: `exercises\ex1.txt`

</tip-box>

In a path, you can use the  dot `.` as a shorthand to refer to the current working directory. Similarly, `..` can be used to refer to the parent directory. 


<tip-box> 

:package: If the current working directory is `C:\modules\te3201`, you can use any of the following to refer to `C:\modules\te3201\exercises\ex1.txt`. 
* `exercises\ex1.txt`
* `.\exercises\ex1.txt`
* `..\te3201\exercises\ex1.txt`
* `..\..\modules\te3201\exercises\ex1.txt`

<panel type="seamless" header="%%another example%%">

![](https://automatetheboringstuff.com/images/000032.jpg)
</panel>

</tip-box>

You can use `os.mkdirs()` function to create folders and `os.removedirs()` to delete folders.

<tip-box> 

:package: Example code showing how to create/delete directories

<table> 
<tr>
  <td>

```python
print(os.getcwd())
os.makedirs('ex\\w1')
os.chdir('ex\\w1')
print(os.getcwd())
os.chdir('..') # go to parent dir
print(os.getcwd())
os.chdir('..')
os.removedirs('ex\\w1')
```
  </td>
  <td><br><br><br><br><br>&nbsp;→&nbsp;</td>
  <td><br><br><br><br><br>

```
C:\repos\nus-te3201\sample-code
C:\repos\nus-te3201\sample-code\ex\w1
C:\repos\nus-te3201\sample-code\ex
```
  </td>
</tr>
</table>

</tip-box>

`os.path` module has many functions that can help with paths. For example, `os.paths.join()` function can be used to generate file path that matches the current operating system.

<tip-box> 

:package: Consider the code below: 

```python
cwd = os.getcwd()
print(os.path.join(cwd, 'ex', 'w2'))
```

If you run it on a Windows computer in the folder `C:\modules\te3201`, it prints `C:\modules\te3201\ex\w2`.<br>
If your run it on a OS-X computer in the folder `/Users/john`, it prints `/Users/john/ex/w2`.

</tip-box>

:exclamation: To ensure that your code can work on any OS, you are advised to use `os.path.join()` function instead of hard-coding the <tooltip content="i.e., `\\` on Windows and `/` on OS-X/Linux">path separators</tooltip>.

<tip-box> 

:package: contrasting hard-coding the separator vs using `os.path.join()`:

:x: Works only on Windows | :white_check_mark: Works on both Windows and OS-X
--------------------- | ------------------------------
`os.makedirs('ex\\w1')` | `os.makedirs(os.path.join('ex', 'w1'))`

</tip-box>

<panel type="danger" header=":muscle: Exercise: Create Directory" expanded no-close>
  <include src="e-createDir.md" />
</panel><p/>