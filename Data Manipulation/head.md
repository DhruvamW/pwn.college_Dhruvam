# EXTRACTING FIRST LINES WITH HEAD
In this challenge I have to grab just the first 7 lines of a file.

## My solve
**Flag:** `pwn.college{EiDtue2gKGy1Nti7lTFBT5ZLYd5.0lNxEzNxwiN4EzNzEzW}`

It was mentioned in the problem statement that /challenge/pwn outputs a bunch of data, and I'll need to pipe it through head to grab just the first 7 lines and then pipe them onwards to /challenge/college, which will give me the flag. I used -n 7 argument with head command to grab the first 7 lines of /challenge/pwn and used pipes(|) to pipe the data to various commands.
```bash
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7| /challenge/college
Congratulations, you piped the right codes!
pwn.college{EiDtue2gKGy1Nti7lTFBT5ZLYd5.0lNxEzNxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-  head command is used to display the first few lines of its input
-  It shows the first 10 lines, but we can control this with the -n option

## References
No references used.

