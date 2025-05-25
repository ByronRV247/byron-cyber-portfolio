"The NTFS file system provides applications the ability to create alternate data streams of information. 
By default, all data is stored in a file's main unnamed data stream, but by using the syntax 'file:stream', 
you are able to read and write to alternates." 

![Image](https://github.com/user-attachments/assets/02caf0d2-8dfd-4488-b05d-06634bef9848)

The streams output tells us there's a hidden alternate data stream (ADS) named ads.txt attached to file.txt.
Now that you've found the stream, just run:

notepad "C:\Users\Administrator\Desktop\file.txt:ads.txt"

This will open the hidden stream (ads.txt) inside file.txt using Notepad.
