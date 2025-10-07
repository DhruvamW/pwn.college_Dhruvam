# BACKGROUNDING PROCESSES
In this challenge I have to run a file in the background.

## My solve
**Flag:** `pwn.college{sjUsC0lhVBgyYDaAWhqXPdmC0e7.QX3QDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that /challenge/run wants to see another copy of itself running, not suspended, and using the same terminal. I first suspended /challenge/run using Ctrl+Z and then ran it in the background using the bg command.

```bash
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         146 S+   bash /challenge/run
root         148 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the 
background, and then launch a new version of me! You can background me with 
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to 
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         146 S    bash /challenge/run
root         156 S    sleep 6h
root         157 S+   bash /challenge/run
root         159 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{sjUsC0lhVBgyYDaAWhqXPdmC0e7.QX3QDO0wiN4EzNzEzW}

```

## What I learned
Through this challenge I learnt that:
-  bg resumes processes in the background
- we can see running status of a process using ps -0
- T means that the process is suspended due to Ctrl-Z
- S in STAT column means that process is sleeping while waiting for input.
- R in stat column means that process is actively running, and the + means that it's in the foreground.

## References
No references used.

