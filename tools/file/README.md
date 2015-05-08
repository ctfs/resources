# File command

`file` returns the detected type of a file.

# Use

Pass any file as a parameter for `file` to get the filetype

```
$ file file.c
file.c: C program text
```
# How it Wroks
file compares the [magic numbers](http://en.wikipedia.org/wiki/Magic_number_%28programming%29#Magic_numbers_in_files) which are the first few bytes of a file that identifies a file and compares it against a local database on a system. Most files with tampered magic numbers won't run on it's native editor (for instance, if you tamper with magic numbers of a docx file and try to open it with Microsoft Word, Microsoft Word will yell at you in all likelihood)

You can manually do this if somehow you don't have file. Generally it's represented in hex so you could dump it with xxd and google the first few bytes. In some cases it's even valid ASCII (for instance PNG's magic numbers consist of the ASCII characters PNG)

# More

* `man file`

* [file](https://en.wikipedia.org/wiki/File_command)

