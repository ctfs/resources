# Cryptography

## Quick Start

1. Is the text relatively small? a few sentences?

    * Is the text 32 characters long? Most likely an [md5](./md5/) hash

    * 40 characters long? Most likely a [SHA1](./sha1/) hash

    * Are there equal signs spread out through the text, often next to each other? Probably a [base64](./base64/) encoded string

    * Is the text only letters, without numbers or special characters?

        * Check if it is a [Caesar](./caesar-cipher/), [Vigenere](./vigenere-cipher/), or other type of cipher

    * Rarely, it may be a keyboard map as found in the [Olympic CTF 2014](https://github.com/ctfs/write-ups/tree/master/olympic-ctf-2014/crypting)

2. Any hints about keys? signing? most likely [RSA](./rsa/)


##About

> Cryptography is the practice and study of techniques for secure communication in the presence of third parties. - [Wikipedia](http://en.wikipedia.org/wiki/Cryptography)

In the case of CTFs, the goal is usually to crack or clone cryptographic objects or algorithms to reach the flag.

###Example

If you look around the folders in this page you should be able to find a suitable way to solve this simple cipher:

```
Hint: Julius Caesar's favorite cipher

kxn iye lbedec
```

##Sources/See More

[Introduction to Cryptography](http://www.cs.umd.edu/~waa/414-F11/IntroToCrypto.pdf)

