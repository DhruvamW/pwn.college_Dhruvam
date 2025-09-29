# MATCHING WITH []
In this challenge I have to run an argument using [] glob.

## My solve
**Flag:** `pwn.college{8m2g8BGALqZBoQGdVkpiOjeSkmf.QXzIDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to change my directory to /challenge/files and then run the /challenge/run command using [] glob. As all the files that I had to call in the arguement had names of the type files_ I used that part as it is and included the end letters in the [] glob.
```bash
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[absh]
You got it! Here is your flag!
pwn.college{8m2g8BGALqZBoQGdVkpiOjeSkmf.QXzIDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that another glob is []. It instead of matching any character, [] is a wildcard for some subset of potential characters, specified within the brackets.
## References
No references used.

