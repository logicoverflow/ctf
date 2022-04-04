# 0x13 Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level17@trainer:~$ su - level18
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

Welcome to Level 18

For this level you are going to continue familiarizing yourself with user artifacts.  Look in this user's home directory to see if there are any files left behind that may contain useful information.

type: man bash

level18@trainer:~$ ls -la
total 64
drwxr-x---  5 level18 level18 4096 Mar 24 18:04 .
drwxr-xr-x 26 root    root    4096 Aug 22  2021 ..
-r--r--r--  1 level19 level18  299 Aug 23  2021 .bash_history
-rw-r--r--  1 level18 level18  220 Apr 18  2019 .bash_logout
-rw-r--r--  1 level18 level18 3526 Apr 18  2019 .bashrc
drwx------  3 level18 level18 4096 Mar 24 14:15 .gnupg
-r--r-----  1 level18 level18  504 Aug 23  2021 helpme
-rw-------  1 level18 level18 1812 Mar 23 20:04 key.txt
-rw-------  1 level18 level18   38 Mar 24 14:17 .lesshst
drwxr-xr-x  3 level18 level18 4096 Sep 15  2021 .local
-rw-r--r--  1 level18 level18   15 Mar 23 21:15 plain
-rw-r--r--  1 level18 level18  807 Apr 18  2019 .profile
drwx------  2 level18 level18 4096 Mar 24 17:57 .ssh
-rwx--x--x  1 level18 level18 7735 Mar 24 18:04 .viminfo
-r--r-----  1 level18 level18  246 Aug 23  2021 welcome_message

level18@trainer:~$ cat .bash_history
whoami
uanme -a
w
id
ps -ef
netstat -an
cat /proc/version
cat /etc/*-release
pwd
ls -la
cat /etc/profile
cat ~/.bashrc
awk -F ":" '!/nologin/{print $1}' /etc/passwd
find / -perm -g=s -type f 2>/dev/null
ssh level19@localhost
b06a246b0646b337f319316b9232151c
whoami
ssh level19@127.0.0.1
pwd
ls -la
```

## Flag

```b06a246b0646b337f319316b9232151c```
