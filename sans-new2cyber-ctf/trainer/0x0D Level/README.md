# 0x0D Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level11@trainer:~$ su - level12
Password:

    ====================================================================
    ||                                                                ||
    ||     .--.          Welcom to the Linux Trainer!                 ||
    ||    | o_o|                                                      ||
    ||    | ==>|          To view the level instructions again        ||
    ||   / /   \ \         type: cat welcome_message                  ||
    ||  ( |     | )                                                   ||
    || /' |_____/'\       Getting Stuck? Need help with a level?      ||
    || \___)--(___/         type:  cat helpme                         ||
    ||                                                                ||
    ||                    Use "su - level#"  to change levels         ||
    ||                                                                ||
    ||                    feedback: nopresearcher@gmail.com           ||
    ||                                                                ||
    ||                                                                ||
    ====================================================================

Welcome to Level 12

For this level you are going to find SUID and SGID binaries in common locations.  This is a common privilege escalation technique seen in CTFs and real world.  Remember the user you are looking to escalate privileges to is level13.

type: man find
      google SUID
      google SGID

level12@trainer:~$ find / -perm -u=s -type f 2>/dev/null
/usr/lib/dbus-1.0/dbus-daemon-launch-helper
/usr/lib/openssh/ssh-keysign
/usr/sbin/mysecret
/usr/bin/chsh
/usr/bin/mount
/usr/bin/umount
/usr/bin/newgrp
/usr/bin/su
/usr/bin/chfn
/usr/bin/gpasswd
/usr/bin/sudo

level12@trainer:~$ find / -perm -u=s -type f 2>/dev/null
/usr/lib/dbus-1.0/dbus-daemon-launch-helper
/usr/lib/openssh/ssh-keysign
/usr/sbin/mysecret
/usr/bin/chsh
/usr/bin/mount
/usr/bin/umount
/usr/bin/newgrp
/usr/bin/su
/usr/bin/chfn
/usr/bin/gpasswd
/usr/bin/sudo

level12@trainer:~$ cd /usr/sbin/

level12@trainer:/usr/sbin$ ./mysecret
f4736e1eb28b1d9055c5f5d58a49b5a6
```

## Flag

```f4736e1eb28b1d9055c5f5d58a49b5a6```
