# REDIRECTING OUTPUT
In this challenge I have to redirect a word to a new file.

## My solve
**Flag:** `pwn.college{8UvjR9g9VZjZvN1wZCvRCzWZR42.QX0YTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to use output redirection to write the word PWN to the filename COLLEGE.
```bash
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
flag:
pwn.college{8UvjR9g9VZjZvN1wZCvRCzWZR42.QX0YTN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that we can redirect stdout files using the > character. hacker@dojo:~$ echo hi > asdf
This will redirect the output of echo hi (which will be hi) to the file asdf.

## References
No references used.

