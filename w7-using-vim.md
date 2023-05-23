# walkthrough: editing files with vim through a remote server
in this week's lab report, i will be dmonstrating how to edit a file through vim in the command line, then commiting and pushing those changes to my github account to actualize the change in the repository file. i am working on a macbook, so keep that in mind for some of the special characters.

## the task
![Image](/w7/tasks.png)
here is the task outlined on the CSE15L course page! i will walk through each one of these steps by stating what keystrokes were used and providing a brief explanation.

## keystrokes & explanations

### Log into ieng6
![Image](/w7/ieng6.png)
*keystrokes:* `ssh <space> cs15lsp23sc@ieng6-201.ucsd.edu <enter>` 

logged into my student account through secured shell

### clone your fork of the repository from your Github account
![Image](/w7/removing.png)
*keystrokes:* `git <space> clone <space> <cmd>+v <enter>`, then `rm <space> -rf <space> lab7 <enter>`

tried to clone the repo into a new directory (pasted the ssh from github with `<cmd>+c` and pasted with `<cmd>+v`), received an error message that lab7 already exists (from the last lab class), then removed this file to make room for the new lab7

![Image](/w7/clone_fork.png)
*keystrokes:* `git <space> clone <space> <cmd>+v <enter>`

tried again and succeeded!

### run the tests, demonstrating that they fail
i forgot what test to run, so I referred to my notes from last week's lab:
![Image](/w7/notes_lab.png)

from here, i copied the bash command with `<cmd>+c` and pressed `<cmd>+<tab>` to return to vscode.

![Image](/w7/tests_fail.png)
*keystrokes*: `pwd <enter>`, `ls <enter>`, `cd <space> lab7 <enter>`, `<cmd>+v`

i checked what directory i was in with pwd, checked what is inside the directory with ls, changed directories to lab7, and pasted my test command from the notes. the output was `FAILURES!!!` as expected. (why is linux so aggressive T-T)

![Image](/w7/bash_file.png)
*keystrokes:* `cat <space> test.sh <enter>`

i was also curious what is inside this tester file, so i checked the contents with cat. they were just the junit testers ^^

### edit the code file to fix the failing test
![Image](/w7/vim.png)
*keystrokes:* `vim <space> List <tab> .java <enter>`

i then ran vim on the buggy file, which is called `ListExamples.java`. instead of typing out the full file, i typed the first few letters and clicked `<tab>` to autofill until `ListExamples` then finished typing out the extension and entered vim.

![Image](/w7/search_index1.png)
*keystrokes:* `/index1 <enter>`

since i already knew that the bug was with incrementing `index1` rather than `index2`, i navigated to the error through the search function. the forward slash starts the search function, then i looked for `index1`.

![Image](/w7/n9times_l5times_r2.png)
*keystrokes:* `nnnnnnnnnlllllr2 <enter>`

once in search mode, i clicked n 9 times to navigate to the 9'th instance of `index1` (which is where the error occurred), then used l to move my cursor to the right, and r to replace the 1 with a 2.

![Image](/w7/colon_wq_enter.png)
*keystrokes:* `:wq <enter>`

i then saved these changes and exited vim.

### run the tests, demonstrating that they now succeed
![Image](/w7/tests_pass.png)
*keystrokes:* `<up> <up> <up> <enter>`

since I ran the bash tests earlier, i accessed the command from my bash history by clicking the up arrow until i found `bash test.sh` to run the tests. they passed!

### commit and push the resulting change to your Github account (you can pick any commit message!)
![Image](/w7/commit_push.png)
*keystrokes:* `git <space> add List <tab> .java <enter>`, `git <space> commit <space> -m <space> "Updated the final while loop to increment index2, not index1." <enter>`, `git <space> push`

lastly, i added this file to the staging area (using `<tab>` to autocomplete the file name) using `git add`, saved those changes to the repository with a message using `git commit -m`, and finally uploaded those local commits to the remote repository (ieng6) using `git push`.

## takeaways

overall, i had fun learning how to use vim with this simple task! i initially tried to write this lab report on vim, but realized writing on github was much easier for me when i need to write a lot of text. i think vim would be more useful if i'm editing files that are already written and i just want to look through the contents and make small changes.
