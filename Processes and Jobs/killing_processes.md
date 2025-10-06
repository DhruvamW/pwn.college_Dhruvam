# LISTING PROCESSES
In this challenge I have to kill a running process to get the flag.

## My solve
**Flag:** `pwn.college{81BWFjl87-8TI_Dh094VH5NdT4q.QXyQDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that /challenge/run will refuse to run while /challenge/dont_run is running. So I first got the PID of /challenge/dont_run by ps -ef. The I used kill command with the PID as the argument to kill the process. Then I ran /challenge/run to get the flag. 
```bash
hacker@processes~killing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 08:04 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 08:04 ?        00:00:00 /run/dojo/bin/sleep 6h
root         135       1  0 08:04 ?        00:00:00 su -c /challenge/.launcher hacker
hacker       136     135  0 08:04 ?        00:00:00 /challenge/dont_run
hacker       137     136  0 08:04 ?        00:00:00 sleep 6h
hacker       148       1  0 08:04 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --interface 0.0.0.
hacker       152     148  0 08:04 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       167     152  0 08:05 pts/0    00:00:00 ps -ef
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{81BWFjl87-8TI_Dh094VH5NdT4q.QXyQDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- kill will terminate a process in a way that gives it a chance to get its affairs in order before ceasing to exist.
- sleep is a program that simply hangs out for the number of seconds specified on the commandline
- kill to terminate it by passing the process identifier (the PID from ps) as an argument.

## References
No references used.

