# ESET crackme writeup - Part 1

This post is a description of my solution to the [ESET crackme](https://join.eset.com/en/challenges/crack-me). It will cover the analysis and solution of the first file, that can be downloaded from the link above.

## Downloading and opening
When clicking the "DOWNLOAD THE CRACKME.EXE PROGRAM" button on the website, the file received is named crackme.zip. Since I couldn't open it as a zip archive, I analyzed it with a Hex Editor:

![First few bytes of crackme.zip](./file_format.PNG)

Apparently, this is simply a PE file. I changed its name to crackme.exe and executed it (within a VM, of course).

![Executing crackme.exe](./run_first_time.PNG)

So far, so standard.

## Initial Analysis

The next step would be opening the file within IDA and running it with a debugger. While I do have access to an IDA license, it does not include an x86 Decompiler, and thus the analysis will be done in assembly.
IDA recognizes the file as a standard PE and auto-analyzes it properly. Once it is done, I take a look at the Strings window and find nothing interesting at all. Specifically, the prompt displayed when running is not there:

![Only boring strings here.](./no_strings_attached.PNG)

[Link back home](../README.md).
