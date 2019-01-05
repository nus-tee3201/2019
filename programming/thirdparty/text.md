# Appendix A: Installing 3rd-Party Modules

In addition to built-in modules you get with Python by default, there are many modules written by others that you can make use of. **You can install third-party modules using Python’s `pip` tool**. This tool downloads and installs Python modules onto your computer from https://pypi.python.org/ (aka _PyPi_ or _Python Package Index_).

First, ensure that you have `pip` installed by running this command in a command shell (not Python interpreter shell), which should print out the version of the pip tool you have.

```
pip --version
```

After that, to install a third-party module (or _packages_ as they are sometimes called), you can run the `pip install {packagename}` command.

<tip-box> 

:package: The example below shows how to install the `colorama` module that allows you to colorize text printed out to the console.

```bash
pip install colorama
```
:arrow_heading_down:
```
Collecting colorama
  Downloading colorama-0.3.9-py2.py3-none-any.whl
Installing collected packages: colorama
Successfully installed colorama-0.3.9
```
After installing colorama, you can import it into your code and use its features to print colorized text.
```python
import colorama

colorama.init()  # one-time initialization

print(colorama.Fore.YELLOW + ' Some yellow text')
print(colorama.Fore.BLUE + colorama.Back.WHITE + ' Some blue text in a white background')
print(colorama.Style.RESET_ALL + ' Back to normal now')
```
:arrow_heading_down:<br>

<img src="{{baseUrl}}/thirdparty/images/coloramaOutput.png" /></p>

</tip-box>

<tip-box> 

**:bulb: Some useful third-party modules:**
  * [`colorama`](https://pypi.python.org/pypi/colorama): For colorizing text printed in the console
  * [`selenium`](https://pypi.python.org/pypi/selenium): For automating the Browser
  * [`pyzmail`](http://www.magiksys.net/pyzmail/): For sending emails
  * [`twilio`](https://www.twilio.com/docs/libraries/python): For sending SMS
  * [`PyPDF2`](https://pythonhosted.org/PyPDF2/): For working with PDF files
  * [`pyperclip`](https://pypi.python.org/pypi/pyperclip/1.6.0): To access the clipboard of the operating system
  * [`dateparser`](https://pypi.python.org/pypi/dateparser/0.7.0): To parse natural language repsentation of dates e.g., `in 2 days`, `tomorrow`

</tip-box>

**:paperclip: Resources**:
* [More about installing 3rd-party modules](https://automatetheboringstuff.com/appendixa/)

<panel type="danger" header=":muscle: Exercise: Print Errors in Red" expanded no-close>
  <include src="e-printErrorsInRed.md" />
</panel><p/>