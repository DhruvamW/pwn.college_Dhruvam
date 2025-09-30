# PROCESS SUBSITUTION FOR INPUTS
In this challenge I have to use process substitution with diff to compare the outputs of two programs and find the flag.

## My solve
**Flag:** `pwn.college{s-sjn8oBmUqbVXE4zrUNERtMFyt.0lNwMDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to use process substitution with diff to compare the outputs of two programs and find the flag. To get the output of /challenge/print_decoys and /challenge/print_decoys_and_flag as named pipes I used <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag) and compared thes two named pipes using diff which gave me the flag.
```bash
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
1a2
> pwn.college{s-sjn8oBmUqbVXE4zrUNERtMFyt.0lNwMDOxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- Linux follows the philosophy that "everything is a file".
- The shell follows this philosophy, allowing us to, for example, use any utility that takes file arguments on the command line   and hook it up to the output of programs.
- We can hook input and output of programs to arguments of commands. This is done using Process Substitution.
- <( command ) → treat command’s output like a file
- >( command ) → treat command’s input like a file

## References
No references used.

