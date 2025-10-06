# SUSPENDING PROCESSES
In this challenge I have to launch and suspend a processes to get the flag.

## My solve
**Flag:** `pwn.college{stZIXis81EF5onpiw3n50DWBiz2.QXzQDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that run wants to see another copy of itself running and using the same terminal. For this I first ran /challenge/run and then used Ctrl+Z to suspend the process to the background and then invoked /challenge/run again to get the flag.
```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{stZIXis81EF5onpiw3n50DWBiz2.QXzQDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-   You can suspend processes to the background with Ctrl-Z.

## References
No references used.

