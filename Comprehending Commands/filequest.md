# AN EPIC FILEQUEST SYSTEM
In this challenge I have to find a flag hidden in some file.

## My solve
**Flag:** `pwn.college{IZCsPuQPpC-MhMdzoGEI7hpQoZi.QX5IDO0wiN4EzNzEzW}`

It was mentioned in the problem statement that I have to use my knowledge of 'cd', 'ls', and 'cat' to find a file hidden in some directory.
```bash
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
BRIEF  challenge  flag  lib32   media  opt   run   sys  var
bin    dev        home  lib64   mnt    proc  sbin  tmp
boot   etc        lib   libx32  nix    root  srv   usr
hacker@commands~an-epic-filesystem-quest:/$ cat BRIEF
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/arch/sh/boards/mach-ap325rxa

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ ls /opt/linux/linux-5.4/arch/sh/boards/mach-ap325rxa
DOSSIER-TRAPPED  Makefile  sdram.S  setup.c
hacker@commands~an-epic-filesystem-quest:/$ cat /opt/linux/linux-5.4/arch/sh/boards/mach-ap325rxa/DOSSIER-TRAPPED
Yahaha, you found me!
The next clue is in: /usr/share/doc/bison/examples/c/reccalc
hacker@commands~an-epic-filesystem-quest:/$ ls /usr/share/doc/bison/examples/c/reccalc
Makefile  README.md  TIP  parse.y  scan.l
hacker@commands~an-epic-filesystem-quest:/$ cat  /usr/share/doc/bison/examples/c
/reccalc/TIP
Great sleuthing!
The next clue is in: /usr/share/locale/ha/LC_MESSAGES

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/$ ls -a /usr/share/locale/ha/LC_MESSAGES
.  ..  .REVELATION  iso_3166-1.mo  iso_3166.mo
hacker@commands~an-epic-filesystem-quest:/$ cat  /usr/share/locale/ha/LC_MESSAGE
S/.REVELATION
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/arch/arm64/kernel/vdso
hacker@commands~an-epic-filesystem-quest:/$ ls /opt/linux/linux-5.4/arch/arm64/kernel/vdso
Makefile  gen_vdso_offsets.sh  sigreturn.S  vdso.lds.S
SECRET    note.S               vdso.S       vgettimeofday.c
hacker@commands~an-epic-filesystem-quest:/$ cat /opt/linux/linux-5.4/arch/arm64/
kernel/vdso/SECRET
Great sleuthing!
The next clue is in: /opt/busybox/busybox-1.33.2/include/config/feature/call

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/busybox/busybox-1.33.2/include/config/feature/call
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/call$ ls
EVIDENCE  telinit.h
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/call$ cat./EVIDENCE
bash: cat./EVIDENCE: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/call$ cat /opt/busybox/busybox-1.33.2/include/config/feature/call/EVIDENCE
Tubular find!
The next clue is in: /usr/share/man/sv
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/call$ ls /usr/share/man/sv
NUGGET  man1  man5  man8
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/call$ cat /usr/share/man/sv/NUGGET
Yahaha, you found me!
The next clue is in: /usr/share/icons/hicolor/64x64/stock/text
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/call$ ls /usr/share/icons/hicolor/64x64/stock/text
GIST
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/call$ cat /usr/share/icons/hicolor/64x64/stock/text/GIST
Tubular find!
The next clue is in: /usr/lib/x86_64-linux-gnu/gedit/girepository-1.0

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/call$ ls -a ^C
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/call$ ls -a /usr/lib/x86_64-linux-gnu/gedit/girepository-1.0
.  ..  .ALERT  Gedit-3.0.typelib
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/call$ cat /usr/lib/x86_64-linux-gnu/gedit/girepository-1.0/.ALERT
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{IZCsPuQPpC-MhMdzoGEI7hpQoZi.QX5IDO0wiN4EzNzEzW}
```

## What I learned
Through this challenge I made use of my knowledge of all the file handling commands I have learnt so far.

## References 
No references used.
