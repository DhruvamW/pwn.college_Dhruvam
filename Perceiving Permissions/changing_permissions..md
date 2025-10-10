# CHANGING PERMISSIONS
In this challenge I have to change the permissions of a file to read the flag.

## My solve
**Flag:** `pwn.college{Eqpe4zfuiTJBNUpb7FKAphDKXmJ.QXzcjM1wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to  change the permissions of the /flag file to read it. The /flag file is owned by root and I can't change that. So I used chmod to change the permission of the file such that other users and groups have access to read the file. Then I catted /flag.
```bash
hacker@permissions~changing-permissions:~$ chmod go+r /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{Eqpe4zfuiTJBNUpb7FKAphDKXmJ.QXzcjM1wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-  the first character there is the file type
- The next nine characters are the actual access permissions of the file or directory.
- 3 characters denoting permissions for the owning user
- 3 characters denoting the permissions for the owning group
-  characters denoting the permissions that all other access
- r - user/group/other can read the file (or list the directory)
- w - user/group/other can modify the files (or create/delete files in the directory)
- x - user/group/other can execute the file as a program (or can enter the directory, e.g., using `cd`)
- - - nothing 
- Like ownership, file permissions can also be changed. This is done with the chmod (change mode) command.
- chmod [OPTIONS] MODE FILE
- u+r, as above, adds read access to the user's permissions
- g+wx adds write and execute access to the group's permissions
- o-w removes write access for other users
- a-rwx removes all permissions for the user, group, and world

## References
No references used.

