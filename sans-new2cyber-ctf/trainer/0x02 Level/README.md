# 0x02 Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
┌──(logicoverflow㉿ALNLPTRV)-[~]
└─$ ssh level1@trainer.threatsims.com
level1@trainer.threatsims.com's password:
Linux trainer 4.19.0-19-cloud-amd64 #1 SMP Debian 4.19.232-1 (2022-03-07) x86_64

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Thu Mar 24 19:14:21 2022 from 100.40.222.34

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

Welcome to Level 1

The password for the next level is in this user's home directory, but you may have to dig a bit.

level1@trainer:~$ ls
helpme  some_directory  welcome_message

level1@trainer:~$ cd some_directory/

level1@trainer:~/some_directory$ ls
level2_password  level2_password.save  maybe

level1@trainer:~/some_directory$ cat level2_password
943430e07fd566bc96aa05fca3c96e48
```

## Flag
```943430e07fd566bc96aa05fca3c96e48```
