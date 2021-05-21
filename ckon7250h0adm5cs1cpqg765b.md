## Automate Cowin Vaccine slots Availability using Python

Hello Reader! 

I hope you all are safe and sound and at home. Do not step out of your house unless it’s absolutely necessary with proper precautions.

Coronavirus cases are increasing day by day. The second wave has hit very badly in many areas. It’s very important to get vaccinated. But, getting a slot seems next to impossible. Even I am not able to get my hands on one. So I was trying to think of a better idea possible and if you know me, you must know by now that I am a python freak, so I tried to automate the availability of the slot.

So in this blog post, I am going to tell you how you can automate the vaccine slots availability and get notified when a slot is available. We will see the implementation in python.

For your ease, you can use the code and it's available at my GitHub repository.  Spread this article as much as possible so that everyone can get notified about the availability of slots and we all can get vaccinated.

[Check out the Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

You can refer to my **YouTube video Tutorial** to see a working tutorial for better understanding and a step-by-step guide of the same. 

%[https://www.youtube.com/watch?v=HrTQqSKWClE]

## What will be covered in this Blog

```python
1. What is Web Scraping?
2. The Web-Scaping Process and its Uses.
3. What is Coronavirus and CoWin?
4. How to Automate vaccine slots availability
```

*Let's get started!*

## **What is Web Scrapping?**:

### **Introduction**

If you’ve ever copy and pasted information from a website, you’ve performed the same function as any web scraper, only on a microscopic, manual scale.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1620927483952/aZsYiKSmv.png)
**Web scraping**, also known as web data extraction, is the process of retrieving or “scraping” data from a website. This information is collected and then exported into a format that is more useful for the user. Be it a spreadsheet or an API.

**Two important points** to be taken into consideration here:

1. Always be respectful and try to get permission to scrape, do not bombard a website with scraping requests, otherwise, your IP address may get blocked!
2. Be aware that websites change often, meaning your code could go from working to totally broken from one day to the next.

### **The process: three simple steps**

1. Request for a response from the webpage
2. Parse and extract with the help of Beautiful soup and `lxml`
3. Download and export the data with pandas into excel

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1620927507127/6RR_Ifg0p.png)
### **Its Uses**:

It can serve several purposes, the most popular ones are Investment Decision Making, Competitor Monitoring, News Monitoring, Market Trend Analysis, Appraising Property Value, Estimating Rental Yields, Politics and Campaigns, and many more.

If you wish to know about it further. I am attaching the [Wikipedia](https://en.wikipedia.org/wiki/Web_scraping) link here. You can have a look.

## **What is Coronavirus?**

I do not think **Coronavirus** needs an introduction, but just in case if someone does not know, Coronavirus disease (COVID-19) is an infectious disease caused by a newly discovered coronavirus.

The COVID-19 virus spreads primarily through droplets of saliva or discharge from the nose when an infected person coughs or sneezes

If you wish to know about it further. I am attaching the [Wikipedia](https://en.wikipedia.org/wiki/Coronavirus) link here. You can have a look.

## **What is CoWin?**

Under the universal immunization program, for several years, India has been using a vaccine intelligence system called eVIN (electronic vaccine intelligence network),  CoWIN is an extension of eVIN. CoWIN stands for Covid Vaccine Intelligence Work. 

> it is the gateway to vaccination and the backbone of the vaccination drive.

## The data source
We will make use of the cowin official website. 
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1620927620877/1pKYIYAkc.png)

## Module Used:

#### requests Module:

- Use the requests library to grab the page.
- This may fail if you have a firewall blocking Python.
- Sometimes you need to run this twice if it fails the first time.

Now that you are familiar with *Coronavirus and CoWin* and have acquired basic knowledge of *Web Scrapping and requests module,* we can move forward to *the coding section.*

## Time to Code!

You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/CoWin-Vaccine-Notifier). **Drop a star** if you find it useful.

![carbon.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1620927692352/fMB_taYIQ.png)

*Let's understand this!*

In order to access the Python library, you need to install it into your Python environment

```python
pip install requests
```

Now, we need to import the package into our python script. Use the following command to do so.

```python
import requests

from datetime import datetime, timedelta
import time

import json
```

Now that we have imported the libraries, let's proceed. 

Let's display a welcome message. we will make use of `print` method for the same.

```python
print("Starting search for Covid vaccine slots!")
```

Now, let's set some basic parameters,

```python
age = 52
pinCodes = ["462003"]
print_flag = 'Y'
num_days = 2
```

- The Slots are available in two categories, Age 45+ and Age 18+. Let's proceed with `Age 45+ ` for now, you can set it according to your need.
- You can perform the search based on `Pincode` or `District`. Since we are looking for the slots available nearby, I am making use of Pin-code. You can also pass multiple pin-codes, separated by `commans` in the list.
- We only want to check for slots availability for the next two days for let's give` num_days`as `2` here.
- Lastly, set the flag value to `y`.

Now let's make use of `datetime` method to calculate today's date.

```python
actual = datetime.today()

#output:
2021-05-13 13:35:24.396612
```

Now, run a loop to convert it into list format. We will make use of `timedelta` method to convert it into list format

```python
list_format = [actual + timedelta(days=i) for i in range(num_days)]

#Output:
[datetime.datetime(2021, 5, 13, 13, 39, 18, 496330), datetime.datetime(2021, 5, 14, 13, 39, 18, 496330)]
```

we will again run a loop to fetch the dates from the list and we will make use of `strftime` method to do so. Note that we are storing date in `date-month-year` format.

```python
actual_dates = [i.strftime("%d-%m-%Y") for i in list_format]

#Output:
['13-05-2021', '14-05-2021']
```

Next, we will run a while loop to fetch the details of the slots. Initially let's set the counter to zero.

Let's introduce two more loops here:

- one in order to fetch details for each pin-code.
- second in order to fetch details for each date in the given pin-code.

Now in order to get requests, let's define the URL.

```python
URL = "https://cdn-api.co-vin.in/api/v2/appointment/sessions/public/calendarByPin?pincode={}&date={}".format(pinCode, given_date)
```

If you observe, I have added parameters in the URL itself using string formatting. We are passing in two parameters here, `pincode` and `date`.  Every time the inner loop runs, this URL will be called and the respective date and pin-code will be passed as arguments for each case.

Now, in order to get the request, let's define the `header`.

```python
header = {'User-Agent': 'Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/56.0.2924.76 Safari/537.36'}      
```

Once done, let's call `requests` and we will make use of `get` method.

```python
result = requests.get( URL, headers=header)
```

Now, our response is stored in the result. Let's try printing it out. We will make use of `text` method for the same.

```python
print(result.text)

#OUTPUT:

{"centers":[{"center_id":691508,"name":"Navin Girls HSS Tulsi Nagar 18","address":"1250 Tulsi Nagar HOSPITAL","state_name":"Madhya Pradesh","district_name":"Bhopal","block_name":"PHANDA","pincode":462003,"lat":23,"long":77,"from":"09:00:00","to":"17:00:00","fee_type":"Free","sessions":[{"session_id":"b63ce111-23dd-4d4e-9f1c-c97073c57a52","date":"13-05-2021","available_capacity":0,"min_age_limit":18,"vaccine":"COVAXIN","slots":["09:00AM-11:00AM","11:00AM-01:00PM","01:00PM-03:00PM","03:00PM-05:00PM"]}]},{"center_id":570554,"name":"SAHTI Vaishali Kotra 
KNK","address":"Govt. Higher Sec. Kamla Nehru Girls School Teenshed TT Nagar","state_name":"Madhya Pradesh","district_name":"Bhopal","block_name":"PHANDA","pincode":462003,"lat":23,"long":77,"from":"09:00:00","to":"17:00:00","fee_type":"Free","sessions":[{"session_id":"93144388-6dca-4f7c-9aba-ecd5b120fa94","date":"13-05-2021","available_capacity":215,"min_age_limit":45,"vaccine":"COVISHIELD","slots":["09:00AM-11:00AM","11:00AM-01:00PM","01:00PM-03:00PM","03:00PM-05:00PM"]}]},{"center_id":592476,"name":"25 Battalion Campus BhadBhada","address":"25th Battalion Bhadbhada Bhopal","state_name":"Madhya Pradesh","district_name":"Bhopal","block_name":"PHANDA","pincode":462003,"lat":23,"long":77,"from":"09:00:00","to":"17:00:00","fee_type":"Free","sessions":[{"session_id":"b857cd10-b46f-404f-a5de-81032b667e46","date":"13-05-2021","available_capacity":0,"min_age_limit":45,"vaccine":"COVAXIN","slots":["09:00AM-11:00AM","11:00AM-01:00PM","01:00PM-03:00PM","03:00PM-05:00PM"]}]},{"center_id":570591,"name":"GHMC- Ward 29 Office 18","address":"Pandit Khushilal Sharma Parisar","state_name":"Madhya Pradesh","district_name":"Bhopal","block_name":"PHANDA","pincode":462003,"lat":23,"long":77,"from":"09:00:00","to":"17:00:00","fee_type":"Free","sessions":[{"session_id":"5bcd92b4-a476-4c47-a203-3e96179e5beb","date":"13-05-2021","available_capacity":0,"min_age_limit":18,"vaccine":"COVISHIELD","slots":["09:00AM-11:00AM","11:00AM-01:00PM","01:00PM-03:00PM","03:00PM-05:00PM"]}]},{"center_id":609392,"name":"Govt School Nayabasera 18","address":"NAYABASERA SANJEEVANI","state_name":"Madhya Pradesh","district_name":"Bhopal","block_name":"PHANDA","pincode":462003,"lat":23,"long":77,"from":"09:00:00","to":"17:00:00","fee_type":"Free","sessions":[{"session_id":"60306cc5-15a4-4195-876a-2889676631c0","date":"13-05-2021","available_capacity":0,"min_age_limit":18,"vaccine":"COVISHIELD","slots":["09:00AM-11:00AM","11:00AM-01:00PM","01:00PM-03:00PM","03:00PM-05:00PM"]}]},{"center_id":561924,"name":"Saraswati Shisu Mandir Sch Cov","address":"Saraswati Shishu Mandir School Shivaji Nagar Bhopal Madhya Pradesh India","state_name":"Madhya Pradesh","district_name":"Bhopal","block_name":"PHANDA","pincode":462003,"lat":23,"long":77,"from":"09:00:00","to":"17:00:00","fee_type":"Free","sessions":[{"session_id":"e1f4f7a1-42d5-4f58-934b-ed031fc3e7c0","date":"13-05-2021","available_capacity":137,"min_age_limit":45,"vaccine":"COVISHIELD","slots":["09:00AM-11:00AM","11:00AM-01:00PM","01:00PM-03:00PM","03:00PM-05:00PM"]}]},{"center_id":591027,"name":"CD RAJ BHAVAN CVX","address":"RAJ BHAVAN BHOPAL","state_name":"Madhya Pradesh","district_name":"Bhopal","block_name":"PHANDA","pincode":462003,"lat":23,"long":77,"from":"09:00:00","to":"17:00:00","fee_type":"Free","sessions":[{"session_id":"52de668d-5526-4e09-8c41-f34c1912302d","date":"13-05-2021","available_capacity":0,"min_age_limit":45,"vaccine":"COVAXIN","slots":["09:00AM-11:00AM","11:00AM-01:00PM","01:00PM-03:00PM","03:00PM-05:00PM"]}]},{"center_id":667429,"name":"CD Vallabh Bhawan CVX","address":"Vallabh Bhawan Bhopal","state_name":"Madhya Pradesh","district_name":"Bhopal","block_name":"PHANDA","pincode":462003,"lat":23,"long":77,"from":"09:00:00","to":"17:00:00","fee_type":"Free","sessions":[{"session_id":"e8202c2d-b545-401c-b266-8bf9102687e2","date":"13-05-2021","available_capacity":0,"min_age_limit":45,"vaccine":"COVAXIN","slots":["09:00AM-11:00AM","11:00AM-01:00PM","01:00PM-03:00PM","03:00PM-05:00PM"]}]},{"center_id":561310,"name":"Govt Kanya School Nehru Nagar","address":"Govt Kanya School Nehru Nagar","state_name":"Madhya Pradesh","district_name":"Bhopal","block_name":"PHANDA","pincode":462003,"lat":23,"long":77,"from":"09:00:00","to":"17:00:00","fee_type":"Free","sessions":[{"session_id":"85a85c27-cabd-4058-b902-7b0bf457cb44","date":"13-05-2021","available_capacity":114,"min_age_limit":45,"vaccine":"COVISHIELD","slots":["09:00AM-11:00AM","11:00AM-01:00PM","01:00PM-03:00PM","03:00PM-05:00PM"]}]},{"center_id":636442,"name":"CD VIDHAN SABHA COVISHIELD","address":"VIDHAN SABHA","state_name":"Madhya Pradesh","district_name":"Bhopal","block_name":"PHANDA","pincode":462003,"lat":23,"long":77,"from":"09:00:00","to":"17:00:00","fee_type":"Free","sessions":[{"session_id":"6010b80f-a818-4cf5-ad67-90a0cb49f1d6","date":"13-05-2021","available_capacity":0,"min_age_limit":45,"vaccine":"COVISHIELD","slots":["09:00AM-11:00AM","11:00AM-01:00PM","01:00PM-03:00PM","03:00PM-05:00PM"]}]},{"center_id":611640,"name":"Kopal HSS Nehru Nagar18","address":"Kopal HSS Nehru Nagar Bhopal","state_name":"Madhya Pradesh","district_name":"Bhopal","block_name":"PHANDA","pincode":462003,"lat":23,"long":77,"from":"09:00:00","to":"17:00:00","fee_type":"Free","sessions":[{"session_id":"b4a74e1f-cc5b-498a-b92d-25bf5c3bc072","date":"13-05-2021","available_capacity":0,"min_age_limit":18,"vaccine":"COVAXIN","slots":["09:00AM-11:00AM","11:00AM-01:00PM","01:00PM-03:00PM","03:00PM-05:00PM"]}]},{"center_id":639426,"name":"BANGANG WARD 25 CVX","address":"SANJEEVNI BANGANGA","state_name":"Madhya Pradesh","district_name":"Bhopal","block_name":"PHANDA","pincode":462003,"lat":23,"long":77,"from":"09:00:00","to":"17:00:00","fee_type":"Free","sessions":[{"session_id":"def621bf-2e3e-4514-a605-9debd696d8ef","date":"13-05-2021","available_capacity":0,"min_age_limit":45,"vaccine":"COVAXIN","slots":["09:00AM-11:00AM","11:00AM-01:00PM","01:00PM-03:00PM","03:00PM-05:00PM"]}]},{"center_id":636455,"name":"JAHANGIRABAD SANJEEVANI","address":"JAHANGIRABAD","state_name":"Madhya Pradesh","district_name":"Bhopal","block_name":"PHANDA","pincode":462003,"lat":23,"long":77,"from":"09:00:00","to":"18:00:00","fee_type":"Free","sessions":[{"session_id":"a58f02b7-a252-4daf-a541-b7ddf9bae21c","date":"19-05-2021","available_capacity":0,"min_age_limit":45,"vaccine":"COVISHIELD","slots":["09:00AM-11:00AM","11:00AM-01:00PM","01:00PM-03:00PM","03:00PM-06:00PM"]}]},{"center_id":627202,"name":"CD Sewaniya Gaud","address":"CD Sewaniya Gaud","state_name":"Madhya Pradesh","district_name":"Bhopal","block_name":"PHANDA","pincode":462003,"lat":23,"long":77,"from":"09:00:00","to":"18:00:00","fee_type":"Free","sessions":[{"session_id":"80130fd2-483a-4bb7-876a-9f2130484994","date":"19-05-2021","available_capacity":0,"min_age_limit":45,"vaccine":"COVISHIELD","slots":["09:00AM-11:00AM","11:00AM-01:00PM","01:00PM-03:00PM","03:00PM-06:00PM"]}]}]}
```

This data is not structured. So, we will make use of `json` here. Let's cast the data into `json` file.

```python
if result.ok:
    response_json = result.json()
```

Now, In order to retrieve the information for each center, we will run a loop for the same. Initially, let's set the `flag` as `false`

```python
flag = False
if response_json["centers"]:            
    if(print_flag.lower() =='y'):
        for center in response_json["centers"]:
```

Now, let's display and verify our data for each center

```python
print(center)

#OUTPUT:

{'center_id': 691508, 'name': 'Navin Girls HSS Tulsi Nagar 18', 'address': '1250 Tulsi Nagar HOSPITAL', 'state_name': 'Madhya Pradesh', 'district_name': 'Bhopal', 'block_name': 'PHANDA', 'pincode': 462003, 'lat': 23, 'long': 77, 'from': '09:00:00', 'to': '17:00:00', 'fee_type': 'Free', 'sessions': [{'session_id': 'b63ce111-23dd-4d4e-9f1c-c97073c57a52', 'date': '13-05-2021', 'available_capacity': 0, 'min_age_limit': 18, 'vaccine': 'COVAXIN', 'slots': ['09:00AM-11:00AM', '11:00AM-01:00PM', '01:00PM-03:00PM', '03:00PM-05:00PM']}]}
```

And now finally we can retrieve the information for each session. We will apply the check parameters as the arguments we saved earlier.

```python
for session in center["sessions"]:
    if (session["min_age_limit"] <= age and session["available_capacity"] > 0 ):
```

If it stratifies our conditions, let's display the result. 

```python
print('Pincode: ' + pinCode)
print("Available on: {}".format(given_date))
print("\t", center["name"])
print("\t", center["block_name"])
print("\t Price: ", center["fee_type"])
print("\t Availablity : ", session["available_capacity"])

if(session["vaccine"] != ''):
    print("\t Vaccine type: ", session["vaccine"])
    print("\n")
```
At the end, let's increase the counter by one. 
```
counter += 1
```

Let's cover the edge case:

```python
if(counter == 0):
    print("No Vaccination slot avaliable!")
else:
    print("Search Completed!")
```

Lastly, let's sync the data in real-time.

```python
dt = datetime.now() + timedelta(minutes=3)

while datetime.now() < dt:
    time.sleep(1)
```

Let's have a look at the output and let's compare it with the actual website.


![output.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1620928058807/gr7IbLcQT.png)

![Screenshot_1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1620928072634/0ZWiUXgeq.png)


![Screenshot_2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1620928105083/EeLymW8CK.png)
And with that, it's a wrap! You can host the script at the server to get notified every time a slot is available near you. You can find all the code at my [GitHub Repository](https://github.com/ayushi7rawat/CoWin-Vaccine-Notifier). **Drop a star** if you find it useful.

Simple, isn't it? Hope this tutorial has helped. I would strongly recommend you to Check out the [YouTube video](https://www.youtube.com/watch?v=HrTQqSKWClE) of the same and **don't forget to subscribe to my Channel**. 

I write about career, Blogging, programming, and productivity, If this is something that interests you, please share the article with your friends and connections. You can also subscribe to my newsletter to get updates every time I write something!

Thank you for reading, If you have reached so far, please like the article, It will encourage me to write more such articles.  Do share your valuable suggestions, I appreciate your honest feedback!

I would love to connect with you at [Twitter](https://twitter.com/ayushi7rawat) | [LinkedIn](https://www.linkedin.com/in/ayushi7rawat/).


You should definitely check out my other Blogs:

- [Python 3.9: All You need to know](https://ayushirawat.com/python-39-all-you-need-to-know)
- [The Ultimate Python Resource hub](https://ayushirawat.com/the-ultimate-python-resource-hub)
- [GitHub CLI 1.0: All you need to know](https://ayushirawat.com/github-cli-10-all-you-need-to-know)
- [Become a Better Programmer](https://ayushirawat.com/become-a-better-programmer)
- [How to make your own Google Chrome Extension](https://ayushirawat.com/how-to-make-your-own-google-chrome-extension-1)
- [Create your own Audiobook from any pdf with Python](https://ayushirawat.com/create-your-own-audiobook-from-any-pdf-with-python)
- [You are Important & so is your Mental Health!](https://ayushirawat.com/you-are-important-and-so-is-your-mental-health)

## Resources:

- [https://apisetu.gov.in/public/marketplace/api/cowin#/Appointment%20Availability%20APIs/calendarByPin](https://apisetu.gov.in/public/marketplace/api/cowin#/Appointment Availability APIs/calendarByPin)
- https://www.cowin.gov.in/home
- https://pypi.org/project/requests/

See you in my next Blog article, Take care