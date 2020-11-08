## Jokes Generator with python

In this Blog article, we will learn how to **Create Jokes Generator with Python.** We will see the implementation in **python**.

[Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my YouTube video tutorial for better Understanding

%[https://www.youtube.com/watch?v=nFfItgJnX6M]

## What will be covered in this Blog

```python
1. Pyjokes Introduction
2. Generating jokes with Pyjokes
```

## Pyjokes Introduction:

Pyjokes is a python library  for one line jokes for programmers (jokes as a service). You can get funny one-liner, mostly related to **programming**. This is a fun python library. It returns a random joke from the given category in the given language.

### Supported Languages By Pyjokes

- English – ‘en’ 
- Spanish – ‘es’ 
- Italian – ‘it’ 
- German – ‘de’ 
- Galician – ‘gl’ 
- Basque – ‘eu’ 

### Categories Included In Pyjokes

- For geeky jokes -’neutral’ (It is chosen by default) 
- For Chris Norris Jokes – ‘chuck’. 
- If you want all type of jokes – ‘all’ 
- There is one more category known as ‘twister’ which only works for the German Language (‘de’) and mostly includes **tongue twister.**

If you wish to know more about it, you can refer to [Pyjokes Documentation](https://pyjok.es/). Use this link to navigate to the documentation.

Now that you are aware of Pyjokes basics, we can move forward to the coding section. 

## Time to Code!

In order to access the Python library, you need to install it into your Python environment, use the following command to install `pyjokes`  

![code.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1604803567735/81y2d_3Mp.png)
```
pip install pyjokes
```

Now, let's import the package in our python script.

```python
import pyjokes
```

There are two methods in pyjokes-

- **get_joke() **
- **get_jokes()**

#### **1. get_joke() **

It only returns one joke at a time. It is generated randomly. 

**Parameters** – It has two parameters- *language and category*.  

**Return Type** – *It returns string type (str).* 

Now, let's retrieve the joke

```python
joke1 = pyjokes.get_joke(language='en', category= 'all')  

#display the joke
print(joke1)

#output:
#A programmer was found dead in the shower. Next to their body was a bottle of shampoo with the instructions 'Lather, Rinse and Repeat'.
```

Let's try a different category:

```python
joke2 = pyjokes.get_joke(language='en', category= 'neutral')

#display the joke
print(joke2)

#output:
#There are 10 types of people: those who understand trinary, those who don't, and those who have never heard of it.
```

#### **2. get_jokes() **

It returns a list of jokes. 

**Parameter**– The parameters are the same as above- language and category. 

**Return type**– **It returns a list.* 

Now let's fetch some jokes. 

```python
jokes = pyjokes.get_jokes(language='en', category= 'neutral')

for i in range(5):
    print(i+1,".",jokes[i])
```

And you will get a list of jokes. You can alter the number the times the loop runs to fetch more number of jokes.

This is how you generate jokes. This is all about the **generating jokes with Python**. That's it! simple, isn't it? Hope this tutorial has helped.

You can play around with the library and explore more features and even make use of Python GUI using Tkinter.

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Build%20a%20translater). **Drop a star** if you find it useful.

Thank you for reading, I would love to connect with you at [Twitter](https://twitter.com/ayushi7rawat) | [LinkedIn](). I would recommend you to Check out the [YouTube video](https://www.youtube.com/watch?v=nFfItgJnX6M) of the same and **don't forget to subscribe my Channel**.

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

- https://pyjok.es/
- https://github.com/pyjokes/pyjokes
- https://pypi.org/project/pyjokes/

See you in my next Blog article, Take care