# GREPPING STORED RESULTS
In this challenge I have to redirect output of a file to another file and then extract the flag.

## My solve
**Flag:** `pwn.college{0IYPElm5CAjtoIyiFFubOM_2Gut.QX4EDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to redirect the output of /challenge/run to /tmp/data.txt. I did that by    /challenge/run > /tmp/data.txt. Then I had to search for the flag in all the data. I did that by grep pwn /tmp/data.txt and got the flag.
```bash
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep pwn /tmp/data.txt
pwning
pwn.college{0IYPElm5CAjtoIyiFFubOM_2Gut.QX4EDO0wiN4EzNzEzW}
pwned
pwns
pwn
```

## What I learned
Through this challenge I learnt that we can redirect the output of a file to another file and use grep command to extract the required values.

## References
No references used.

