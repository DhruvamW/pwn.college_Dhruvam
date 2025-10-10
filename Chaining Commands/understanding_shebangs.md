# UNDERSTANDING SHEBANGS
In this challenge I have to create a script using proper shebang.

## My solve
**Flag:** `pwn.college{Qal52Jlgbtpfmro9tj_we8F7l51.0VOzMDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to  create a script at /home/hacker/solve.sh that has a proper shebang and outputs "hack the planet". I have to make it executable, then run /challenge/run.  
```bash
hacker@chaining~understanding-shebangs:~$ touch /home/hacker/solve.sh
hacker@chaining~understanding-shebangs:~$ cat > /home/hacker/solve.sh
#!/bin/bash
echo "hack the planet"
^C
hacker@chaining~understanding-shebangs:~$ chmod a+x /home/hackr/solve.sh
chmod: cannot access '/home/hackr/solve.sh': No such file or directory
hacker@chaining~understanding-shebangs:~$ chmod a+x /home/hacker/solve.sh
hacker@chaining~understanding-shebangs:~$ /challenge/run
Testing your script...
Perfect! Your flag:
Flag: pwn.college{Qal52Jlgbtpfmro9tj_we8F7l51.0VOzMDOxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- When a program is invoked in Linux, the Linux kernel first inspects the file to determine how it should be run.
- This does NOT use the extension
- ather, Linux looks at the first few bytes of the file for this information.
- There are a bunch of different types of programs, but if the program file starts with the characters #! (often termed a "shebang"), Linux treats the file as an interpreted program, and the contents of the rest of the line as the path to the interpreter. It then invokes the interpreter with the path to the program file as its only argument.
- #!/bin/bash for bash scripts
- #!/usr/bin/python3 for Python scripts

## References
No references used.

