## Currency Converter using Python

Hello world!

A currency is a system of money in common use, especially for people in a nation, eg, INR, USD and Bitcoin (₿) is a cryptocurrency. In this Blog article, we will learn how to **Create Currency Converter.** We will see the implementation in Python.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my **YouTube video Tutorial** to see a working tutorial for better Understanding and a step by step Guide of the same. 

%[https://www.youtube.com/watch?v=ixB2YHGSiAQ]

## What will be covered in this Blog

```python
1. What is BitCoin?
2. What is Currency?
3. Basics of forex-python Module
4. Create Currency Converter using python
```

*Let's get started!*

## What is BitCoin?:

Bitcoin is a cryptocurrency,an innovative payment network, invented in 2008 by an unknown person or group of people using the name Satoshi Nakamoto and started in 2009.

If you wish to know more about it, you can refer to [**BitCoin** Wikipedia Page](https://en.wikipedia.org/wiki/Bitcoin). 

## What is Currency?:

**Currency** is a medium of exchange for goods and services. In short, it's **money**, in the form of paper or coins, usually issued by a government and generally accepted at its face value as a method of payment.

If you wish to know more about it, you can refer to [**Currency** Wikipedia Page](https://en.wikipedia.org/wiki/Currency). 

## Module Used:

### forex-python Module:

Forex Python is a Free Foreign exchange rates and currency conversion. 

#### Features:

- List all currency rates. 

- BitCoin price for all curuncies. 
- Converting amount to BitCoins. 
- Get historical rates for any day since 1999. 
- Conversion rate for one currency(ex; USD to INR). 
- Convert amount from one currency to other.(‘USD 10$’ to INR). 
- Currency symbols, Currency names, etc.

If you wish to know more about it, you can refer to [**forex-python Module** Documentation](https://forex-python.readthedocs.io/en/latest/). 

Now that you are familiar with *BitCoin and Currency* and have acquired basic knowledge of *forex-python module,* we can move forward to *the coding section.*

## Time to Code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Currency%20Converter). **Drop a star** if you find it useful.

![code.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1607657920134/kl69ac27_.png)

In order to access the Python library, you need to install it into your Python environment

```python
pip install forex-python
```

Now, we need to import the package in our python script. Use the following command to do so.

```python
from forex_python.converter import CurrencyCodes, CurrencyRates
from forex_python.bitcoin import BtcConverter
```

Let's create an instance of `CurrencyCodes`. I am naming it as `test1`.

```python
test1 = CurrencyCodes()
```

Once done, let's fetch the currency symbol. I am making use of `get_symbol` method for the same and passing the currency code as a parameter. Let's store it in `cur_symbol`. 

```python
cur_symbol = test1.get_symbol('INR')
```

Let's fetch the currency name. I am making use of `get_currency_name` method for the same and passing the currency code as a parameter. Let's store it in `cur_name`. 

````python
cur_name = test1.get_currency_name('INR')
````

Let's display the output.

```python
print('The currency name is: ' + cur_name)
print('The currency symbol is: ' + cur_symbol)

#let's see for another example
print('\n' + test1.get_symbol('USD'))
print(test1.get_currency_name('USD'))

#OUTPUT:
The currency name is: Indian rupee
The currency symbol is: ₹
    
US$
United States dollar
```

Now, let's move forward and create an instance for `CurrencyRates`. 

```python
test2 = CurrencyRates()
```

Once done, let's fetch the Conversion rate. I will make use of `get_rate` method for the same. Let's fetch what `1 United States Dollar` equals-to in `Indian rupee`.

```python
rate = test2.get_rate('USD', 'INR')
print(rate)

#OUTPUT:
73.6702434998
```

Now that we have successfully fetched the conversion rate, let's try converting `10 US$` to `Indian rupee`. I will make use of `convert` method for the same.

```python
res = test2.convert('USD', 'INR', 10)
print(res)

#OUTPUT:
736.702434998
```

I am passing three parameters here,

- original currency 
- the converted currency
- conversion amount 

### BONUS:

Let's fetch BITCOIN's latest price details. Let's start by creating an instance of `BtcConverter`

```python
bitcoin = BtcConverter()
```

Now, let's fetch the latest price, I will make use of `get_latest_price` method for the same. Finally, you can printout the result.

```python
price = bitcoin.get_latest_price('INR')

#display the output
print(price)
```

With these steps, we have successfully **Created Currency Converter using python.** That's it! 

Simple, isn't it? Hope this tutorial has helped. I would strongly recommend you to Check out the [YouTube video](https://www.youtube.com/watch?v=ixB2YHGSiAQ) of the same and **don't forget to subscribe my Channel**.

You can play around with the `forex-python` library and even explore more features. You can even make use of Python GUI using `Tkinter`.

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Currency%20Converter). **Drop a star** if you find it useful.

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

- https://pypi.org/project/forex-python/
- https://en.wikipedia.org/wiki/Bitcoin
- https://en.wikipedia.org/wiki/Currency
- https://github.com/MicroPyramid/forex-python
- https://forex-python.readthedocs.io/en/latest/

See you in my next Blog article, Take care!!