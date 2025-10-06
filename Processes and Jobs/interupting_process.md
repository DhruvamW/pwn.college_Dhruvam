# INTERUPTING PROCESSES
In this challenge I have interupt a file to get the flag.

## My solve
**Flag:** `pwn.college{stZIXis81EF5onpiw3n50DWBiz2.QXzQDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that /challenge/run will refuse to give the flag until I interrupt it. I used Ctrl+C to interupt it.
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
-   Ctrl-C (e.g., holding down the Ctrl key and pressing C) sends an "interrupt" to whatever application is waiting on input from the terminal and, typically, this causes the application to cleanly exit.

## References
No references used.

