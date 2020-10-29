## Create URL Shortner with Python

In this Blog article, we will learn how to **Create a URL Shortner**. URL shortening is the process of reducing the length of the URL. There are many messaging platforms where the length of the message is limited.  Here, anyone can face the issue in sharing the long URLs, so that it can be shared easily on platforms like Twitter, where number of characters is an issue. There are so many URL Shorteners available in the market today, We will implementation it in **Python**.

[Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my YouTube video tutorial for better Understanding

%[https://www.youtube.com/watch?v=PDdSsex3M3E]

## What will be covered in this Blog

```
1. URL Introduction
2. What is Pyshorteners?
3. Creating a URL Shortner
```

## URL Introduction:

The Dictionary defination: 

>  A **URL** is a reference to a [web resource](https://en.wikipedia.org/wiki/Web_resource) that specifies its location on a [computer network](https://en.wikipedia.org/wiki/Computer_network) and a mechanism for retrieving it.

A **URL** stands for **Uniform Resource Locator**. 

 An **example** of a **URL** is https://www.youtube.com/ayushirawat which is the **URL** for my **YouTube channel.** 

URL Breakdown: URL = Protocol + Domain + path (simplest breakdown, it can be divided further!)

A basic URL breakdown of my blog will look like this.


![Screenshot_13.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1603852869288/1wmsDI1U9.png)


If you wish to know more about it, you can refer to [URL Wikipedia Page](https://en.wikipedia.org/wiki/URL). Use this link to navigate to the URL's Wikipedia Page.

## What is Pyshorteners?

pyshorteners is a Python lib to help you short and expand urls using the most famous URL Shorteners availables. With the help of pyshorteners , you can generate a short url or expand another one which is as easy as typing. This is basically a library in Python that provides implementation of few popular URL Shorteners.

If you wish to know more about it, you can refer to [Pyshorteners Documentation](https://pyshorteners.readthedocs.io/en/latest/). Use this link to navigate to the documentation.

Now that you are aware of URL and Pyshorteners basics, we can move forward to the coding section. 

## Time to code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/GIF%20Converter). **Drop a star** if you find it useful.


![carbon (5).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1603852844364/v2b4xiH6D.png)

### Installing Pyshorteners

Open your terminal and run the following command

```python
pip install pyshorteners
```

Now that we have the package, we are ready to import it in our python script.

```python
import pyshorteners as sh
```

Now, lets store the URL that we will use for URL shortening. 

```python
link = 'https://www.youtube.com/ayushirawat/videos'
```

I am storing my [YouTube channel URL](https://www.youtube.com/ayushirawat) in `link`. You can even take the URL as a user input if you like, so you wont have to make changes in your program everytime you wish to shorten a URL.

```python
s = sh.Shortener()
```

Now, let's call `Shortener` method and store it.

```python
print(s.tinyurl.short(link))
```

Now, I am calling `tinyurl.short` on `s` and passing the URL stored in `link`. Finally lets `print` our result.

```python
https://tinyurl.com/y533jl6f
```

and here is our shortened URL. 

This is all about Creating a URL Shortner. That's it! simple, isn't it? Hope this tutorial has helped.

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/GIF%20Converter). **Drop a star** if you find it useful.

Thank you for reading, I would love to connect with you at [Twitter](https://twitter.com/ayushi7rawat).

Do share your valuable feedback and suggestions! 

You should definitely check out my other Blogs:

- [Python 3.9: All You need to know](https://ayushirawat.com/python-39-all-you-need-to-know)
- [The Ultimate Python Resource hub](https://ayushirawat.com/the-ultimate-python-resource-hub)
- [GitHub CLI 1.0: All you need to know](https://ayushirawat.com/github-cli-10-all-you-need-to-know)
- [Become a Better Programmer](https://ayushirawat.com/become-a-better-programmer)
- [How to make your own Google Chrome Extension](https://ayushirawat.com/how-to-make-your-own-google-chrome-extension-1)
- [Create your own Audiobook from any pdf with Python](https://ayushirawat.com/create-your-own-audiobook-from-any-pdf-with-python)
- [You are Important & so is your Mental Health!](https://ayushirawat.com/you-are-important-and-so-is-your-mental-health)

## Resources:

- https://en.wikipedia.org/wiki/URL
- https://pyshorteners.readthedocs.io/en/latest/

See you in my next Blog article, Take car
