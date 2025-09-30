# REDIRECTING ERRORS
In this challenge I have to redirect output and errors to separate files.

## My solve
**Flag:** `pwn.college{siYNNOqam_ZJyO-hrmh2SlH5m5T.QX3YTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to redirect the out of /challenge/run to myflag and errors to instructions. I used > to redirect output and 2> to redirect errors. Then I just read both the files using cat and got the flag.
```bash
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat instructions
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{siYNNOqam_ZJyO-hrmh2SlH5m5T.QX3YTN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-A File Descriptor (FD) is a number that describes a communication channel in Linux.
-FD 0: Standard Input
-FD 1: Standard Output
-FD 2: Standard Error
-a > without a number implies 1>, which redirects FD 1 (Standard Output)

## References
No references used.

