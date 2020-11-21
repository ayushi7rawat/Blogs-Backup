## How To Add A Progress Bar In Python

Hello world!

When you happen to install a software, download an application or media or load a page, you see a progress bar give you an estimate of how long the process would take to complete or render. You can add one in your code too. In this Blog article, we will learn how to **Create Progress Bar.** We will see the implementation in Python.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my **YouTube video Tutorial** to see a working tutorial for better Understanding and a step by step Guide of the same. 

%[https://www.youtube.com/watch?v=wbYqz71WVvI]

## What will be covered in this Blog

```python
1. tqdm Introduction
2. How to Create Progress Bar
```

# `tqdm` Introduction:

A progress bar is a graphical control element used to visualize the progression of an extended computer operation, such as a download, file transfer, or installation. We will make use of the Python library **tqdm**, to create simple progress bars which can be added in the code and make it look lively!

`tqdm` means "progress" in Arabic (*taqadum*, تقدّم) and is an abbreviation for "I love you so much" in Spanish (*te quiero demasiado*).  `tqdm` is Fast and Extensible Progress Meter.

If you wish to know more about it, you can refer to [`tqdm`Documentation](https://pypi.org/project/speedtest-cli/). Use this link to navigate to the documentation.

Now that you are aware of `tqdm`  basics, we can move forward to the coding section. Let's get started!

## Time to Code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/create%20progress%20bar). **Drop a star** if you find it useful.



In order to access the Python library, you need to install it into your Python environment, use the following command to install `tqdm` 

```python
pip install tqdm
```

Now, let's import the package in our Python script.

```python
from tqdm import tqdm, trange
```

We will require time package, so lets import that one as well

```python
import time
```

Let's run a loop for an iterable

```python
for i in range(10):
    pass
```

In order to see the progress, lets make use of `time` module

```python
for i in range(10):
    time.sleep(0.4)
```

Once done, let's add a progress bar for the loop. In order to do so, let's wrap the iterable with `tqdm` method.

```python
for i in tqdm(range(10)):
    time.sleep(0.4)
```

Let's have a look at the output. It will look something like this:

![ezgif.com-gif-maker.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1605924026724/2xM1w9uPi.gif)

If you wish to get rid of the iterable, you can do so by wrapping the iterable in `trange` module.

```
for i in trange(5):
    sleep(0.4)
```

This is how you can add a progress bar in your python script. That's it! 

Simple, isn't it? Hope this tutorial has helped. I would strongly recommend you to Check out the [YouTube video](https://www.youtube.com/watch?v=wbYqz71WVvI) of the same and **don't forget to subscribe my Channel**.

You can play around with the `tqdm` library and even explore more features. You can even make use of Python GUI using Tkinter.

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/create%20progress%20bar). **Drop a star** if you find it useful.

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

- https://pypi.org/project/tqdm/
- https://tqdm.github.io/
- https://github.com/tqdm/tqdm

See you in my next Blog article, Take care