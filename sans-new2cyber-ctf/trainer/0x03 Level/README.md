# 0x03 Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
┌──(logicoverflow㉿ALNLPTRV)-[~]
└─$ ssh level2@trainer.threatsims.com
level2@trainer.threatsims.com's password:
Linux trainer 4.19.0-19-cloud-amd64 #1 SMP Debian 4.19.232-1 (2022-03-07) x86_64

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Thu Mar 24 19:18:10 2022 from 100.40.222.34

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

Welcome to Level 2

The password for the next level is in this user's home directory, but you have to dig even deeper.

level2@trainer:~$ ls
dir  helpme  welcome_message

level2@trainer:~$ cd dir/another_dir/another_another_dir/some_directory/

level2@trainer:~/dir/another_dir/another_another_dir/some_directory$ ls
level3_password

level2@trainer:~/dir/another_dir/another_another_dir/some_directory$ cat level3_password
2cadca6148093c403d82396252b8c4db
```

The ability to tab to see the list and prepopulate the next directory helps save time from typing _cd directory_ over and over.

## Flag

```2cadca6148093c403d82396252b8c4db```
