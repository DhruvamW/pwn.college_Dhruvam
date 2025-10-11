# FINDING SESSIONS
In this challenge I have to find the screen sessions that contains the flag.

## My solve
**Flag:** `pwn.college{kHikWfIeRRMutX37ZsEiQn9fNyr.01N4IDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that there are three screen sessions and one of them contains the flag.
```bash
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls
There are screens on:
        158.pts-0.terminal-multiplexing~launching-screen        (Remote or dead)
        147.pts-0.terminal-multiplexing~detaching-and-attaching (Remote or dead)
        157.pts-0.terminal-multiplexing~detaching-and-attaching (Remote or dead)
        146.session_8364905f6c66593f    (Detached)
        149.session_0fcda58a27e9af50    (Detached)
        152.session_ef944d36cd9ed893    (Detached)
6 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~finding-sessions:~$ screen -r 152
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{kHikWfIeRRMutX37ZsEiQn9fNyr.01N4IDOxwiN4EzNzEzW}
pwn.college{kHikWfIeRRMutX37ZsEiQn9fNyr.01N4IDOxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- we can list multiple sessions running using screen -ls
- The identifiers of the sessions are the PID of each respective screen process, a dot, and the name of the screen session.
- To attach to a specific one, you use its name or its PID by giving it as an argument to screen -r.

## References
No references used.

