# REDIRECTING MORE OUTPUT
In this challenge I have to redirect an output to a new file.

## My solve
**Flag:** `pwn.college{85TQxre1-b_orGNVPbaxibId_I0.QX1YTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to redirect output of the file /challenge/run to myflag.
```bash
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{85TQxre1-b_orGNVPbaxibId_I0.QX1YTN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that we can redirect output of any command to another file using > character.

## References
No references used.

