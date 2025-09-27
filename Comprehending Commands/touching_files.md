# TOUCHING FILES
In this challenge I have to create two files in a particular directory to get the flag.

## My solve
**Flag:** `pwn.college{06u5tLT2I7KjQkx41987o3QS7rY.QXwMDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to create '/tmp/pwn' and '/tmp/college' files using the 'touch' command and then run '/challenge/run' file to get the flag.
```bash
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ ls
bin  college  hsperfdata_root  pwn  tmp.4mK6TfTSUV
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{06u5tLT2I7KjQkx41987o3QS7rY.QXwMDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that 'touch' command is used to new blank file.

## References 
No references used.

