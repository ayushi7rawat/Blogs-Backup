## Web Scraping Coronavirus Data into MS Excel

You can refer to my video tutorial for the same at YouTube 

%[https://www.youtube.com/watch?v=CTRYYz1u7Y8]

Coronavirus cases are increasing rapidly worldwide. This tutorial will guide you on how to web scrape Coronavirus data and into Ms-excel.

## **What will be covered in this blog**
- Introduction to Web Scrapping
- Understanding HTML basics
- How to scrape a website
- How to export the data into excel file

## **Pre Requisites**
```
- python
- Beautiful soup
- pandas
- HTML
- CSS
```

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/cei3i2ma6vbk415590d9.png)

## **What is Web Scrapping?**

### **Introduction**
If you’ve ever copy and pasted information from a website, you’ve performed the same function as any web scraper, only on a microscopic, manual scale.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/0kd6oj5a2en38mjz8kt3.png)

**Web scraping**, also known as web data extraction, is the process of retrieving or “scraping” data from a website. This information is collected and then exported into a format that is more useful for the user. Be it a spreadsheet or an API.

**Two important points** to be taken into consideration here:

1. Always be respectful and try to get permission to scrape, do not bombard a website with scraping requests, 
otherwise, your IP address may get blocked!

2. Be aware that websites change often, meaning your code could go from working to totally broken from one day to the next.

### **The process: three simple steps**

1. Request for a response from the webpage 
2. Parse and extract with the help of Beautiful soup and lxml
3. Download and export the data with pandas into excel

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/v5wz5n3rhrtfchk4so97.png)

### **Its Uses**
It can serve several purposes, most popular ones are Investment Decision Making, Competitor Monitoring, News Monitoring, Market Trend Analysis, Appraising Property Value, Estimating Rental Yields, Politics and Campaigns and many more.

If you wish to know about it further. I am attaching the [Wikipedia](https://en.wikipedia.org/wiki/Web_scraping) link here. You can have a look.

## **What is Coronavirus?**
I do not think **Coronavirus** needs an introduction, but just in case if someone does not know, Coronavirus disease (COVID-19) is an infectious disease caused by a newly discovered coronavirus.

The COVID-19 virus spreads primarily through droplets of saliva or discharge from the nose when an infected person coughs or sneezes

If you wish to know about it further. I am attaching the [Wikipedia](https://en.wikipedia.org/wiki/Coronavirus) link here. You can have a look.

## **The data source**
We need a webpage to fetch the coronavirus data from. So I am using the [Worldometer](https://www.worldometers.info/coronavirus/#countries) website here.

You can use the attached link to navigate to the website. You can also refer [WHO](https://www.who.int/health-topics/coronavirus#tab=tab_2) website
Worldometer's webpage will look something like this

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/vwniebtxy3x0rxdn7a7o.png)

We are interested in the data contained in a table at Worldometer’s website, where it lists all the countries together with their current reported coronavirus cases, new cases for the day, total deaths, new deaths for the day, etc

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/jwm8t3oeuamll91txi6a.png)

Now we are ready to start the coding.

## **Time to Code**
You can find the code at my [Github Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Web%20Scraping%20Coronavirus%20Data%20into%20MS%20Excel)

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/1fcd9og7mcudm4bkggpl.png)

*Let's Understand it*

There are a few libraries you will need, so first, you need to install them.
Go to your command line and install them.

```
pip install requests
pip install lxml
pip install bs4
```
Now let's see what we can do with these libraries.

### **Understanding HTML basics**
This is the basic syntax of an HTML webpage. Every <tag> serves a block inside the webpage:

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/b59h2xf3v5om22c9bmn5.png)

- `<!DOCTYPE html>`: HTML documents must start with a type declaration.
- The HTML document is contained between `<html>` and `</html>` .
- The meta and script declaration of the HTML document is between `<head>` and `</head>` .
- The visible part of the HTML document is between `<body>` and `</body>` tags.
- Title headings are defined with the `<h1>` through `<h6>` tags.
- Paragraphs are defined with the `<p>` tag.
- Other useful tags include `<a>` for hyperlinks, `<table>` for tables, `<tr>` for table rows, and `<td>` for table columns.

### **requests**
- Use the requests library to grab the page.
- This may fail if you have a firewall blocking Python/Jupyter.
- Sometimes you need to run this twice if it fails the first time.

```
import requests

#make requests from webpage
result = requests.get('https://www.worldometers.info/coronavirus/country/india/')

print(result.text)
```
The request library that we downloaded goes and gets a response, to get a request from the webpage, we use `requests.get(website URL)` method. 

If the request is successful, it will be stored as a giant python string. We will be able to fetch the complete webpage source code when we run `result.text` . 

But the code will not be structured.

### **Beautiful soup**

BeautifulSoup library already has lots of built-in tools and methods to grab information from a string of this nature (basically an HTML file). 
It is a Python library for pulling data out of HTML and XML files. 

Using BeautifulSoup we can create a "soup" object that contains all the "ingredients" of the webpage. 

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/oreg0sk1h9nmbfbxfqtu.png)

If u wish to know more about BeautifulSoup, I am attaching the [Documentation](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) link here. You can have a look.

```
import bs4

soup = bs4.BeautifulSoup(result.text,'lxml')
print(soup)
```

And now import B.S. for the next step is to actually create the `soup` variable. And we're gonna pass on two things here, `result.text` string and `lxml` as a string.

Lxml goes through this HTML document and then figure out what is a CSS class, What is a CSS I.D. , Which are the different HTML elements and tags etc.

### **Extracting the data**
**Find the div**
To find the element you need to right-click and hit inspect on the number of cases. Refer the attached snapshot below.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/55ubcz0husi4ive93y94.png)

we need to find the right class. `class_= 'maincounter-number'` serves our purpose. Refer the attached snapshot below.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/jynok67bmoznvaz9bccp.png)

The Beautiful Soup object has been created in our Python script and the HTML data of the website has been scraped off of the page. Next, we need to get the data that we are interested in, out of the HTML code.

```
cases = soup.find_all('div' ,class_= 'maincounter-number')
print(cases)
```

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/56x8eckaanh2egl3ri4j.png)

There is still a lot of HTML code that we do not want. Our desired data entries is wrapped in the HTML div element and inside `class_= 'maincounter-number'` . We can use this knowledge to further clean up the scraped data.

### **Storing the data**

we need to save the scraped data in some form that can be used effectively. For this project, all the data will be saved in a Python **List**. To achieve this we will:

```
data = []
  
#find the span and get data from it
for i in cases:
    span = i.find('span')
    data.append(span.string)

print(data)
```

we will use `span` to fetch data from `div`.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/1fnn5xcrnml0lmgmcs88.png)

We need the numbers, we do not want us to be dealing with the tags. So we will use `span.string` to get the numbers. 

We will update the numbers into the `data ` list

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/7f0qrt6jpxyrma61o4qq.png)

Now that we have the numbers we are ready to export our data into an excel file.

### **Exporting the data**
Our last step is to export the data to Ms-excel. To fulfil the purpose, I am making use of **Pandas**

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/gujja45g5md39qhjih67.jpg)

To load the pandas package and start working with it, import the package. The community agreed alias for pandas is pd, so loading pandas as pd is assumed standard practice. 

If u wish to know more about Pandas, I am attaching the [Documentation](https://pandas.pydata.org/docs/) link here. You can have a look.

```
import pandas as pd
  
df = pd.DataFrame({"CoronaData": data})

#naming the coloumns
df.index = ['TotalCases', ' Deaths', 'Recovered']

#file-name
df.to_csv('Corona_Data.csv')
```

DataFrame is a 2-dimensional labelled data structure, potentially heterogeneous tabular data structure with labelled axes (rows and columns).

`df = pd.DataFrame({"CoronaData": data})` is used to create a DataFrame and give it a name and map it to the `data` list that we created earlier.

Next, we will give column names with `df.index` . It will look something like this.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/2zg8j2x66mx463j65xy1.png)

Final step,
We are ready to export the data into Ms-excel. We will use `df.to_csv` for the same

Here's our result

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/5n7ljqgcyocuovdugja5.png)

NOTE: The output depends on the current statistics

You can find the code at my [Github Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Web%20Scraping%20Coronavirus%20Data%20into%20MS%20Excel)


You can also connect with me on [Twitter](https://twitter.com/ayushi7rawat)

I hope this helped you in understanding how to Web scrape coronavirus data into excel. 

If you have any Queries or Suggestions, feel free to reach out to me in the Comments Section below.

Resources:
- https://www.crummy.com/software/BeautifulSoup/bs4/doc/
- https://pandas.pydata.org/docs/
- https://en.wikipedia.org/wiki/Web_scraping
- https://en.wikipedia.org/wiki/Coronavirus
- https://www.worldometers.info/coronavirus/#countries