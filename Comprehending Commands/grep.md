# THE ROOT
In this challenge I have to read the flag from a file.

## My solve
**Flag:** `pwn.college{s48coNuI8oRoyH4AE7VI6nusOWA.QX3EDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to read the flag from 'data.txt' file whose path is '/challenge/data.txt'. It was mentioned that 'data.txt' file has many lines of code. So instead of simply using the 'cat' command to read all the contents of the file, I used 'grep' command with 'pwn.college' and file path as the argument to grab the flag.
```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{s48coNuI8oRoyH4AE7VI6nusOWA.QX3EDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that 'grep' command is used to read out particular string from a give file. Its syntax looks like: grep <STRING_TO_BE_SEARCHED> <FILE_PATH>

## References 
No references used.
