# DETACHING AND ATTACHING
In this challenge I have to launch a screen and detach from it and reattach to it to get the flag.

## My solve
**Flag:** `pwn.college{MMAkF-j3U4Dyv-YaLRpka7yiWdO.0lN4IDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to launch screen. Then detach from it and run /challenge/run and
reattach to see the flag. I first used the screen command to start the screen. I detached using Ctrl+A and then d. Then I ran /challenge/run. I reattached to the screen using screen -r.
```bash
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen
[detached from 157.pts-0.terminal-multiplexing~detaching-and-attaching]
hacker@terminal-multiplexing~detaching-and-attaching:~$ /challenge/run
Found detached screen session: 157.pts-0.terminal-multiplexing~detaching-and-attaching
Sending flag to your screen session...

Flag sent! Now reattach to your screen session with:

  screen -r

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching:~$
hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{MMAkF-j3U4Dyv-YaLRpka7yiWdO.0lN4IDOxwiN4EzNzEzW}
Yes! Flag is: pwn.college{MMAkF-j3U4Dyv-YaLRpka7yiWdO.0lN4IDOxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- You detach by pressing Ctrl-A, followed by d (for detach).
- This leaves your session running in the background while you return to your normal terminal.
- To reattach, you can use the -r argument to screen
- Ctrl-A is screen's activation key for all of its shortcuts in its default configuration. All screen functionality is activated by some command combination starting with Ctrl-A.

## References
No references used.

