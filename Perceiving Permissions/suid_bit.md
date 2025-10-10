# THE SUID BIT
In this challenge I have to SUID bit to a program to read the flag.

## My solve
**Flag:** `pwn.college{AW_aatViMFYu1XaFCW0VMaiOSHc.QXzEjN0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to add the SUID bit to the /challenge/getroot program in order to spawn a root shell to cat the flag. I used chmod u+s on /challenge/root to run it as an owner. This spawned root shell when i ran /challenge/getroot and then i catted /flag.
```bash
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ ls -l /challenge/getroot
-rwsr-xr-x 1 root root 155 Jan 14  2025 /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root! 
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{AW_aatViMFYu1XaFCW0VMaiOSHc.QXzEjN0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-  the "Set User ID" (SUID) permissions bit allows the user to run a program as the owner of that program's file.
- The s part in place of the executable bit means that the program is executable with SUID. It means that, regardless of what user runs the program (as long as they have executable permissions), the program will execute as the owner user (in this case, the root user).
- chmod u+s [program]
-  Giving the SUID bit to an executable owned by root can give attackers a possible attack vector to become root.

## References
No references used.

