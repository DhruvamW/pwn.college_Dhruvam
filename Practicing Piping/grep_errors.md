# GREPPING ERRORS
In this challenge I have to pipe error of a command to another command and then extract the flag.

## My solve
**Flag:** `pwn.college{Arz3eewMbkC0Uua-rNGzTzyR1ro.QX1ATO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to pipe the error of /challenge/run directly to grep command so as to extract the flag.
```bash
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{Arz3eewMbkC0Uua-rNGzTzyR1ro.QX1ATO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that we can grep through errors directly by using  >& operator, which redirects a file descriptor to another file descriptor. This means that we can have a two-step process to grep through errors: first, we redirect standard error to standard output (2>& 1) and then pipe the now-combined stderr and stdout as normal (|).

## References
No references used.

