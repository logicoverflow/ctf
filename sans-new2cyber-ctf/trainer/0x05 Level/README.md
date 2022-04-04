# Ox05 Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level3@trainer:~$ su - level4
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

Welcome to Level 4

The password for the next level is in this user's home directory, just like the last levels you might have to dig.

type: man ls    read about files and folders that start with a dot (.)

level4@trainer:~$ ls -la
total 100
drwxr-x---  7 level4 level4 4096 Mar 24 17:08  .
drwxr-xr-x 26 root   root   4096 Aug 22  2021  ..
-rw-r--r--  1 level4 level4 9756 Mar 23 20:38  -a
-rw-r--r--  1 level4 level4  220 Apr 18  2019  .bash_logout
-rw-r--r--  1 level4 level4 3526 Apr 18  2019  .bashrc
drwx------  3 level4 level4 4096 Mar 24 14:24  .gnupg
-r--r-----  1 level4 level4  438 Aug 22  2021  helpme
drwx------  2 level4 level4 4096 Mar 24 19:28  .hidden_dir
drwxr-xr-x  3 level4 level4 4096 Sep 15  2021  .local
-rw-r--r--  1 level4 level4 9835 Nov 17 13:03 'ls - a'
-rw-r--r--  1 level4 level4 9835 Nov 17 13:05 'ls -a'
-rw-r--r--  1 level4 level4 9835 Nov 17 13:01  ls-a
-rw-r--r--  1 level4 level4  807 Apr 18  2019  .profile
drwx------  2 level4 level4 4096 Feb  4 17:02  .ssh
drwxr-xr-x  2 level4 level4 4096 Sep 15  2021  .vim
-rw-------  1 level4 level4 1762 Mar 24 17:08  .viminfo
-r--r-----  1 level4 level4  208 Aug 22  2021  welcome_message

level4@trainer:~$ cd .hidden_dir/

level4@trainer:~/.hidden_dir$ ls -la
total 28
drwx------ 2 level4 level4 4096 Mar 24 19:28  .
drwxr-x--- 7 level4 level4 4096 Mar 24 17:08  ..
-rw-r----- 1 level5 level4   34 Aug 22  2021  .level5_password
-rw-r--r-- 1 level4 level4 1024 Mar 24 19:28  ..level5_password.swp
-rw-r--r-- 1 level4 level4 9835 Nov 17 13:05 'ls -a'

level4@trainer:~/.hidden_dir$ cat .level5_password
7b6c2552940f47a27fbd729ae0e2893c
```

Hint: _read about files and folders that start with a dot (.)_

## Flag

```7b6c2552940f47a27fbd729ae0e2893c```
