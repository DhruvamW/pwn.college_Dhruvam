# WRITING TO MULTIPLE PROGRAMS
In this challenge I have to duplicate command's output as input to two other commands.

## My solve
**Flag:** `pwn.college{Quuuv-DnS1TH12fwXNFfKuM0XwO.QXwgDN1wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to run the /challenge/hack command, and duplicate its output as input to both the /challenge/the and the /challenge/planet command. I firstly used the pipe(|) operator to hook up the output of /challenge/hack to the named pipes of other files which I connected using the tee operator and created the output named pipes by >(/challenge/the) >(/challenge/planet). 
```bash
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and 
/challenge/planet. Don't try to copy-paste it; it changes too fast.
3210628679301368864
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{Quuuv-DnS1TH12fwXNFfKuM0XwO.QXwgDN1wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- For writing to a command (output process substitution), use >(command)
- If you write an argument of >(rev), bash will run the rev command (this command reads data from standard input, reverses its order, and writes it to standard output).

## References
No references used.

