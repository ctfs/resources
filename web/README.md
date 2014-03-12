#Web

Web challenges in CTF competitions usually involve the use of HTTP (or similar protocols) and technologies involved in information transfer and display over the internet like PHP, CMS's (e.g. Django), SQL, Javascript, and more.  There are many tools used to access and interact with the tasks which are usually hosted on servers which are then connected to by the client, typically the competitor.  Although web browsers are the most common and well known way of interacting with the internet, tools like `curl` and `nc` allow for extra options and parameters to be passed and utilized.

###Example

*Need a Server*

##Detection

Web challenges are usually easy to find and reach, as they are always presented as either urls, `www.example.com`, or IP addresses, `127.0.0.1:8080`. Some may require special services like telnet or netcat, `nc`, to work correctly, but in general most work in the web browser.

##Command Line and the Web

If you are running linux and want extended functionality (like passing custom headers and parameters) in web challenges, bash (terminal) commands are your best bet.  `cURL` is a simple but extensible [command-line tool for transferring data using various protocols](http://en.wikipedia.org/wiki/CURL), and allows users to use HTTP to interact with servers, including [POST and GET methods](http://en.wikipedia.org/wiki/HTTP#Request_methods).

###Example

To see `curl` at work, you can simply run `curl 8.8.8.8` (Google), and the html of Google's home page should appear.

There are many other options and flags that can be passed to `curl`, making it an extremely useful tool in CTFs

##Sources/See More

[Wikipedia and HTTP](http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)
