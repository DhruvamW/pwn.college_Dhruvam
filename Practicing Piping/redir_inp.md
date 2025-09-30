# REDIRECTING INPUT
In this challenge I have to redirect input to a file and redirect that file to get the flag.

## My solve
**Flag:** `pwn.college{kNJXkr6yl-GZIaM0YImgJYR_Umh.QXwcTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to redirect the value COLLEGE in a file called PWN and then redirect that file to /challenge/run.
```bash
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{kNJXkr6yl-GZIaM0YImgJYR_Umh.QXwcTN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that we can redirect input to programs. This is done using <.

## References
No references used.

