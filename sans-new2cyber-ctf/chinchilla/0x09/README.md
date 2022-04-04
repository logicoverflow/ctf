# 0x09 Cuzco's Great Adventure Flag
> 20 (Web)

## Challenge

Cuzco was aware that the file had information about Parkour that would help her learn even more, so she decided it was safe, downloaded it, and tried to open it. That’s when she learned the file had been encrypted. Can you help her crack the password?

She had one additional piece of information, this MD5 Hash: 51F8571B1EC5D507670802B3A5F06B65

author: [@CarpeDiemT3ch](https://twitter.com/CarpeDiemT3ch)

## Solution

```
┌──(logicoverflow㉿kali)-[~/Downloads]
└─$ cat md5hash 
51F8571B1EC5D507670802B3A5F06B65

┌──(logicoverflow㉿kali)-[~/Downloads]
└─$ sudo hashcat -m 0 md5hash /usr/share/wordlists/rockyou.txt --force
[sudo] password for logicoverflow: 
hashcat (v6.2.5) starting

You have enabled --force to bypass dangerous warnings and errors!
This can hide serious problems and should only be done when debugging.
Do not report hashcat issues encountered when using --force.

OpenCL API (OpenCL 2.0 pocl 1.8  Linux, None+Asserts, RELOC, LLVM 11.1.0, SLEEF, POCL_DEBUG) - Platform #1 [The pocl project]
=============================================================================================================================
* Device #1: pthread-0x000, 1439/2942 MB (512 MB allocatable), 2MCU

Minimum password length supported by kernel: 0
Maximum password length supported by kernel: 256

Hashes: 1 digests; 1 unique digests, 1 unique salts
Bitmaps: 16 bits, 65536 entries, 0x0000ffff mask, 262144 bytes, 5/13 rotates
Rules: 1

Optimizers applied:
* Zero-Byte
* Early-Skip
* Not-Salted
* Not-Iterated
* Single-Hash
* Single-Salt
* Raw-Hash

ATTENTION! Pure (unoptimized) backend kernels selected.
Pure kernels can crack longer passwords, but drastically reduce performance.
If you want to switch to optimized kernels, append -O to your commandline.
See the above message to find out about the exact limits.

Watchdog: Temperature abort trigger set to 90c

Host memory required for this attack: 0 MB

Dictionary cache built:
* Filename..: /usr/share/wordlists/rockyou.txt
* Passwords.: 14344392
* Bytes.....: 139921507
* Keyspace..: 14344385
* Runtime...: 1 sec

51f8571b1ec5d507670802b3a5f06b65:Parkour                  
                                                          
Session..........: hashcat
Status...........: Cracked
Hash.Mode........: 0 (MD5)
Hash.Target......: 51f8571b1ec5d507670802b3a5f06b65
Time.Started.....: Sat Mar 26 22:34:24 2022, (0 secs)
Time.Estimated...: Sat Mar 26 22:34:24 2022, (0 secs)
Kernel.Feature...: Pure Kernel
Guess.Base.......: File (/usr/share/wordlists/rockyou.txt)
Guess.Queue......: 1/1 (100.00%)
Speed.#1.........:  2512.1 kH/s (0.07ms) @ Accel:256 Loops:1 Thr:1 Vec:4
Recovered........: 1/1 (100.00%) Digests
Progress.........: 437760/14344385 (3.05%)
Rejected.........: 0/437760 (0.00%)
Restore.Point....: 437248/14344385 (3.05%)
Restore.Sub.#1...: Salt:0 Amplifier:0-1 Iteration:0-1
Candidate.Engine.: Device Generator
Candidates.#1....: STAR22 -> PHOTO
Hardware.Mon.#1..: Util: 42%

Started: Sat Mar 26 22:34:22 2022
Stopped: Sat Mar 26 22:34:26 2022
```

## Flag

```Parkour```
