## Draw Heart with Python using Turtle

In this Blog article, we will learn how to **Create a heart with Turtle**, we will implementation it in **Python**.

[Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my YouTube video tutorial for better Understanding:

%[https://youtu.be/F1c_aA6Ldvo]

## What will be covered in this Blog:
```
1. Turtle Introduction
2. Creating a heart with Turtle
```

## What is Turtle?

`Turtle` is a pre-installed Python library. It that enables users to create pictures and shapes by providing them with a virtual canvas. The onscreen pen that you use for drawing is called as **turtle**. 

The turtle has three attributes: a location, an orientation (or direction), and a pen.

### Moving the Turtle Head

The turtle can move in four directions:

- Forward
- Backward
- Left
- Right

If you wish to know more about it, you can refer to [Turtle Documentation](https://docs.python.org/3/library/turtle.html). Use this link to navigate to the documentation.

Now that you are aware of Turtle basics, we can move forward to the coding section. 

## Time to code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Heart%20with%20turtle). **Drop a star** if you find it useful.

![carbon (6).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1604579899829/JsfvIBoaR.png)

In order to access the Python library, you need to import it into your Python environment, use the following command to import `turtle`it in your python script.

```python
import turtle
```

Now let's define some properties, 

- Let's set the speed as `3` using `speed` method, that means the heart will not just appear on the screen, the drawing will have some animation. 
- If you wish to change the background color, you can use the `bgcolor` method, by default it is white. 
- You can adjust the pen's thickness using `pensize` method, it will be slightly bold.

```python
turtle.speed(3)
#turtle.bgcolor("black")
turtle.pensize(3)
```

Now let's define a function to define the curve, I am calling it as `myfunc`.

```python
def curve():
    for i in range(200):
        turtle.right(1)
        turtle.forward(1)
turtle.color("black", "red")  
turtle.begin_fill()

turtle.left(140)
turtle.forward(111.65)
curve()
```

I will define a loop here for the first curve, we will set the direction right and move forward. Now let's set the `turtle` color using the `color` method

- the first parameter will be the border color, the pen color, which we are passing as `black`
- the second parameter, `red` is the color used to fill inside our heart.

And once we have set the color, we can begin the fill using `begin_fill` method. 

we call `left` and `forward` and finally call our function to get the first curve. It will look something like this.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1604544930305/vifnuIkKB.png)

```
turtle.left(120)
```
In order to change the `pen`'s direction, use `left` method. 
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1604545908996/w9r15WoEF.png)

```
curve()
```
Now let's call the curve function again.
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1604546181595/foqqQVMGH.png)
```
turtle.forward(111.65)

turtle.end_fill()
```
Let's make it touch the starting point and complete our heart. We will make use of `forward` method here. Once our heart is completed, we can now use `end_fill` to fill color in our heart.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1604546487737/8lik8zENj.png)

If you closely observed you can see the pen head at the end. We will use `hideturtle` method to get red of it.

```
turtle.hideturtle()
turtle.done()
```
`done` method is used to hold the output Turtle screen.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1604546711323/jOaP3JFqV.png)
This is all about **Creating a heart with Turtle**. That's it! simple, isn't it? Hope this tutorial has helped.

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Heart%20with%20turtle). **Drop a star** if you find it useful.

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

- https://docs.python.org/3/library/turtle.html
- https://en.wikipedia.org/wiki/Turtle_graphics

See you in my next Blog article, Take care