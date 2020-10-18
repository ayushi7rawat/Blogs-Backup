## How to make an Instagram Bot with Python

Do you use Instagram? 
Do you want to know how to build an Instagram Bot?

This tutorial will teach you how to automate Instagram activities with the help of an Instagram bot.
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/47hqhlejs2u3q196q0zf.png)
*Let's get started!*

[Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

## **Prerequisites for making one (Bot)**
```
- Python
- Instapy module in Python
- An Instagram account, which you will use to run the bot script.
```
That's it. Now let's dive straight into the code.

## **Time To Code!**
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/mo5hnxro9pod2xknybeh.png)
 
## **Now let's Understand the code.**

### **Installation of instapy**
```
pip install Instapy 
```
**Important:**  *Depending on your system, make sure to use pip3 and python3 instead.*

If you would like to install a specific version of Instapy you may do so with:

```
pip install instapy==0.1.1
```

### **Set the login credentials**

You can put in your account details now by passing the username and password parameters to the InstaPy() function in your bot script, like so:
```
InstaPy(insta_username="abc", 
        insta_password="123")
```
If want InstaPy to run in the background pass the `--headless-` browser option when running from the CLI
Or add the `headless_browser=True` parameter to the `InstaPy(headless_browser=True)` constructor.

### **Liking**
The bot will fetch posts with hashtag python3 and javascript.
Set the amount to the number of posts you wish to like.
```
session.like_by_tags(['python3','javascript'], amount=300)
```
### **Follow**

By default `enabled=False`, follows every 2nd user from the images
```
session.set_do_follow(True, percentage=50)
```
### **Comment**

Enable comments (by default enabled=False) and set commenting probability to 100% so ~ every image will be commented on
```
session.set_do_follow(True, percentage=100)
```

Configure a simple list of optional comments, one will be selected at random when commenting:
```
session.set_comments(['Comment1', 'Comment2', 'Comment3'])
```
### **Excluding friends**

will prevent commenting on and unfollowing your good friends (the images will still be liked)
```
session.set_dont_include(['friend1', 'friend2', 'friend3'])
```
### **Interactions based on the number of followers and/or following a user has**

This is used to check the number of followers and/or following a user has and if these numbers either exceed the number set OR does not pass the number set OR if their ratio does not reach desired potency ratio then no further interaction happens

```
session.set_relationship_bounds(enabled=True,
                                    delimit_by_numbers=True,
                                    max_followers=3000,
                                    min_followers=150,
                                    min_following=50)
```
### **Quota Supervisor**

Take full control of the actions with the most sophisticated approaches

```
session.set_quota_supervisor(enabled=True,
                                    peak_comments_daily=250,
                                    peak_comments_hourly=30,
                                    peak_likes_daily=250,
                                    peak_likes_hourly=30,
                                 sleep_after=['likes', 'follows'])
```
Once done, we will end the session by `session.end()`.

You are ready to run the bot!

Once you have your bot script configured you can execute the script with the following commands.
```
python instagrambot.py
```
You can find my code at [GitHub](https://github.com/ayushi7rawat/Instagram-Bot).


You can also connect with me on [Twitter](https://twitter.com/ayushi7rawat)
Also, have a look at my other Blogs:
- [Python 3.9: All You need to know](https://ayushirawat.com/python-39-all-you-need-to-know)
- [The Ultimate Python Resource hub](https://ayushirawat.com/the-ultimate-python-resource-hub)
- [GitHub CLI 1.0: All you need to know](https://ayushirawat.com/github-cli-10-all-you-need-to-know)
- [Become a Better Programmer](https://ayushirawat.com/become-a-better-programmer)
- [How to make your own Google Chrome Extension](https://ayushirawat.com/how-to-make-your-own-google-chrome-extension-1)
- [Create your own Audiobook from any pdf with Python](https://ayushirawat.com/create-your-own-audiobook-from-any-pdf-with-python)
- [You are Important & so is your Mental Health!](https://ayushirawat.com/you-are-important-and-so-is-your-mental-health)

Good luck with making your own.
If you have any Queries or Suggestions, please reach out to me in the Comments Section below.