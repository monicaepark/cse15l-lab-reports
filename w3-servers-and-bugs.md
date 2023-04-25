# Tutorial: How to create servers and troubleshoot bugs
a quick introduction to how to set up a server, as well as deal with failure-inducing inputs through jUnit testing

in this week's lab report, we'll be creating a server called `StringServer` to learn about URLhandlers and servers. After that, we will explore how to find and fix bugs in code by analyzing different inputs, symoptoms, and fixes to our code.

## Part 1: let's get started with StringServer!
To begin, every student created a fork of the provided repository ([click here](https://github.com/ucsd-cse15l-f22/wavelet)), which contains an implementation of the URL handler interface that we needed to create the server. From here, we forked the repository, created a clone in github desktop, then opened the folder in VS Code. From here, I used the provided NumberServer template to craft my StringServer.
![Image](/w2/w2-1stringserver.png)
![Image](/w2/w2-2stringserver2.png)
Here, the handleRequest method uses getPath and getQuery method calls to decipher what the input url is saying, breaking down the user's url address into a path (`add-message`) as well as the query (`?s=<string>`) which is the string that the user writes in the url to be printed on the server! Each input gets added to a running string, and each added string is printed on a new line using the line break escape key, `\n`. Here are some examples of queries added to the url, which then print out to the server!
![Image](/w2/w2-3localhost6050.png)
![Image](/w2/w2-4addmessage.png)
![Image](/w2/w2-5spaces.png)
![Image](/w2/w5-6manymessage.png)
One interesting thing to note is that spaces typed in the omnibar are converted into `%20` which prints out as a space in the server below. Even if you directly type in %20, this will not print out but is interpretted as a space symbol in the server.

## Part 2: bugs, symptoms, and debugging

more text blah blah

![Image](2a pw.png)

## Part 3: some things I learned in this lab

text

Thank you for reading :)
