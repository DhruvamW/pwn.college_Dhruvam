# CHANGING FILE OWNERSHIP
In this challenge I have to change ownership of a file to read the flag.

## My solve
**Flag:** `pwn.college{cFy-xdki-_nAYPZdJK3oGFzSr_d.QXxEjN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to change the owner of the /flag file to the hacker user, and then read the flag. First I saw all the files and their owners using the ls -l command. Then I changed user using the chown hacker /flag command. Then I read the flag.
```bash
hacker@permissions~changing-file-ownership:~$ ls -l
total 36
-rw-r--r-- 1 hacker hacker   4 Sep 30 07:42 COLLEGE
drwxr-xr-x 1 hacker hacker   0 Sep 22 12:24 Desktop
-rw-r--r-- 1 hacker hacker   8 Sep 30 10:30 PWN
-rw-r--r-- 1 root   hacker  60 Sep 25 20:42 f
lrwxrwxrwx 1 hacker hacker   5 Sep 28 11:25 flag_new -> /flag
-rw-r--r-- 1 hacker hacker 829 Sep 30 08:21 instructions
-rw-r--r-- 1 hacker hacker  95 Sep 30 08:21 myflag
-rw-r--r-- 1 hacker hacker   0 Sep 30 07:53 myflah
-rw-r--r-- 1 root   hacker  77 Sep 30 14:02 need
lrwxrwxrwx 1 hacker hacker   5 Sep 28 11:32 not-the-flag -> /flag
-rw-r--r-- 1 hacker hacker 437 Sep 30 08:09 the-flag}
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{cFy-xdki-_nAYPZdJK3oGFzSr_d.QXxEjN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-   Every file in Linux is owned by a user on the system.
- we can change the ownership of files. This is done via the chown (change owner) command
- chown [username] [file]
- chown can only be invoked by the root user

## References
No references used.

