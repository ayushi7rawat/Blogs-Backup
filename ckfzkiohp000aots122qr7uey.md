## How to generate QR Code using Python

You all must have heard about or seen a lot of  QR codes, I was thinking to create one for my blogging website and I decided to do the same with python. How cool right?

Do you wish to know how to create one? Here's how you can do it!

You can also refer to the YouTube Tutorial video of the same.

%[https://www.youtube.com/watch?v=I5yruIDWCNI]

### Pre-requisites:
```
1. Basic knowledge about Python
2. Basic knowledge about QR Code 
3. pyqrcode module
```

### What will be covered in this Article:
1. QR Code Basics
2. Short differentiation between QR Code and Barcode
3. QR Code Usecases
4. How to create your own QR Code

Let's understand the basics!

## What is QR Code?
### Introduction

QR is short for Quick Response. A QR code is a type of matrix barcode first designed in 1994 for the automotive industry in Japan. A barcode is a machine-readable optical label that contains information about the item to which it is attached.


### QR Code vs Barcode
While QR Codes and Barcodes are similar in practice, QR Codes contain more information because they have the ability to hold information both horizontally and vertically.

Barcodes only use horizontal information.

### Types of QR Code:
### 1. Static QR Code:
A Static QR Code contains information that is fixed and uneditable once the Code has been generated.

**Usecases:**
- QR Codes in business cards or product packaging
- QR Codes for personal use like a party invitation 
- QR Codes for Gyms

### 2. Dynamic QR Code:
Dynamic QR Codes allow you to update, edit and modify the type of the QR Code however many times you need i.e. the content is editable.

**Usecases:**
- QR Codes for Coupons
- QR Codes for Social media

Now that you have a basic understanding of what a QR code is, let's create one!

## Time To Code!
You can find all the code [at my GitHub Repository.](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Create%20QR%20Code)

![carbon (4).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1602043629437/HRctx1An0.png)
### Necessary Packages:
Open your terminal and run the following command.
```
pip install pyqrcode
pip install pypng
```
Pyqrcode module is used to create QR Codes. It is designed to be as simple and as possible. It does this by using sane defaults and autodetection to make creating a QR Code very simple.

Once Installed now we can import it inside our python script. So first create a new python file.

Import the `pyqrcode` package inside the python script using the following command.
```
import pyqrcode
```
 
Next, we need some text that we want to convert as our QR Code. Since I am creating the QR Code for my blogging website, I will `ayushirawat.com` as data here. Let's store inside a variable.
```
data = 'ayushirawat.com'
```

Now that we have the data with us, we can move forward and make use of the package we just imported. Let's create an object, I am naming it as `img`.
```
img = pyqrcode.create(data)
```
We will use the `create` method (as it results in a cleaner looking code) on `data`. 

Now let's store it in `.png` format with proper scaling.
```
img.png('blogwebsite.png', scale= 10)
```

That's it, simple isn't it? Let's see our result! 

![Screenshot_7.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1602045825661/hYsjtq-O_.png)


This is the [QR Code of my Blog Website](https://ayushirawat.com/). Scan and check it out!

I hope this helped in understanding how to create to your own QR Code with python.
You can find all the [Code at my GitHub Repository.](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Create%20QR%20Code)

You can connect with me on [Twitter](https://twitter.com/ayushi7rawat).

You should definitely check out my other Blogs:

- [GitHub CLI 1.0: All you need to know](https://ayushirawat.com/github-cli-10-all-you-need-to-know)
- [Python 3.9: All You need to know](https://ayushirawat.com/python-39-all-you-need-to-know)
- [How to make your own Google Chrome Extension](https://ayushirawat.com/how-to-make-your-own-google-chrome-extension-1)
- [How to create your own captcha with python](https://ayushirawat.com/how-to-create-your-own-captcha-with-python)
- [You are Important & so is your Mental Health!](https://ayushirawat.com/you-are-important-and-so-is-your-mental-health)

Resource:
- https://en.wikipedia.org/wiki/QR_code
- https://pypng.readthedocs.io/en/latest/
- https://pythonhosted.org/PyQRCode/

See you in my next article, Take care!