# 0x16 Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level20@trainer:~$ su - level21
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

Welcome to Level 21

For this level you are going to continue familiarizing yourself with user artifacts.  Look in this user's home directory to see if there are any files left behind that may contain useful information.

type: man file

level21@trainer:~$ ls -la
total 48
drwxr-x---  4 level21 level21 4096 Mar 24 16:36 .
drwxr-xr-x 26 root    root    4096 Aug 22  2021 ..
-rw-r--r--  1 level21 level21  220 Apr 18  2019 .bash_logout
-rw-r--r--  1 level21 level21 3526 Apr 18  2019 .bashrc
drwx------  3 level21 level21 4096 Mar 24 14:19 .gnupg
-r--r-----  1 level21 level21  561 Aug 23  2021 helpme
-rw-rw----  1 level22 level21   62 Aug 23  2021 mybackup
-rwxrwx--x  1 level21 level21   33 Aug 23  2021 mybackup.out
-rw-r--r--  1 level21 level21  807 Apr 18  2019 .profile
drwx------  2 level21 level21 4096 Nov  6 19:03 .ssh
-rw-------  1 level21 level21  703 Feb  5 18:38 .viminfo
-r--r-----  1 level21 level21  247 Aug 23  2021 welcome_message

level21@trainer:~$ cat mybackup
BZh91AY&SY&�I� "��&��!�L,U���8�V><�?rE8P�&�/

level21@trainer:~$ cat mybackup.out
643b2616b33de99b179c33950970d519
```

## Flag

```643b2616b33de99b179c33950970d519```
