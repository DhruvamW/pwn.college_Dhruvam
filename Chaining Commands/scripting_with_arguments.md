# SCRIPTING WITH ARGUMENTS
In this challenge I have to create a script which takes two arguments and prints their reverse.

## My solve
**Flag:** `pwn.college{QNLHdCmKKFlT53J1g2DtPw-yDHu.0VNzMDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that I have to  write a script at /home/hacker/solve.sh that takes two arguments and
outputs them in REVERSE order (second argument first, then the first argument). 
```bash
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Not quite right!
Expected: college_JKQx8stu6wU pwn_aOZd0Wq5ALw
Got: college_JKQx8stu6wUpwn_aOZd0Wq5ALw
hacker@chaining~scripting-with-arguments:~$ cat > ./solve.sh
echo "$2 $1"
^C
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{QNLHdCmKKFlT53J1g2DtPw-yDHu.0VNzMDOxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- The script can access these arguments using special variables:
$1 contains the first argument
$2 contains the second argument
$3 would contain the third argument
...and so on

## References
No references used.

