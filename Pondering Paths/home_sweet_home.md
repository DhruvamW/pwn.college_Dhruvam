# THE ROOT
In this challenge I have to write an argument to a command to write a copy of the flag.

## My solve
**Flag:** `pwn.college{sxDUq0LKebOO4-YbxvLKL5MsLHv.QXzMDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that '/challenge/run' will write a copy of the flag to any file I specify as an argument on the commandlint. The argument had certain constraints like: argument must be an absolute path, The path must be inside the home directory and before expansion, the argument must be three characters or less.
```bash
hacker@paths~home-sweet-home:~$ /challenge/run ~/f
Writing the file to /home/hacker/f!
... and reading it back to you:
pwn.college{sxDUq0LKebOO4-YbxvLKL5MsLHv.QXzMDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that every user has a home directory, typically under '/home' in the filesystem. The ~ in a prompt is the current working directory, with ~ being shorthand for /home/hacker. The expansion of '~' is an absolute path, and only the leading '~' is expanded. This means, for example, that '~/~' will be expanded to '/home/hacker/~' rather than '/home/hacker/home/hacker'.

## References 
No References used.
