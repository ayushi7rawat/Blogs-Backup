## YouTube Video Downloader using Python

In this Blog article, we will see how to download YouTube video. We will see the implementation in python. 

[Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my YouTube video tutorial for better Understanding

%[https://youtu.be/7BXJIjfJCsA]

## Introduction
YouTube is a very popular video-sharing platform. Downloading a video from YouTube can be a tough job. Python can make the job easier for you. 

## What will be covered in this Blog
```
1. Pytube Introduction
2. How to fetch the Video Title
3. How to fetch the Thumbnail Image
4. Download a YouTube Video
```

## What is Pytube?
pytube is a lightweight, Pythonic, dependency-free, library (and command-line utility) for downloading YouTube Videos.

Features
- Support for Both Progressive & DASH Streams
- Easily Register on_download_progress & on_download_complete callbacks
- Command-line Interfaced Included
- Caption Track Support
- Outputs Caption Tracks to .srt format (SubRip Subtitle)
- Ability to Capture Thumbnail URL.
- Extensively Documented Source Code
- No Third-Party Dependencies

If you wish to know more about it, you can refer to [Pytube Documentation](https://python-pytube.readthedocs.io/en/latest/). Use this link to navigate to the documentation.

Now that you are aware of `pytube` basics, we can move forward to the coding section. 

## Time to code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/YouTube%20Video%20Downloader). **Drop a star** if you find it useful.

![carbon (5).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1602826116595/YVbRMYOQ6.png)

### Installing Pytube
Open your terminal and run the following command
```
pip install pytube3
```
I would recommend you to use pytube3 library. I am using the same in this tutorial. Now that we have the package, we are ready to import it in our python script.

### Fetching the Title
The first step is to import the YouTube class from the `pytube` module.
```
from pytube import YouTube
url = 'Your URL goes here'
my_video = YouTube(url)
```

Now get the URL, I am storing it in `url`. Next, I am calling the `YouTube` method on `my_video` and passing out URL.

```
print(my_video.title)
```
Now let's fetch the title of the YouTube Video Using the `title` method. Next, let's fetch the thumbnail image.

### Fetching the Thumbnail Image

In order to fetch the Thumbnail Image of YouTube Video, we will use the `thumbnail_url` method.

```
print(my_video.thumbnail_url)
```
`Print` method will display the Thumbnail Image of the YouTube Video.

### Downloading the YouTube Video
In order to download the YouTube video, we need to set the `stream resolution` first.
```
my_video = my_video.streams.get_highest_resolution()
or
my_video = my_video.streams.first()
```
You can choose the first stream resolution or you can go for one with the stream resolution.

If you wish to get all the stream resolution for the video and then choose the appropriate one then you can use the following command.
```
for stream in my_video.streams:
    print(stream)
```
You can use the filter() function to extract only specific streams. This is useful when you want to download all the different resolutions of the YouTube video.

Moving forward, now let's download the video! We will use the `download` method on the specific stream to download the YouTube video. 

```
my_video.download()
```
Your YouTube Video will be downloaded in the same folder where your python script resides.

That's it! simple, isn't it?

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/YouTube%20Video%20Downloader). **Drop a star** if you find it useful.

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
- https://python-pytube.readthedocs.io/en/latest/

See you in my next Blog article, Take care