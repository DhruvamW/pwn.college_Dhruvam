# EXECUTABLE FILES
In this challenge I have to change the permissions of a file to read the flag.

## My solve
**Flag:** `pwn.college{A7_ykjNNxPnByCfugHmgvS4FuLA.QXyEjN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to  change the permissions of the /challenge/run file to execute it. So I used chmod to change the permission of the file such that the owner aka me(hacker) and groups have access to read the file. Then I ran /challenge/run.
```bash
hacker@permissions~executable-files:~$ chmod u+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{A7_ykjNNxPnByCfugHmgvS4FuLA.QXyEjN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt how to change executable permissions of a file.

## References
No references used.

