# GROUPS AND FILES
In this challenge I have to change group of a file to read the flag.

## My solve
**Flag:** `pwn.college{QzXJEPn3Pvca8M0SUIHUP54ps61.QXxcjM1wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to change the group ownership of the flag file, and read the flag. I first checked what group owns the flag file. Then I used chgrp to change the group to hacker which I was a part of. Then I read the flag.
```bash
hacker@permissions~groups-and-files:~$ ls -l /flag
-r--r----- 1 root root 60 Oct 10 06:48 /flag
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{QzXJEPn3Pvca8M0SUIHUP54ps61.QXxcjM1wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-    Files have both an owning user and group
- A group can have multiple users in it, and a user can be a member of multiple groups.
- graphical output can be done via the special /dev/fb0 file. This file is a special device file (type c means it is a "character device"), and interacting with it results in changes to the display output (rather than changes to disk storage, as for a normal file)
- group ownership can be changed with the chgrp (change group) command
- Unless you have write access to the file and membership in the new group, this typically requires root access

## References
No references used.

