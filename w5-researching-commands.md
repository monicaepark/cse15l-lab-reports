# Walkthrough: researching and running commands in linux
in this week's lab report, we'll be researching about different commands in linux and running them in a directory called "technical" from a class repository called "docsearch."

## Part 1: Researching commands
This week, we were given 3 commands we could explore further: `less`, `find` or `grep`. I wanted to know a little more about the differences between find and grep, and decided to do a quick google search. I landed at [this](https://stackoverflow.com/questions/43165447/what-is-the-difference-between-find-with-grep) stack overflow page, where I found this helpful response by TheSprinter:
![Image](/w5/w5-sprinter.png)

Based on this response, I learned that find is used to filter through a directory to locate specific files or folders, while grep (short for globally search a regular expression 
and print) searches through a specific file to find a specific pattern. This makes sense, since find takes the input of the command `find` followed by a directory, while `grep` 
also requires a regular expression that the program tries to match against the files in the specified directory. Since `find` seems a bit broader, I decided to search the manual for 
how to use find, by running `man find`. The result I got was:
![Image](/w5/w5-man.png)
By scrolling down, I found a list of different filter options we can use under the `find` command! Two options that stood out to me were `-depth` and `-maxdepth` since we just started looking to graph traversals in our CSE12 class. The commands were described likeso:

```
-depth n
             True if the depth of the file relative to the starting point of the traversal is n.
-maxdepth n
             Always true; descend at most n directory levels below the command line arguments.
             If any -maxdepth primary is specified, it applies to the entire expression even if
             it would not normally be evaluated.  “-maxdepth 0” limits the whole search to the
             command line arguments.
```
To find two more options, I decided to try chat gpt. I searched for "what commands can i use with find in linux?" and got the response below:
![Image](w5/w5-chatgpt.png)
I will be exploring `-type` and `-print`. Print seems to be used in conjunction with a lot of the other commands, since the `find` command does not print the output to the terminal by default.

## Part 2: -depth

## Part 3: -maxdepth
## Part 4: -type
## Part 5: -print
