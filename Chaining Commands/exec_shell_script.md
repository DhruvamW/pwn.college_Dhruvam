# EXECUTABLE SHELL SCRIPT
In this challenge I have to run a shell script without explicitly calling bash.

## My solve
**Flag:** `pwn.college{YWlBU_VJUxzZeBPVvtvv-LfW_7w.0lM0MDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to make a shellscript that will invoke /challenge/solve, make it executable, and run it without explicitly invoking bash. I first creat a shellscript x.sh using touch. Then I took input in it usind stdin.  Then I changed its permission such that the owner aka hacker aka me can execute the file. Then i executed the file.
```bash
hacker@chaining~executable-shell-scripts:~$ touch ./x,sh
hacker@chaining~executable-shell-scripts:~$ touch ./x.sh
hacker@chaining~executable-shell-scripts:~$ cat > ./x.sh
/challenge/solve
^C
hacker@chaining~executable-shell-scripts:~$ chmod u=rwx ./x.sh
hacker@chaining~executable-shell-scripts:~$ ./x.sh
Congratulations on your shell script execution! Your flag:
pwn.college{gn6sO3ogLJ97Pk1RInslnWkH75c.QX0cjM1wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- If your shell script file is executable, you can simply invoke it via its relative or absolute path

## References
No references used.

