# NAMED PIPES
In this challenge I have to create a FIFO file and redirect the stdout of a command to it.

## My solve
**Flag:** `pwn.college{gsrfvqqy4UFj-AcMBgeCpBiA1GM.01MzMDOxwiN4EzNzEzW`

It was mentioned in the problem statement that I have to create a /tmp/flag_fifo file and redirect the stdout of /challenge/run to it. I created the named pipe using mkfifo /tmp/flag_fifo. Then I redirected the stdout of /challenge/run to it using /challenge/run > /tmp/flag_fifo. Then I opened another terminal and catted /tmp/flag_fifo to get the flag.
```bash
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo! 
Bash will now try to open the FIFO for writing, to pass it as the stdout of 
/challenge/run. Recall that operations on FIFOs will *block* until both the 
read side and the write side is open, so /challenge/run will not actually be 
launched until you start reading from the FIFO!
---------------------------------------------------------------------------------
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo
You've correctly redirected /challenge/run's stdout to a FIFO at 
/tmp/flag_fifo! Here is your flag:
pwn.college{gsrfvqqy4UFj-AcMBgeCpBiA1GM.01MzMDOxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
- We can also create our own persistent named pipes that stick around on the filesystem, for this we create a FIFO using the mkfifo command
- You control where FIFOs are created
- They persist until you delete them
- Any process can write to them by path (e.g., echo hi > my_pipe)
- You can see them with ls and examine them like files
- One problem with FIFOs is that they'll "block" any operations on them until both the read side of the pipe and the write side of the pipe are ready.
- No disk storage: FIFOs pass data directly between processes in memory - nothing is saved to disk
- Ephemeral data: Once data is read from a FIFO, it's gone (unlike files where data persists)
- Automatic synchronization: Writers block until the readers are ready, and vice-versa. This is actually useful! It provides automatic synchronization.
- Complex data flows: FIFOs are useful for facilitating complex data flows, merging and splitting data in flexible ways, and so on. For example, FIFOs support multiple readers and writers.

## References
No references used.

