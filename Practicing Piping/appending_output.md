# REDIRECTING MORE OUTPUT
In this challenge I have to append an output to a new file.

## My solve
**Flag:** `pwn.college{cqZ8ffXM5MzXpn6Nqgxgd6ztH43.QX3ATO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to run /challenge/run with an append-mode redirect of the output to the file /home/hacker/the-flag. For this I ivoked the command /challenge/run >> /home/hacker/the-flag to append the output to the-flag file and then used the cat command to read the file.
```bash
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do 
the first write directly to the file, and the second write, I'll do to stdout 
(if it's pointing at the file). If you redirect the output in append mode, the 
second write will append to (rather than overwrite) the first write, and you'll 
get the whole flag!
hacker@piping~appending-output:~$ cat the-flag
 | 
\|/ This is the first half:
 v 
pwn.college{cqZ8ffXM5MzXpn6Nqgxgd6ztH43.QX3ATO0wiN4EzNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>) 
rather than *append* mode (>>), and so the write of the second half to stdout 
overwrote the initial write of the first half directly to the file. Try append 
mode!
```

## What I learned
Through this challenge I learnt that we can redirect output in append mode using >> instead of >. This will prevent the deletion of the old contents of the file.

## References
No references used.

