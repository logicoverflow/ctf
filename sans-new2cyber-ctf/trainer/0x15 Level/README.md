# 0x15 Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level19@trainer:~$
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

Welcome to Level 20

For this level you are going to continue familiarizing yourself with user artifacts.  Look in this user's home directory to see if there are any files left behind that may contain useful information.

type: man file
      man tar

level20@trainer:~$ ls -la
total 51
drwxr-x---  3 level20 level20 4096 Mar 24 23:56 .
drwxr-xr-x 26 root    root    4096 Aug 22  2021 ..
-rw-rw----  1 level21 level20 2048 Aug 23  2021 backup.tgz
-rw-r--r--  1 level20 level20  220 Apr 18  2019 .bash_logout
-rw-r--r--  1 level20 level20 3526 Apr 18  2019 .bashrc
-rw-r--r--  1 level20 level20    0 Mar 24 22:02 .cloud-locale-test.skip
-r--r-----  1 level20 level20  466 Aug 23  2021 helpme
-rw-------  1 level20 level20   32 Mar 24 18:10 .lesshst
-rw-rw----  1 level20 level20   64 Aug 23  2021 level20_password
-rw-r--r--  1 level20 level20  807 Apr 18  2019 .profile
drwxr-x---  2 level20 level19 4096 Nov  6 19:01 .ssh
-rw-------  1 level20 level20 1407 Feb  5 21:01 .viminfo
-r--r-----  1 level20 level20  260 Aug 23  2021 welcome_message

level20@trainer:~$ tar -xvf backup.tgz
level21_password

level20@trainer:~$ cat level21_password
65230da2ead4ba2ed76ee2605cadcd4d
```
## Flag

```65230da2ead4ba2ed76ee2605cadcd4d```
