# MAKING DIRECTORIES
In this challenge I have to create a new directory and create a file in that directory to get the flag.

## My solve
**Flag:** `pwn.college{0-BC9JsKcGvIqtDTbLf1SvM3z8R.QXxMDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I make '/tmp/pwn' directory and in that directory I have to create a file named 'college' and then run '/challenge/run' to get the flag. I used 'mkdir' command to create the directory and 'touch' command to create the file. 
```bash
hacker@commands~making-directories:~$ ls /tmp
bin  hsperfdata_root  tmp.4mK6TfTSUV
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ ls /tmp
bin  hsperfdata_root  pwn  tmp.4mK6TfTSUV
hacker@commands~making-directories:~$ touch /tmp/pwn/college
hacker@commands~making-directories:~$ ls /tmp/pwn
college
hacker@commands~making-directories:~$ /challenge/run
Success! Here is your flag:
pwn.college{0-BC9JsKcGvIqtDTbLf1SvM3z8R.QXxMDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that 'mkdir' command is used to create a new directory.

## References 
No references used.

