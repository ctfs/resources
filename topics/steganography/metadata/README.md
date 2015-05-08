# What is Metadata

Metadata is identifying information written in a file, almost always in plaintext. This information can include, but is not limited to, copyright information, original file editor, image title and/or description, etc. A few of the most common types are XMP and Exif. Exif can be easily torn apart [here](exifdata.com/exif.php) but be wary of "click here for more details", as knowing CTFs they've probably put information there. Flags have even been put in directly as a metadata field. 

Another raw and dirty way to view metadata is to run *strings whateverfile.jpg | more* or if you support it *strings whateverfile.jpg | column | more*

Strings works for more than just metadata and is basically cat but filters out non-human readable information.
