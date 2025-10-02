# DELETING CHARACTERS
In this challenge I have to delete some decoy characters in my flag..

## My solve
**Flag:** `pwn.college{U44zJS7K5Qbm_lD22JFPquvjitc.0FNxEzNxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to remove ^ and % characters present in the flag to get the correct flag.
``` bash
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%
Your character-stuffed flag:
pwn.college{U44zJS7K5Qbm_lD22JFPquvjitc.0FNxEzNxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- tr can also translate characters to nothing (i.e., delete them). 
-  deletion is done via a -d flag and an argument of what characters to delete

## References
No references used.

