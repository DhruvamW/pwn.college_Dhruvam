# HIDDEN FILES
In this challenge I have to read a dot-prepended file to get the flag.

## My solve
**Flag:** `pwn.college{oiGJjOHeDp3nwvV878oyh-LUyXg.QXwUDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to find a dot-prepended file in '/' directory. To see all the files in '/' I used the 'ls -a' command with '/' as an argument. Then I used 'cat' to read the contents of the flag file. 
```bash
hacker@commands~hidden-files:~$ ls -a /
.   .dockerenv            bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-14261209963584  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:~$ cat /.flag-14261209963584
pwn.college{oiGJjOHeDp3nwvV878oyh-LUyXg.QXwUDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that I need to invoke 'ls' command with the '-a' flag to view dot-prepended files in a directory.

## References 
No references used.

