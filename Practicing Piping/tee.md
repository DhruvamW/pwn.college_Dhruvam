# DUPLICATING PIPED DATA WITH TEE
In this challenge I have to pipe the output of one command into another  and intercept it to read the secret code to get flag.

## My solve
**Flag:** `pwn.college{UmhWIK8qncuKDmxeLWCBh6yiaBL.QXxITO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to pipe the output of /challenge/pwn into /challenge/college but I need to intercept it first. I did it using /challenge/pwn | tee need | /challenge/college. I intercepted the output using a new file called need. Then I read the need file using cat to get the secret code. Then I got the flag using the secret value as told by the need file. 
```bash
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee need | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat need
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "UmhWIK8q"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret UmhWIK8q | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{UmhWIK8qncuKDmxeLWCBh6yiaBL.QXxITO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that we can duplicate data flowing through our pipes to any number of files provided on the command line using the tee command.

## References
No references used.

