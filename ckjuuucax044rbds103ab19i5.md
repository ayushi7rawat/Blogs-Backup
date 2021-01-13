## Generate Wiki Summary using Python

Hello world!

In this Blog article, we will learn how to **Generate Wiki Summary.** We will see the implementation in Python.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my **YouTube video Tutorial** to see a working tutorial for better Understanding and a step by step Guide of the same. 

%[https://www.youtube.com/watch?v=ixB2YHGSiAQ]

## What will be covered in this Blog

```python
1. What is Wikipedia?
3. Basics of pywhatkit Module
4. Generating Wiki Summary using Python
```

*Let's get started!*

## What is **Wikipedia**?:

**Wikipedia** is a free, open content online encyclopedia created through the collaborative effort of a community of users known as **Wikipedians**. Anyone registered on the site can create an article for publication.

If you wish to know more about it, you can refer to [**Wiki's** Wikipedia Page](https://en.wikipedia.org/wiki/Wikipedia). 

## Module Used:

### pywhatkit Module:

[PyWhatKit](https://pypi.org/project/pywhatkit/) is a Python library with various helpful features. It is an easy to use library which does not requires you to do some additional setup. 

This module has lots of other cool features as well. Feel free and go ahead to explore them or if you wish I can write an article about them.

If you wish to know more about it, you can refer to [**pywhatkit Module** Documentation](https://github.com/Ankit404butfound/PyWhatKit). 

Now that you are familiar with *Wikipedia* basics and have acquired basic knowledge of *pywhatkit module,* we can move forward to *the coding section.*

## Time to Code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Turn%20any%20image%20to%20ASCII). **Drop a star** if you find it useful.

![code.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1609991939729/Gsr-anS7U.png)

In order to access the Python library, you need to install it into your Python environment

```python
pip install pywhatkit as kt
```

Now, we need to import the package in our python script. Use the following command to do so.

```python
import pywhatkit as kt
```

Now that we have imported the library using the command `import pywhatkit as kt`, let's proceed. 

Let's display a welcome message. we will make use of `print` method for the same.

```python
print("Lets Generate Wiki Summary!")
```

Be sure of what you want to search and once you decide, let's store it in `target1`.

```python
target1 = "Python"
```

Finally, let's call `info` method. 

```python
kt.info(target1,lines=3)
```

NOTE: Here we are passing in two parameters:

- the 1st parameter depicts the topic of search used to generate wiki summary
- 2nd parameter depicts the number of lines of summary you want

Let's have a look at the output search result.

![output.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1609991953445/gzsryhAsA.png)

Let's have a look at another example.

```python
target2 = 'coronavirus'
print('\n')
kt.info(target2,lines=3)
```

With these steps, we have successfully **Performed Google search using python.** That's it! 

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

See you in my next Blog article, Take care!!
