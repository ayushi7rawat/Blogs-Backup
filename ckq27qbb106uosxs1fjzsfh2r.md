## Build a Break Scheduler using Python

Hello reader! 

**Working from home is the new normal**. and It is a must to ensure a healthy work-life balance. You cannot just grab a laptop and keep working all day long, it will affect your health drastically.

Schedule your breaks, by far the way out. It works out well for me. In this blog post, we will learn how to build a **breaks Scheduler.** We will see the implementation in **Python**.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

%[https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub]

You can refer to my **YouTube video Tutorial** to see a working tutorial for better understanding and a step-by-step guide of the same. 

%[https://www.youtube.com/watch?v=qF8QG7Fr1Vk]

## What will be covered in this Blog

```python
1.	Why breaks are important & how to Utilize them?
2.	What is webbrowser Module
3.	How to build a simple breaks Scheduler using Python.
```

*Let's get started!*

## Why breaks are important & how to Utilize them?

Working from home can be a tiring desk job. You need to take care of your mental health. Well you can schedule your breaks to

- Take small five minutes break every hour

- Drink water frequently.

- Stretch your muscles.

- Prepare Tea/Coffee or any healthy drink and take a small walk for few minutes.

- When you receive a non-work call, again do a little walk and talk.

  How do you Utilize and plan your breaks?

## Module Used:

### webbrowser Module:

The [`webbrowser`](https://docs.python.org/3/library/webbrowser.html#module-webbrowser) module provides a high-level interface to allow displaying Web-based documents to users. Under most circumstances, simply calling the `open()` function from this module will do the right thing. The script **webbrowser** can be used as a command-line interface for the module. It accepts a URL as the argument. 

If you wish to know more about it, you can refer to [**webbrowser Module** Documentation](https://docs.python.org/3/library/webbrowser.html#module-webbrowser).

Now that you are familiar with *Why breaks are important & how to Utilize them?* and have acquired basic knowledge of *webbrowser  module,* we can move forward to *the coding section.*

## Time to Code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Break%20Scheduler). **Drop a star** if you find it useful.

![carbon.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1624018042376/imPMoj2F9.png)
In order to access the Python library, we need to import the package into our python script. Use the following command to do so.

```python
import time 
import webbrowser
	
from random import choice
```

Now that we have imported the library using the command `import requests`, let's proceed.

Let's display a welcome message.

```python
print("Initiating the Break Scheduler!")
```

Let's ask the user to input the number of breaks he wishes to take or since you are running the script for yourself, you can also hardcode the value.

```python
breaks = input('input the number of times you wish to take break today! ')
print(breaks)

#breaks = 2
```

Now, you can set the break interval according to your need. I am setting the break interval as every hour for now.

```python
gap = 60*60
```

Initially let's set the counter as zero

```python
counter = 0
```

Now, let's define the URL, you wish to open in the interval

```python
url = "https://www.youtube.com/c/AyushiRawat"
```

Let's make use of `random` module to display a random message at every break interval. Let's store the messages to be displayed in `messages` for the same.

```python
messages = ["Time for a break!", "Let's take a break!"]
```

Our resultant data is stored in `res`. We will make use of the `text` method to extract our desired weather details and let's display the result.

Now, let's run a while loop until the counter becomes equal to the number of desired breaks.

```python
while(counter < breaks):
    time.sleep(gap)

    #Let's print the break message
    print(choice(messages))

    #opening the browser window.
    webbrowser.open(url)
```

We will introduce `sleep` here to schedule the breaks. A random message will be displayed on the screen and the URL will open automatically at every interval.

At last, let's increase the counter by one.

```python
counter += 1
```

And finally, let's display the termination message when the scripts end.

```python
print("Terminating the Break Scheduler!")
```

That's it. That all we have to do to build a simple break scheduler. And with that, it's a wrap!  I hope you found the article useful! Share in the comments below.

I create content about **Career, Blogging, Programming, and Productivity**, If this is something that interests you, please share the article with your friends and connections. You can also subscribe to my newsletter to get updates every time I write something!

Thank you for reading, If you have reached so far, please like the article, It will encourage me to write more such articles. Do share your valuable suggestions, I appreciate your honest feedback!

I would strongly recommend you to Check out the [YouTube video](https://www.youtube.com/watch?v=jAOkWehMF6E) of the same and **don't forget to subscribe to my Channel**. I would love to connect with you at [Twitter](https://twitter.com/ayushi7rawat) | [LinkedIn](https://www.linkedin.com/in/ayushi7rawat/).

You should definitely check out my other Blogs:

- [Python 3.9: All You need to know](https://ayushirawat.com/python-39-all-you-need-to-know)
- [GitHub CLI 1.0: All you need to know](https://ayushirawat.com/github-cli-10-all-you-need-to-know)
- [How to make your own Google Chrome Extension](https://ayushirawat.com/how-to-make-your-own-google-chrome-extension-1)
- [Run Javascript from Python](https://ayushirawat.com/run-javascript-from-python)
- [Automate WhatsApp using Python](https://ayushirawat.com/automate-whatsapp-using-python)
- [Automate Cowin Vaccine slots Availability using Python](https://ayushirawat.com/automate-cowin-vaccine-slots-availablity-using-python)
- [What is Competitive Programming](https://ayushirawat.com/what-is-competitive-programming-or-beginners-guide)

#### Resources:

- https://docs.python.org/3/library/webbrowser.html

See you in my next Blog article, Take care!!