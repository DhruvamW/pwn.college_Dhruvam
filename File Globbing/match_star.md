# MATCHING WITH *
In this challenge I have to change my directory using globbing.

## My solve
**Flag:** `pwn.college{QneC6iAj6RbnxMzqKHiOp1l1FiN.QXxIDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to change my directory to /challenge using cd command and using no more than four characters in my argument. I used globbing technique to pass the address of /challenge as the argument to cd command.
```bash
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ ./run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{QneC6iAj6RbnxMzqKHiOp1l1FiN.QXxIDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that globbing lets us reference files without typing them all out, or typing out their full paths. One such glob is *. When the shell encounters a * character in any argument, the shell will treat it as a "wildcard" and try to replace that argument with any files that match the pattern.When zero files are matched, by default, the shell leaves the glob unchanged.The * matches any part of the filename except for / or a leading . character. 

## References
No references used.

