# 0x04 Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level2@trainer:~$ su - level3
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

Welcome to Level 3

The password for the next level is in this user's home directory, but you might not see it at first.

type: man ls    read about files that start with a dot (.)

level3@trainer:~$ ls -la
total 176
-rw-r--r--  1 level3 level3  9957 Mar 23 21:09 ''$'\033'
drwxr-x---  6 level3 level3  4096 Mar 24 21:31  .
drwxr-xr-x 26 root   root    4096 Aug 22  2021  ..
-rw-r--r--  1 level3 level3  9756 Mar 23 20:17  -a
-rw-r--r--  1 level3 level3   220 Apr 18  2019  .bash_logout
-rw-r--r--  1 level3 level3  3526 Apr 18  2019  .bashrc
drwx------  3 level3 level3  4096 Feb  4 17:46  .config
drwx------  3 level3 level3  4096 Mar 24 14:21  .gnupg
-r--r-----  1 level3 level3   355 Aug 22  2021  helpme
-rw-------  1 level3 level3    33 Mar 24 00:07  .lesshst
-rw-r-----  1 level4 level3    34 Aug 22  2021  .level4_password
-rw-------  1 level3 level3 12288 Sep 15  2021  .level4_password.swp
drwxr-xr-x  3 level3 level3  4096 Sep 15  2021  .local
-rw-r--r--  1 level3 level3   807 Apr 18  2019  .profile
drwx------  2 level3 level3  4096 Feb  4 16:58  .ssh
-rwxr-xr-x  1 level3 level3 81512 Feb  4 18:29  tree
-rw-------  1 level3 level3  7897 Mar 24 21:31  .viminfo
-r--r-----  1 level3 level3   182 Aug 22  2021  welcome_message

level3@trainer:~$ cat .level4_password
72f6af6b0005adb15fbc91e1b140115f
```

Hint: _read about files and folders that start with a dot (.)_

## Flag

```72f6af6b0005adb15fbc91e1b140115f```
