## HTTP Status Codes that You must know

Hello reader! 

Whenever a client sends a request to the server, the response always contains a status code. You might not see it always but it's returned at every client-server interaction. Well, even if you are not a programmer, you would still know about the 404 Not Found error.

In this blog post, we will discuss all about HTTP and its response status codes. Consider this as a small cheat sheet, for your references, every time you encounter one.

## What will be covered in this Blog

```python
1. What is HTTP?
2. What is Status code?
3. 1XX - Informational codes
4. 2XX - Success codes
5. 3XX - Redirection codes
6. 4XX - Client error codes 
7. 5XX - Server error codes
```

*Let's get started!*

## What is HTTP?

HTTP which stands for **Hypertext Transfer Protocol**. According to the Wikipedia definition:

> The Hypertext Transfer Protocol is an application layer protocol for distributed, collaborative, hypermedia information systems.

HTTP is a client-server protocol, acts as the foundation of any data exchange on the Web. Each interaction between the client and server is called a message. HTTP messages are requests or responses. Client devices submit HTTP requests to servers, which reply by sending HTTP responses back to the clients.

## What is Status code?

At every client request, the server responds with a code that helps to communicate the status of the request. It is a quick way to inspect if the request was successful or not without investing in the response body. 

These codes are formed by three numbers indicating the status of a web element. There are basically five standard groups in which status codes are divided and they can be identified by the first digit of the code. They are as follows:

1. **1XX - Informational codes** 
2. **2XX - Success codes** 
3. **3XX - Redirection codes** 
4. **4XX - Client error codes** 
5. **5XX - Server error codes**

Let's have a look at each group briefly and discuss the most common status codes.

## 1XX - Informational Response

An informational response indicates that the request was received and understood. It is issued on a provisional basis while request processing continues. 

**100 - Continue:** The server has received the request headers and the client should proceed to send the request body. It states that the client request is good and processing.

**101 - Switching Protocols**: The requester has asked the server to switch protocols and the server has agreed to switch. Basically, the request may involve file operations, requiring a long time to complete the request.

**102 - Processing**: This code indicates that the server has received and is processing the request, but no response is available yet.

**103 - Early Hints**: Used to return some response headers before final HTTP message.

## 2XX - Success

This class of status codes indicates the action requested by the client was received, understood, and accepted.

**200 - OK: **Standard response for successful HTTP requests. Everything's normal and the requested resource has been returned through the message body.

**201 - Created: **The request has been fulfilled, resulting in the creation of a new resource and the server has acknowledged it. 

**202 - Accepted:** This code indicates that the server has received and is processing the request, but no response is available yet.

**204 - No Content:** The server successfully processed the request, and is not returning any content. Generally, the PUT method is used for a 204 response.

## 3XX - Redirection

This group of status code indicates that the client must take additional action to complete the request.

**301 - Moved Permanently**: This indicates that the URL has been moved once and for all. This is used to inform the browser that the requested file has been moved and can be used to redirect from a page that is no longer in existence.

**305 - Use Proxy**: The requested resource is available only through a proxy, the address for which is provided in the response.

**307 - Temporary Redirect**: In this scenario, the response code indicates that the requested resource has been temporarily moved to another URI. however, future requests should still use the original URI.

## 4XX - Client errors

This class of status code is intended for situations in which the error seems to have been caused by the client.

**400 - Bad Request**: The server cannot or will not process the request due to wrong syntax causing an error.

**401 - Unauthorized**: Response is similar to *403 Forbidden*, but specifically for use when authentication is required and has failed or has not yet been provided. The requested file can be a protected one.

**403 - Forbidden**: The request contained valid data and was understood by the server, but the server is refusing action. It's possible that the server might not have permission to share the file with the client.

**404 - Not Found**: The requested resource could not be found or does not exist but may be available in the future.

**405 - Method Not Allowed:** A request method is not supported for the requested resource; eg, a PUT request on a read-only resource.

**414 URI Too Long**: The URI provided was too long for the server to process as a result of too much data being encoded as a query string of a GET request.

**429 Too Many Requests**: The user has sent too many requests in a given amount of time, helps increase the security.

## 5XX - Server errors

You can encounter a server error when the client has raised a valid request, The server failed to fulfill the request.

**500 - Internal Server Error**: An error message, displayed when an unexpected situation was encountered that does not match any other class errors.

**501 - Not Implemented**: The server either does not recognize the request method, or it lacks the ability to fulfill the request.

**502 - Bad Gateway**: The server acts as a gateway and received an invalid response from the server while making the request.

**503 - Service Unavailable**: The server cannot handle the request because it is overloaded or down for maintenance.

That's all for this article and with that, it's a wrap! I hope you found the article useful. Thank you for reading, If you have reached so far, please like the article, It will encourage me to write more such articles. Do share your valuable suggestions, I appreciate your honest feedback!

I create content about **Career, Blogging, Programming, and Productivity**, If this is something that interests you, please share the article with your friends and connections. You can also subscribe to my newsletter to get updates every time I write something!

I would strongly recommend you to Check out the [YouTube video](https://www.youtube.com/watch?v=jAOkWehMF6E) of the same and **don't forget to subscribe to my Channel**. I would love to connect with you at [Twitter](https://twitter.com/ayushi7rawat) | [LinkedIn](https://www.linkedin.com/in/ayushi7rawat/).

You should definitely check out my other Blogs:

- [Python 3.9: All You need to know](https://ayushirawat.com/python-39-all-you-need-to-know)
- [GitHub CLI 1.0: All you need to know](https://ayushirawat.com/github-cli-10-all-you-need-to-know)
- [How to make your own Google Chrome Extension](https://ayushirawat.com/how-to-make-your-own-google-chrome-extension-1)
- [Run Javascript from Python](https://ayushirawat.com/run-javascript-from-python)
- [Automate WhatsApp using Python](https://ayushirawat.com/automate-whatsapp-using-python)
- [Automate Cowin Vaccine slots Availability using Python](https://ayushirawat.com/automate-cowin-vaccine-slots-availablity-using-python)
- [What is Competitive Programming](https://ayushirawat.com/what-is-competitive-programming-or-beginners-guide)

### Resources:

- https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol
- https://en.wikipedia.org/wiki/List_of_HTTP_status_codes

See you in my next Blog article, Take care!!