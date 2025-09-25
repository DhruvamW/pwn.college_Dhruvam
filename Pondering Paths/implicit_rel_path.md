# THE ROOT
In this challenge I have to execute a program using a relative path.

## My solve
**Flag:** `pwn.college{kVz8aJFX9S1QSHCcKdFdGg_kqLa.QX5QTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to run execute the '/challenge/run' program in a current working directory (cwd) of '/' using a relative path. I changed my directory using the 'cd' command with the '/' directory as an argument and finally exceuted the 'challenge/run' command.

```bash
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{kVz8aJFX9S1QSHCcKdFdGg_kqLa.QX5QTN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that cwd doesn't matter for absolute paths but does for relative paths. Relative paths don't start with '/'. A relative path is interpreted relative to the current working directory (cwd). The cwd is the directory in which the prompt is currently located at. 

## References 
https://www.youtube.com/watch?v=b67Jq6IZ3U8&list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC&t=1144s


