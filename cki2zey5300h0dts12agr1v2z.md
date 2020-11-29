## Create a Random Password Generator using Python

Hello world!

We all make use of passwords on a daily basis, to keep your account safe and prevent your password from being hacked we have to make our password is hard enough that nobody can guess.

Password generator is a Random Password generating program which generates a password mix of upper and lowercase letters, as well as numbers and symbols strong enough to provides great security.

In this Blog article, we will learn how to **Create a Random Password Generator.** We will see the implementation in Python.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my **YouTube video Tutorial** to see a working tutorial for better Understanding and a step by step Guide of the same. 

%[https://www.youtube.com/watch?v=AjiGVu2xbx8]

## What will be covered in this Blog

```python
1. What is Password
2. Random and String Module
3. how to Create a Random Password Generator
```

Let's get started!

## What is Password:

A password, sometimes called a passcode, is a memorized secret, typically a string of characters, usually used to confirm the identity of a user, In other words is a string of characters used to verify the identity of a user during the authentication process.

If you wish to know more about it, you can refer to [Password Wikipedia Page](https://en.wikipedia.org/wiki/Password). 

## Modules Used: 

### Random Module:

Random module is used to perform the random generations. We are making use of `random.sample` module here. If you will observe in the output all characters will be unique. `random.sample()` never repeats characters. If you don’t want to repeat characters or digits in the random string, then use `random.sample()` but it is less secure because it will reduce the probability of combinations because we are not allowing repetitive letters and digits.

### String Module:

The [string module](https://www.pythonforbeginners.com/basics/strings) contains a number of useful constants, classes and a number of functions to process the standard python string.

1. **`string.ascii_letters`**: Concatenation of the ascii (upper and lowercase) letters
2. **`string.ascii_lowercase`**: All lower case letters
3. **`string.ascii_uppercase`**: All Upper case letters
4. **`string.digits`**: The string ‘0123456789’.
5. **`string.punctuation`**: String of ASCII characters which are considered punctuation characters in the C
   locale.

Now that you are familiar with password use cases and have acquired basic knowledge of `random` and `string` module, we can move forward to the coding section. 

## Time to Code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Random%20Password%20Generator). **Drop a star** if you find it useful.


![code.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1606623119249/Tf3BrIIEw.png)

In order to access the Python library, we need to import the package in our Python script.

```python
import random
import string
```

Once done, let's greet the user!

```python
print('hello, Welcome to Password generator!')
```

Next, let's ask the user for the length of the password.

```python
length = int(input('\nEnter the length of password: '))                      
```

Its time to define the data. We will make use of `string` module for the same.

````python
lower = string.ascii_lowercase
upper = string.ascii_uppercase
num = string.digits
symbols = string.punctuation
````

We have stored lowercase and uppercase letters along with numbers and symbols. Let's combine the data and store the data.

```python
all = lower + upper + num + symbols
```

Now that we have the data, let's make use of `random` module to finally generate the password.

```python
temp = random.sample(all,length)

password = "".join(temp)
```

We are passing in the the combined data along with the length of password, and joining them at the end.

Now that you have a clear understanding of the script, we can even reduce the number of lines of code by eliminating the storage of data. Let's have a look.

```python
all = string.ascii_letters + string.digits + string.punctuation
pass = "".join(random.sample(all,length))
```

Finally, let's print the password!

```python
print(password)
```

Let's have look at few sample outputs:

```
#SAMPLE O/P: (length = 16)

3Atza*qP#h-vJoK+
7c%A4gOt#M[}qr2
@JmFf"awbQ1Ts4dx
```


With these steps, we have successfully created a random password generator project using python. That's it! 

Simple, isn't it? Hope this tutorial has helped. I would strongly recommend you to Check out the [YouTube video](https://www.youtube.com/watch?v=AjiGVu2xbx8) of the same and **don't forget to subscribe my Channel**.

You can play around with the Instaloader library and even explore more features. You can even make use of Python GUI using Tkinter.

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Random%20Password%20Generator). **Drop a star** if you find it useful.

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

- https://en.wikipedia.org/wiki/Password

See you in my next Blog article, Take care!!