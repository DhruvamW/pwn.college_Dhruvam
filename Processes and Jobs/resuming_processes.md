# RESUMING PROCESSES
In this challenge I have to resume a process to get the flag.

## My solve
**Flag:** `pwn.college{4BHmxY0Aj3M-oCsohMwcZAeBYUO.QX2QDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that /challenge/run needs me to suspend it, then resume it. I suspended it using Ctrl+Z and then resumed it using fg command.
```bash
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{4BHmxY0Aj3M-oCsohMwcZAeBYUO.QX2QDO0wiN4EzNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```

## What I learned
Through this challenge I learnt that:
-   fg command, a builtin that takes the suspended process, resumes it, and puts it back in the foreground of your terminal.

## References
No references used.

