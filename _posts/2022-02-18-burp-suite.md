---
 title: What is Burp Suite. 
 tags: [burp suite, burp]
 style: fill
 color: success
 description: Hello Everyone, This blog will be focusing on installation and use of Burp Suite.
---

# Burp Suite

## Introduction
This article will give a brief introduction to what Burp Suite is and the tools offered by BurpSuite. If you are a complete beginner in Web Application Pentest/Web App Hacking/Bug Bounty, we would recommend you to just read through without thinking too much about any term.

## What is Burp Suite?
Burp Suite is an application that consists of a set of tools used for penetration testing of web applications. It is developed by a company called Portswigger.
Burp Suite aims to be an all-in-one set of tools and its capabilities can be enhanced by installing add-ons that are called BApps.
Burp Suite is available in three versions, that are: 
1. Community edition.
2. Professional edition.
3. Enterprise edition.
Burp Suite is the most popular tool in the midst of all professional web application security researchers and bug bounty hunters.
It is very easy to use and this reason makes it a more suitable choice over all other free alternatives like Netsparker, Veracode, and OWASP ZAP.

## Some of the tools offered by Burp Suite are :
1. Target.
2. Proxy. 
3. Intruder.
4. Repeater.
5. Sequencer. 
6. Decoder. 
7. Comparer.
8. Logger.
9. Extender.

Now let us explore these tools in detail,

#### 1. Target
The Target tool gives you an overview of your target application's content and functionality, and lets you drive key parts of your testing workflow. The target tool consists of three tabs, that are as follows : 

- Site Map
- Scope
- Issue Definitions

***Site map***

The site map displays information about the contents and security issues that have been discovered in target applications. It lets you view the full requests and responses for individual items, and the full details about the issues found.

<img src="/assets/images/bp1.png" alt="image" width="650" height="760">


***Scope*** 

Target scope is used to tell Burp Suite what you're currently interested in testing. By defining a target scope, you can include only what you need to test right now and exclude every content that is outside your work. Doing this also improves performance and memory usage.

<img src="/assets/images/bp2.png" alt="image" width="650" height="760">

***Issue definitions*** 

It is a list that contains the definitions of all issues that can be detected by Burp Scanner.

<img src="/assets/images/bp3.png" alt="image" width="650" height="760">


### 2. Proxy 
The proxy tool operates as a web proxy server and gives you a direct view of how your target application works at the back end. It lets you intercept, view, and modify all requests and responses passing between your browser and destination web servers. The proxy tool consists of four tabs, that are as follows :

- Intercept
- HTTP history
- Websocket history
- Options

***Intercept***  

If intercept is on, it prevents every request from continuing to a destination to get a response.

<img src="/assets/images/bp4.png" alt="image" width="650" height="760">

***HTTP history*** 

Proxy history maintains a full record of all messages that have passed through the Proxy. It updates automatically even if the intercept is turned off. You can also put filters settings that filter by Request type, MIME type, Status code, Search item, file extension, annotation, and listener.

<img src="/assets/images/bp5.png" alt="image" width="650" height="760">

***Websocket history*** 

This displays the history of all WebSocket traffic sent between Burp's browser and your target applications. WebSockets provide long-lived connections for streaming data and other asynchronous traffic.

<img src="/assets/images/bp6.png" alt="image" width="650" height="760">

***Options*** 

Through this tab, you can perform many operations like: 

- You can configure your browser to use one of the listeners as its proxy server. 
- You can control which requests, responses, and WebSocket messages should be stalled for viewing and editing in the intercept tab. 
- You can use this tab to perform the automatic modification of responses.
- You can use this tab to automatically replace parts of requests and responses passing through the proxy.

By using this tab, you can specify destination web servers for which Burp will directly pass through a TLS connection.

You can also control some specific details of Burp Proxy's behavior by using this tab.

<img src="/assets/images/bp7.png" alt="image" width="650" height="760">


### 3. **Intruder**
An intruder is a tool for automating customized attacks against web applications. It is used for Bruteforce attacks on passwords and other such forms, Also used for testing and attacking web applications. This tool has four tabs:

- Positions
- Payload
- Resource Pool
- Options


***Positions*** 

This tab is used to select the attack type and configure the positions where the payload will be inserted.

<img src="/assets/images/bp8.png" alt="image" width="650" height="760">

***Payloads*** 

Through this tab, you can define one or more payload sets, configure a list of payloads, can define rules to perform various processing tasks on each payload before it is used, and can also do URL-encoding with the final payload for safe transmission within HTTP requests.

<img src="/assets/images/bp9.png" alt="image" width="650" height="760">

***Resource Pool*** 

Through this tab, you can specify the resource pool(used to manage the use of system resources accross multiple tasks) in which the attack will run.

<img src="/assets/images/bp10.png" alt="image" width="650" height="760">

***Options***

This tab performs many functions like: 

- It allows you to save your attack to your current project file.
- It controls whether the intruder updates the configured request headers and handles network errors during the attack.
- It controls what information is captured in the attack result.
- It controls how Burp handles redirection when performing the attack.
- It controls Grep-match, Grep-extract, and Grep-payloads.

<img src="/assets/images/bp11.png" alt="image" width="650" height="760">

### 4. **Repeater**
This tool lets a user send requests repeatedly with manual modifications.

<img src="/assets/images/bp12.png" alt="image" width="650" height="760">


### 5. **Sequencer**
A sequencer is a tool that checks the quality of randomness in an application's session tokens or other important data items that are intended to be unpredictable, such as anti-CSRF tokens, password reset tokens, and many more. This tool consists of three tabs, that are:

- Live Capture
- Manual Load
- Analysis Options

***Live Capture*** 

This tab sends requests here from other tools to configure a live capture, configure other options below like selecting the location in the response where the token appears, and control the engine used for making HTTP requests and harvesting tokens while performing live capture. After configuring all the options, we can click on 'start live capture'.

<img src="/assets/images/bp13.png" alt="image" width="650" height="760">

***Manual load***

This tab allows you to load sequencer with a sample of tokens that you have already obtained, and then perform the statistical analysis on the sample.

<img src="/assets/images/bp14.png" alt="image" width="650" height="760">

***Analysis options***

This tab helps to control how tokens are handled during the analysis and the types of analysis that are performed at the character level.

<img src="/assets/images/bp15.png" alt="image" width="650" height="760">

### 6. **Decoder**

A decoder is a simple tool for transforming encoded data into readable form, or for transforming raw data into encoded and hashed format creating a payload for various vulnerabilities.

<img src="/assets/images/bp16.png" alt="image" width="650" height="760">

### 7. **Comparer**

This function lets you do a comparison between different requests or responses. You can load, paste, or send data here from other tools and then select the comparison you want to perform.

<img src="/assets/images/bp17.png" alt="image" width="650" height="760">

### 8. **Logger**

A logger is a tool for recording network activity. It records all HTTP traffic that Burp Suite generates, for investigation and analysis of the data.

<img src="/assets/images/bp18.png" alt="image" width="650" height="760">

### 9. **Extender**

The extender allows you to use Burp add-ons, to extend Burp's functionality using your own or third-party code. You can load and handle these add-ons, view details about installed add-ons, install add-ons from the BApp Store, view the current Burp Extender API, and configure options for how add-ons are handled.

<img src="/assets/images/bp19.png" alt="image" width="650" height="760">

I HOPE THIS BLOG MAY HELP ALL THE READERS
THANK YOU FOR READING MY BLOG :)
