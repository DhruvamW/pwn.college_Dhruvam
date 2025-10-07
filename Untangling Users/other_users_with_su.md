# OTHER USERS WITH SU
In this challenge I have to become other user by using su command.

## My solve
**Flag:** `pwn.college{UMB0hZ-TlffM20Ef09K3WA0o41H.QX2UDN1wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to switch to the zardus user and then run /challenge/run. Zardus' password is dont-hack-me.
```bash
hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{UMB0hZ-TlffM20Ef09K3WA0o41H.QX2UDN1wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-  you can also give a username as an argument to su to switch to that user instead of root

## References
No references used.

