#Reversing

Reversing in the context of CTFs is usually the reverse engineering of software (executables/bin files) into assembly code and at times the original source to understand what is happening in a program, break a program (e.g. buffer overflows), or to decrypt encryptions done by a program.

##Detection

The easiest way to analyze a file for reversing is to use the `file` command in linux, which will tell you what any file is detected to be. For example most linux executables will be ELF files, while respective source files like `.c` or `.py` will be presented as their respective file-types.

##Solution

By far the most prominent tool for dealing with binaries is the tool [IDA](https://www.hex-rays.com/products/ida/).  IDA is an extremely thorough tool which allows for a variety of interactions with binaries, but ultimately allows you to see the assembly for programs and how code blocks flow throughout a program.

##Sources/See More

[File command](http://unixhelp.ed.ac.uk/CGI/man-cgi?file)

[IDA](https://www.hex-rays.com/products/ida/)