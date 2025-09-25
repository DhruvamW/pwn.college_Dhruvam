# THE ROOT
In this challenge I have to execute a program from a specific path which is not intially given to me.

## My solve
**Flag:** `pwn.college{cVK5DDNCc0-411_juIKvm0DKOAj.QX2QTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to run execute the '/challenge/run' command in a particular which was not given initially. When I tried to run that file initially it showed that I was in the wrong directory and gave me the correct directory. I changed my directory using the 'cd' command with the given directory as an argument and finally exceuted the '/challenge/run' command.

```bash
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /proc/131 directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /proc/131
hacker@paths~position-thy-self:/proc/131$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{cVK5DDNCc0-411_juIKvm0DKOAj.QX2QTN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that I can navigate around directories by using the cd (change directory) command and passing a path to it as an argument. Also, '~' shows the current path that my shell is located at.

## References 
https://www.youtube.com/watch?v=b67Jq6IZ3U8&list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC&t=1144s


