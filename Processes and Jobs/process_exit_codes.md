# PROCESS EXIT CODES
In this challenge I have to retrieve an exit code of a process.

## My solve
**Flag:** `pwn.college{wvF6OA_0twR8VSZ5kXu5cPymX-2.QX5YDO1wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to  retrieve the exit code returned by /challenge/get-code and then run /challenge/submit-code with that error code as an argument. I read the error code using $? and printed it on the terminal using the echo command.
```bash
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
9
hacker@processes~process-exit-codes:~$ /challenge/submit-code 9
CORRECT! Here is your flag:
pwn.college{wvF6OA_0twR8VSZ5kXu5cPymX-2.QX5YDO1wiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-  Every shell command, including every program and every builtin, exits with an exit code when it finishes running and terminates.
- This can be used by the shell, or the user of the shell to check if the process succeeded in its functionality (this determination, of course, depends on what the process is supposed to do in the first place).
- You can access the exit code of the most recently-terminated command using the special ? variable and prepend it with $ to read its value.

## References
No references used.

