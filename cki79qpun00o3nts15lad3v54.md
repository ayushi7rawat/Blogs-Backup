## Automate Notion with Python

Hello world!

Have you heard about Notion? Do you use Notion? 

[Notion](https://www.notion.so/) is a super-clean and deceptively minimalist note-taking app. I am still learning how to use Notion because I have recently started using it, and If you are a regular reader you must know by now, I am big Python fan. So I was exploring how to use Notion a week earlier and it it hit me, is there a way I can automate it with Python. So in this Blog article, we will learn how to **Automate Notion.** We will see the implementation in Python.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my **YouTube video Tutorial** to see a working tutorial for better Understanding and a step by step Guide of the same. 

%[https://www.youtube.com/watch?v=6sJFI8LbhpY]

## What will be covered in this Blog

```python
1. What is Notion?
2. Modules Used
2. How to Automate Notion Using Python
```

*Let's get started!*

## What is Notion?:

The Dictionary Definition:

> Notion is an application that provides components such as databases, kanban boards, wikis, calendars and reminders. Users can connect these components to create their own systems for knowledge management, note taking, data management, project management, among others.

A new tool that blends your everyday work apps into one. It's the all-in-one workspace for you and your team. If you wish to know more about it, you can refer to:

- [**Notion's** Wikipedia Page](https://en.wikipedia.org/wiki/ZIP_(file_format). 
- [Notion's About Page](https://www.notion.so/about)

## Module Used:

### Notion Module:

`Notion ` module is Unofficial Python API client for Notion.so. It also works for both free and as well as paid accounts.

#### Let's look at some of its Features:

- **It has Object-oriented interface** (mapping database tables to Python classes/attributes)
- **Automatic conversion** between internal Notion formats and appropriate Python objects.
- **Callback system** for responding to changes in Notion(e.g. for triggering actions, updating another API, etc)
- **Local cache of data in a unified data store** *(Note: disk cache now disabled by default; to enable, add `enable_caching=True` when initializing `NotionClient`)*

If you wish to know more about it, you can refer to [**Notion Module** Documentation](https://notion-py.readthedocs.io/en/latest/py-modindex.html). 

Now that you are familiar with ***Notion use cases*** and have acquired basic knowledge of ***Notion module*** we can move forward to *the coding section.*

## Time to Code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Automate%20Notion). **Drop a star** if you find it useful.

![carbon (1).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1606904906385/Ap9mn6XxS.png)

In order to access the Python library, you need to install it into your Python environment, use the following command to install `Notion` 

```python
pip install notion
```

I will make use of Habit Tracker template. We will prepare a script that will add a new row at the end with proper formatted date.

![Screenshot_1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1606797457013/dkBjt41ir.png)

Once you open Notion, you can spot Templates in the Navigation left Side bar. 

![Screenshot_2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1606797475240/CxQ1mPjZ6.png)

If you open it, a new pop window will open, expand the Personal Tab.

![Screenshot_3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1606797484597/Tv4snkEpv.png)

Once you expand the Personal Tab, you will be able to spot the Habit Tracker Template. Post successful selection, hit Use this template. 

![Screenshot_4.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1606797503909/TPg4FPGTp.png)

If the template appears in your Left Navigation bar, you have successful imported it in your Notion.

Now, we need to import the package in out python script. Use the following command to do so.

```python
from notion.client import NotionClient
```

Next, we require the authentication token. For this, open Notion in your browser. Post successful login, open DevTools.

![Screenshot_5.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1606797557358/6uooOjuWx.png)

To open DevTools, hit Right click and select Inspect. You can also use the shortcut (Ctrl + Shift + I ) for Windows. 

![Screenshot_6.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1606797568007/_SHuxb6ie.png)
Next,

- navigate to Applications Tab 
- Go to Storage section in the Left menu
- Expand Cookies
- Search for row with Name`token_v2`
- Copy `token_v2`'s value and save it someplace safe.

![Screenshot_7.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1606797578631/mvlRxgYOZ.png)

Close the DevTools window. Next, Copy the Tracker URL and store it with you for now. 

```python
token = 'your token goes here'

client = NotionClient(token_v2=token)
```

The value that you copied for `token_v2` is reffered to as `token` here. 

```
tracker_url = 'Your collection url goes here'

collection_view = client.get_collection_view(tracker_url)
```

The Habit Tracker’s URL is reffered to as Collection URL here.

Once we have setup the connection, let's add a new row. We will make use of `add_row` method here.

```python
new_row = collection_view.collection.add_row()
```

Now let's populate values in the newly created row.

```python
new_row.running = True
new_row.Journaling = True
new_row.screen_time_minutes = 30
```

Save and Run the python script. You will observe a new row gets created and

- Running checkbox is enabled.
- Journaling checkbox is enabled.
- screen_time_minutes value is set to 30 mins

It will look something like this:

![Screenshot_8.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1606797599693/b3lODcVrX.png)

At last, let's automate our script by formatting the date of the new entry in Habit Tracker.

```python
from datetime import datetime

today = datetime.today()
new_row.title = today.strftime('%d.%m.%Y')
```

With these steps, we have successfully **Created an easy bot to automate a workflow in Notion using Python.** That's it! 

Simple, isn't it? Hope this tutorial has helped. I would strongly recommend you to Check out the [YouTube video](https://www.youtube.com/watch?v=6sJFI8LbhpY) of the same and **don't forget to subscribe my Channel**.

You can play around with the Notion library and even explore more features. Tag me on [Twitter](https://twitter.com/ayushi7rawat) when you do so.

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Automate%20Notion). **Drop a star** if you find it useful.

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

- https://notion-py.readthedocs.io/en/latest/py-modindex.html
- https://pypi.org/project/notion/
- https://github.com/jamalex/notion-py
- https://en.wikipedia.org/wiki/Notion_(app)
- https://www.notion.so/

See you in my next Blog article, Take care!!


