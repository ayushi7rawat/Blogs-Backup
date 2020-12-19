## Automate WhatsApp using Python

Hello world!

In this Blog article, we will learn how to **Automate WhatsApp.** We will make use of web.whatsapp.com webpage to automate messages and we will see the implementation in Python.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my **YouTube video Tutorial** to see a working tutorial for better Understanding and a step by step Guide of the same. 

%[https://www.youtube.com/watch?v=muBeg5NE5MQ]

## What will be covered in this Blog

```python
1. What is WhatsApp?
3. Basics of pywhatkit Module
4. Automate WhatsApp using Python
```

*Let's get started!*

## What is **WhatsApp**?:

I do not think **WhatsApp** needs an introduction but for those who do now know, **WhatsApp** is a free, multiplatform messaging app that lets you make video and voice calls, send text messages, and more — all with just a Wi-Fi connection.

If you wish to know more about it, you can refer to [**WhatsApp** Wikipedia Page](https://en.wikipedia.org/wiki/WhatsApp). 

## Module Used:

### pywhatkit Module:

[PyWhatKit](https://pypi.org/project/pywhatkit/) is a Python library with various helpful features. It is an easy to use library which does not requires you to do some additional setup. 

This module has lots of other cool features as well. Feel free and go ahead to explore them or if you wish I can write an article about them.

If you wish to know more about it, you can refer to [**pywhatkit Module** Documentation](https://github.com/Ankit404butfound/PyWhatKit). 

### getpass Module:
getpass() prompts the user for a password without echoing. The `getpass` module provides a secure way to handle the password prompts where programs interact with the users via the terminal.

Now that you are familiar with *WhatsApp* and have acquired basic knowledge of *pywhatkit and getpass module,* we can move forward to *the coding section.*

## Time to Code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Currency%20Converter). **Drop a star** if you find it useful.

![code.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1608263115462/DrYkCYICb.png)

In order to access the Python library, you need to install it into your Python environment

```python
pip install pywhatkit
```

Now, we need to import the package in our python script. Use the following command to do so.

```python
import pywhatkit as kt
```

Now that we have imported the library using the command `import pywhatkit as kt`, let's proceed and automate whatsapp.

Before we move forward make sure you have an active session or previously used web.whatsapp.com webpage in your browser. 

![Screenshot_3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1608263157943/sMRVoUUx9.png)

We will make use of `sendwhatmsg` method for the same. Let's understand the parameters to be used:

- **phone_num**: A mandatory parameter
  - Phone number of target with proper country code

- **message**: A mandatory parameter.  
  - The message that you want to send.
- **time_hour**: A mandatory parameter.  
  - Hours at which you want to send message in 24 hour format
- **time_min**: A mandatory parameter. 
  - Minutes at which you want to send message
- **wait_time**: An optional parameter. 
  - The `default value = 20` i.e. post 20 Seconds the message will be sent after opening the web
- **print_waitTime**: An optional parameter. 
  - The `default value = True`  i.e. will print the remaining time if set to true.

Let's display a welcome message and let's capture the target phone number here.

```python
print("Let's Automate Whatsapp!")
p_num = 'the taget phone number goes here!'

#or you can use getpass module to capture cell num
import getpass as gp
p_num = gp.getpass(prompt='Phoneumber: ', stream=None)
```

Let's capture the message. I am storing it in `msg`.

```python
msg = "I love Python"
```

Finally, let's call `sendwhatmsg` method. 

```python
kt.sendwhatmsg(p_num, msg, 10, 25)
```

NOTE: This module follows the **24 hrs time format**.

```
OUTPUT:
In 360 seconds web.whatsapp.com will open and after 60 seconds message will be delivered.
```

![Screenshot_4.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1608263177371/fVXPbqaBk.png)
Also, you should try and provide atleast 4-5 minutes future time from the current time when running the script otherwise if you set the time 1-2 minute prior current time, then the module might give error.

![Screenshot_5.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1608263192658/SX35PNXPW.png)
Post successful run, the WhatsApp web will open and the message will be sent to the targeted mobile number. You can use this script to automate WhatsApp to send Birthday or Anniversary greetings to your friends and family, send daily morning message to your parents or use it for other business idea. You can send bulk messages or you can easily create a list of phone number and message on which you can add a ‘For loop’. 

Now that you have understood it all, you can write the same in 2 lines of code.

![code2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1608263251084/njaNcwKnV.png)

With these steps, we have successfully **Automate WhatsApp using python.** That's it! 

Simple, isn't it? Hope this tutorial has helped. I would strongly recommend you to Check out the [YouTube video](https://www.youtube.com/watch?v=ixB2YHGSiAQ) of the same and **don't forget to subscribe my Channel**.

You can play around with the `pywhatkit` library and even explore more features. 

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Currency%20Converter). **Drop a star** if you find it useful.

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

- https://en.wikipedia.org/wiki/WhatsApp
- https://chromedriver.chromium.org/getting-started
- https://chromedriver.chromium.org/
- https://pypi.org/project/pywhatkit/
- https://github.com/Ankit404butfound/PyWhatKit

See you in my next Blog article, Take care!