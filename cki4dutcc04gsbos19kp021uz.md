## Find IP Address of any Website Using Python

Hello world!

IP address helps in connecting our computer to other devices on our network and all over the world. In this Blog article, we will learn how to **Find IP Address of any Website.** We will see the implementation in Python.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my **YouTube video Tutorial** to see a working tutorial for better Understanding and a step by step Guide of the same. 

%[https://www.youtube.com/watch?v=7C-6pCsw8gM]

## What will be covered in this Blog

```python
1. What is IP address?
2. Find IP Address of any Website
```

*Let's get started!*

## What is IP address?:

The Dictionary Defination:

> **IP address** stands for Internet Protocol address, is a numerical label assigned to each device connected to a [computer network](https://en.wikipedia.org/wiki/Computer_network) that uses the [Internet Protocol](https://en.wikipedia.org/wiki/Internet_Protocol) for communication. 

IP (Internet Protocol) Address is an address of your network hardware. An IP Address is made up of numbers or characters. All devices that are connected to an internet connection have a unique IP address

There are are two IP versions: 

- IPv4
- IPv6.

There are a few other types of IP addresses as well like private IP addresses, public IP addresses, static IP addresses and dynamic IP addresses. 

If you wish to know more about it, you can refer to [**IP address** Wikipedia Page](https://en.wikipedia.org/wiki/IP_address). 

Now that you are familiar with *IP address basics*, we can move forward to *the coding section.* 

## Time to Code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Find%20IP%20Address). **Drop a star** if you find it useful.


![code.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1606707335833/1qjgFbicG.png)

In order to access the Python library, we need to import the package in our Python script. 

```python
import socket as s
```

We will make use of `socket` module to get the IP Address of any Website. Now that we have imported it in our python script, let's start by fetching our hostname.

```python
my_hostname = s.gethostname()
```

We will make use of `gethostname` method from socket and store it in `my_hostname`. Let's display our hostname by using `print` method.

```python
print('Your Hostname is: ' + my_hostname)

#OUTPUT:
--> Your Hostname is: AyushiRawat
```

Its time to fetch the IP Address. We will make use of `gethostbyname` method for the same and pass in our hostname, `my_hostname`. Let's store it in `my_ip`

````python
my_ip = s.gethostbyname(my_hostname)
````

Once done, let's display the IP Address.

```python
print('Your Ip Address is: ' + my_ip)

#OUTPUT:
--> Your Ip Address is: 192.168.1.3
```

Now, let's fetch the IP Address of [**my blogging webiste**](https://ayushirawat.com/), `https://ayushirawat.com/`. We will store the hostname in `host`.

```python
host = 'ayushirawat.com'
```

Let's fetch the IP Address using the `gethostbyname` method and pass in `host`. 

```python
ip = s.gethostbyname(host)
```

Finally, let's display the IP Address of [**my blogging webiste**](https://ayushirawat.com/)!

```python
print('The IP Address of ' + host + ' is: '  + ip)

#OUTPUT:
--> The IP Address of ayushirawat.com is: 192.241.200.144
```


With these steps, you can successfully get the IP Address of any website using python. That's it! 

Simple, isn't it? Hope this tutorial has helped. I would strongly recommend you to Check out the [YouTube video](https://www.youtube.com/watch?v=7C-6pCsw8gM) of the same and **don't forget to subscribe my Channel**.

You can play around with the socket library and even explore more features. You can even make use of Python GUI using Tkinter.

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Find%20IP%20Address). **Drop a star** if you find it useful.

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

- https://docs.python.org/3/library/socket.html#socket

See you in my next Blog article, Take care!!