#Web

##Quick Start

1. Login field/text input a central part of website? Likely a [SQL injection](./sql-injections/)

##About

Web challenges in CTF competitions usually involve the use of HTTP (or similar protocols) and technologies involved in information transfer and display over the internet like PHP, CMS's (e.g. Django), SQL, Javascript, and more.  There are many tools used to access and interact with the web tasks, and choosing the right one is a major facet of the challenges. Although web browsers are the most common and well known way of interacting with the internet, tools like `curl` and `nc` allow for extra options and parameters to be passed and utilized.

##Getting Started

###Command Line and the Web

If you are running linux and want extended functionality (like passing custom headers) in web challenges, bash (terminal) commands are your best bet.  `cURL` is a simple but extensible [command-line tool for transferring data using various protocols](http://en.wikipedia.org/wiki/CURL), and allows users to use HTTP to interact with servers, including [POST and GET methods](http://en.wikipedia.org/wiki/HTTP#Request_methods). Additionally, some challenges will be accessed through interactive processes, which can be connected to with programs like [netcat](https://en.wikipedia.org/wiki/Netcat) or [telnet](https://en.wikipedia.org/wiki/Telnet).

####Example

To see `curl` at work, you can simply run `curl 8.8.8.8` (Google), and the html of Google's home page should appear.

There are many other options and flags that can be passed to `curl`, making it an extremely useful tool in CTFs

##Sources/See More

[HTTP](http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)

[cURL](http://en.wikipedia.org/wiki/CURL)
