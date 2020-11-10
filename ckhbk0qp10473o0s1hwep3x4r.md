## Run Javascript from Python

Hello Reader, hope you and your family is in good health! 

**Javascript** is a very **powerful** language, honestly, I am a baby in Js but I have always wondered, can **Js** integrated with **Python**. Recently, I was surfing the Internet and **Js2Py** module appeared in my **Google Search**.

I am attending a [Technical Writing Bootcamp](https://hashnode.com/bootcamp/batch-2) at @hashnode. **Hashnode Bootcamp II** is a free virtual Bootcamp to help beginner technical writers to improve their writing skill.

This article is inspired by the latest session by Chris, @dailydevtips, he suggested to write about something that I have encountered and googled in past.

In this Blog article, we will learn how to **Run Javascript commands from inside Python script .** We will make use of the Js2Py module.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my **YouTube video Tutorial** for better Understanding and a step by step Guide of the same. 

%[https://www.youtube.com/watch?v=dTiu7Y9j4WY]

## What will be covered in this Blog

```python
1. Js2Py Introduction
2. How to Run Javascript commands from inside Python script 
```

# Js2Py Introduction:

You can translate JavaScript to Python using Js2Py. Js2Py is a Python module which can used to translator JavaScript to Python & acts as a JavaScript interpreter written in 100% pure Python. 

- It translates any valid JavaScript (ECMA Script 5.1) to Python.
- Translation is fully automatic.
- Does not have any dependencies - uses only standard python library.

### Limitations:

It has three limitations:

- **strict mode** is ignored.

- **with statement** is not supported.

- Indirect call to eval will is treated as direct call to eval (hence
  always evals in local scope)

  

If you wish to know more about it, you can refer to [Js2Py Documentation](https://github.com/PiotrDabkowski/Js2Py). Use this link to navigate to the documentation.

Now that you are aware of Js2Py basics, we can move forward to the coding section. Let's get started!

## Time to Code!
You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Run%20javascript%20in%20python). **Drop a star** if you find it useful.

![code.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1604987128341/oIR1VImmR.png)

In order to access the Python library, you need to install it into your Python environment, use the following command to install `Js2Py `  

```
pip install js2py 
```

Now, let's import the package in our Python script.

```python
import js2py
```

Let's start with a simple `Hello World!`. 

```javascript
#example 1
#a js command
js1 = 'console.log( "Hello World!" )'

res1 = js2py.eval_js(js1)
```

Let's look at the Equivalent `python` code:

```python
print('Hello World!')
```

So here, we stored the `javascript` command in `js1` . We will make use of `eval.js` method from `js2py` module here, pass in our js code in it and store it in `res1`.  Finally we are output our result.

```python
#print the result
res1

#OUTPUT: Hello World!
```

Now, let's look at another example! Let's create a addition function in **Javascript**.

```javascript
#exapmle 2
#a js function
js2 = '''function add(a, b){
    return a + b;
    }'''
```

Let's look at the Equivalent `python` code:

```python
def add(a, b):
    return a+b
```

Let's store it in `js2` and in order to make our program more interactive, let's take the input from user inside the python script.

```python
a = int(input('Enter a num: '))
```

We will make use of `eval.js` method from `js2py` module here, pass in our js function in it and store it in `res2`.  

```python
res2 = js2py.eval_js(js2)
```

Finally, let's print out our result. So, save and run the python script.

```python
print(res2(a,3))
```

And it will output the addition of two numbers. It will vary as it depends upon the user input.

This is a basic working example of Js2Py. This is all about the **Running Javascript commands from inside Python script**. That's it! 

Simple, isn't it? Hope this tutorial has helped. I would strongly recommend you to Check out the [YouTube video](https://www.youtube.com/watch?v=dTiu7Y9j4WY) of the same and **don't forget to subscribe my Channel**.

You can play around with the Js2Py library and even explore more features.

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Run%20javascript%20in%20python). **Drop a star** if you find it useful.

Thank you for reading, I would love to connect with you at [Twitter](https://twitter.com/ayushi7rawat) | [LinkedIn]().

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

- https://github.com/PiotrDabkowski/Js2Py
- https://pypi.org/project/Js2Py/0.27/

See you in my next Blog article, Take care