## Create Digital Clock with Python

Hi everyone,

In this tutorial, I am going to teach you how to build your own digital clock with Python. We will use **Tkinter** to do the same.

You can refer to my YouTube video tutorial for a better understanding.

%[https://youtu.be/Cw206ZAUW6Y]

Let's get started.
## It's Time to Code!
You can find all the code at [my GitHub Repository.]()


![Screenshot_3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1601817747383/FUxKAo2_z.png)

Create a python file, I am naming it as demo.py. You can name it anything you want.

### Importing the necessary packages.

```
from tkinter import *
from tkinter.ttk import *
```
we have imported the `tkinter` , now lets import `time`. We require `from time import strftime` from `time`.
```
from time import strftime
```
Next, we need to create UI for our digital clock. 
```
root = Tk()
```
Now we need to set the title of our clock. Let's set the title using `title` method.
```
root.title('Digital Clock')
```
Now, let's define a method to get the time. I will name it as `clock`. We will use `strftime` method to get the time and store it inside a string. Let's name the string as `tick`. Now it's time to provide the time format.

```
def clock():
	tick = strftime('%H:%M:%S %p')
```
Now, let's set the label using `config` method.
```
label.config(text = tick)
```
Now, we can call our clock function and use the `after` method to do the same. We would like to call it every second, so that will be our first parameter.
```
label.after(1000, clock)
```
 
Once done with the `title`, we will require a `label`. The `label` will be used to store our `title`. so let's create a `label`. we will do the same using `label` method. 
```
label = Label(root, font=('ds-digital', 100), background = 'black', foreground = 'red')
```
Let's design it.
-  set background
- set foreground
- choose font 
- set the color

Now that we have designed our label, we are ready to pack it. We will do so with the `pack` method. You can also define the alignment of the label using the `anchor` method.
```
label.pack(anchor='center')
```

Moving forward let's call our `clock` function and at the end we will cal `mainloop`.
```
That's it and we are done! It will look something like this!


![Screenshot_1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1601817624677/OqhZG5UH0.png)
You can find the code at my [GitHub Repository]()

If you have any queries or suggestions, feel free to reach out to me.

You can connect with me on [Twitter](https://twitter.com/ayushi7rawat).

You should definitely check out my other Blogs:

- [GitHub CLI 1.0: All you need to know](https://ayushirawat.com/github-cli-10-all-you-need-to-know)
- [Python 3.9: All You need to know](https://ayushirawat.com/python-39-all-you-need-to-know)
- [How to make your own Google Chrome Extension](https://ayushirawat.com/how-to-make-your-own-google-chrome-extension-1)
- [How to create your own captcha with python](https://ayushirawat.com/how-to-create-your-own-captcha-with-python)
- [You are Important & so is your Mental Health!](https://ayushirawat.com/you-are-important-and-so-is-your-mental-health)

See you in my next article, Take care!