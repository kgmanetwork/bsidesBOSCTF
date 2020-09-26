# Forensics
# Amnesia Challenge

This challenge is mostly about waiting for a tool or a command to run. There are two ways to do this challenge, you can either use GUI or command

# For GUI

Autopsy will be one of the best choice for this file since it seems to be a file system

(If you don't know how to use Autopsy, here is a pretty detail guideline for the older version of Autopsy https://www.sans.org/blog/a-step-by-step-introduction-to-using-the-autopsy-forensic-browser/)

Note: Autopsy supports Windows more than Linux but this write-up is for Linux only

After adding the image to a case on GUI Autopsy, we 'ANALYZE' it, because we don't know what kind of image it is (FAT, NTFS, etc.), so we can't find data based on file system but instead we will use
'Keyword Search' Tab on the top of the screen.

The keyword that we will use for this scenario is 'flag{'. So type in 'flag{' in the 'Enter the keyword string or expression to search for:' box, keep everything default except the 'Unicode' box. If
we search using 'Unicode', a bunch of negative results will be returned back

This is the result if you run with 'Unicode' searching on:

![ASCII+UNICODE](https://user-images.githubusercontent.com/71739262/94349139-dbf97400-000f-11eb-96ce-ce46ef8eaee3.JPG)

So ASCII is good for now, after that click 'SEARCH'

Now we wait...

After a few seconds or a few minutes depends on your system, there should be only one result appears, choose ASCII to show the result.
Take the flag!
![image](https://user-images.githubusercontent.com/71739262/94349297-26c7bb80-0011-11eb-89f0-3f124cf362a4.png)
# For CLI

We will use 'dd' command to extract information and pipe it to 'xxd' command to show it on hexadecimal. At the end, we will use 'grep' to find what we need

Note: Because 'grep' only shows the line containing match pattern, but 'xxd' usually shows output in multiple line and the ASCII column is really small, so to avoid missing out important parts of the flag,
we will use -A flag to show the number of lines after the line containing match pattern

Using command:

dd bs=1024 if=image.bin | xxd | grep flag{ -A 6

Now we wait...

Output of the command should contain the flag. Grab it!
![image](https://user-images.githubusercontent.com/71739262/94349314-5e366800-0011-11eb-867c-030d308ec549.png)

