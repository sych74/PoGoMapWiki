## Common Errors

**Q**: My computer says Python is not recognized!

**A**: First, restart to make sure it wasn't because some changes weren't applied and try again.
if that doesn't fix it, open an explorer window and find your Python installation, it should either be in C:\Python27 or C:\Users\YOURUSERNAME\AppData\Programs\Python\Python27 (The python directories could be named differently depending on which version you installed, so don't just copy and paste!)
Once you find where python is, copy it down, then open cmd as an administrator and enter:
setx PATH "%PATH%;PATH TO YOUR PYTHON INSTALLATION"
and replace PATH TO YOUR PYTHON INSTALLATION with the actual path to where pip is, including your drive letter and everything. You'll probably need to log out and log back in or restart for the changes to take effect.

Exception , e

Invalid syntax.
-------------------------------------------------------------------
You are using python 3, download python 2.7 instead.


pip or python is not recognized as an internal or external command.
-------------------------------------------------------------------

use this:

replace pip with C:\Python27\Scripts\pip 

replace python with C:\Python27\python