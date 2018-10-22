# Hex Editor

> With a hex editor, a user can see or edit the raw and exact contents of a file, as opposed to the interpretation of the same content that other, higher level application software may associate with the file format. For example, this could be raw image data, in contrast to the way image editing software would interpret and show the same file. - [Wikipedia](http://en.wikipedia.org/wiki/Hex_editor)

In CTF challenge tasks, hex editors have many use cases - like Steganography, Reverse Engineering.

## Linux / OSX

Most people seem to prefer [xxd](http://linuxcommand.org/man_pages/xxd1.html), as it is fairly simple to use, and you don't have to leave your terminal console.

Sample output:

```
$ xxd isengard2 | head
00000000: 7f45 4c46 0201 0100 0000 0000 0000 0000  .ELF............
00000010: 0300 3e00 0100 0000 380f 0000 0000 0000  ..>.....8.......
00000020: 4000 0000 0000 0000 0000 0000 0000 0000  @...............
00000030: 0000 0000 4000 3800 0300 4000 0000 0000  ....@.8...@.....
00000040: 0100 0000 0500 0000 0000 0000 0000 0000  ................
00000050: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00000060: 2b18 0000 0000 0000 2b18 0000 0000 0000  +.......+.......
00000070: 0000 2000 0000 0000 0100 0000 0600 0000  .. .............
00000080: 0000 0000 0000 0000 0020 0000 0000 0000  ......... ......
00000090: 0020 0000 0000 0000 0000 0000 0000 0000  . ..............
```

There is also [hexdump](http://man7.org/linux/man-pages/man1/hexdump.1.html), which is shipped by default.

Sample output:

```
$ hexdump isengard2 | head
0000000 7f 45 4c 46 02 01 01 00 00 00 00 00 00 00 00 00
0000010 03 00 3e 00 01 00 00 00 38 0f 00 00 00 00 00 00
0000020 40 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0000030 00 00 00 00 40 00 38 00 03 00 40 00 00 00 00 00
0000040 01 00 00 00 05 00 00 00 00 00 00 00 00 00 00 00
0000050 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
0000060 2b 18 00 00 00 00 00 00 2b 18 00 00 00 00 00 00
0000070 00 00 20 00 00 00 00 00 01 00 00 00 06 00 00 00
0000080 00 00 00 00 00 00 00 00 00 20 00 00 00 00 00 00
0000090 00 20 00 00 00 00 00 00 00 00 00 00 00 00 00 00
```

In case you are interested in a GUI based application - try [wxHexEditor](http://sourceforge.net/projects/wxhexeditor/). It is cross-platform so you can use the same setup over multiple OSes.

Another excellent alternative is [010 Editor](https://www.sweetscape.com/010editor), by SweetScape Software.

## Windows

There is a port of xxd for Win32 available in this [package](http://www.weihenstephan.de/~syring/win32/UnxUtilsDist.html).

[HxD](http://mh-nexus.de/en/hxd/) is a nice GUI based editor.

## References

[Comparison of Hex Editors](http://en.wikipedia.org/wiki/Comparison_of_hex_editors)
