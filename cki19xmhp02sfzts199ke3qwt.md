## Download Display Picture of an Instagram Account Using Python

Hello world!

I am attending a [Technical Writing Bootcamp](https://hashnode.com/bootcamp/batch-2) at [@hashnode](https://hashnode.com/@hashnode). **Hashnode Bootcamp II** is a free virtual Bootcamp to help beginner technical writers to improve their writing skill. This article is inspired by the latest session by **Anna McDougall**, [@AnnaJMcDougall]

**TASK:** *In 7 days, write a blog post from one of the topics you learned during the session* 

In this Blog article, I will share my thoughts on the same. Let's get started.

Have you heard about Instagram? Do you Use Instagram? Well, In this Blog article, we will learn how to **Download Display Picture of an Instagram Account.** We will see the implementation in Python.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my **YouTube video Tutorial** to see a working tutorial for better Understanding and a step by step Guide of the same. 

%[https://www.youtube.com/watch?v=7C-6pCsw8gM]

## What will be covered in this Blog

```python
1. Instagram Introduction
2. Instaloader Introduction
3. How to Download Display Picture of an Instagram Account
```

## Instagram Introduction:

I do not think Instagram needs an Introduction but for those who do not know, Instagram is an photo and video sharing social networking platform owned by Facebook. If you wish to know more about Instagram, you can refer [its Wikipedia page](https://en.wikipedia.org/wiki/Instagram).

Instagram Link: https://www.instagram.com/

## `Instaloader` Introduction:

The *Instaloader* module is python package having great functionalities to scrap instagram, it’s functions can be used as command line utility. It can be used for download pictures (or videos) along with their captions and other metadata from Instagram.

### Key Features of Instaloader:

- downloads **public and private profiles, hashtags, user stories, feeds and saved media**,
- downloads **comments, geotags and captions** of each post,
- automatically **detects profile name changes** and renames the target directory accordingly,
- allows **fine-grained customization** of filters and where to store downloaded media,
- automatically **resumes previously-interrupted** download iterations.

If you wish to know more about it, you can refer to [Instaloader Documentation](https://instaloader.github.io/). Use this link to navigate to the documentation.

Now that you are aware of Instaloader basics, we can move forward to the coding section. Let's get started!

## Time to Code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Download%20Insta%20DP). **Drop a star** if you find it useful.

![code.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1606534182811/nq-lIyuEG.png)

In order to access the Python library, you need to install it into your Python environment, use the following command to install Instaloader 

```python
pip install instaloader 
```

Now, let's import the package in our Python script and create an instance `test` 

```python
import instaloader

test = instaloader.Instaloader()
```

Once done, let's take user input to get the username of the account you wish to download the profile picture ! I am storing it in `acc`

```python
acc = input('Enter the Account Username: ')

#acc = 'leomessi'
```

So here, Assuming you all must have heard the name of [Lionel Messi](https://en.wikipedia.org/wiki/Lionel_Messi), we have entered the account username as `leomessi`.

Finally, its time to download the data. 

We will make use of `download_profile` method here and pass in two parameters:

- `acc`: the username 
- `profile_pic_only`: we will set this to be `True`.

```python
test.download_profile(acc, profile_pic_only = True) 
```

A new folder will be created with the account username, in our case, `leomessi` and it will contain the Display Picture.

![2018-10-23_13-55-58_UTC_profile_pic.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1606534125170/CnxuuyFtq.jpeg)

Let's have a look at the output. It will look something like this:

![ezgif.com-gif-maker.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1606534123685/BbUo1vcaF.gif)


This is how you can Download Display Picture of an Instagram Account using python script. That's it! 

Simple, isn't it? Hope this tutorial has helped. I would strongly recommend you to Check out the [YouTube video](https://www.youtube.com/watch?v=7C-6pCsw8gM) of the same and **don't forget to subscribe my Channel**.

You can play around with the Instaloader library and even explore more features. You can even make use of Python GUI using Tkinter.

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Download%20Insta%20DP). **Drop a star** if you find it useful.

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

- https://pypi.org/project/instaloader/	
- https://instaloader.github.io/
- https://github.com/instaloader/instaloader

See you in my next Blog article, Take care!!