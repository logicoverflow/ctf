# 0x0C Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level10@trainer:~$ su - level11
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

Welcome to Level 11

For this level you are given a file that contains the password to the next level.  The password is a md5 hash.  Research md5 hashes and find it in the file.

type: man grep
      man md5sum
      google md5 hash

level11@trainer:~$ ls
checkmd5.md5  helpme  index.html  md5find  welcome_message

level11@trainer:~$ awk 'length($1) == 32 { print $1 }' md5find > results.txt

level11@trainer:~$ cat results.txt
0982e2a869857644074d06b1a4fd1bea
```

## Flag

```0982e2a869857644074d06b1a4fd1bea```
