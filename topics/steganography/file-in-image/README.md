# Hiding a file in an image

One of the most common steganography tricks is to hide a file inside of an image.  The file will open normally as an image but will also hold hidden files inside, commonly zip, text, and even other image files.

The reason this works is because when an image file is read it has starting and ending bytes dictating the size of the image.  The image viewer that you use will use the information between these bytes to present an image to you, ignoring anything after the terminating byte.

For example, The terminating byte for a JPEG is FF D9 in hex, so using a hex viewer ([xxd](http://linuxcommand.org/man_pages/xxd1.html) is good for linux, or something like [HxD](http://mh-nexus.de/en/hxd/) for windows) you can find out where the image finishes.  These bytes are sometimes hard to find in a sea of numbers though, so looking at the dump of the hex (the text representing the hex bytes) can also help you find hidden .txt or .zip files.

### Example

A very simple implementation of this strategy is used in the [example.jpg](example.jpg) file in this directory. If you save it to your computer and open it up with an image viewer, you should be presented with a simple jpg image.

Now lets try to find the flag. Open up the image in your favorite hex editor and start looking around for something odd (You may find the flag itself from the dump at this point, but for the sake of example try extracting it). Near the bottom of the file you should see the terminating byte of a jpg `ffd9`:

`01e17a0: 685c 7fab 8eb4 5b32 61f1 c4ff d950 4b03  h\....[2a....PK.`

Another important part of this line is the `PK` near the end. `PK` are the initials of Phil Katz, the inventor of the zip file, and indicate that a zip file starts at that point.

Using this information we can use another handy linux tool, [`dd`](http://en.wikipedia.org/wiki/Dd_(Unix)). The `dd` command is very versatile and allows for the copying and converting of a multitude of files. In our case, we are going to be using it to extract the zip file.

We know where the location of the zip file is, but `dd` only takes decimal values, so we convert the hexadecimal location 0x01e17ad from hex to decimal to get 1972141.

Pluging this into dd:

`dd if=example.jpg bs=1 skip=1972141 of=foo.zip`

This takes in the image example.jpg, the 'in file' if, reads one block at a time, 'block size' bs,  skips to block 1972141, skip,  and writes it to the 'out file' zip we call foo.zip. When this completes you should have a zip file you can easily unzip to access the text file inside.

This is the long way of solving a simple steganography problem but shows how the strategy works. In the Solving section more concise and efficient methods are described.

## Detecting

These challenges are usually presented as a simple picture with no other instructions, and it is up to the competitor to run it through a hex editor to find out if it involves steganography.  If you are presented with an image and no instructions, your safest bet is that is has something hidden after the closing tags of the image.

## Solving

Although it is possible and at times practical to solve these tasks using linux tools like `dd`, there are some tools that make it much easier. [`Binwalk`](http://binwalk.org/) is an immensely useful tool which automatically detects and extracts files hidden with steganography tools

## CTF Example

Steganography of this type is usually not scored very highly but is decently widespread. BackdoorCTF 2014 created one which is generally straightforward, [ctfexample.jpg](ctfexample.jpg), but involves multiple layers.

## Sources/See More

[XXD](http://linuxcommand.org/man_pages/xxd1.html)

[HxD](http://mh-nexus.de/en/hxd/)

[DD](http://en.wikipedia.org/wiki/Dd_(Unix)

[Binwalk](http://binwalk.org/)
