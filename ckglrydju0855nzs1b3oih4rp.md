## Create Desktop Notifier using Python

In this Blog article, we will learn **how to send Desktop notifications** . We will see the implementation in **Python**. 

[Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my YouTube video tutorial for better Understanding

%[https://youtu.be/5w37EAV4IKY]

## What will be covered in this Blog

```
1. Desktop Notification Introduction
2. What is Plyer?
3. Create a Desktop Notifier
```

## Desktop Notification:

Dictionary defination:

> the action of notifying someone or something.

The Purpose:

> The **purpose** behind a **notification** is to inform about an event and encourage him to take action.

Notifications help people to remember things. It is a small piece of text which appears on the desktop or mobile screen to inform the user about the updates or any other important pieces of information. 

## What is Plyer?

Plyer is a Python library for accessing features of your hardware / platforms.

If you wish to know more about it, you can refer to [Plyer Documentation](https://plyer.readthedocs.io/en/latest/). Use this link to navigate to the documentation.

## **Other areas where you can use this approach**

1. Set daily tracker for COVID stats
2. Daily notification to take medicine.
3. Hourly notification to drink water.

and many more, it’s completely up to you how to use this application. 

Now that you are aware of Desktop Notification and Plyer basics, we can move forward to the coding section. 

## Time to code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Desktop%20Notifier). **Drop a star** if you find it useful.

![code.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1603422010537/3Kx2WWf79.png)

### Installing Plyer

Open your terminal and run the following command

```python
pip install plyer
```

Now that we have the package, we are ready to import it in our python script.

```python
from plyer import notification
```

Now let's specify the parameters. Lets define the `title` and `message`.

```python
title = 'Hello Amazing people!'

message= 'Thankyou for reading! Take care!'
```

Let's look at what the parameters mean:

- `title`: Title of the notification
- `message`: Message of the notification
- `app_name`: Name of the app launching this notification
- `app_icon`: Icon to be displayed along with the message
- `timeout`: time to display the message for, defaults to 10
- `ticker`: text to display on the status bar as the notification arrives
- `toast`: simple message instead of full notification

Now, let's pass the parameters using `notify` method.

```python
notification.notify(title= title,
                    message= message,
                    app_icon = None,
                    timeout= 10,
                    toast=False)
```

I am passing:

- the `title` as  `'Hello Amazing people!'``
- ``message` as `'Thankyou for reading! Take care!'`
- `app_icon` as `None`
- `timeout` as `10 secs`
- and `toast` as `False`.

That's it! We are done. Now let's save and run our python script. 

![Screenshot_9.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1603421991427/n9uSDe081.png)


Here is our desktop Notification. Simple, isn't it? Hope this tutorial has helped.

You can play around with the library, explore more features and even customize it further.

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Desktop%20Notifier). **Drop a star** if you find it useful.

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

- https://plyer.readthedocs.io/en/latest/
- https://github.com/kivy/plyer

See you in my next Blog article, Take care