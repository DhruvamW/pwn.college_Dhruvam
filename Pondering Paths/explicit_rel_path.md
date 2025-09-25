# THE ROOT
In this challenge I have to execute a program using an explicit relative path.

## My solve
**Flag:** `pwn.college{gghOPz3b20hDMYYULmzfSTZ6DdP.QXwUTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to run execute the '/challenge/run' program in a current working directory (cwd) of '/' using an explicit relative path. I changed my directory using the 'cd' command with the '/' directory as an argument and finally exceuted the './challenge/run' command which is explicitly relative.

```bash
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ challenge/run
Incorrect...
This challenge must be called with a relative path that explicitly starts with a `.`!
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{gghOPz3b20hDMYYULmzfSTZ6DdP.QXwUTN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that implicit relative path directly specified the directory to descend into from the current directory. '.', refers right to the same directory.

## References 
https://www.youtube.com/watch?v=b67Jq6IZ3U8&list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC&t=1144s

