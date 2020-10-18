## Email Slicer with Python

In this Blog article, we will see how to slice any email into username and domain. We will see the implementation in python. 

You can refer to my YouTube video tutorial for better Understanding

%[https://www.youtube.com/watch?v=SrvqNAZ2Mh4]

[Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

## Introduction

The **email slicer ** is a quite handy program to get the username and domain name from an email address. You can play around and even customize it further and send a message to the user with this information.

We use make use of email in our day to day life, is one of the most widely used features of the Internet. Email short for **electronic mail** is a method of exchanging messages between people using electronic devices, along with the web. It allows you to send and receive messages to and from anyone with an email address, anywhere in the world.

## E-mail address breakdown:

![Screenshot_1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1602735793870/7bFJlGGaq.png)

- The first portion of all e-mail addresses, the part before the @ symbol, contains the alias, user, group, or department of a company. In our above example, **demoayushi** is the username.

- Next, the @ (at sign) is a divider in the e-mail address. It's required for all SMTP e-mail addresses since Ray Tomlinson sent the first message.

- Finally, gmail.com is the domain. 

Now that you are aware of the basics, its time to code!

## Let's get started!
You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Email%20Slicer). **Drop a star** if you find it useful.

![carbon (5).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1602736670920/nbAYZkEZP.png)

I am using my demo email address `demoayushi@gmail.com`. So first, let's input the user's email address.
```
# Get the user's email address
email = input("What is your email address?: ").strip()
```

I am using the `strip()` method to remove spaces at the beginning and at the end of the string if any. The email address is stored in `email`.

Next, we will slice out the username. It is similar to what do with string slicing.
```
# Slice out the user name
user_name = email[:email.index("@")]
```

I am storing the sliced username to `user_name`. Moving forward let's slice out the domain
```
# Slice out the domain name
domain_name = email[email.index("@")+1:]
```
I am storing the sliced domain to `domain_name. Now that we have the domain and username, let's format it.
```
# Format message
res = "Your username is '{}' and your domain name is '{}'".format(user_name,domain_name)
```
I am storing the formatted data into `res`. Once done, we can finally display our result.
```
# Display the result message
print(res)
```
 I am using the `print` method to do the same.
```
#the output
Your username is 'demoayushi' and your domain name is 'gmail.com'
```

That's it! simple, isn't it?

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Email%20Slicer). **Drop a star** if you find it useful.

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


See you in my next Blog article, Take care!