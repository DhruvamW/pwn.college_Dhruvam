# BECOMING ROOT WITH SU
In this challenge I have to become root by using su command.

## My solve
**Flag:** `pwn.college{ADN5mVMMVKXoXNqT8RPjJBQFk9J.QX1UDN1wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to provide the password: hack-the-planet to su command to become the root and then read the flag.
```bash
hacker@users~becoming-root-with-su:~$ su
Password:
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{ADN5mVMMVKXoXNqT8RPjJBQFk9J.QX1UDN1wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-  The full list of users on a Linux system is specified in the /etc/passwd file
- Each line contains, separated by :s, the username
- an x as a placeholder for where the password used to be
- the numerical user ID, the numerical default group ID, long-form user details, the home directory, and the default shell.
-  root: the system administrator
-  su (the substitute user command)
- su is a setuid binary
- Because it has the SUID bit set, su runs as root
- it checks to make sure that the user knows the root password
- Modern systems very rarely have root passwords

## References
No references used.

