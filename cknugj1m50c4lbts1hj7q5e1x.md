## Internet Speed Test using Python

Hello there,
I am attending a [Technical Writing Bootcamp](https://hashnode.com/bootcamp/batch-3) at [@hashnode](https://hashnode.com/@hashnode). **Hashnode Bootcamp III** is a free virtual Bootcamp to help beginner technical writers to improve their writing skill. This article is inspired by the latest session by **Sam Julien**, @samjulien

TASK: *Write 1 TIL format blog post on Hashnode to test out your own content system from drafting all the way to promoting.*

Running a speed test can be very useful to verify the current state of an internet connection. In this Blog article, we will learn how to **Test Internet Speed.** We will see the implementation in Python.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

*Let's get started.*

## What will be covered in this Blog

```python
1. speedtest Introduction
2. How to Test internet speed
```

# Speedtest Introduction:

The internet connections in our homes and offices can differ by internet service providers (ISPs), allowable traffic limit, and most importantly speed. So what do you usually do when you want to test the speed our connection? You google it, right? How about testing the internet speed using Python from your machine! 

Speedtest cli library provides Command line interface for testing internet bandwidth using speedtest.net

If you wish to know more about it, you can refer to [Speedtest Documentation](https://pypi.org/project/speedtest-cli/). Use this link to navigate to the documentation.

Now that you are aware of Speedtest basics, we can move forward to the coding section. Let's get started!

## Time to Code!

![code.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1605667262526/U5OIvfOnm.png)

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Test%20Internet%20Speed). **Drop a star** if you find it useful.



In order to access the Python library, you need to install it into your Python environment, use the following command to install `Speedtest `  

```python
pip install speedtest-cli
```

Now, let's import the package in our Python script.

```python
import speedtest
```

Let's create an instance of `Speedtest` and call it `st`

```python
st = speedtest.Speedtest() 
```

Let's move forward and check for download speed. We will make use of `download` method to fetch the speed and store in `d_st`

```python
d_st = st.download()
```

Similarly, to check for the upload speed, we will make use of `upload` method to fetch the speed and store in `u_st`

```python
u_st = st.upload()
```

Once done, let's display the download and upload speed. 

```python
print("Your Download speed is", d_st) 
print("Your Upload speed is", u_st) 
```

Let's have a look at the output:

```
Your Download speed is 4786516.020362539
Your Upload speed is 851493.59380959
```

It will look something like this. Here's the download and upload speed in bits.

#### BONUS:

Let's check for ping. We can do so by making use of the following command.

```python
st.get_servers([])
```

Let's  fetch the ping and store it in `ping`, we will make use of `results.ping` for the same.

```
ping = st.results.ping

#display the result
print("Your Ping is", ping)
```

Let's display the `ping` using `print`. 

```
Your Ping is 50.846
```

This is how you can test your Internet speed. That's it! 

Simple, isn't it? Hope this tutorial has helped.You can play around with the Speedtest library and even explore more features. You can even make use of Python GUI using Tkinter.

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Test%20Internet%20Speed). **Drop a star** if you find it useful.

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

- https://pypi.org/project/speedtest-cli/
- https://github.com/sivel/speedtest-cli
- https://www.mankier.com/1/speedtest-cli

See you in my next Blog article, Take care