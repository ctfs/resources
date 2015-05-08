# Hex Editor

> With a hex editor, a user can see or edit the raw and exact contents of a file, as opposed to the interpretation of the same content that other, higher level application software may associate with the file format. For example, this could be raw image data, in contrast to the way image editing software would interpret and show the same file. -- [Wikipedia](http://en.wikipedia.org/wiki/Hex_editor)

> Hex is an abstraction between ASCII and Binary essentially. So it's a slightly simpler way to show data compared to binary using [0-9][A-F] for default ASCII (example: 5A in hex means Z in ASCII)

In CTF challenges hex editors have many use cases like Steganography, Reverse Engineering

*Todo: Basic usage of one of the editors.*

## Linux

Most people seem to prefer the [xxd](http://linuxcommand.org/man_pages/xxd1.html) command as it is fairly simple to use and you don't have to leave your terminal.

xxd isn't used as an interactive hex editor per-se as much as a converting tool. xxd infile.in outfile.out will take the hex from infile.in and dump it to outfile.out. After manipulating it as needed, one can do xxd -r to reverse it back from hex to ASCII.

By default if there isn't an outfile provided, the hex of the infile will be dumped to your terminal (more formally known as stout).

In case you are interested in a GUI based application - try [wxHexEditor](http://sourceforge.net/projects/wxhexeditor/). It is cross-platform so you can use the same setup over multiple OSes.

## Windows

There is a port of xxd for Win32 available in this [package](http://www.weihenstephan.de/~syring/win32/UnxUtilsDist.html).

[HxD](http://mh-nexus.de/en/hxd/) is a nice GUI based editor.

## References

[Comparison of Hex Editors](http://en.wikipedia.org/wiki/Comparison_of_hex_editors)
