# THE ROOT
In this challenge I have to execute a program using a relative path.

## My solve
**Flag:** `pwn.college{859IcJS0IKxBRjE3Xaj0gNEtBk3.QXxUTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to run execute the '/challenge/run' program directly from '/challenge' directory using a relative path. I changed my directory using the 'cd' command with the '/challenge' directory as an argument and finally exceuted the './run' command.

```bash
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{859IcJS0IKxBRjE3Xaj0gNEtBk3.QXxUTN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that Linux does execute a program with a simple path like 'run' when the shell is located a particular directory. This is a safety measure as if Linux searched the current directory for programs every time I enter a naked path, I could accidentally execute programs in my current directory that happen to have the same names as core system utilities. As a result, the above command will yield the following error:
```bash
bash: run: command not found
```
## References 
https://www.youtube.com/watch?v=b67Jq6IZ3U8&list=PL-ymxv0nOtqqRAz1x90vxNbhmSkeYxHVC&t=1144s

