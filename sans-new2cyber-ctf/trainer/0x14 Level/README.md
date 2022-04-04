# 0x14 Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level18@trainer:~$ su - level19
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

Welcome to Level 19

For this level you are going to continue familiarizing yourself with user artifacts.  Look in this user's home directory to see if there are any files left behind that may contain useful information.

type: man ssh

level19@trainer:~$ cd .ssh

level19@trainer:~/.ssh$ ls -la
total 16
drwxr-x--- 2 level19 level19 4096 Jun 27 18:34 .
drwxr-x--- 5 level19 level19 4096 Jun 27 20:02 ..
-rw-r--r-- 1 level19 level19 1502 Jun 27 18:34 known_hosts
-rw------- 1 level19 level19 1811 Mar  3 23:54 level20_id_rsa

level19@trainer:~/.ssh$ ssh -i level20_id_rsa  level20@localhost

level20@trainer:~$ ls -la
total 52
drwxr-x---  6 level20 level20 4096 Jun 27 20:36 .
drwxr-xr-x 26 root    root    4096 Mar  5 10:06 ..
-rw-r-----  1 level20 level20 2048 Jun 27 20:25 backup.tar.gz
-rw-rw----  1 level21 level20 2048 Mar  4 22:39 backup.tgz
drwx------  3 level20 level20 4096 Jun  5 16:31 .config
drwx------  3 level20 level20 4096 May 30 17:28 .gnupg
-r--r-----  1 level20 level20  466 Mar 24 13:30 helpme
-rw-rw----  1 level20 level20   64 Mar  4 00:22 level20_password
-rw-r--r--  1 level20 level20   32 Mar  4 22:20 level21_password
drwxr-xr-x  3 level20 level20 4096 Jun 27 17:41 .local
drwxr-x---  2 level20 level19 4096 Jun 27 16:05 .ssh
-rw-------  1 level20 level20  798 Jun 27 18:58 .viminfo
-r--r-----  1 level20 level20  260 Mar  4 22:39 welcome_message
level20@trainer:~$ cat level20_password 
The password for level20 is:

5cf82d972614f73422f899f90cfce80f
```

## Flag

```5cf82d972614f73422f899f90cfce80f```
