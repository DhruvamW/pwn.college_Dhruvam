# GREPPING LIVE OUTPUT
In this challenge I have to pipe the output of one command to another command.

## My solve
**Flag:** `pwn.college{QOTE1yYGqB6UVA09z2-5x3zx19W.QX5EDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to pipe the output of /challenge/run to grep pwn.college to find the flag.
```bash
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{QOTE1yYGqB6UVA09z2-5x3zx19W.QX5EDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that we can redirect the output of a command to another command directly using the |(pipe) operator.

## References
No references used.

