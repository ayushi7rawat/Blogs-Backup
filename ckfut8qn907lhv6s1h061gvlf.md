## Create your own Audiobook from any pdf with Python


Do you read books? Do you like listening to Audiobooks? Do you wish to create your own Audiobook from any pdf? Here's how you can do it.

You can also follow along with the video tutorial of the same!

%[https://www.youtube.com/watch?v=ZWjXbe9DOVA]

[Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

Its time to code!
## Let's get started!

You can find the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Create%20AudioBook%20from%20pdf)

First, we need to install the necessary libraries. We require two libraries to build Audiobook using Python. 
### 1. PyPDF2
A Pure-Python library built as a PDF toolkit. It is capable of extracting document information splitting documents page by page merging documents page by page cropping pages merging multiple pages into a single page encrypting and decrypting PDF files and more!

So open your terminal and run the following command.
```
pip install PyPDF2
``` 
If you wish to know more about it, you can refer to [the documentation](https://pythonhosted.org/PyPDF2/). 
### 2. pyttsx3
pyttsx3 is a text-to-speech conversion library in Python. Unlike alternative libraries, it works offline, and is compatible with both Python 2 and 3.

So open your terminal and run the following command.
```
pip install pyttsx3
``` 
If you wish to know more about it, you can refer to [the documentation](https://pyttsx3.readthedocs.io/en/latest/). 

![carbon (3).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1601740270063/ACeHcOpry.png)
Now that we have installed the packages, we can import them in our program.

```
import pyttsx3
import PyPDF2
``` 
Now we need to open our file in reading format and store into `book`. The name of my pdf file is `demo.pdf`. `rb` stands for reading mode.
```
book = open('demo.pdf','rb')
```

Now I will call `PyPDF2`'s `PdfFileReader` method on `book` and store it into `pdf_reader`
```
pdf_reader = PyPDF2.PdfFileReader(book)
```

Now let's calculate the number of pages in our pdf by using `numPages` method on `pdf_reader ` and store in `num_pages`.
```
num_pages = pdf_reader.numPages
```
Now let's initialize `pyttsx3` using `init` method and let's print `playing Audiobook`
```
play = pyttsx3.init()
print('Playing Audio Book')
```
Now, let's run a loop for the number of pages in our pdf file. A `page` will get retrieved at each iteration.

```
for num in range(0,num_pages):
    page = pdf_reader.getPage(num)
    data= page.extractText()
    play.say(data)
    play.runAndWait() 
```

Moving forward, let's extract the text from our page using `extractText` method on our page and store it into `data`.

Next, we will call `say` method on `data` and finally we can call `runAndWait` method at the end. 

Run the python script and your Audiobook will play.

That's it. We are done. You can find the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Create%20AudioBook%20from%20pdf)

If you have any queries or suggestions, feel free to reach out to me.

You can connect with me on [Twitter](https://twitter.com/ayushi7rawat).

You should definitely check out my other Blogs:

- [Python 3.9: All You need to know](https://ayushirawat.com/python-39-all-you-need-to-know)
- [The Ultimate Python Resource hub](https://ayushirawat.com/the-ultimate-python-resource-hub)
- [GitHub CLI 1.0: All you need to know](https://ayushirawat.com/github-cli-10-all-you-need-to-know)
- [Become a Better Programmer](https://ayushirawat.com/become-a-better-programmer)
- [How to make your own Google Chrome Extension](https://ayushirawat.com/how-to-make-your-own-google-chrome-extension-1)
- [You are Important & so is your Mental Health!](https://ayushirawat.com/you-are-important-and-so-is-your-mental-health)



Resources:

- https://pyttsx3.readthedocs.io/en/latest/
- https://pythonhosted.org/PyPDF2/

See you in my next article, Take care!