## How to make your own Google Chrome Extension

You can refer to my video tutorial for the same on [YouTube](https://youtu.be/ZWbPtPHR4hY)

%[https://youtu.be/ZWbPtPHR4hY]
*Do you use chrome extensions?*
*Have you ever thought of making one?*

This tutorial will guide you on how easily to build a chrome extension on your own. 

[Repository for Ultimate Resource in python](https://github.com/ayushi7rawat/Ultimate-Python-Resource-Hub). Drop a star if you find it useful! Got anything to add? Open a PR on the same!

## **What is a Chrome Extension?**
**Extensions** are small software programs that customize the browsing experience. They enable users to tailor Chrome functionality and behaviour to individual needs or preferences.

They are built on web technologies such as **HTML, JavaScript, and CSS**.

Extension files are zipped into a single `.crx ` package that the user downloads and installs. This means extensions do not depend on content from the web, unlike ordinary web apps.

Extensions are distributed through the **Chrome Developer Dashboard** and published to the Chrome Web Store.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/zh30o139rn2qu32fbv5r.jpg)

## **Time to Code!**
You can find the code and necessary files at my [Github Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Google%20Chrome%20Extension)

Start by creating a new directory to store the extension's files.

### **manifest.json**
We first need to define a `manifest.json` file. So create a new JSON file in the directory.

The manifest.json file contains important information that defines the extension. The format of the information in the file is JSON.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/0so7m1mkrhzsxepvrtz0.png)

Define the *name*, *version*, *description* of the extension seperated by commas, give the version as `"version": "0.0.1"` and `"manifest_version": 2`  

Next, we will define the *browser action*. It will display the extension to the top right corner of your Chrome browser. We will define *default_popup* and *default_icon* inside *browser action*.

When you click on the extension, *default_popup* will open `demo.html` file. We will create the `demo.html` file next.

`"default_icon": "logo.png"` will define the default image that you see as the extension icon. 
Now we are ready to create `demo.html` file.

### **demo.html**

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/dnw68s16xek08tbi9nmg.png)

Define the H1 tag `<h1> Hello there, I am working! </h1>` 

When you click on the extension, *default_popup* will open `demo.html` file.

## **Adding the Extension**
Go the Chrome Extensions. You can click on this [link](chrome://extensions/) to navigate to the extension page.
Once you open the page, it will look something like this.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/7ra6rn8rlm7t8916z5k8.png)

Now you need to turn on the **Developer Mode** on the top right corner of the page. You can see it highlighted in the above image.

Once you enable it, your webpage should reload and it will look like this.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/198ywlvlaplx65fyiqvs.png)


Now, you need to click **Load Unpack** option and Locate the directory that you have just created and select the folder. 
Once done you will see something like this.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/p1git2bp39skrjkhz13f.png)

And your extension is loaded to your local machine. Next, you need to navigate to your extension manager.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/bzcaiwiemw4nbsihe1h0.png)

And pin your extension so that is it becomes visible on extension bar.

And your extension is ready! Click on the extension.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/1z11e2w36x82m6a2wli1.png)

You can play around with your HTML, CSS and Javascript code files to make your own chrome extension. 

You can also publish your extension. Follow the steps if you wish to do so.

## **Publishing the Extension**

In order to publish your extension, you need to navigate to **Chrome webstore** by clicking this [link](https://chrome.google.com/webstore/devconsole/register)

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/sy4pyzmj3r9pvdafao5b.png)

You need to first accept the **agreement** and pay 5$ to **Register** and follow along with the steps to get it published.

You can find the code and necessary files at my [Github Repository](https://github.com/ayushi7rawat/Youtube-Projects/tree/master/Google%20Chrome%20Extension)


You can also connect with me on [twitter](https://twitter.com/ayushi7rawat)

I hope this helped you in understanding how to build your own chrome extension.
If you have any Queries or Suggestions, please reach out to me in the Comments Section below.
Also, have a look at my other Blogs:
- [Python 3.9: All You need to know](https://ayushirawat.com/python-39-all-you-need-to-know)
- [The Ultimate Python Resource hub](https://ayushirawat.com/the-ultimate-python-resource-hub)
- [GitHub CLI 1.0: All you need to know](https://ayushirawat.com/github-cli-10-all-you-need-to-know)
- [Become a Better Programmer](https://ayushirawat.com/become-a-better-programmer)
- [Create your own Audiobook from any pdf with Python](https://ayushirawat.com/create-your-own-audiobook-from-any-pdf-with-python)
- [You are Important & so is your Mental Health!](https://ayushirawat.com/you-are-important-and-so-is-your-mental-health)

Resource:
https://developer.chrome.com/extensions