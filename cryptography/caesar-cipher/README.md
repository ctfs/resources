#Caesar Cipher

The [Caesar Cipher](http://en.wikipedia.org/wiki/Caesar_cipher) is a very simple and common encryption method which does not appear often in full-fledged CTFs but is a good basis for cryptography.

A Caesar Cipher is the shift of a string of letters a certain number of positions up or down the alphabet.

###Example

Let's say we want to encrypt the string `hello world` to give to our right-handed friend whose favorite number is 3.  We will shift our string **left 3**.

Taking the first letter `h` in our string and going 3 places up the alphabet(as it is a left shift) gives us the letter `e`. We then start our new, encrypted string with the letter.

Doing so for the whole original string creates a jumbled mess of incomprehensible letters to anyone but the reader with the proper decryption shift:

**Original:** `hello world`

**Final:**    `ebiil tloia`

To give this to our friend, we would send him the final string with the instructions **right 3**, and either by hand, with a website, or with a script, he would be able to extract our extremely important message.

##Detection

Caesar ciphers are usually presented in very low-point tasks, if at all, and can be easy to detect and check for.  Strings containing incomprehensibly jumbled letters can very likely be Caesar ciphers and should be checked.

##Solution

There are many approaches to cracking Caesar ciphers, but most commonly the best way to solve them is to write a script or run the string through a website (Options presented below) which will print out all the possible shifts of a string.  At that point the most comprehensible and logical solution can be chosen.

##Sources/See More

[Wikipedia and Caesar Ciphers](http://en.wikipedia.org/wiki/Caesar_cipher)

[Quick and Simple Decryption Tool](http://www.xarg.org/tools/caesar-cipher)
