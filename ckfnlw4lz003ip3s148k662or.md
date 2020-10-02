## How to create your own captcha with python

We perform daily activities on the internet. You must often encounter **CAPTCHA** and **reCAPTCHA **tests on the Internet. CAPTCHAs are used by any website that wishes to restrict usage by bots. Do you wish to know how to create one?

You can also follow along with the video Tutorial for better Understanding!

%[https://www.youtube.com/watch?v=fAFIY_3OaO4]

Let's look at what will be covered in this Blog:
## Contents:
- What is CAPTCHA
- How to create an Image CAPTCHA
- How to create an Audio CAPTCHA 

## Prerequisites:
```
1. Basic knowledge about Python
2. Basic knowledge about CAPTCHA 
3. CAPTCHA module
```

## What is CAPTCHA

CAPTCHA stands for:
![Screenshot_1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1601341077271/jwXiRNQe9.png)

Its primary motive is to determine whether the user is a real human or a spam robot. CAPTCHA is an example of one-way conversion and a type of challenge-response test used in computing to determine whether or not the user is human.

The most common form is Image CAPTCHA. You are shown an image and if you are a real person, then you need to enter its text in a separate field.

Now that you are aware of the basics, we can get started.

## Time to code!
You can find the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Create%20and%20Decode%20captcha/Create%20Image%20and%20Audio%20CAPTCHA). Make sure you follow along! 

**Note:**

I am using `Juyptr Notebook` here, so the Image and Audio CAPTCHA will be created in the same folder where my python file is located.
### Image CAPTCHA

The CAPTCHA presents characters in a way that is alienated and requires interpretation. Alienation can involve scaling, rotation, distorting characters. It can also involve overlapping characters with graphic elements such as colour, background noise, lines, arcs, or dots. This alienation provides protection against bots with insufficient text recognition algorithms but can also be difficult for humans to interpret.


![carbon (2).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1601344390041/rJlvVkhZM.png)


So the very first step, we require CAPTCHA package so open your command prompt and run the following command.

```
pip install captcha
```
Once done, we can now `import the CAPTCHA` package using the following command.
```
from captcha.image import ImageCaptcha
```
If it runs successfully, you are good to go. Moving forward, we will now store it in a variable and call it as an `image` . We can also specify image dimensions like its `height` or `width` .

```
image = ImageCaptcha(width = 280, height = 90)
```

Next, let's generate the characters or numbers which will be displayed in the CAPTCHA. We will use the `generate method` to do the same.

we will call generate method on our `image` and store this inside `data` . I am using `hello17world` as our text here. You can use your own text here.
```
data = image.generate('hello17world')

```
At last, let's write it in a file using the following command. I am naming it as `demo` . It will be created in `png` format.
```
image.write('hello17world', 'demo.png')
```

And we're done! Simple, isn't it?

Let's see what our final result will look like.

![k3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1601343677119/I2CTQyhkr.png)

Now, Let's look at how to create an **Audio CAPTCHA*

### Audio CAPTCHA
Audio CAPTCHAs were developed as an alternative that grants accessibility to visually impaired users. These CAPTCHAs are often used in combination with text or image-based CAPTCHAs. Audio CAPTCHAs present an audio recording of a series of letters or numbers which a user then enters.

These CAPTCHAs rely on bots not being able to distinguish relevant characters from background noise. Like text-based CAPTCHAs, these tools can be difficult for humans to interpret as well as for bots.

You can find the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Create%20and%20Decode%20captcha/Create%20Image%20and%20Audio%20CAPTCHA). 

![carbon (4).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1601344635966/wi-edhKle.png)

we will `import the CAPTCHA` package using the following command.
```
from captcha.audio import AudioCaptcha 
```
If it runs successfully, you are good to go. Moving forward, we will now store it and call it as `audio` .

```
audio = AudioCaptcha()
```
Next, let's generate the numbers which will be used in the Audio CAPTCHA. We will use the `generate method` to do the same.

we will call generate method on `audio` and store this inside `data` . 
```
data = audio.generate('789') 

```
At last, lets write it in a file using the following command. I am naming it as `demo2` . It will be created in `wav` format.
```
audiofile.write('789','demo2.wav')
```

That's it! You are good to go! 

You can find the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Create%20and%20Decode%20captcha/Create%20Image%20and%20Audio%20CAPTCHA). 

You can connect with me on [Twitter](https://twitter.com/ayushi7rawat).

I hope this helped you in understanding how to create your own Image and Audio CAPTCHA. If you have any Queries or Suggestions, please reach out to me in the Comments Section below.

You will also like my other Blogs:

- [Python 3.9: All You need to know](https://ayushirawat.com/python-39-all-you-need-to-know)
- [GitHub CLI 1.0: All you need to know](https://ayushirawat.com/github-cli-10-all-you-need-to-know)
- [How to make an Instagram Bot with Python](https://ayushirawat.com/how-to-make-an-instagram-bot-with-python)
- [Web Scraping Coronavirus Data into MS Excel](https://ayushirawat.com/web-scraping-coronavirus-data-into-ms-excel)
- [How to make your own Google Chrome Extension](https://ayushirawat.com/how-to-make-your-own-google-chrome-extension-1)


See you in the next article! Take care!
