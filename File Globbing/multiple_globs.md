# MULTIPLE GLOBS
In this challenge I have to reference multiple files using multiple globs in a single command.

## My solve
**Flag:** `pwn.college{IQmXiv_-p2dl-VZq1vRg8L6uzVR.0lM3kjNxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to provide a single argument to /challenge/run which is 3 characters using two * globs in it that covers every word that contains the letter p. *p* refers to every file that contains the letter p in it.
```bash
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{IQmXiv_-p2dl-VZq1vRg8L6uzVR.0lM3kjNxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that for a command like /*fl*  the shell looks for all files in / that start with anything (including nothing), then have an f and an l, and end in anything.

## References
No references used.

