# LISTING PROCESSES
In this challenge I have to find a file name from the running processes.

## My solve
**Flag:** `pwn.college{UtVBjtjQB5ohIA8n3wgiTF7_9AY.QX4MDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that /challenge/run has been renamed to a random filename, and we cannot ls the /challenge directory. But it is launched so I can find it in the running process list. I used ps -ef to view all the running processes and found the secret file name.
```bash
hacker@processes~listing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 07:54 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 07:54 ?        00:00:00 /run/dojo/bin/sleep 6h
root         132       1  0 07:54 ?        00:00:00 /challenge/14610-run-768
root         135     132  0 07:54 ?        00:00:00 sleep 6h
hacker       146       1  0 07:54 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --interface 0.0.0.
hacker       150     146  0 07:54 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       160     150  0 07:54 pts/0    00:00:00 ps -ef
hacker@processes~listing-processes:~$ /challenge/14610-run-768
Yahaha, you found me! Here is your flag:
pwn.college{UtVBjtjQB5ohIA8n3wgiTF7_9AY.QX4MDO0wiN4EzNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
```

## What I learned
Through this challenge I learnt that:
-  ps just lists the processes running in your terminal.
- "Standard" Syntax: in this syntax,we can use -e to list "every" process and -f for a "full format" output, including arguments. These can be combined into a single argument -ef.
- "BSD" Syntax: in this syntax, we can use a to list processes for all users, x to list processes that aren't running in a terminal, and u for a "user-readable" output. These can be combined into a single argument aux.
- Both ps -ef and ps aux truncate the command listing to the width of your terminal.
-  we can pass the w option twice (e.g., ps -efww or ps auxww) to disable the truncation.

## References
No references used.

