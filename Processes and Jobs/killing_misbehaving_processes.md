# KILLING MISBEHAVING PROCESSES
In this challenge I have to terminate a misbehaving process.

## My solve
**Flag:** `pwn.college{kxN-UfYxPfEcsS7GUYsN6IbeSp1.0FNzMDOxwiN4EzNzEzW}`

It was mentioned in the problem statement that there's a decoy process that's hogging a critical resource - a named pipe (FIFO) at /tmp/flag_fifo into which (like in the Practicing Piping FIFO challenge) /challenge/run wants to write the flag. I need to kill this process. First I found this process using ps -ef. Then I killed the process. Then I invoked /challenge/run which wrote a lot of flags in the fifo. I catted fifo in another terminal. Then I invoked /challenge/run again and catted fifo again to get the correct flag.
```bash
hacker@processes~killing-misbehaving-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 08:51 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 08:51 ?        00:00:00 /run/dojo/bin/sleep 6h
root         137       1  0 08:51 ?        00:00:00 /bin/bash /challenge/.init
root         138       1  0 08:51 ?        00:00:00 /bin/bash /challenge/.init
root         139       1  0 08:51 ?        00:00:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
root         140     137  0 08:51 ?        00:00:00 sleep 6h
root         141     138  0 08:51 ?        00:00:00 sleep 6h
hacker       142     139  0 08:51 ?        00:00:00 /usr/bin/python /challenge/decoy
hacker       153       1  5 08:51 ?        00:00:00 /nix/store/a1kxazxkgw7mjbjgisvah95p1r3n5ykl-nodejs-22.16.0/bin/node /nix/store/5hs5m65ajn7i3s6k20gzks9s7g5avn3w-code-server/libexec/code
hacker       176     153 28 08:51 ?        00:00:04 /nix/store/a1kxazxkgw7mjbjgisvah95p1r3n5ykl-nodejs-22.16.0/bin/node /nix/store/5hs5m65ajn7i3s6k20gzks9s7g5avn3w-code-server/libexec/code
hacker       215     176 17 08:51 ?        00:00:01 /nix/store/a1kxazxkgw7mjbjgisvah95p1r3n5ykl-nodejs-22.16.0/bin/node --dns-result-order=ipv4first /nix/store/5hs5m65ajn7i3s6k20gzks9s7g5a
hacker       233     176  4 08:51 ?        00:00:00 /nix/store/a1kxazxkgw7mjbjgisvah95p1r3n5ykl-nodejs-22.16.0/bin/node /nix/store/5hs5m65ajn7i3s6k20gzks9s7g5avn3w-code-server/libexec/code
hacker       287     233  0 08:52 pts/1    00:00:00 /run/dojo/bin/bash --init-file /nix/store/5hs5m65ajn7i3s6k20gzks9s7g5avn3w-code-server/libexec/code-server/lib/vscode/out/vs/workbench/c
hacker       315     233  0 08:52 ?        00:00:00 /bin/sh -c "/nix/store/5hs5m65ajn7i3s6k20gzks9s7g5avn3w-code-server/libexec/code-server/lib/vscode/out/vs/base/node/cpuUsage.sh" 287
hacker       316     315  0 08:52 ?        00:00:00 /nix/store/ih68ar79msmj0496pgld4r3vqfr7bbin-bash-5.2p37/bin/bash /nix/store/5hs5m65ajn7i3s6k20gzks9s7g5avn3w-code-server/libexec/code-se
hacker       319     316  0 08:52 ?        00:00:00 sleep 1
hacker       320     287  0 08:52 pts/1    00:00:00 ps -ef
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
----------------------------------------------------------------------------------------------------------------------------------
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{AcYC76hhEBLK9J0HMFrBp6CAgWcSM.N7ikHpwzOL2oQYkWH}
pwn.college{51y7vP.7CbVL7okk1TyPHbaApQyi5CsprJ7gLnd1Xgq9WLs}
pwn.college{E5XDDsnPv.bX9ssyUjD4VsRtRSaGiAN0Dw1TFuwdhTwJfki}
pwn.college{.bd427Tmh8Qi4jTBRCudRfzuHhe5CuRZVmOD7g6ovYrjXQ0}
pwn.college{eLzhcd.cYmqL8riXVlscZE-tXUeCjUE50.jKKOlC-8vAUf3}
pwn.college{7ydVDALaU9ScIAbYmh5mKEYt70s4ISME2qy86ek4UEa19dp}
pwn.college{-CEDxgPqx.nMz5cmGTWPItjnUkJetL6.QT.O-7w1gy3yGx5}
pwn.college{E1fwau4f5VouQUmW2cqNBRaO7hJ95RCHBmUoMb-p1U635OV}
pwn.college{Hzi995630Rx-tpcvi.Sck3vblgLabIBk0eDzK9TVCFv-oPA}
pwn.college{4SmP7e4irWT7PIV7muYTOEv.R6mczgaueOCV8LeUXejqU-n}
pwn.college{myPSWukY7dXPZYrnRDxjrwh4yir4SS-UiS02KWpdN0PcSMk}
pwn.college{f.7L80.77iS0CTmbUtLifG5YyDLK9aZ39d9DnF6ZleTMr5o}
pwn.college{y9A7vo0ZONz5Sax2KA0AZrQrh5SjAdl0yB7Bx75S0T9X-A2}
pwn.college{hVILGtgi0N1umUh8JZqofpQhv9glbdDLzA.HIrJpEYCM8Ao}
pwn.college{GVq9SSwYsxC2z.rb5zbirqD8pP8PwdCFkk2767NdPyr8ern}
pwn.college{K.9ZhfadvJhSISAmNLXkiKTXY2iEE9xrR8.nk32LnnslPZK}
pwn.college{0lWiaSZjUlYpv68-LMlnUYBgCIoXjrfyDStsp8MfVvfl6Jh}
pwn.college{rmpJdgPa8a92vEWQgKE7PcmpnfksUy1vhRmhdHy1t3jYQlb}
pwn.college{JxGq9sHEbqmhpRzlwE2GWw57z.X-MTpNImuJG9HwjYidNBZ}
pwn.college{tOgn77rucpvmXGQ4tJlvyra6XyUtDbciINt9wom9M60kJGa}
pwn.college{A.SlpA4HQSP.wzff.zPnYaSVsm34WMBV6hcZ1ELdAl4o8Bd}
pwn.college{qVnfLZG9jHi5TrF9jToKLIRSfP6nPKVohyYcbyaEAYUr1m3}
pwn.college{hcVPfTP9ZMHvG3XAfKwTCmb3j9idQmCOn9VhM8KbDkr.QTZ}
pwn.college{SZKqPBQ3v-jejtU16VJhDLA2sNPcYDthbRsQnWl.u0ElCo9}
pwn.college{4E0PyLw0ypYSpqEq3zjHID3JQJ4wcWft.IXuIR3ndRrCjdJ}
pwn.college{OZtamW2anxNpTnIZVgoLFDRQQVHoG612zOffSpDmQMXYroN}
pwn.college{XgC.xPsoMofhFRnIcLjAU6YkXCUsiGCE4p4zArmPctCL7xA}
pwn.college{o-wRYfz8PNXeiCkeu-hrQYnXK973anQykFD5F3XXrvIQ4JV}
pwn.college{VJLkwK.jA0abTr1VRk6vNthh7ayrvNkaTzCy5nUoKcZ3Add}
pwn.college{ML9t4TkphjP6FJTNbmjD9tbkRsttpn-bdnmso5SwgkCIcmj}
pwn.college{AdU2yxrgvikAmJedOxsM68QOxnCy2.qN0Aw2wnoZTcVQiPB}
pwn.college{nqvtGhWV3BfjIef.2k-9RjC14zu1JFfunUJHdG74BKVHX-.}
pwn.college{pvcD-xi5kzHS4zhYoDXInUsruVZRVqu0jlRnZ8EhBnqh5iI}
pwn.college{us8gPPPfNCu7prHQJbyVmcmMZij6TJ5NEZPpLk87RA9KRLh}
pwn.college{oZ9Pv0pg62fuAEMjN3PL6W3s2z4mdmr-YSl6ldZWqT6tVaV}
pwn.college{7oJ-6Z5Sy752cuwrFJXeq533RifF2MzIw5KQqek14yekL2t}
pwn.college{FVMw64lOXZWsNd6dBpPx8jQYUAlLUHMW3Ied5UXGHIdqE17}
pwn.college{wXneFUnTPNJgtBLMD1guQoRPgVSzLJeqTGkvNrjliBFsfZU}
pwn.college{ChgkGzPZ9sCPuFWZ-xNIz-Na.wisnkew59t2e0nvk7b9gcf}
pwn.college{4gjboUbwle29Yr.2.QW7IKUbprXzzNksxWlwgfadeu2Cj5U}
pwn.college{Zp8QyaOQNBUAbcyLZzbHhOuGm1bziM4WG8cLUbDvnQTwjbM}
pwn.college{-F-N-M1D5thH3N1kvofS3pMp1JksaGfGW7P0VJVeXzCryb0}
pwn.college{NLDbzxNsrIpchsZiK-61iRKcCJI.eMp0961RGaDqsJ.N6ju}
pwn.college{kxigjKlXIVwatDtlZhXbGz-xh6HBphcT5xe5x-ENee.6kyf}
pwn.college{HzK-CzGREdogitkiDVW86LkYOs5E0INI56IAOlMWSo9Mqjj}
pwn.college{h8ZQd2cW-CyayQXCP44ov.ueunfKwzisPym1L1MVExEv8jF}
pwn.college{ehpdrFKxmSMHBNerGocVY5G8Ms9ztt7pCa37fJGwvldwd8.}
pwn.college{IJ2PA6kIt2eeUIMNrJYr-MMXD291Aw5Qv9Xf2pRlrBGH4nJ}
pwn.college{Po5nZkxFhnGB97taRzJrn.CvkH1vcRFyDzSFLNvol8qoc8r}
pwn.college{hN6pH7ryvADi5nJR7fTAZmSzBMiW7ooa1X8zIrUyNJkQdSM}
pwn.college{Sfzze9Ki.-LAVJZSWvBcd2QwRhLKPtr2qq4g1zEQ0L1hYlQ}
pwn.college{p.RilyQWjnD5fg1hOyeNmWXPwjbxmAU6nT9vEhV5fXG-Wiu}
pwn.college{6nOifOl8XXItKdmO42JZ42tt3Ts0lFNs7HHxNxdK5V0HgD6}
pwn.college{LFSvBMp8OiwDao1yW8kT5LMES633mwTILQTCNg5AoMsi11n}
pwn.college{PeMzMXZAvRWDIBo7yWvkWme9D9GGy6Zn3WCLbtqyXSbwV7q}
pwn.college{ocmotERo4-NdfkBlEVgM0J1rRxrL1cK8zdqq18WcCPbvgcC}
pwn.college{t8RYbackCCJD8uyeJFtVbs.O1GC6vjgmx0HFup8HzSKbJJA}
pwn.college{Flr7lecS6-wfkhCvJEXu1sIu2Ai4yFSni7qH7b-G9QUsLRv}
pwn.college{kpsNQGAE-MbX1Dg4Eh9yI30yf0BFccZbFenmYzVkwostUJU}
pwn.college{Hvd7hy6De-vLSPyVVbQWg-nTfh1sU6EfvVCOo-9wTv5vL2T}
pwn.college{pWWC7ddAC8fAFxS0g8M.7F.PGXBY7W.Xj.PoHcN0zNGIMTm}
pwn.college{1bUjrKkeNbLyUh265Uwiv9Oo3zg-jyF2N4GBWFNlIaZUqGJ}
pwn.college{mjN5lH7kUpTBPeMUuSM5iA7euhBskAGlSCV5ko8Kr8pD6Xt}
pwn.college{7zHYUKjztmBHkHc36Fqn8b.D0.cnEDDXFl14y4.LsgDkO8.}
pwn.college{27mL9qJQBd6ezs04pmbdap11dIuyTUvp4pi56-4ua1hXLeM}
pwn.college{GYvvYByOSk3xLAGFNMhBLcR.Md-w5bpq0Tastz0BmmPP.xy}
pwn.college{ViX7WxPAJBXioUv-zmaeoeGWQL1WgkAZLjhYUtAFQFrUzc0}
pwn.college{FhyFtgqVXIl2x1X6peF6PNSj-bJ6K3TIY50Xyt7rUGsv3rV}
pwn.college{dgDTAGlSCjbqUqoNkc9zdV76RSFsJykMFq5C-8JrNCfex1o}
pwn.college{czrO-sa0fI5xFdKn.Zm.j9n-UrjR6O.mbjrS3pUD808Xl-a}
pwn.college{oKH17TSO0SRLQkfo2SLGvVI-NuAPS2BR0aP4wSZ1MWgXCUI}
pwn.college{HWk.ZLK3J1nxm6LIUoCi0yNXTJVy24h08WvRd1gUsN5EgcR}
pwn.college{-mJWtK3fF5e2ljCVv2T4XEq3ZawWqWZYrHN4UY3AwQajtPa}
pwn.college{x50zccz9JQveMFHiArAT6hPeO9egnCcr-M11fovVJi2MSgR}
pwn.college{jq22XudEyirj9IrzuIkhEGUAktDUHLLUnHbHzUuOFSVyxLq}
pwn.college{7zF9X05GVOlhq8AW6brSHm4nEJQP2Yf2-zqMa1eGpVmicAr}
pwn.college{nlx7l-RF6jyfqkxvAMi3uUDhUh7zV5wuzscFBYKybkedrrM}
pwn.college{hE5KmcaVDqV9EPDXFLv1df1OdgVvu0kHymrGddHJhzSkjW4}
pwn.college{MIwop73lDSNtKFKXobe-o9NdowMvd8ySmnY.tgEMgTzQPJt}
pwn.college{YrCYgSd9U4Jxsy4ps8Vt.jiRafPeNmNUQ8YyFRQvZeddJTT}
pwn.college{y8yeQEUzBsfVHHTsZXI6k3MCdSmFaRcW2PPKEm9g2fyA--b}
pwn.college{1qCFcyYYexYQLpL4OT3s6WOHwjyI5Idm1YJ-oLiYcgO0Oom}
pwn.college{5gc66PxdS7YOAe5iIDs1mEm3a2exDJi61nCdQxGzSFg46ny}
pwn.college{f3mC5ArY..LHm6HdjRpDlDHYbVcDC4DjX1362.lGS0IVPQl}
pwn.college{afCheyi0HsvCYawAQfIe0iy-F.jYrtrK6GCDOIBxISTDzoe}
pwn.college{9cLGATHs1wZg1n1qldZLxRwoCeCN5.WZqhxZPLayZAEjJns}
pwn.college{rAEEedcw-ABldJMOFudD7s9yYpGkePA.9ZuYea-uOeleV4c}
pwn.college{jClhlCZBmdhOfTBlPuOna3JjrjFd-41P.G.MvXUGh3gbaB.}
pwn.college{FKoNUqPkDjRRCLZm-WmpWWyTUToDRT6ALIqZZgDWyaly-kk}
pwn.college{DSWOzsa2CMa2tQtzL-JHwFBLdMvtOIhArLt1DoaPzEptWUF}
pwn.college{oya8mQ-Kne5mQDXx3UdfXBWpk3CtwocqPyFMPa1WwQLLK6-}
pwn.college{mK7mN9i.V4514y7OZ5yUC9ygWw993V0I0R3.0k5y7sS4E3S}
pwn.college{9VQQCOucmihvoMJ2UuHXGUHronG4IcOU9YNOaR1wZcGqPO6}
pwn.college{bOqEClE5fAiUdXELwpxLmq3JTbhbPEZ301Tja-C81aH0eDh}
pwn.college{c7txJdB2BEfAWAwHXeiZAygH3MI53VcvOwAeVoZpCyFGakx}
pwn.college{V7bhMynSchU-eOEQu0l6xkwpp7pRKpmnYzyMU2qCOxNwuZl}
pwn.college{1i.WcFiF8Rr20mw6NVxCezoLn2oOh.NEou9n5rEdu9T48VL}
pwn.college{JeOHsfTCJcUn5n9jBfq7nwGsC941THuA0kT3opQrG5tVnbt}
pwn.college{UKPHriIvIEN9CUX00oP-9wbV0yozZUebgwoJ42lPc8Oxcmc}
pwn.college{I1ZaL3WIjmKLfxo9WihYIg-8tYMQla7rGfaRXwMSUWliulR}
pwn.college{Q5g.WAYwDYOSENjIG5m2aK0nSDEZKceSqJWRtABNHTs0eEs}
pwn.college{jyhxwJ4OFVkJuL2woqCH9ltwbctE1va93Ac4rxv3M.jdJps}
pwn.college{FIvoeQbP18clcNOGoOooOldSTGToa5Ai78pmZotXiQHbiCq}
pwn.college{DATMC1kCGOSvyNT1N3-PQZBM1bEWxvSFlfgVwLTuOlltLVd}
pwn.college{8U9jGQqxOxda0SaExBVbOokr1RUF38Dcesz7xoPGHb-durK}
pwn.college{GwfqQjQsTzzx3WoGtCiosutXQqewPTK0.1L47ydodAp-uoM}
pwn.college{lxMl-hdf9RrnhEpNlxj3XJGlY3uDJ4OCh85RKFC8L0aqzoW}
pwn.college{GxdjzdOgVZMPnmEUXEcsGh9x108N10Cd7.kzt1cdx3bGl32}
pwn.college{X23RFnbjLnS.TzA3optT-va8CEe4JmB6SHBD2P8iiFk0w2p}
pwn.college{T9wON2X1nDZLgiR0bx5FyzDYGESxApf6SI7Tievi0R78MY5}
pwn.college{2MAod8TyXHsE0rpznDKDVoJ.a0T-zBY43TG74qSxwzLlgKX}
pwn.college{-gPnwMfaWYkdBUIoo9yp-9P2X3f0A.CBZuKHXIqG7FbbkiZ}
pwn.college{AKjzO6f9RauqCk7raTUm4jIxFr1KA-Cgad0OPKULVBbHZEp}
pwn.college{aZzNFKXf71jrVPZ4dFTPXvg12rKsaf5Ujc3UrCaD7qkYP5Z}
pwn.college{orOKlUK-OnLmWWOErzl46A76G7k4KxdUK6bN7pEuveFGP80}
pwn.college{WYBaL1glFkJm5TZzRTqzNtxGC1n7HJoaBbYXKLqW9KB4UpC}
pwn.college{BT8khnOpcnkwuxtryXEwXFtAWa3IgcYLHBbH2mTTGVWlOin}
pwn.college{pP3gp65ocJY89fv18UtsSRmU5elsIUkKJa-pqhh7MkNe-fD}
pwn.college{LQBUMgeZU7aglHn9ZDNFTKazMC630dEFzyyQvkMze05hgx9}
pwn.college{pCnNVAe2rilNx8yOH3C9vHFiWNnmgUmNkhCk5hQZ7-e9L1P}
pwn.college{QOP9hD6SEXNFWaO1v7EuCT6kB7GoOtl9L.XeCh2n0ykY.o3}
pwn.college{brxuYW4t1ztHOn4EvQZOzEc6Jrj8suLwD7aAqK3zeA0d82H}
pwn.college{X-Ph3wIe7bTRyCnfwS8JNSxM1fMUFNaajw6CyzvkPEn.ld8}
pwn.college{SPxVmI-ZiJc1bJDO3g.otPdmgDcpw33wT80MnyQxArGfer-}
pwn.college{.l3JIEXOLwLhr2DdRY.kZ10srVeKpVwPqBz0HoQc.tG3sw1}
pwn.college{xuyjWbpPGeiGSKZZrknwZv.3thh0hGN1G0.h8hWGYxDxJGC}
pwn.college{WnjIj7p3l.lwJDNV0r-HtHygZmnW-sYvfVBW4B1AhY0bCk8}
pwn.college{8fy.thD6t9NUUfjWLU-O2EtiHDUxOmVasvPZ11AU7Bs57VU}
pwn.college{LfTYZQKotQsiIJB4SGvtVfyqJ9EZFTY.NFPxkZpY4-BiXva}
pwn.college{OWUsW1uUDTK0VPcZJ1PZlPukrK9GRO1ylHhrMTIZuh9Pp6R}
pwn.college{bHsSu.kgr4O2Tj3tQk-8.wHaFdW1.6FbXar2unQI0bjA95Q}
pwn.college{cb2xEirrwfFj1Jmlq5VrTu8PZ.9H-aBS-Y4EPA3Ia8O749Y}
pwn.college{W80n-QT.t0-47C.LnCYkPdbqmIONIGJdO3OLoL94yAXxh7L}
pwn.college{XCOt56M.w-IRfuhShKoPzCcZcE9PHtzBkobhN3UypEM2bUO}
pwn.college{kxN-UfYxPfEcsS7GUYsN6IbeSp1.0FNzMDOxwiN4EzNzEzW}
^C
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
----------------------------------------------------------------------------------------------------------------------------------
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{kxN-UfYxPfEcsS7GUYsN6IbeSp1.0FNzMDOxwiN4EzNzEzW}
```

## What I learned
Through this challenge I learnt that:
-   You might see a few decoy flags show up even after killing the decoy process. This happens because Linux pipes are buffered: conceptually, they have a sort of length through which data flows, and you might kill the decoy process while data is in the pipe. That data, having already entered the pipe, will proceed to the other end (your cat).

## References
No references used.

