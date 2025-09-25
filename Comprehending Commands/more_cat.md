# THE ROOT
In this challenge I have to read the flag from a file.

## My solve
**Flag:** `pwn.college{sQpUhg9jcyTCbfuvHu0ymCRhSHw.QXxcTN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to read the 'flag' file 'cat' command and the path to 'flag' as an argument to get the flag. Also I can't the 'cd' to change my directory.
```bash
You cannot use the 'cd' command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory! You can find it
in the file /usr/share/sgml/flag. Go cat it out **without** cding into that
directory!
hacker@commands~more-catting-practice:~$ cat /usr/share/sgml/flag
pwn.college{gHo65nlgUAQqg_mEENlaHRFzamw.QXwITO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that 'cat' command is most often used for reading out files.

## References 
No references used.
