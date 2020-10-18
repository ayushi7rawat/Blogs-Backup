## Convert any .py to .exe with python

When you create a python program and you want to share it with the world and you want them to run your script without having to install python. You can do this by converting the .py file to .exe file. In this article, I will show you how you can do it.

You can refer to the YouTube video Tutorial for better Understanding!

%[https://youtu.be/R8V9ZeeYFtY]

[Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

I recently created [a digital clock with python using Tkinter.](https://ayushirawat.com/create-a-digital-clock-with-python?guid=e536081b-afeb-44e4-8e68-a187d554c330&deviceId=80e56b1c-2c34-484c-b8a4-b157a6bce4ac) I am going to use the same program to demonstrate the conversion of .py file to .exe file.

## What will be covered in this Blog:

```
- What is an executable file?
- Types of executable file formats 
- how to convert .py file to .exe file
```

### What is an executable file?

- In computing, executable code, executable file, or executable program, sometimes simply referred to as an executable or binary, causes a computer **"  to perform indicated tasks according to encoded instructions"**.

- Unlike a data file, an executable file cannot be read because it's compiled.

- A file with an executable file extension means that the file format supports some ability to run an automatic task. 

If you wish to know more about it, You can use this [link to navigate to its Wikipedia Page](https://en.wikipedia.org/wiki/Executable)

## Types of Executable Files

**Note:** Please exercise caution before opening any executable file, especially those received in suspicious emails or downloaded from unfamiliar websites.
So, let's get started!

- Programs, Mac OS X applications, scripts, and macros are all considered executable files. Since these file types run code when opened, unknown executable files, such as those received as e-mail attachments should not be opened.

Use this link to navigate to [list of executable file formats](https://en.wikipedia.org/wiki/Category:Executable_file_formats) at Wikipedia Page

It's Time to code! You can find [all the code at my GitHub Repository.](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/.py%20to%20.exe)

## how to convert .py file to .exe file

### Install the necessary packages.

- Open the folder where you will find the python script which you will convert to .exe file

- Press Shift and hit Right-click

![Screenshot_2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1602210730502/psiiggMg9.png)

- Select **Open power shell window here**

- Next, run the following command in your terminal.

```
pip install pyinstaller
```
PyInstaller bundles a Python application and all its dependencies into a single package. The user can run the packaged app without installing a Python interpreter or any modules. PyInstaller supports Python 3.5 or newer. 

PyInstaller is tested against Windows, Mac OS X, and GNU/Linux.  If you wish to know more about it, Use this [link to navigate](https://pyinstaller.readthedocs.io/en/stable/) to its documentation.
Once the necessary package is installed, let's move forward!

## converting .py file to .exe file

```
pyinstaller -w -F -i "C:\Users\imar\OneDrive\Desktop\YouTube Tutorial/pytoexe/icon.ico" clock.py
```

Let's Understand this now.

Once the command runs successfully, the executable file will get created inside `dist` folder. 

## Flags:

1. **-w **: When you run the executable file, a terminal window will get opened at the back while the executable runs. To prevent this from happening. you can use `-w` flag.

2. **-F **: When you convert your `.py` file to `.exe` file, it comes with a lot of other dependencies. The dependency files will be created along with the `.exe` file inside the `dist` folder. So this flag gives you the power to bind all the dependencies into a single file instead of multiple ones. 

This comes in handy as if you wish you wish to share your program file to someone you would want to give them a single file rather than sharing a folder containing the `.exe` file along with a bunch of other dependency files.

3. **-i **: This flag is used if you wish to add an icon to you `.exe` file. 

Note: The icon must be in `.ico` format only. You can use this [link to navigate](https://convertico.com/) to a website that does this job for you or you can use any other website of your choice to perform this task.

- You need to specify the path of your icon with this flag in order to set the icon of your executable file. 

Finally hit enter and run the command. A new `dist` folder will be created which contains your executable file. Note that now no terminal window opened at the back, no separate dependency file is generated and you have your icon for the application.

That's it. we are done! Simple isn't it?

You can find [all the code at my GitHub Repository.](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/.py%20to%20.exe)

If you have any queries or suggestions, feel free to reach out to me.

You can connect with me on [Twitter](https://twitter.com/ayushi7rawat).

You should definitely check out my other Blogs:

- [Python 3.9: All You need to know](https://ayushirawat.com/python-39-all-you-need-to-know)
- [The Ultimate Python Resource hub](https://ayushirawat.com/the-ultimate-python-resource-hub)
- [GitHub CLI 1.0: All you need to know](https://ayushirawat.com/github-cli-10-all-you-need-to-know)
- [Become a Better Programmer](https://ayushirawat.com/become-a-better-programmer)
- [How to make your own Google Chrome Extension](https://ayushirawat.com/how-to-make-your-own-google-chrome-extension-1)
- [Create your own Audiobook from any pdf with Python](https://ayushirawat.com/create-your-own-audiobook-from-any-pdf-with-python)
- [You are Important & so is your Mental Health!](https://ayushirawat.com/you-are-important-and-so-is-your-mental-health)


Resources: 
- https://pyinstaller.readthedocs.io/en/stable/
- https://en.wikipedia.org/wiki/Executable
- https://en.wikipedia.org/wiki/.exe
- https://en.wikipedia.org/wiki/Category:Executable_file_formats

See you in my next article, Take care!
