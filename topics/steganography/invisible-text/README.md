# Invisible Text

A simple steganography trick that is often used for watermarks instead of outright steganography is the act of hiding nearly invisible text in images.  The text can be hidden by making it nearly invisible (turning down it's opacity to below 5%) or using certain colors and filters on it.  Although the text is undiscernable to the naked eye, it is still there, and there are a variety of tools which allow the text to be extracted.

### Example

Using the tactics detailed below, can you find the flag in this image?

![flag](example.png)

## Detecting

Detecting this type of steganography can be somewhat challenging, but once you know it is being used there are a multitude of tools you can use to find the flag. If you find that there are no other files hidden in the image (e.g. .zip files), you should try to find flags hidden with this method.

## Solving

There are multiple ways to find flags hidden in this manner:

* [GIMP](http://www.gimp.org/) or [Photoshop](http://www.photoshop.com/) can be used to uncover the flag by using different filters and color ranges. [This](http://www.wikihow.com/Create-Hidden-Watermarks-in-GIMP) tutorial works remarkably well for finding hidden text.

* [Stegsolve](https://www.wechall.net/forum/show/thread/527/Stegsolve_1.3/page-1) is an immensly useful program for many steganography challenges, allowing you to go through dozens of color filters to try to uncover hidden text.

* There are many scripts that have been written to substitute certain colors and make hidden the text legible, for example [this](http://pastebin.com/46VmzrRU) Ruby script highlights colors passed to it in the image.

## CTF Example

PlaidCTF 2014 had a steganography challenge recently with this image:

![ctf-example](ctf-example.png)

The write-up for this challenge can be found [here](https://github.com/ctfs/write-ups/tree/master/plaid-ctf-2014/doge-stege)

## Sources/See More


