# READING FILES
In this challenge I have to read the contents of a file directly in a variable.

## My solve
**Flag:** `pwn.college{sV07-8D0UJH7xDLaQrqMkNjNbMs.QXwIDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to read /challenge/read_me into the PWN environment variable. The /challenge/read_me will keep changing so I need to read it using one command: read PWN < /challenge/read_me.
```bash
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{sV07-8D0UJH7xDLaQrqMkNjNbMs.QXwIDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- You can read files with the shell directly
- Example: read VAR < some_file; (redirects some_file into the standard input of read, and so when read reads into VAR, it reads from the file)


## References
No references used.

