# 0x0F Level
> 10 (Linux)

## Challenge

The password to level

Note: Not the standard flag format

author: [@nopresearcher](https://twitter.com/NopResearcher)

## Solution

```
level13@trainer:~$ su - level14
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

Welcome to Level 14

For this level you are going to familiarize yourself with the kernel version.  We are just looking for the Kernel and Major version (the first two sets of numbers) example: if the version is 2.62.26.1 the password will be 2.62

Understanding Kernel versions can help when search for exploits with tools like searchsploit or exploitdb (Sorry, there isn't any kernel exploits for this box, I hope)

type: man uname
      google linux kernel

level14@trainer:~$ uname -a
Linux trainer 4.19.0-19-cloud-amd64 #1 SMP Debian 4.19.232-1 (2022-03-07) x86_64 GNU/Linux
```

## Flag

```4.19```
