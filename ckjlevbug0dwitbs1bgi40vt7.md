## Turn any Image to ASCII Art using Python

Hello world!

In this Blog article, we will learn how to **Turn any image to an ASCII art.** We will see the implementation in Python.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my **YouTube video Tutorial** to see a working tutorial for better Understanding and a step by step Guide of the same. 

%[https://www.youtube.com/watch?v=AOa4T_xW9cc]

## What will be covered in this Blog

```python
1. What is ASCII?
3. Basics of pywhatkit Module
4. Converting any image to ASCII art using Python
```

*Let's get started!*

## What is ASCII?:

ASCII, abbreviated from American Standard Code for Information Interchange.

ASCII is a character encoding standard for electronic communication. ASCII codes represent text in computers, telecommunications equipment, and other devices.

If you wish to know more about it, you can refer to [**ASCII's** Wikipedia Page](https://en.wikipedia.org/wiki/ASCII). 

## Module Used:

### pywhatkit Module:

[PyWhatKit](https://pypi.org/project/pywhatkit/) is a Python library with various helpful features. It is an easy to use library which does not requires you to do some additional setup. 

This module has lots of other cool features as well. Feel free and go ahead to explore them or if you wish I can write an article about them.

If you wish to know more about it, you can refer to [**pywhatkit Module** Documentation](https://github.com/Ankit404butfound/PyWhatKit). 

Now that you are familiar with *ASCII* basics and have acquired basic knowledge of *pywhatkit module,* we can move forward to *the coding section.*

## Time to Code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Turn%20any%20image%20to%20ASCII). **Drop a star** if you find it useful.

![code_snippet.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1609906793268/9HHJuWvAo.png)

In order to access the Python library, you need to install it into your Python environment

```python
pip install pywhatkit as kt
```

Now, we need to import the package in our python script. Use the following command to do so.

```python
from pywhatkit as kt
```

Now that we have imported the library using the command `import pywhatkit as kt`, let's proceed. 

Let's display a welcome message. we will make use of `print` method for the same.

```python
print("Let's turn images to ASCII art!")
```

Now, let's capture the image you wish to convert to ASCII art and let's store it in source_path. 


![flower.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1609906812180/E27jSAzDt.png)

This is the image I am going to use as demo here. The image depicts a flower. Make sure to give the correct path here. If the python script could not locate an image with the given name at the mentioned path, it will result into an error.

Next, create a placeholder to store the output. As its an ASCII file, make sure to use the correct extension, i.e. `.text` and let's store it in `target_path`.

```python
source_path = 'flower.png'
target_path = 'demo_ascii_art.text'
```

Finally, let's call `image_to_ascii_art` method. 

```python
kt.image_to_ascii_art(source_path, target_path)
```

NOTE: The output file will be generated in the same folder where the python script resides if no alternate path is mentioned.

Let's have a look at the output file and its comparison with the actual image file.

![output1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1609906848976/_r15ZQFLA.png)

Let's have a look at another example. I am making use of my image as demo here. Post successful run, a new text file will get created and will look something like this

![output2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1609906870364/FSY3GpLcV.png)

With these steps, we have successfully **Turned an image to an ASCII art using python.** That's it! 

Simple, isn't it? Hope this tutorial has helped. I would strongly recommend you to Check out the [YouTube video](https://www.youtube.com/watch?v=ixB2YHGSiAQ) of the same and **don't forget to subscribe my Channel**.

You can play around with the `pywhatkit` library and even explore more features. 

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Turn%20any%20image%20to%20ASCII). **Drop a star** if you find it useful.

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

- https://en.wikipedia.org/wiki/ASCII
- https://pypi.org/project/pywhatkit/
- https://github.com/Ankit404butfound/PyWhatKit

See you in my next Blog article, Take care!