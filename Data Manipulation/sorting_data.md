# SORTING DATA
In this challenge I have to sort a file to get the flag.

## My solve
**Flag:** `pwn.college{kGcKH7UlcntYVmeolSkvlVoBx4A.0FM0MDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that there's a file at /challenge/flags.txt containing 100 fake flags, with the real flag mixed among them. When sorted alphabetically, the real flag will be at the end. So I sorted the data in reverse order to get the correct flag first.
```bash
hacker@data~sorting-data:~$ /challenge/flags.txt | sort -r
bash: /challenge/flags.txt: Permission denied
hacker@data~sorting-data:~$ sort /challenge/flags.txt -r
pwn.college{kGcKH7UlcntYVmeolSkvlVoBx4A.0FM0MDOxwiN4EzNzEzW}
pwn.college{kGcKH7UlcntYVmeolSkvlVoBx4A.0FM0MDOxwiN4EzNzEzW}
pwn.college{kGcKH7UlcntYVmeolSkvlVoBx4A.0FM0LDOxwiN4EzNzEzW}
pwn.college{kGcKH7UlcntYVmeolRkvlVoBx4A.0FM0MDOxwiN4EyNzEzW}
pwn.college{kGcKH7UlcntYVlenlSkvlVoBx4A.0FM0MDNxwiM4EzNzEzW}
pwn.college{kGcKH7UlbmtYVmeolSkvlVoBx4A.0EM0MDOwwiN4EyNzDzW}
pwn.college{kGcKH6UlcntYUmeolSjvlVnBw4A.0FM0MCNwwiN4EzNzEzW}
pwn.college{kGcKG7UlcntYVmeolSkvlVoBx4A.0FM0MDOxwiM4EzNzEzW}
pwn.college{kGcKG7TkcntYUlenlSjulUoBx4A.0FM0MDOxwiN4EzMyEzW}
pwn.college{kGcJH7UlcntYVleolSkvlVoBw4A.0FM0MDOxwiM4EzNzEzW}
pwn.college{kGbKH7UlcntYVmeolSkvlVoBx4A.0FM0MDOxwiN4DzNyEzW}
pwn.college{jGcKH7UlcntYVmeolSkvlVoBx4A.0FM0MDOxwiN4EzNzEyW}
pwn.college{jGcKH7UlcntYVleokSkvlVoBx4A.0FM0MDOxviN4EyNyEyW}
pwn.college{jGcKH7UlbntYVmeokSkvlVoBx3A.0EM0MCOxwiN4EzNzDzW}
pwn.college{jGcKG7UlcmtYVmeolSjvlUoAx4A.0FM0MDOxwiN4EyNzEzV}
pwn.college{jGbKG7TlcntYVleolSkvkUoAx4A.0EL0MDOxwhN3EzNzEzW}
pwn.collegd{kGcKG7UlcntYVmeolSkvlVoBx4A.0FM0MDOwwhN4EzNyEzW}
pwn.collegd{kGbKH7UlcnsYVleolSkvlVoAx4A.0FM0MDOxwhN3EzMzEzW}
pwn.collegd{kFcKG7UlcntYVmeolSkvlVoBx4A.0FM0LDNxwiN3DzNzDzW}
pwn.collefe{kGbKH7UlcntYVmeolSjukVoBw3A.0FL0MDOwwiN3EzMyEyW}
pwn.collefe{jGcKG6UlbmtYVleolRkvlVnAx4A.0FM0MDNxvhN4EzNzEyW}
pwn.collefd{kGcKG6UlcntXVleolSkvlVoAw4A.0FM0MDNwwiN4DzNzEyV}
pwn.colldge{kGcKH7UlcntXVmdolSkvlVoBx4A.0FL0MCOxwiN4EzNzEzW}
pwn.colldge{kGcKH7UkcntXVmeolSjvlVoBx4A.0FM0MDOxwiN4EzNzEzW}
pwn.colldge{kGcKH7UkcmtYVmeolRkvlVoAx4A.0FM0MDOxwhN4EzNzEzW}
pwn.colldge{jGcKH7UlcmsYVmeokSkvlUoAw4A.0EM0MDOxwiN4EyNzDyW}
pwn.colldfe{kGcKH6UlcntYVmdolRkvlVoBx4A.0FM0MCOxwiN4DzNzDzW}
pwn.colldfe{kGcJH7UlcntYVleokSkvlVoAw4A.0FM0LDOwwiN4EyNyEzV}
pwn.colkege{kGcKH7UlcmtYVmeolSkvlVoAx4A.0FM0MDOxwiN4EzNzEzW}
pwn.colkege{kGcKG7UlcntYVmeolSkvlVoBx4A.0FM0MDOxwiN4EzNzEzW}
pwn.colkege{kGbKH7UlcntYUmeolSkvlVoBx4A.0FM0MCNxwiM3EzNzDzW}
pwn.colkege{kFcKH7TlcnsXVleokRkulUnBx3A.0FM0MDOxwhN3EzMzEyW}
pwn.colkefe{kGcKH7UlcntYVmeolSkvlVoBx4A.0FM0LDOxwiN4EzNzEzW}
pwn.colkefe{kGcJH6UkcnsYVmenlRjvlUoBx4A.0FM0MDOxwiN4EzMyDyV}
pwn.coklege{jGbKG7TlbntYVmeolSkvlVoBw4A.0EM0MDOxwhN4DzNyEzW}
pwn.coklegd{kGcKH7TlcntYUmenlSjulUoBx4A.0FM0MDOxwhN4EzNzEzW}
pwn.coklegd{kGbKH7UlcnsYVmdnlRkvlVoBx3A.0FL0MDOxwiN4EyNzEzW}
pwn.coklefe{kFcJH7UlcntXVmenlSkvkVoBw4A.0FM0MDOxwiN4EzNzEzW}
pwn.cokldfe{kGbKH7UlcntYVmeolRkvkUnBx4A.0FM0MDOxwiM4DzNzEzW}
pwn.cokkege{kGcKH7UkcmsXVmeolSkvlVoBx3A.0FM0MDOxwiN4EzNyEyV}
pwn.cokkege{kGcJH7UlcnsYVleolSkvlVoBx4A.0EM0LDOxwiM4EzNzEzV}
pwn.cokkege{kFbKG7UlbnsYUmeokRkvkUoBx3A.0FL0MDNwwhN3EzMzEyW}
pwn.cnllege{kGbKH7UkbntXVleolSkvlUnBx3A.0FM0MDOxwiN4EyNzEzW}
pwn.cnllefe{kGcKH7UlcntYUmeolSkvlVoBw4A.0FL0MDOxwiM3EzNyEzW}
pwn.cnllefe{jGcKH7UlbntXUmenlSkvlUnAw4A.0EM0LDOwviM4DzNyEzW}
pwn.cnlldge{kGcJH6UlcntXVleokSkukUnBx4A.0FM0MCOxwhN4EzMyDyV}
pwn.cnlkege{jGcJG7TlbmtYVmeolRkvlVoBx4A.0EL0LCOwwiN3EzNzDzV}
pwn.cnklegd{jGcKH6UkbmtYVmdolRjvlVoBx3A.0EM0LCNwwiN4EyNzEyW}
pwn.cnklefe{kGcKH6UkcmtXVldnlRkvlVnBx4A.0FM0MDOxwiN4DzMzEzV}
pwn.cnkkdfd{kFbKG6TkcnsYVleolRkukVoBx4A.0FM0MDOxwiN4DzNzEzV}
pwn.bollege{kGcKH7UkcmtYVmeolSkvkVnBx4A.0FM0MDOxwhN4EzNzDzV}
pwn.bollege{kGbKG7UlcntYVmeolSkvlVoBx4A.0FM0MDOxwiN4DzNyEzW}
pwn.bollege{kFcKH7UlbnsYVmeolRjvkVoBx4A.0FL0MDOwwiM4EyNzEyW}
pwn.bollege{jFcJH7TlbntYVmenkSjulVoBx4A.0FM0MDNwviN3EzMzDyW}
pwn.bollegd{kGcKH6UlcntXUmeolRkvkVnBx4A.0FM0MDOxwiM3DyNzEzW}
pwn.bolldgd{kFcKH7TkcntXVmenlSkvlVnBx4A.0FL0LCNxvhM4EyNzEzW}
pwn.bolkege{kGcKH7UlcntYVmeolSkvlVoBx4A.0FM0MDOxwiN4EzNzEzW}
pwn.bolkege{kGcKG6UkbntYVmeolSkvlVnBx4A.0FL0MDOxvhN4EzNzEyW}
pwn.bolkege{jGcJG6UlcntYVmenlSkulVoBx3A.0EL0MCOxwhN4DzNzEyV}
pwn.boklege{kGcJH7TkcmtYVmenlSkulVoBw4A.0EM0MDOwwiN4EzNzDzW}
pwn.bnllegd{kFcKG6UlcmtYUmeolSjvlVoAw3A.0FM0MDOxwiN4EyMzEzV}
pwn.bnlkdge{kGcKH6TkcmsYVmenkRkulUnBx3A.0FM0MDNxwiN4DzNzDyW}
pwm.college{kGcKH7UlcntYVmeolSkvlVoBx4A.0FM0MDOxwiN3EzNzEzW}
pwm.college{kGcKH7UlbntYVmeolSkvlVoBx3A.0FM0MDNxwhN4DzNzEyV}
pwm.colkdfd{kGcKH7TlcmtYVmeolSjulVnBx4A.0EL0MDOxviN4EyNyEyW}
pwm.coklegd{kGcJH7UlbmtYVmeolSkvlUoAx4A.0FL0MDNxwhN4EyMyDzW}
pwm.cokldge{jFcJH6TlcmsXUldolSkvlUoAx4A.0FM0LDOxwhM4EyNzEzV}
pwm.cnllege{jGcKG6UlcmtYUmeokSjvkVoBx4A.0FM0MDOxwiM4EyNzEyW}
pwm.cnlkege{kGcKG7UkbmtXVlenlRjvkVnBx3A.0FM0MDOxviN4EzNyEzW}
pwm.cnlkege{kGcJG7TkbnsYVmeokSjukVoBw4A.0EM0LDNxviN3EzMzDzW}
pwm.bokkefd{jGcKH7UkcntYVmeolSkulVnBx4A.0FM0MDNxwiN4EyNzEzV}
pvn.college{kGcKH7UlbmtYVleokSkvlVnBx4A.0FM0MDOxwhN4EzNzEzV}
pvn.college{kGcKH6TlcntYVmeolSjukVoBw4A.0FM0MDNxwiM4EzNzEzW}
pvn.college{kFbKG7TlcmtYVldolRkvlVoBw4A.0FL0MDOxwiN4DyNzEzW}
pvn.college{jGbKG6TkbnsYUlenlRkulUoAx3A.0FM0MDOxvhN4EyNzEyW}
pvn.collefe{kGcKG7UlcntYVmeolSkvlVoBx4A.0FM0MDNwwiN4EzNzEzW}
pvn.collefe{kFcKH7UkcntYUlenlSkvlVoBx4A.0EM0MDOxwiN4EzNzDyW}
pvn.cokldge{jFcJH6TlcnsYVleolRkvkVoBx3A.0FL0MDNxwiN4EyNzDzV}
pvn.cnllege{kGcKH7TlcnsYVmeolSkvlVnBx3A.0FL0MDNwwiN4EzNzDyW}
pvn.cnlldge{kGcKG7UlbntYVleolRkvkVoBw4A.0FM0MDOxwhN4DzMzEzW}
pvm.college{kFcKH6UkcntYVmenlSkulUoBx4A.0FM0LDOxviN3EzNzDzW}
pvm.collefe{kGcKH7UlcntYVleolSkvlUnBx4A.0FL0MDNxwiN4EzNzEzW}
pvm.coklege{kGbKG7UlcnsXVleokSjvkVoBw3A.0EM0LCOxwiM4DyNyEzW}
pvm.cnkldfd{jGbKG7UlcnsYUmeolSkvlUnBx4A.0FM0LCOxwiN3EzMyEzW}
pvm.bolldge{jGcKG6UlcmsYVleokSjvlVoAx3A.0FM0MDNwwiM4EzNzEzW}
own.collefe{kFcJH6TlbntYVlenkSkvlUoBx4A.0FM0LDOwwhN4EzMyDyV}
own.collefe{jGcKG7UlcntYVmeolRjvlVoBx4A.0EM0MDOxwiN4EyNzEzW}
own.cokkege{jGcKH6TlcntYVmdolSjvlUoBx4A.0FM0MDNxwiN4EyNzEyW}
own.cnlkdge{jFcKH7UlcmtYVmenlRjukUnBw4A.0FM0MDNxviM4EzMzEzV}
own.cnklefd{kGbKH7UlbntYUleokRkvkVnAw4A.0EM0MDNxviN4EyNzDzW}
own.boklegd{kFcKH7UlcmtYVmeokRjvkUoBx3A.0FM0MDOxwhN3EyNyDyW}
own.bnllege{kGbKH7UlcmsYVmeolSkvlVoBx4A.0FM0MDOxwiN4DzNyDyW}
ovn.college{jFcKH7UlcntYVmeokRkvlUoBx4A.0FM0MDOxwiN4EzNzEzW}
ovn.colldfe{kGcKH7UkcntYUmenkSkvlUoBw3A.0EM0MDNxvhN4EzNyEzW}
ovn.colldfe{jGbJH7UkbmtYUmenkRkvlVnBx4A.0FM0MCNwviN4EzNzEzV}
ovn.cnlldge{kFbJG7UlbntXVmeokSkulVoBw4A.0EM0MCOxwhN4EyMzEyV}
ovn.bnklege{kFbKH7TlbntYUmeolSkvlVnAx3A.0FM0MDOxwhN4EzNzEzW}
ovn.bnklefe{jGcJH6UkcnsYVmeokRkulUoAx4A.0FL0MDNxwiM4DzNyEyW}
ovm.colkegd{kGcJH7UlcmtYVmenlSkvlUoBx4A.0FL0MCOxwiN4EzMzDzW}
ovm.colkdge{kGcJH7UlcmtXVmeolSkulUnBx4A.0EM0MCNwwiN4EyMyDzV}
ovm.cnkldfe{kGcKG7TkcntXVmeolSkvlVoBx4A.0FM0LDOxvhN3EyMyEzV}
```

## What I learned
Through this challenge I learnt that:
- sort orders lines alphabetically
- -r: reverse order (Z to A)
- -n: numeric sort (for numbers)
- -u: unique lines only (remove duplicates)
- -R: random order!

## References
No references used.

