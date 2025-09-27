# LISTING FILES
In this challenge I have to find and run the file with the flag in it.

## My solve
**Flag:** `pwn.college{cYMOBeQl9qK-KIeGpGwPHkmdAlx.QX4IDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to read the flag from '/challenge/run/ file but the run had be renamed to a random name which I had to find out. I found the file using the 'ls' command with '/challenge' as the argument to list out all the files in the /challenge directory.
```bash
hacker@commands~listing-files:~$ ls /challenge
27991-renamed-run-29683  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/27991-renamed-run-29683
Yahaha, you found me! Here is your flag:
pwn.college{cYMOBeQl9qK-KIeGpGwPHkmdAlx.QX4IDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that 'ls' command lists all the contents of the directory that has been given as an argument to the command.

## References 
No references used.

