## Build a Translator using Python


In this Blog article, we will learn how to **Create a Translator** . We will see the implementation in **python**.

[Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my YouTube video tutorial for better Understanding

%[https://youtu.be/pPvhIj7WUnY]

## What will be covered in this Blog

```python
1. Translator Introduction
2. What is Googletrans?
3. Create a Translator with Python
```

## Translator Introduction:

The Dictionary definition: 

> The definition of a **translator** is someone who helps people who speak different languages to communicate or who takes something (such as a speech or a book) in one language and who puts it into a different language for people to **understand**.

If you wish to know more about it, you can refer to [Translation Wikipedia Page](https://en.wikipedia.org/wiki/Translation). Use this link to navigate to the GIF's Wikipedia Page.

## What is Googletrans?

Googletrans is a **free** and **unlimited** python library that implemented Google Translate API. This uses the [Google Translate Ajax API](https://translate.google.com/) to make calls to such methods as detect and translate.

- Fast and reliable - it uses the same servers that translate.google.com uses
- Auto language detection
- Bulk translations
- Customizable service URL
- Connection pooling (the advantage of using requests.Session)
- HTTP/2 support

If you wish to know more about it, you can refer to [Googletrans Documentation](https://py-googletrans.readthedocs.io/en/latest/). Use this link to navigate to the documentation.

Now that you are aware of Translator and Googletrans basics, we can move forward to the coding section. 

## Time to code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/GIF%20Converter). **Drop a star** if you find it useful.

![carbon (6).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1604115469214/bpJGegX_F.png)

### Installing Googletrans 

Open your terminal and run the following command

```python
pip install googletrans
```

Now that we have the package, we are ready to import it in our python script.

```python
from googletrans import Translator
```

Let's store some text that we will use for translation. You can use any text segment of your choice. I am using of one of my favourite poem [**Daffodils**](https://www.poetryfoundation.org/poems/45521/i-wandered-lonely-as-a-cloud) by **WILLIAM WORDSWORTH**. Let's store it in `text`. It's the last stanza of the poem. 

The language I am using is `French`. You can choose any language of your choice.

You can even take the text as a user input if you like, so you wont have to make changes in your program every time you wish to use the translator.

```python
text = '''  Pour souvent, quand sur mon canapé je mens
D'humeur vacante ou songeuse,
Ils clignotent sur cet œil intérieur
Quel est le bonheur de la solitude;
Et puis mon cœur se remplit de plaisir,
Et danse avec les jonquilles. '''
```

Let's create an instance of Translator to use. 

```python
translator = Translator()
```

This uses the [Google Translate Ajax API](https://translate.google.com/) to make calls to such methods as detect and translate. Now, let's call the `detect` method on `translator` and pass in our data stored in `text` and store it in `lang`. 

```python
lang = translator.detect(text)
print(lang)
```

 Now let's `print` it out.

- `lang=fr` means the detected language is French.
- `confidence=0.9365149` is how much percentage the translator is confident about the language detection.

```python
Detected(lang=fr, confidence=0.9365149)
```

Once done, let's move forward and actually translate it. I am calling the `translate` method here on `translator` and passing two parametrs.

- `text`: our data in original language
- `dest`: our destination language

Now, to refer the other language codes you can refer to the [google language documentation](https://cloud.google.com/translate/docs/languages)

**NOTE:** If you do not specify any destination language, it will automatically switch to the default one i.e. `English`.

```python
res = translator.translate(text, dest = 'en')
```

At last, let's verify it by printing our `res`.

```python
Often when on my couch I lie
In a vacant or pensive mood,
They blink on that inner eye
What is the happiness of solitude;
And then my heart fills with pleasure,
And dance with the daffodils.
```

This is how the conversion is done. This is all about the **creating a Translator with Python**. That's it! simple, isn't it? Hope this tutorial has helped.

You can play around with the library and explore more features and even make use of Python GUI using Tkinter.

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/GIF%20Converter). **Drop a star** if you find it useful.

Thank you for reading, I would love to connect with you at [Twitter](https://twitter.com/ayushi7rawat) | [LinkedIn](). I would recommend you to Check out the [YouTube video]() of the same and **don't forget to subscribe my Channel**.

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

- https://py-googletrans.readthedocs.io/en/latest/

- https://github.com/ssut/py-googletrans

- https://github.com/Zulko/moviepyhttps://pypi.org/project/googletrans/

- https://www.poetryfoundation.org/poems/45521/i-wandered-lonely-as-a-cloud

- https://cloud.google.com/translate/docs/languages

  

- See you in my next Blog article, Take care