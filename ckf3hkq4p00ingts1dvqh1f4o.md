## Python 3.9: All You need to know

Python is always evolving with the community needs and it will be most used language in the future. 

The next version of Python brings a faster release schedule, performance boosts, handy new string functions, dictionary union operators, and more consistent and stable internal APIs.

[Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub#Python-Community-and-Groups). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

This Blog post will cover:
```
- Dictionary Unions and Update with Iterables
- String methods
- Type hinting
- New math Functions
- New parser
- IPv6 Scoped Addresses
- New Module: Zoneinfo
- Other Language Changes
```

## **Dictionary Unions**
One of my favourite new features with a sleek syntax. 
**Python 3.9** dict class. If you have two dictionaries a and b, you can now use these operators to do merge and update them.

We have the merge operator `|`:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/58uaf41f6uw8zaeq4bfw.png)

And the update operator` |=`, which updates the original dictionary:
```
a = {1: 'a', 2: 'b', 3: 'c'}
b = {4: 'd', 5: 'e'}
a |= b
print(a)
{1: 'a', 2: 'b', 3: 'c', 4: 'd', 5: 'e'}
```
If our dictionaries share a common key, the key-value pair in the second dictionary will be used:
```
a = {1: 'a', 2: 'b', 3: 'c', 6: 'in both'}
b = {4: 'd', 5: 'e', 6: 'but different'}
print(a | b)
{1: 'a', 2: 'b', 3: 'c', 6: 'but different', 4: 'd', 5: 'e'}
```

### **Dictionary Update with Iterables**

Another cool behavior of the` |=` operator is the ability to update the dictionary with new key-value pairs using an iterable object — like a list or generator:
```
a = {'a': 'one', 'b': 'two'}
b = ((i, i**2) for i in range(3))
a |= b
print(a)
{'a': 'one', 'b': 'two', 0: 0, 1: 1, 2: 4}
```
If we attempt the same with the standard union operator` | `we will get a *TypeError* as it will only allow unions between dict types.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/wcdlle015y4zq5w7oqy0.png)

## **String methods**
### **removeprefix() and removesuffix()**

`str.removeprefix(substring: string)` is a method which returns a new string with the trimmed prefix if the str starts with it else it will return the original string.

`str.removesuffix(substring: string)` is a method which returns a new string with the trimmed suffix if the str ends with it else it will return the original string.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/rmw33rogdw19i4sij2zt.png)

These 2 functions perform what you would otherwise achieve using `string[len(prefix):]` for prefix and `string[:-len(suffix)]` for the suffix. These are very simple operations and therefore also very simple functions, but considering that you might perform these operations quite often, it's nice to have a built-in function that does it for you.

## **Type hinting**

Python is dynamically typed, Python dynamically specifies datatypes to a variable, meaning we don’t need to specify datatypes in our code.

This is okay, but sometimes it can be confusing!

For static allocation of data types, type hinting is used. This was introduced in Python 3.5. Since 3.5, we could specify types, but it was pretty cumbersome. 

This update has truly changed that, You can now use built-in collection types (list and dict ) as generic types. 

Earlier, you had to import the capital types (List or Dict) from typing.
```
def greet_all(names: list[str]) -> None:
    for name in names:
        print("Hello", name)
```
Now there is no need to call `List` from `typing.List`.

## **New math Functions**
in the math module, a bunch of miscellaneous functions were added or improved. Starting with the improvement to one existing function.
```
import math

# Greatest common divisor
math.gcd(80, 64, 152)
# 8
```
Previously `gcd` function which calculates the Greatest Common Divisor could only be applied to 2 numbers, forcing programmers to do something like this `math.gcd(80, math.gcd(64, 152))`, when working with more numbers. Starting with Python 3.9, we can apply it to any number of values.

First new addition to `math` module is `math.lcm` function:
```
# Least common multiple
math.lcm(4, 8, 5)
# 40
```
`math.lcm` calculates Least Common Multiple of its arguments. Same as with GCD, it allows a variable number of arguments.

## **New parser**

This one is more of an out-of-sight change but has the potential of being one of the most significant changes for the future evolution of Python.

Python 3.9 uses a new parser which is a PEG-based parser. Previously, Python used LL(1). PEG is more flexible than LL(1) when it comes to building new features in the language. The official documentation says that this flexibility will be seen in Python 3.10 and later.

The `ast` module uses the new parser and produces the same AST as the old parser.

## **IPv6 Scoped Addresses**
Another change introduced in Python 3.9 is the ability to specify the scope of IPv6 addresses. IPv6 scopes are used to specify in which part of the internet is the respective IP address valid. 

Scope can be specified at the end of IP address using `%` sign - for example: `3FFE:0:0:1:200:F8FF:FE75:50DF%2` - so this IP address is in scope `2` which is link-local address.

So, in case you need to deal with IPv6 addresses in Python, you can now do so like this:
```
from ipaddress import IPv6Address
addr = IPv6Address('ff02::fa51%1')
print(addr.scope_id)
# "1" - interface-local IP address
```

**Note**
Two addresses with different scopes are not equal when compared using basic Python operators.

## **New Module**
### **Zoneinfo**

The `zoneinfo` module brings support for the IANA time zone database to the standard library. It adds `zoneinfo.ZoneInfo`, a concrete `datetime.tzinfo` implementation backed by the system’s time zone data.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/t96ldr53ueo36y3cqzo2.png)

## **Other Language Changes**
* ` __import__()` now raises `ImportError` instead of `ValueError`, which used to occur when a relative import went past its top-level package. 

* `"".replace("", s, n)` now returns `s` instead of an empty string for all non-zero `n`. It is now consistent `with "".replace("", s)`.


### **Python becomes faster by default**
Every revision of Python enjoys performance improvements over the previous version. Python 3.9 rolls in two big improvements that boost performance without requiring any changes to existing code.

The first improvement involves more use of vectorcall protocol. This makes many common function calls by minimising or eliminating temporary objects. Python 3.9 introduces several new built-ins including range, tuple, set, frozenset, list, dict — use vectorcall, which speed up the execution.

### **Python switches to a yearly release cycle**

Up until this point, Python has been developed and released on an eighteen-month cadence. PEP 602 proposed that the Python development team adopt an annual release cycle, and that proposal has been accepted. 

**Conclusion**
With every new release, Python has become faster and powerful. Python makes it easy to manipulate common data types. 

Probably not all of these changes are relevant to your daily programming, but I think it's good to be at least aware as they might come in handy at some point.

You can connect with me on [twitter](https://twitter.com/ayushi7rawat)

Also, have look at my other blogs:
- [GitHub CLI 1.0: All you need to know](https://ayushirawat.com/github-cli-10-all-you-need-to-know)
- [How to make your own Google Chrome Extension](https://ayushirawat.com/how-to-make-your-own-google-chrome-extension-1)
- [Create your own Audiobook from any pdf with Python](https://ayushirawat.com/create-your-own-audiobook-from-any-pdf-with-python)
- [How to make an Instagram Bot with Python](https://ayushirawat.com/how-to-make-an-instagram-bot-with-python)
- [You are Important & so is your Mental Health!](https://ayushirawat.com/you-are-important-and-so-is-your-mental-health)

## **Resources**
- https://www.python.org/downloads/release/python-390a5/
- https://docs.python.org/3.9/whatsnew/3.9.html
