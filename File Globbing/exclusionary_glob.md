# EXCLUSIONARY GLOBBING
In this challenge I have to reference multiple files using exlusionary globbing in a single command.

## My solve
**Flag:** `pwn.college{0CakVI2XR7gJPskBWXvp6zkgHY8.QX2IDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to provide a single argument to /challenge/run to reference all the files that don't start with p, w, or n.
```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{0CakVI2XR7gJPskBWXvp6zkgHY8.QX2IDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that if the first character in the brackets is a ! or (in newer versions of bash) a ^, the glob inverts, and that bracket instance matches characters that aren't listed. The ! character has a different special meaning in bash when it's not the first character of a [] glob. ^ does not have this problem, but is also not compatible with older shells.

## References
No references used.

