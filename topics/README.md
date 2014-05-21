# Topics

CTF challenges are usually categorized into one of these broad groups, and although at times they may be labeled, it is usually up to the competitor to find out what type of challenge it is. Here are some broad guidelines to finding out what type of challenge is presented:

1. Is the challenge given as a web link? If following the link does not download a file, the challenge is most likely a [web](./web/) one.

2. Is the file provided an image or music file? If so, the challenge is most likely a [steganography](./steganography/) one.

3. If the file is a jumbled text file, it is most likely a [cryptography](./cryptography/) challenge.

4. If the file provided is not readily identifiable, the best tool to use is the [file](../tools/file/README.md) command, which tells you what type of file it is.

    * If the file output is PCAP or relating to packets, the challenge is a [web](./web) one.

    * If the file output is an ELF file, it is most likely a [reversing](./reversing/) challenge.

    * If the file output is an executable, it is most likely a [reversing](./reversing/) challenge.
