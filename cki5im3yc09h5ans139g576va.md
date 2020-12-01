## Unzip any File Using Python

Hello world!

The ZIP file format is a common archive and compression standard. In this Blog article, we will learn how to **Unzip a File.** We will see the implementation in Python.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my **YouTube video Tutorial** to see a working tutorial for better Understanding and a step by step Guide of the same. 

%[https://www.youtube.com/watch?v=cw9r3HLmCbU]

## What will be covered in this Blog

```python
1. What is Zip files?
2. How to Unzip a File Using Python
```

*Let's get started!*

## What is Zip file?:

The Dictionary Definition:

> ZIP is an archive file format that supports lossless data compression. A ZIP file may contain one or more files or directories that may have been compressed.

Zip files can come handy for a lot different things, we make use of it on a regular basis. 

### Uses for Zip File:
- Zip files help you to put all related files in one place.
- Zip files help to reduce the data size.
- Zip files transfer faster than the individual file over many connections.

If you wish to know more about it, you can refer to [**Zip file** Wikipedia Page](https://en.wikipedia.org/wiki/ZIP_(file_format)). 

## Module Used:

### ZipFile Module:

`ZipFile ` module provides tools to create, read, write, append, and list a ZIP file. Any advanced use of this module will require an understanding of the format, as defined in [PKZIP Application Note](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT).

If you wish to know more about it, you can refer to [**ZipFile Module** Documentation](https://docs.python.org/3/library/zipfile.html). 

Now that you are familiar with *Zip file use cases* and have acquired basic knowledge of *ZipFile module,* we can move forward to *the coding section.*

## Time to Code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Unzip%20a%20File). **Drop a star** if you find it useful.


![carbon (6).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1606738734570/VXsOm6mDu.png)

In order to access the Python library, we need to import the package in our Python script. 

```python
import zipfile as z
```

We will make use of `zipfile` module to Unzip the file. Now that we have imported the package in our python script, let's start by defining the target zipped file.

```python
target = 'demo.zip'
```

`demo.zip` is the zip file we are targeting to Unzip. Let's display a start message.

```python
print('Starting to Unzip the File!')
```

Let's make use of  `ZipFile` method from `zipfile` and pass in our target file. I am storing it in `root` 

````python
root = z.ZipFile(target)
````

Once done, let's define our destination details. We will make use of `extractall` method for the same.

If the folder with name `new` already exists, it will create an unzipped file inside it. Otherwise, a new folder will be created with the given name.

**What if NO parameter is passed?** 

Well, in that case, a new folder will be created with name same as the zipped file name i.e. `demo`. 

```python
#CASE 1:
# Destination folder exist with name 'dest'

root.extractall('C:\\Users\imar\Desktop\python\dest')

#CASE 2:
# Create a new Destination folder at the time of Script execution

root.extractall('new')

#CASE 3:
# No parameter is Passed!

root.extractall()
```

Once done, let's end the process using `close` method.

```python
root.close()
```

As soon you end the terminate the process, File will get Unzipped. Let's display a message for user indicating the Successful termination of the process.

```python
print('\nFile is Succesfully Unzipped!')
```


With these steps, we have successfully **Unzipped the File using python.** That's it! 

Simple, isn't it? Hope this tutorial has helped. I would strongly recommend you to Check out the [YouTube video](https://www.youtube.com/watch?v=cw9r3HLmCbU) of the same and **don't forget to subscribe my Channel**.

You can play around with the zipfile library and even explore more features. You can even make use of Python GUI using Tkinter.

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Unzip%20a%20File). **Drop a star** if you find it useful.

Thank you for reading, I would love to connect with you at [Twitter](https://twitter.com/ayushi7rawat) | [LinkedIn](https://www.linkedin.com/in/ayushi7rawat/).

Do share your valuable suggestions, I appreciate your honest feedback!

You should definitely check out my other Blogs:

- [Python 3.9: All You need to know](https://ayushirawat.com/python-39-all-you-need-to-know)
- [The Ultimate Python Resource hub](https://ayushirawat.com/the-ultimate-python-resource-hub)
- [GitHub CLI 1.0: All you need to know](https://ayushirawat.com/github-cli-10-all-you-need-to-know)
- [Become a Better Programmer](https://ayushirawat.com/become-a-better-programmer)
- [How to make your own Google Chrome Extension](https://ayushirawat.com/how-to-make-your-own-google-chrome-extension-1)
- [Create your own Audiobook from any pdf with Python](https://ayushirawat.com/create-your-own-audiobook-from-any-pdf-with-python)
- [You are Important & so is your Mental Health!](https://ayushirawat.com/you-are-important-and-so-is-your-mental-health)

## Resources:

- https://en.wikipedia.org/wiki/ZIP_(file_format)

- https://docs.python.org/3/library/zipfile.html

See you in my next Blog article, Take care!!