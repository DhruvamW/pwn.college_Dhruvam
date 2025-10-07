# STTARTTING BACKHROUNDED PROCESSES
In this challenge I have to launch a process directly in the background.

## My solve
**Flag:** `pwn.college{wjAyvyl17YseBVbt948YPGDLIOQ.QX5QDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that /challenge/run will give me the flag if I launch it directly in the background.
```bash
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 146
hacker@processes~starting-backgrounded-processes:~$ 


Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{wjAyvyl17YseBVbt948YPGDLIOQ.QX5QDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-  to start a process backgrounded all you have to do is append a & to the command.

## References
No references used.

