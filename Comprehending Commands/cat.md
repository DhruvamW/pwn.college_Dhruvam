# THE ROOT
In this challenge I have to read the flag from a file in home directory.

## My solve
**Flag:** `pwn.college{sQpUhg9jcyTCbfuvHu0ymCRhSHw.QXxcTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to read the 'flag' file in my 'home' directory with 'cat' command and the path to 'flag' as an argument to get the flag.
```bash
hacker@commands~cat-not-the-pet-but-the-command:~$ cat ./flag
pwn.college{sQpUhg9jcyTCbfuvHu0ymCRhSHw.QXxcTN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that 'cat' command is most often used for reading out files. 'cat' will concatenate (hence the name) multiple files if provided multiple arguments. 

## References 
No references used.
