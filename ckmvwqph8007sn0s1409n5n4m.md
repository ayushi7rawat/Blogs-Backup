## Fetch All Information of any Country using Python

Hello, world!

In this Blog article, we will learn how to **Fetch data of any Country.** We will see the implementation in **Python**.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my **YouTube video Tutorial** to see a working tutorial for better Understanding and a step by step Guide of the same. 

%[https://www.youtube.com/watch?v=Eb3naUPN3G8]

## What will be covered in this Blog

```python
1. Countryinfo Introduction
2. Fetching data of any Country
```

*Let's get started!*

## What is Countryinfo?

`Countryinfo` is a python module for returning data about countries, ISO info and states/provinces within them. To access one of the country properties available, you’ll need to use one of the API methods.

If you wish to know more about it, you can refer to [Countryinfo Documentation](https://pypi.org/project/countryinfo/#api-usage). Use this link to navigate to the documentation.

Now that you are familiar with *with our agenda* and have acquired basic knowledge of *Countryinfo module,* we can move forward to *the coding section.*

## Time to Code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Fetch%20data%20of%20any%20country). **Drop a star** if you find it useful.


![carbon (8).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1617087013741/-1_91928a.png)

In order to access the Python library, you need to install it first. 

```python
pip install countryinfo
```

Once installed, let's import it into your Python environment, use the following command to import `countryinfo` it in your python script.

```python
from countryinfo import CountryInfo
```

Now let's store the Country name for which we want to fetch the information. I wish to fetch details for my country, `India`, so I will store the same in `name`.

```python
name = 'India'
```

Now, let's create an instance. We will make use of `CountryInfo`  and pass `name` as an argument here. 

```python
country = CountryInfo(name)
```

Once done, let's see some of the methods one by one.

### 1. alt_spellings()

Returns alternate spellings for the name of a specified country

```python
data1 = country.alt_spellings()
print(data1)

#Output:
['IN', 'Bhārat', 'Republic of India', 'Bharat Ganrajya']
```

### 2. capital()

Returns capital city for a specified country

```python
data2 = country.capital()
print(data2)

#Output:
New Delhi
```

### 3. currencies()

Returns official currencies for a specified country

```python
data3 = country.currencies()
print(data3)

#Output:
['INR'] 
```

### 4. languages()

Returns official languages for a specified country

```python
data4 = country.languages()
print(data4)

#Output:
['hi', 'en']
```

### 5. timezones()

Returns all timezones for a specified country

```python
data5 = country.timezones()
print(data5)

#Output:
['UTC+05:30']
```

### 6.area()

Returns area (km²) for a specified country

```python
data6 = country.area()
print(data6)

#Output:
3287590      
```

### 7.borders()

Returns array of strings, ISO3 codes of countries that border the given country.

```python
data7 = country.borders()
print(data7)

#Output:
['AFG', 'BGD', 'BTN', 'MMR', 'CHN', 'NPL', 'PAK', 'LKA']
```

### 8.calling_codes()

Returns international calling codes for a specified country

```python
data8 = country.calling_codes()
print(data8)

#Output:
['91']
```

### 9.wiki()

Returns link to Wikipedia page for a specified country

```python
data9 = country.wiki()
print(data9)

#Output:
http://en.wikipedia.org/wiki/india
```

If you wish to extract a summary of the methods altogether, in that case, we can make use of `info` method. It fetches all the data regarding the given country. Let's give it a try.

### 10. info()

Returns all available information for a specified country.

```python
data10 = country.info()

for x,y in data10.items():
    print(f{x} --> {y}')

#Output:
name --> India
altSpellings --> ['IN', 'Bhārat', 'Republic of India', 'Bharat Ganrajya']
area --> 3287590
borders --> ['AFG', 'BGD', 'BTN', 'MMR', 'CHN', 'NPL', 'PAK', 'LKA']
callingCodes --> ['91']
capital --> New Delhi
capital_latlng --> [28.614179, 77.202266]
currencies --> ['INR']
demonym --> Indian
flag -->
geoJSON --> {'type': 'FeatureCollection', 'features': [{'type': 'Feature', 'id': 'IND', 'properties': {'name': 
'India'}, 'geometry': {'type': 'Polygon', 'coordinates': [[[77.837451, 35.49401], [78.912269, 34.321936], [78.811086, 33.506198], [79.208892, 32.994395], [79.176129, 32.48378], [78.458446, 32.618164], [78.738894, 31.515906], [79.721367, 30.882715], [81.111256, 30.183481], [80.476721, 29.729865], [80.088425, 28.79447], [81.057203, 28.416095], [81.999987, 27.925479], [83.304249, 27.364506], [84.675018, 27.234901], [85.251779, 26.726198], [86.024393, 26.630985], [87.227472, 26.397898], [88.060238, 26.414615], [88.174804, 26.810405], [88.043133, 27.445819], [88.120441, 27.876542], [88.730326, 28.086865], [88.814248, 27.299316], [88.835643, 27.098966], [89.744528, 26.719403], [90.373275, 26.875724], [91.217513, 26.808648], [92.033484, 26.83831], [92.103712, 27.452614], [91.696657, 27.771742], [92.503119, 27.896876], [93.413348, 28.640629], [94.56599, 29.277438], [95.404802, 29.031717], [96.117679, 29.452802], [96.586591, 28.83098], [96.248833, 28.411031], [97.327114, 28.261583], [97.402561, 27.882536], [97.051989, 27.699059], [97.133999, 27.083774], [96.419366, 27.264589], [95.124768, 26.573572], [95.155153, 26.001307], [94.603249, 25.162495], [94.552658, 24.675238], [94.106742, 23.850741], [93.325188, 24.078556], [93.286327, 23.043658], [93.060294, 22.703111], [93.166128, 22.27846], [92.672721, 22.041239], [92.146035, 23.627499], [91.869928, 23.624346], [91.706475, 22.985264], [91.158963, 23.503527], [91.46773, 24.072639], 
[91.915093, 24.130414], [92.376202, 24.976693], [91.799596, 25.147432], [90.872211, 25.132601], [89.920693, 25.26975], [89.832481, 25.965082], [89.355094, 26.014407], [88.563049, 26.446526], [88.209789, 25.768066], [88.931554, 25.238692], [88.306373, 24.866079], [88.084422, 24.501657], [88.69994, 24.233715], [88.52977, 23.631142], 
[88.876312, 22.879146], [89.031961, 22.055708], [88.888766, 21.690588], [88.208497, 21.703172], [86.975704, 21.495562], [87.033169, 20.743308], [86.499351, 20.151638], [85.060266, 19.478579], [83.941006, 18.30201], [83.189217, 17.671221], [82.192792, 17.016636], [82.191242, 16.556664], [81.692719, 16.310219], [80.791999, 15.951972], [80.324896, 15.899185], [80.025069, 15.136415], [80.233274, 13.835771], [80.286294, 13.006261], [79.862547, 12.056215], [79.857999, 10.357275], [79.340512, 10.308854], [78.885345, 9.546136], [79.18972, 9.216544], [78.277941, 8.933047], [77.941165, 8.252959], [77.539898, 7.965535], [76.592979, 8.899276], [76.130061, 10.29963], [75.746467, 11.308251], [75.396101, 11.781245], [74.864816, 12.741936], [74.616717, 13.992583], [74.443859, 14.617222], [73.534199, 15.990652], [73.119909, 17.92857], [72.820909, 19.208234], [72.824475, 20.419503], [72.630533, 21.356009], [71.175273, 20.757441], [70.470459, 20.877331], [69.16413, 22.089298], [69.644928, 22.450775], [69.349597, 22.84318], [68.176645, 23.691965], [68.842599, 24.359134], [71.04324, 24.356524], [70.844699, 25.215102], [70.282873, 25.722229], [70.168927, 26.491872], [69.514393, 26.940966], [70.616496, 27.989196], [71.777666, 27.91318], [72.823752, 28.961592], [73.450638, 29.976413], [74.42138, 30.979815], [74.405929, 31.692639], [75.258642, 32.271105], [74.451559, 32.7649], [74.104294, 33.441473], [73.749948, 34.317699], [74.240203, 34.748887], [75.757061, 34.504923], [76.871722, 34.653544], [77.837451, 35.49401]]]}}]}
ISO --> {'alpha2': 'IN', 'alpha3': 'IND'}
languages --> ['hi', 'en']
latlng --> [20, 77]
nativeName --> भारत
population --> 1263930000
provinces --> ['Andaman and Nicobar Islands', 'Andhra Pradesh', 'Arunachal Pradesh', 'Assam', 'Bihar', 'Chandigarh', 'Chhattisgarh', 'Dadra and Nagar Haveli', 'Daman and Diu', 'Delhi', 'Goa', 'Gujarat', 'Haryana', 'Himachal Pradesh', 'Jammu and Kashmir', 'Jharkhand', 'Karnataka', 'Kerala', 'Lakshadweep', 'Madhya Pradesh', 'Maharashtra', 'Manipur', 'Meghalaya', 'Mizoram', 'Nagaland', 'Odisha', 'Puducherry', 'Punjab', 'Rajasthan', 'Sikkim', 'Tamil Nadu', 'Telangana', 'Tripura', 'Uttar Pradesh', 'Uttarakhand', 'West Bengal']
region --> Asia
subregion --> Southern Asia
timezones --> ['UTC+05:30']
tld --> ['.in']
translations --> {'de': 'Indien', 'es': 'India', 'fr': 'Inde', 'ja': 'インド', 'it': 'India'}
wiki --> http://en.wikipedia.org/wiki/india
```

 That's it. we are done. You can customize your code further according to your need. You can do the same for any country of your choice. 

With these steps, we have successfully **Retrieved data of a Country.** That's it! You can play around with the `countryinfo ` library and even explore more features. 

Simple, isn't it? Hope this tutorial has helped. I would strongly recommend you to Check out the [YouTube video](https://www.youtube.com/watch?v=Eb3naUPN3G8) of the same and **don't forget to subscribe to my Channel**.

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Fetch%20data%20of%20any%20country). **Drop a star** if you find it useful.

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

- https://pypi.org/project/countryinfo/
- https://github.com/porimol/countryinfo

See you in my next Blog article, Take care!!