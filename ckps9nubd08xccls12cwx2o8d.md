## Forecast Weather using Python

Hello reader! 

**Weather** is the mix of events that happen each day in our atmosphere and is different in different parts of the world and changes over minutes, hours, days, and weeks. Rain and dull clouds, windy blue skies, cold snow, and sticky heat are very different conditions, yet they are all-weather. According to the Wikipedia definition:

> **Weather** is the state of the atmosphere. 

In this blog post, we will learn how to forecast weather details. We will see the implementation in Python with hardly a few lines of code.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

%[https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub]

You can refer to my **YouTube video Tutorial** to see a working tutorial for better understanding and a step-by-step guide of the same. 

%[https://www.youtube.com/watch?v=jAVVtOzQ5ww]

## What will be covered in this Blog

```python
1.	What is wttr?
2.	What is requests Module
3.	How to forecast the weather using Python
```

*Let's get started!*

## What is wttr?

> wttr — the right way to check the weather!

wttr.in is a console-oriented weather forecast service that supports various information representation methods like terminal-oriented ANSI-sequences for console HTTP clients (curl, httpie, or wget), HTML for web browsers, or PNG for graphical viewers.

wttr.in uses [wego](http://github.com/schachmat/wego) for visualization and various data sources for weather forecast information.

If you wish to know more about it, you can refer to [**wttr's** GitHub Repo](https://github.com/chubin/wttr.in).

## Module Used:

### requests Module:

**Requests** is a simple, yet elegant HTTP library. It allows you to send HTTP/1.1 requests extremely easily. Requests officially support Python 2.7 & 3.5+.

If you wish to know more about it, you can refer to [**Requests Module** Documentation](https://docs.python-requests.org/en/master/).

Now that you are familiar with *Requests Module* basics and have acquired basic knowledge of *wttr,* we can move forward to *the coding section.*

## Time to Code!
You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Weather%20Forecast). **Drop a star** if you find it useful.
![carbon (1).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1623385811809/P3sI8iBxw.png)
In order to access the Python library, you need to install it into your Python environment

```python
pip install requests
```

Now, we need to import the package into our python script. Use the following command to do so.

```python
import requests
```

Now that we have imported the library using the command `import requests`, let's proceed.

Let's ask the user to input the city name for which he/she wishes to fetch the weather details. 

```python
city = input('input the city name')
print(city)
```

You can also hard-code the value if you will only check for yourself.

```python
city = 'bhopal'
```

Now, let's display a simple message.

```python
print('Displaying Weather report for: ' + city)

#output:
Displaying Weather report for: bhopal
```

Let's define the URL, We will make use of `format` to pass city as a parameter here.

```python
url = 'https://wttr.in/{}'.format(city)
```

It's time to make use of the `requests` module.

```python
res = requests.get(url)
```

Our resultant data is stored in `res`. We will make use of the `text` method to extract our desired weather details and let's display the result.

```python
print(res.text)
```

This is how the Weather Forecast will look like:

![output.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1623385775384/Hf5_78w-f.png)

Isn't it beautiful? And with that, it's a wrap!  I hope you found the article useful! Share in the comments below.
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

- https://scied.ucar.edu/learning-zone/how-weather-works/weather
- https://en.wikipedia.org/wiki/Weather
- https://github.com/chubin/wttr.in
- https://pypi.org/project/requests/
- https://docs.python-requests.org/en/master/

See you in my next Blog article, Take care!!

